Not really a howto here but more a collection of tips and tricks on
VMware

Add your license
==================

Once connected to the web interface (IP \ _ESXI / ui) you have to go to
"Manage":

![vmware.tips](../images/vmware.tips.PNG)

Then on "Licensing" and click on "Licensing"

![vmware.tips2](../images/vmware.tips2.PNG)

And enter your license key

![vmware.tips3](../images/vmware.tips3.PNG)

> ** Note **
>
> As a reminder, if you do not do it your ESXi may not be able to
> operate after 60 days

Mounting an NFS datastore with a Synology
========================================

We'll see here how to mount an NFS share from a Synology on
VMware. This allows for example to put the virtual machines on the
Synology (which may have more space than ESXi) or send them
machine backups on Synology

Configuring Synology
-------------------------

You have to go to the control panel and then "Services de
files and check the box "Enable NFS":

![vmware.tips4](../images/vmware.tips4.PNG)

Then you have to click on "Shared folder", then choose the folder to
share (here Backup), click edit then "NFS Authorization" and
finally on create (here I already have one, your list to you should be
empty):

![vmware.tips5](../images/vmware.tips5.PNG)

Then you put the IP of your ESXi and in "Squash" you put
"Map all users to admin" and confirm:

![vmware.tips6](../images/vmware.tips6.PNG)

Then you have to recover the share path (here / volume2 / Backup):

![vmware.tips7](../images/vmware.tips7.PNG)

Here it is finished on the side Synology, we will now pass ESXi side

Configuring the ESXi
-----------------------

You have to go to "Storage":

![vmware.tips8](../images/vmware.tips8.PNG)

Then click on "New database":

![vmware.tips9](../images/vmware.tips9.PNG)

There you select "Mount an NFS Databank" and then make
following :

![vmware.tips10](../images/vmware.tips10.PNG)

Enter the name of the datastore to be created (be careful to avoid spaces and
special characters), put the IP of our Synology and put the path
sharing (see above) and finally validate:

![vmware.tips11](../images/vmware.tips11.PNG)

Click on finish:

![vmware.tips12](../images/vmware.tips12.PNG)

And here is your new datastore should appear (otherwise click on
"Update").

Adding the VAAI Synology plugin for NFS mount
==============================================

Adding this plugin allows you to enable hardware acceleration on
NFS mounts (for explanation see
[Here] (http://www.virtual-sddc.ovh/exploiter-les-vaai-nfs-avec-un-nas-synology/))

To see if you have it, you have to connect with the heavy client
(I did not find the info on the web client) and go to configuration →
storage:

![vmware.tips13](../images/vmware.tips13.PNG)

The implementation is quite simple, first you have to activate the service
SSH of the ESXi (on the web interface it is necessary to go into action ⇒ services
⇒ Enable Secure Shell), then connect in SSH on them (the
identifiers are the same as to access the interface). Then he
you just have to do:

    esxcli software vib install -v https://global.download.synology.com/download/Tools/NFSVAAIPlugin/1.0-0001/VMware_ESXi/esx-nfsplugin.vib -f

You must have :

![vmware.tips14](../images/vmware.tips14.PNG)

Then you have to restart the ESXi, to check that it is ok it is necessary
then return with the heavy client in configuration → storage:

![vmware.tips15](../images/vmware.tips15.PNG)

Install / Update the ESXi Embedded Host Client
================================================== =

ESXi Embedded Host Client is a web interface (in HTML5) of ESXi that
In 95% of cases it is possible to do without the heavy client. She is here
default in version 6.0 update 2, but in version 1.0, it is
strongly advised to update it.

You will find all the information
[Here] (https://labs.vmware.com/flings/esxi-embedded-host-client)

To see if you have the web interface, just go with
your browser on IP \ _ESXI / ui if you have nothing you need
to install it, you must first connect in SSH on the ESXI then do:

    esxcli vib software install -v http://download3.vmware.com/software/vmw-tools/esxui/esxui-signed-latest.vib

If you already have it, to update it you have to do:

    esxcli software vibration update -v http://download3.vmware.com/software/vmw-tools/esxui/esxui-signed-latest.vib

Installing the heavy client
============================

This part is optional if you do not need to manage USB.

You have to go, with your internet browser, on the IP of the ESXi
then click on the "Download vSphere Client for Windows" link:

![vmware.createvm](../images/vmware.createvm.PNG)

Once downloaded you just have to start the installation (I pass
voluntarily on this part because it is enough to validate everything).

Then launch VMware vSphere Client, you must have:

![vmware.createvm1](../images/vmware.createvm1.PNG)

You just have to enter the IP of your ESXi, the username and the
password and here you are connected on:

![vmware.createvm2](../images/vmware.createvm2.PNG)

Update ESXi
=====================

The procedure is quite easy, you must first recover the patch
by going [here] (https://my.vmware.com/group/vmware/patch#search) (there
you will probably need to log in with your VMware account). On the
list "Select a Product" put "ESXi (Embedded and Installable)", in
face leave the latest version of VMware and do "Search". Then
download the desired patch (usually the last one). The build number
first number not the one starting with KB) gives you the version of
patch that you can compare with your build number.

Then transfer the zip to one of your datastores and do:

    esxcli software vib update -d /vmfs/volumes/576c8ab3-fdf64d2f-091b-b8aeedeb87fb/ESXi600-201605001.zip

> ** Note **
>
> Replace the path and the name of the zip well according to your
> configuration

> ** Important **
>
> Be careful to put the full path to the zip otherwise it does not
> not walk

The command above only updates the vib which needs it but
you can force the installation of all the vib of the package (so
watch this can do a downgrade) by doing:

    esxcli software vib install -d /vmfs/volumes/576c8ab3-fdf64d2f-091b-b8aeedeb87fb/ESXi600-201605001.zip

NTP configuration
====================

By default the ESXi does not use the NTP so that it is not
time and that the VMs are not on time, to correct it is very
simple. You have to go from the web version on Manage → System →
Date and time, there you click on "Change settings":

![vmware.tips16](../images/vmware.tips16.PNG)

And in the box "Server NTP" you have to put: 0.debian.pool.n,
1.debian.pool.n, 2.debian.pool.n, 3.debian.pool.n, time.nist.gov

![vmware.tips17](../images/vmware.tips17.PNG)

Then in Actions → NTP Service → Strategy click on "Start and
stop with the host ":

![vmware.tips18](../images/vmware.tips18.PNG)

Still in Actions → NTP Service click on "Start"

This is your ESXi should take the right time alone now.

External access to ESXi
========================

To access the ESXi from the outside you need:

-   open port 443 to 443 of the ESXi

-   open port 902 to 902 of the ESXi

And that is all. Small tip if you have a Synology NAS you
can do (be careful to follow):

-   open the 443 to the Synology NAS 5001

-   open the 80 to the 80 of the NAS (useful just to generate the
    certificates let's encrypt)

-   open port 902 to 902 of the ESXi

Then on the NAS in the control panel then portal
application and proxy reversed (be careful it must be DSM 6):

![vmware.tips19](../images/vmware.tips19.PNG)

Click create and put:

![vmware.tips20](../images/vmware.tips20.PNG)

In "Hostname" (at the source level) you have to set the desired DNS
(eg monesxi.mondsn.synology.me) and in "Hostname" (at the level of
of the destination) it is necessary to put the IP of the ESXi

> ** Note **
>
> You can also do the same thing to access jeedom but
> putting this time the ip of jeedom (of the vm if you are in
> virtualized) and port 80

> ** Note **
>
> Once you have done this and if your DNS points correctly
> on the NAS you can generate a valid SSL certificate for free
> with Let's encrypt, going into Seclusion ⇒ certificate and doing
> add. Then do not forget to click on configure to
> assign it to your inverted proxy

Then to access your ESXi you just need with your browser
to go to your external DNS or IP by adding / ui to the end and that's
good.

> ** Important **
>
> If you go through the reverse proxy of the NAS console web mode of
> VMs does not work (because it goes through websocket), however
> if you go through VMware Remote Console everything should be ok (this
> goes through port 902)

> ** Note **
>
> There is also a Vmware Watchlist application on Android for
> have access to the ESXi as well as to the VM consoles

SSL Certificate
==============

It is possible to import vmware certificates directly into
your pc to no longer have the alert.

In order, you must:

-   have an url (dns) access to your esxi, here we will take
    esxi1.lan

-   configure the name of your esxi, in ssh above do:

<! - ->

    esxcli system hostname set --host = esxi1

-   configure the fqdn:

<! - ->

    esxcli system hostname set --fqdn = esxi1.lan

-   Recover the root certificate of the esxi, it is in
    /etc/vmware/ssl/castore.pem

On post made right click then install the certificate, put it in
"Trusted Root Certification Authority"
