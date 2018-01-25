It is important to have backups of its VMs and this is a point to
especially not neglect, not to mention material failures you can
one day need to return to a backup due to bad
manipulation or problem after an update. Attention here we
talk about complete image of VMs, it's not just an application backup,
it will therefore have a fairly large size.

One of the constraints to make a backup under VMware is to have
absolutely 2 datastores. For this you have several choices:

-   2 hard drives / SSDs with a datastore on each

-   a NAS (Synology type) that shares an NFS mount. In this case
    need to add a network file system to VMware for it to see
    this one as a datastore

For this tutorial I will use the ESXi web interface which is
available either by installing a vib or from the version
6.0 update 2. As a reminder, to access this interface it is enough
to go on IP \ _ESXI / ui

> ** Note **
>
> For this tutorial I will use the ESXi web interface which is
> available either by installing a vib or from the
> version 6.0 update 2. For reminders to access this interface it
> just go on IP \ _ESXI / ui

Installing ghettoVCB
=========================

We must recover this
[Script] (https://raw.githubusercontent.com/lamw/ghettoVCB/master/ghettoVCB.sh)
and transfer it to the ESXi (on the same datastore as the one that will
welcome backups for example).

> ** Note **
>
> In the rest of this tutorial I consider that you put the script
> ghettoVCB.sh in /vmfs/volumes/Backup/ghettoVCB.sh. To you to adapt
> depending on your configuration the commands / scripts provided.

Connection in ssh
================

You will have to connect in SSH on the ESXi, to do this you need to
from the interface

![vmware.backup](../images/vmware.backup.PNG)

Then with putty or kitty log on by putting the IP of
your ESXi and using your credentials from it

Creating the configuration file
====================================

> ** Note **
>
> For the rest of this tutorial I consider that your datastore
> backup a for path / vmfs / volumes / Backup, be careful to change if
> this is not the case at home

On the backup datastore you have to create a ghettoVCB.conf file which
contains:

    VM_BACKUP_VOLUME = / vmfs / Volumes / Backup /
    DISK_BACKUP_FORMAT = thin
    VM_BACKUP_ROTATION_COUNT = 2
    POWER_VM_DOWN_BEFORE_BACKUP = 0
    ENABLE_HARD_POWER_OFF = 0
    ITER_TO_WAIT_SHUTDOWN = 3
    POWER_DOWN_TIMEOUT = 5
    ENABLE_COMPRESSION = 0
    VM_SNAPSHOT_MEMORY = 0
    VM_SNAPSHOT_QUIESCE = 0
    ALLOW_VMS_WITH_SNAPSHOTS_TO_BE_BACKEDUP = 0
    ENABLE_NON_PERSISTENT_NFS = 0
    UNMOUNT_NFS = 0
    NFS_SERVER = 172.30.0.195
    Nfs_mount = / nfsshare
    NFS_LOCAL_NAME = nfs_storage_backup
    NFS_VM_BACKUP_DIR = mybackups
    SNAPSHOT_TIMEOUT = 15
    EMAIL_LOG = 0
    EMAIL_SERVER = auroa.primp-industries.com
    EMAIL_SERVER_PORT = 25
    EMAIL_DELAY_INTERVAL = 1
    EMAIL_TO=auroa@primp-industries.com
    Email_from = root @ ghettoVCB
    WORKDIR_DEBUG = 0
    VM_SHUTDOWN_ORDER =
    VM_STARTUP_ORDER =

The parameters you need to adapt are:

-   ** VM \ _BACKUP \ _VOLUME ** ⇒ location of your backup datastore

-   ** VM \ _BACKUP \ _ROTATION \ _COUNT ** ⇒ number of VM backups to keep

> ** Note **
>
> You can consult
> [here] (https://communities.vmware.com/docs/DOC-8760) the documentation
> Complete ghettoVCB with a description of each parameter

> ** Important **
>
> Be careful to put the / final for the parameter
> VM \ _BACKUP \ _VOLUME otherwise the script will be in error

Backup test
==============

We will start a first initial backup of all VMs for
see if everything is ok. Subsequently we will plan it automatically.
Return to ESXi in SSH (reconnect if necessary) and do:

    /vmfs/volumes/Backup/ghettoVCB.sh -a -g /vmfs/volumes/Backup/ghettoVCB.conf

This will launch a backup of all your VMs (and can take a lot
of time). At the end you should have on your backup datastore a
folder by VM and in each VMs folder a subfolder by date
containing 4 files:

![vmware.backup2](../images/vmware.backup2.PNG)

-   \ * - flat.vmdk ⇒ the virtual disk of your machine

-   \ *. vmdk ⇒ the disk descriptor

-   \ *. vmx ⇒ the file containing the configuration of your machine

-   STATUS.ok ⇒ indicates that the backup is ok

Here is another possibility for the command line:

-   Backup simulation:

<! - ->

    /vmfs/volumes/Backup/ghettoVCB.sh -d dryrun -a -g /vmfs/volumes/Backup/ghettoVCB.conf

-   Launch in debug mode:

<! - ->

    /vmfs/volumes/Backup/ghettoVCB.sh -d debug -a -g /vmfs/volumes/Backup/ghettoVCB.conf

-   Backup only VM "foo"

<! - ->

    /vmfs/volumes/Backup/ghettoVCB.sh -m foo -a -g /vmfs/volumes/Backup/ghettoVCB.conf

Automatic launch of backups
=================================

You have to add the command line to the crontab but under VMware the
Crontab is a little special and especially crushed at each start. For
avoid this so add a little script that will update the
crontab at boot (do not worry it's pretty simple and fast), in
SSH on the ESXi do:

    vi /etc/rc.local.d/local.sh

And before the "exit 0" add the following lines:

    / bin / kill $ (cat /var/run/crond.pid)
    / bin / echo "0 0 1 * * /vmfs/volumes/Backup/ghettoVCB.sh -a -g /vmfs/volumes/Backup/ghettoVCB.conf> / dev / null 2> & 1" >> / var / spool / cron / crontabs / root
    / usr / lib / vmware / busybox / bin / busybox crond

> ** Note **
>
> Here I request a backup every 1st of the month, you can change
> this by modifying: 0 0 1 \ * \ *

> ** Note **
>
> Here I make a backup of all the VMs, you can adapt this in
> replacing -a by -m ma \ _vm, be careful if you want to put
> several VMs it is necessary to duplicate the line "/ bin / echo" 0 0 1 \ * \ *
> /vmfs/volumes/Backup/ghettoVCB.sh -a -g
> /vmfs/volumes/Backup/ghettoVCB.conf &gt; / dev / null 2&gt; & 1 "&gt;&gt;
> / var / spool / cron / crontabs / root "and put one by VM to backuper

> ** Important **
>
> Do not forget to adapt the path to the configuration file of
> ghettoVCB according to your configuration:
> /vmfs/volumes/Backup/ghettoVCB.conf

Last step: you have to restart your ESXi so that the cron is taken
in account, you can see the result by doing (always in SSH):

    cat / var / spool / cron / crontabs / root

Here you must have a line:

    0 0 1 * * /vmfs/volumes/Backup/ghettoVCB.sh -a -g /vmfs/volumes/Backup/ghettoVCB.conf> / dev / null 2> & 1
