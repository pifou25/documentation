Finding the ID of the remote control
====================================

Go to "Plugins", "Plugin Management", "RFX COM"
-------------------------------------------------- ----

![image07](../images/volet.ematronic/image07.png)

In "RFXcom protocol management",
-------------------------------------

![image04](../images/volet.ematronic/image04.png)

check Protocol 8, BlindsT1, Save and exit.

![image08](../images/volet.ematronic/image08.png)

Enable, "Start in debug mode"
-------------------------------

![image03](../images/volet.ematronic/image03.png)

Wait for the window to open, then press the Open button
your Ematronic remote control.

    MainThread - rfxcmd: 2765 - DEBUG - Test message: 09 19 03 01 1F 84 B9 01 01 60
    MainThread - rfxcmd: 2805 - DEBUG - Message OK
    MainThread - rfxcmd: 328 - DEBUG - Verified OK
    MainThread - rfxcmd: 334 - DEBUG - PacketType: 19
    MainThread - rfxcmd: 338 - DEBUG - SubType: 03
    MainThread - rfxcmd: 342 - DEBUG - SeqNbr: 01
    MainThread - rfxcmd: 346 - DEBUG - Id1: 1F
    MainThread - rfxcmd: 350 - DEBUG - Id2: 84
    MainThread - rfxcmd: 359 - DEBUG - Verify correct package length
    MainThread - rfxcmd: 556 - DEBUG - Save packet to log_msgfile

Find the ID of the remote control
-------------------------------------

Note: Ematronic remotes always start with: 09 19 03
therefore the area we are interested in starts from "Test message": 09 19 03.

Locate: Id1 and Id2 and add the following hexadecimal: in my example
Id1 = 1F and Id2 = 84. so you have to spot them in the line, "Test
message "and extract the Id3, here Id3 = B9, ​​Our remote has so
as ID ⇒ 1F84B9.

Stop the Debug Mode by the "Stop / Restart daemon" button
-------------------------------------------------- ---------------

![image06](../images/volet.ematronic/image06.png)

Creation of the remote control under JeeDom
=======================================

Go, in Plugins, Home Protocol, RFXcom.

![image10](../images/volet.ematronic/image10.png)

Click on "Add" and enter a name for your remote
Virtual.

![image00](../images/volet.ematronic/image00.png)

Choose from the list of equipment the template: "Ematronic shutter -
Default ".

Replace the automatic ID with the one you previously extracted
and check "Enable" and "Visible":

![image11](../images/volet.ematronic/image11.png)

Click on "Save" to save your configuration and
load the template "Ematronic shutter - Default".

![image02](../images/volet.ematronic/image02.png)

That's your remote is ready, it must look like this:

![image05](../images/volet.ematronic/image05.png)

Associate your JeeDom virtual remote control with your Ematronic engine:
================================================== ====================

Reset the engine:
---------------------------

-   Electrically disconnect the motor.

-   On the original remote, leave the "Up" button pressed 3 or 4
    seconds, the led becomes red steady.

-   Electrically connect the motor.

-   Release the button on the remote control.

-   The engine will make 5 beeps.

-   Quickly, press with a trombone on the "micro button" a
    the back of the remote control.

-   The engine will make 3 beeps.

Association of the JeeDom virtual remote control with the Ematronic engine:
================================================== ==================

-   Electrically disconnect the motor.

-   On the original remote control, leave the "Up" button Press 3 or 4
    seconds, the led becomes red steady.

-   Electrically connect the motor.

-   Release the button on the remote control.

-   The engine will make 5 beeps.

-   Press the "Up" command on the virtual remote control
    JeeDom. Image :: ../ images / volet.ematronic / image09.png \ [\]

-   The engine will make 3 beeps, to announce that your JeeDoom is associated
    !!


