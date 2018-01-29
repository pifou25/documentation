We will see here how to create a VM under VMware.

There is a little important thing to know about VMware, there is 2
way of the manager:

-   the web interface (present by default in 6.0 update 2, or by the
    vibrate for the other versions), it is accessed by
    IP \ _ESXI / ui

-   the heavy and historic VMware client (vSphere client)

Here I will mainly use the web interface because I think it's
the future of VMware, which is moving away from the heavy client
(By the way all the novelties since the 5.1 are not usable
with the heavy client).

Also note that the web interface is still being set up
at VMware, you will probably encounter some bugs or
slowdowns with but a little refreshment of the page and that
leave without worries.

Login to the web interface
===========================

Go to IP \ _ESXI / ui with your internet browser, you must have:

![vmware.createvm3](../images/vmware.createvm3.PNG)

> **Note**
>
> If you do not have anything I advise you to install
> the web interface, all the information
> [here] (https://jeedom.github.io/documentation/howto/fr_FR/doc-howto-vmware.trucs_et_astuces.html)

Enter your login credentials for ESXI:

![vmware.createvm4](../images/vmware.createvm4.PNG)

As you can see the interface is quite nice and allows to
do a lot of things, I will not go into details but you
can already from this screen:

-   stop / restart the ESXi

-   see the use of resources (CPU, memory and disk)

-   have information about your system (operating time,
    version of VMware, version of bios, display of datastores)

-   button to create a VM (we'll use it right after)

-   an action button that allows you to switch to maintenance mode
    (practical if you have an ESXi cluster otherwise you do not
    will never serve), enable / disable SSH service (is used
    in the backups configuration tutorial)

Sending the installation iso
=============================

After downloading your installation iso
([Here] (http://cdimage.debian.org/debian-cd/8.5.0/amd64/iso-cd/debian-8.5.0-amd64-netinst.iso)
for example for debian 8.5 in netinstall), you have to put it on
your datastore.

For this click on datastore:

![vmware.createvm18](../images/vmware.createvm18.PNG)

Select your datastore (usually it's called datastore1):

![vmware.createvm19](../images/vmware.createvm19.PNG)

Click on "Datastore Browser":

![vmware.createvm20](../images/vmware.createvm20.PNG)

Click on "Download" (the first):

![vmware.createvm21](../images/vmware.createvm21.PNG)

Select the iso previously downloaded and validate:

![vmware.createvm22](../images/vmware.createvm22.PNG)

You can then follow the progress of the shipment:

![vmware.createvm23](../images/vmware.createvm23.PNG)

Once finished you can see that your iso has arrived on the
datastore:

![vmware.createvm24](../images/vmware.createvm24.PNG)

Creating your first VM
=============================

Click on the "Create / Save VM" button:

![vmware.createvm5](../images/vmware.createvm5.PNG)

Click Next:

![vmware.createvm6](../images/vmware.createvm6.PNG)

Then give a name to your machine and specify its system
operating (here we will install a Debian):

![vmware.createvm7](../images/vmware.createvm7.PNG)

Indicate the target datastore:

![vmware.createvm8](../images/vmware.createvm8.PNG)

Here you will be able to configure the parameters of your machine (disk
hard, CPU, memory ...):

![vmware.createvm9](../images/vmware.createvm9.PNG)

> **Note**
>
> All these parameters can be modified afterwards without any problem, to note
> all the same that it is not really possible to reduce the size
> of a hard disk, we can increase it (but we have to know how to manage it at
> OS level next) but not reduce it.

At the CD / DVD player, select "ISO Bank File"
data ":

![vmware.createvm10](../images/vmware.createvm10.PNG)

Then select the location where your ISO is stored (see
previous chapter) and confirm:

![vmware.createvm11](../images/vmware.createvm11.PNG)

Then do next:

![vmware.createvm12](../images/vmware.createvm12.PNG)

Then you have a summary of your configuration, click on
"Finish":

![vmware.createvm13](../images/vmware.createvm13.PNG)

A message at the top will tell you that it's good, then click on
"Virtual Machines":

![vmware.createvm14](../images/vmware.createvm14.PNG)

You must see your virtual machine (if it is not the case click
on "Refresh") click on it:

![vmware.createvm15](../images/vmware.createvm15.PNG)

You must have a page like this, click on the play button:

![vmware.createvm16](../images/vmware.createvm16.PNG)

Your machine will launch and you will be able to install
your OS:

![vmware.createvm17](../images/vmware.createvm17.PNG)

> **Important**
>
> Once your machine is installed, ABSOLUTELY install them
> VMware tools (this allows VMware to have information about your VM
> and extinguish it properly). Under debian just do
> "sudo apt-get -y install open-vm-tools".

For the rest of the installation I invite you to read this
[Tutorial] (https://jeedom.github.io/documentation/howto/fr_FR/doc-howto-debian.installation.html#_installation)

Mount USB peripherals in the VM
=======================================

> **Note**
>
> If you do not have the options below it is necessary to put in
> day the ESXi Embedded Host Client, all the information
> [here] (https://jeedom.github.io/documentation/howto/fr_FR/doc-howto-vmware.trucs_et_astuces.html)

It's a pretty rare need, but I had to use it for Jeedom, in
effect I have on my ESXi the keys Zwave, RFXcom, edisio, enOcean and GSM
connected and I had to connect them to my VM Jeedom to be able to
use it.

> **Note**
>
> For Zwave, RFXcom, edisio and enOcean there is no problem, for
> GSM keys you have to follow this
> [tutorial] (https://jeedom.github.io/documentation/howto/en_US/doc-howto-gsm.huawei_mode_modem.html)
> before to force the key in modem mode only if it is not
> not seen correctly on the ESXi.

Go to your VM then do "Change settings":

![vmware.createvm25](../images/vmware.createvm25.PNG)

Click on "Add another device" then USB controller:

![vmware.createvm26](../images/vmware.createvm26.PNG)

> **Note**
>
> The following step should be repeated for each USB device that
> you want to connect

Save, redo "Change settings", then "Add another
device "and" USB device ":

![vmware.createvm27](../images/vmware.createvm27.PNG)

Choose your USB device from the drop-down list:

![vmware.createvm28](../images/vmware.createvm28.PNG)

And here your device is plugged into your VM. Every
restart it will be auto reconnected to the VM and if you
physically disconnect / connect then it will be reconnected to
your VM. In other words the use is now totally
transparent.
