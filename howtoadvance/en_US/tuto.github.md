This tutorial presents:

-   Creating a GitHub account

-   Jeedom Core Fork or Documentation

-   Editing one or more files

-   Submit a change

-   Updating your fork

To enable you to contribute to Jeedom, you will need to
propose the modifications (PR: Pull Request).

Creating a GitHub account
===========================

We will discuss in this tutorial how to create a GitHub account,
in order to be able to trace bugs (issue in the language GitHub) or
even propose corrections (Pull Request or PR in github language)
for the entire Jeedom project, including its free plugins or the
documentation, or any other github project that you
would like to participate.

Go to <https://github.com> and click on the sign up button.
So you should be on a page similar to the one below and
must fill in a username, an email and a password and then
click on **Create an account**

![tuto.github1](../images/tuto.github1.png)

So you arrive on a 2nd page as below and you do not change
nothing, you click **Continue**

![tuto.github2](../images/tuto.github2.png)

Here you are registered and on the options configuration page of your
account. I advise you to check the email address in order to be able to
recover your account in case of forgotten password for example but
also in order to be able to submit changes. I leave you
also discover the other options if you are curious.

![tuto.github3](../images/tuto.github3.png)

Jeedom Core Fork or Documentation
==========================================

**Fork - Why - How**

Fork is copying a project into your github space, so you can
edit code files, documentation and then submit
a Pull Request to the original project, which will then be studied by the
developer (s) of the said project

Now that you have a Github account and you are identifying
with your verified email address, if you go here
<https://github.com/jeedom/core> you are on the jeedom project, at
right there is a fork button allowing you to copy it into your
github space.

![tuto.github4](../images/tuto.github4.png)

Editing one or more files
---------------------------------------

In my case, I want to push a modification on the file
* history.class.php * This file is located in the core of jeedom and more
precisely here: core / class /

1.  So we are on my repository (TaGGoU91 / core) which is indicated as
    being a fork of Jeedom / core

2.  So we go to / core / class (the first core is in bold, it's
    the deposit where I am (core, cf Petit 1)

3.  So we have our file * history.class.php * - We click on the
    file

![tuto.github5](../images/tuto.github5.png)

1.  So we are in our file

2.  Click on the pencil to enter a modification

![tuto.github6](../images/tuto.github6.png)

In order to search the file, position yourself in the block
text of the file that we just opened in edit mode with the pencil and
we do a "Ctrl + F" to activate the search. You stick or
specify the text you are looking for (a significant element and a
line only, not a whole block at a time). Confirm with "Enter" for
start a reseach.

> **Tip**
>
> If you do not click in the window containing the text or code
> what you are looking for is the browser search that will open and
> in my case, on Google chrome, it does not know how to do research
> in the code or documentation directly.

1.  The field of research, yes it's pretty thin as information, the
    copied line is much larger;).

![tuto.github7](../images/tuto.github7.png)

1.  In yellow, it is the result of research

2.  In blue, what I just selected and that I wish
    edit / replace with my code. My modification

![tuto.github14](../images/tuto.github14.png)

I delete the block then I replace it.

Then, on the bottom part we find this: 1. We indicate a title
explicit if possible 2. Enter a more specific description
(in my case, it would be too long, the link to the forum will be more
speaking) 3. Make sure it's checked like this 4. On commit =
Submit the change

![tuto.github8](../images/tuto.github8.png)

Submit a change
--------------------------

The **commit** done above only concerns the project fork in
your GitHub space. To submit to the original project the changes,
you have to make a PR (Pull Request)

1.  Click on Pull Request tab

2.  New Pull Request (PR for intimates)

![tuto.github9](../images/tuto.github9.png)

1.  The PR will launch a copreship between the jeedom base with your
    repository (the fork).

2.  This indicates the changes (the first is because I am
    have been updated since jeedom, the second one about
    lastchangestateduration function change, perfect !!!)

3.  The old code

4.  The new code

5.  We create the Pull Request (PR)

![tuto.github10](../images/tuto.github10.png)

It is important to explain the changes submitted so that the (s)
developer (s) of the original project understand and can validate your
request.

1.  We click on the three small dots

2.  We copy the information that we previously entered

3.  Ditto, we copy (hence the use of ... in step 1 to
    avoid a rewrite)

4.  We click on Create Pull Request

![tuto.github11](../images/tuto.github11.png)

**It's finished.** You have to wait for your PR to be validated.

NB: Only users with a push right on jeedom who
can validate the PR.

To make sure your change is in the list, you
can click on Pull Requests

![tuto.github12](../images/tuto.github12.png)

We obtain the list of the PRs in expectation of validation One sees well the
our

![tuto.github13](../images/tuto.github13.png)

Updating your fork
============================

To complete
