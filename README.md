Jangaroo Flash Application Project Template for FlashDevelop
============================================================

For Jangaroo background information, please visit the [Jangaroo Home Page](http://www.jangaroo.net).

You need to have installed the usual Jangaroo prerequisites

1. [Java 6](http://java.sun.com/javase/downloads/) and
2. [Maven 3](http://maven.apache.org/download.html).

Note that you do not have to download and / or install Jangaroo itself!

**Checkpoint:** opening a command prompt and entering `mvn -v` should output something like

    Apache Maven 3.0.2 (r1056850; 2011-01-09 01:58:10+0100)
    Java version: 1.6.0_21, vendor: Sun Microsystems Inc.
    Java home: C:\Program Files\Java\jdk1.6.0_21\jre
    Default locale: de_DE, platform encoding: Cp1252
    OS name: "windows 7", version: "6.1", arch: "amd64", family: "windows"

Now, install [FlashDevelop](http://www.flashdevelop.org).

To set up the Jangaroo Flash Project template for FlashDevelop

1. Press the [`Downloads`](https://github.com/fwienber/jooflash-fd-project/archives/master) button at the top right of this page,
2. choose `Download .zip`, and
3. unzip the subfolder `190 ActionScript 3 - Jangaroo Flash Project` contained in the archive into the `Projects` directory of your FlashDevelop installation. (You may have to unzip to a temporary directory and copy over to the program directory to be asked for admin rights.)

Then, you can create Jangaroo HTML5 Flash Applications from FlashDevelop using

1. `Project | New Project...`
2. Select `Jangaroo Flash Project` from the list.
3. Fill in desired `Name`, `Location` and `Package` of your new project.

   Please do not leave the `Package` field empty, or `jooflash.html` will not point to the correct Main class!

   You usually want to check `Create directory for project`.

![screenshot](https://github.com/fwienber/jooflash-fd-project/raw/master/FlashDevelop-Jangaroo-Flash-Project-Screenshot.png "Dialog for creating a Jangaroo project in FlashDevelop")

Now you can build the project using the `Build Project` toolbar button. Maven is invoked and comiles and builds your Web application. Then, a browser is opened at `http://localhost:8080/jooflash.html#joo.debug`. For this to work, you have to start a local Web server serving your Web app in three simple steps:

1. In FlashDevelop, select the file `pom.xml` in the `Project` window.
2. By clicking the `Command Prompt` button, a command window opens with your project root directory as the current path.
3. Enter `mvn jetty:run`. After Jetty has been started, the URL opened on `Build Project` should display `Hello World!`.

Now you can edit source code, click `Build Project`, and watch the result in the browser window. If changes do not appear, try clearing the browser cache.

For debugging, please have a look at the [Jangaroo debugging tutorial](http://www.jangaroo.net/tutorial/debugging).