Goal
========

This article is intended to guide you in using Android
to talk to Jeedom. We will use the Jeedom interaction engine that
allows to formulate requests and that Jeedom responds to them (and also, if
wish, activates different scenarios or elements).

Installation
============

Prerequisites
-------------

Of course, you need an Android device (tablet, phone, PC with
microphone and speakers) and install
[Tasker] (https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm&hl=fr)
and
[Autovoice] (https://play.google.com/store/apps/details?id=com.joaomgcd.autovoice&hl=fr).
This allows you to create your own voice commands for Google Now
to automate his tasks using voice.

Note: AutoVoice is only the component to talk to Jeedom but does not
do not allow Jeedom to answer. For him to do it, no need for
Tasker plugin. This example can also be used by replacing the
voice recognition of AutoVoice by an NFC tag, a geolocation,
an SMS received ...

The principle
-----------

We will use a tasker profile on state. This one will be a
voice recognition of AutoVoice. Then in task, we will ask
Tasker to execute 2 actions. The first will be to call Jeedom and him
transmit the text result of speech recognition. The second
will be to state the return of Jeedom.

Profile creation
==================

A new profile is added with a **state** as a trigger.

![android.autovoice1](../images/android.autovoice1.png)

We select **Plugin** on the first screen.

![android.autovoice2](../images/android.autovoice2.png)

In plugin type, we select **AutoVoice**.

![android.autovoice3](../images/android.autovoice3.png)

In the **AutoVoice** sub-menu, select **Recognized**.

![android.autovoice4](../images/android.autovoice4.png)

You can save the default configuration unless you want to
specify keywords or other parameters.

![android.autovoice5](../images/android.autovoice5.png)

We can give the profile a name like "Jeedom Interactions" and the
backup will be made after linking with a task.

Task
========

A **new task** is added to the newly created profile. By
for example, it could be called "Jeedom API".

![android.autovoice6](../images/android.autovoice6.png)

The task will finally regroup 2 actions: **API call** and ** say the
return**.

![android.autovoice7](../images/android.autovoice7.png)

First we will add an action type **Network**.

![android.autovoice8](../images/android.autovoice8.png)

Then we select **Get HTTP**.

![android.autovoice9](../images/android.autovoice9.png)

There we will fill with Jeedom information. Here is the information at
enter :

-   Server: Port: `https: // mydomain.tld`

-   Path:
    `/jeedom/core/api/jeeApi.php? Apikey votreclef = & type = interact & query = UTF8 & %avcommnofilter = 1`

Do not forget to put your API key in place of the chain
`Votreclef`. You have to leave `%avcommonfilter` at the end, it will be
replaced by the return of Autovoice.

![android.autovoice10](../images/android.autovoice10.png)

Add an action of type **Say**. To do this, filter the actions in
putting "say" at the magnifying glass.

![android.autovoice11](../images/android.autovoice11.png)

And we enter `% HTTPD` in the text field.

![android.autovoice12](../images/android.autovoice12.png)

It's finish. On text recognition by AutoVoice, Jeedom will be
called and you will have the answer configured in the interactions that
will be stated by your phone. Do not forget to configure the
Jeedom interactions and you can ask him anything you
want. From "what is the temperature of the living room" to "turn on the light of the
living room".

> **Tip**
>
> If it does not work from the beginning, it's often because AutoVoice
> is not active. To do this, click on Google Now
> Integration and on the first choice at the top and allow
> AutoVoice.

> **Tip**
>
> By default, AutoVoice turns off Google Now search, it is
> possible to cancel this behavior, for that in Tasker click on
> your profile then "edition" (small pencil), then "advanced" (while
> bottom), and uncheck "Do Google Now Search" (bottom).
