java c
Lab #1
CSCI 201
Environment Setup
Introduction
This lab document will go over the steps to install and set up Eclipse, which is a Java
integrated development environment (IDE). Once set up, some important things will be covered, such as creating a new Java Project, exporting a Java Project, and importing an existing Java Project.
I realize this lab seems really long, but the installation should not take that much time, and the length of this document is based on the screenshots and detailed tutorial we have
provided.If you have programmed in Java and have used Eclipse before, please follow the guide anyway. There are some important steps that will ensure you are able to submit your  homework assignments properly.
Part 1 – Downloading and Installing Java and Eclipse Download JavaTo be able to program in Java, it is necessary to have a Java Development Kit (JDK). For JRE 21 [our recommended version for compatibility with the latest version of Eclipse], you can find the download links here:
https://www.oracle.com/java/technologies/downloads/#java21
Depending on your platform, select either the Windows x64 Installer (.exe) or the macOS Installer (.dmg). Make sure that the software to be downloaded is the JDK Development Kit 21.0.4.
Installing multiple JREsIt is possible to install multiple JVMs (aka JREs) on the same machine and allow Eclipse to use all of them on different projects. The JVM that we support for this class are 14,  17, and 21.
Java 14 is available here:
https://www.oracle.com/java/technologies/javase/jdk14-archive-downloads.html
JRE 17 is available here:
https://www.oracle.com/java/technologies/downloads/#java17
All the versions from 17 and up include JREs for Windows, Linux and macOS for ARM (aka Apple Silicon) and x86 platforms.  See below an example.

On macOS, the JREs are installed in /Library/Java/JavaVirtualMachines. On
Windows it is normally installed in C:\Program Files\Java. The following snapshot assumes JRE 14, 17 and 21 are installed.

Later in this document, you will see how to make all the multiple JRE visible in Eclipse.
Install JavaDouble click on the downloaded ZIP or dmg. First you will have to accept the Oracle Technology Network License Agreement.  Check the box and click on the Download jdk-21.0.x … button (these snapshots still show JDK 14).

You are now prompted to enter your credentials for an Oracle account. Enter your Username and Password and click Sign in or click Create Account.


On Windows, look for the  .exe file at the bottom left of the window for the progress of the download. On macOS, look at the  .dmg file in the download folder.

Windows

macOS
On Windows, click on Open file. You will be asked to “allow this app to make changes to your device.” Click Yes.

On macOS, double-click the  .dmg file to start it. A finder window appears
displaying the JDK volume that contains an icon of an open box and the name of the  .pkg file. Double-click the  .pkg icon to start the installation application.

The installation wizard will now start with the Welcome page (Setup on
Windows and Introduction on macOS). On Windows, click Next >. On macOS click Continue.

Windows

macOS
The next step in the wizard selects the Destination (Folder on Windows, Select on macOS), and will indicate where Java SDK will be installed, as in C:\Program Files\Java\jdk-xx.y.z\ for Windows. Note this path, as it will be used in the
Tomcat installation. You do not need this information for macOS Tomcat installation.
On Windows click Next, then click Install.

On macOS, when the Installation Type window appears, click Install.

On macOS, a window appears that displays the message: Installer is trying to install new software. Enter your password to  allow this. Enter the Administrator username and password and click Install Software.
Once the installation has completed, the Complete screen (Windows) or
Summary screen (macOS) of the wizard will display, hopefully with a message of “JDK xx.y.z Successfully Installed.” Click Close.

Windows

macOS
To verify proper installation, open a Command window in Windows and a
Terminal window in macOS, and at the prompt type: java -version and you  should see the correct version (like “14.0.2” or “17.0.0” or “21.0.1”) displayed.

Windows

macOS
Download and Install Eclipse
For this class, you will be programming in Eclipse. You can find the download links here:https://eclipse.org/downloads/
Windows:
For Windows users, it doesn’t really matter whether you pick the 32-bit or 64-bit version of Eclipse. However, make sure that you match the JDK and Eclipse. 32-bit goes with x32, and
64-bit goes with x64. You can probably use 64-bit, unless you have a very old computer. To
find out what hardware you have, you can go to your system properties in the Control Panel. There should be some link that says something along the lines of “System” or “Properties.”
There you will see whether your hardware is 32-bit or 64-bit.
Regardless whether you picked 32-bit or 64-bit, the instructions are the same. Now that you have the files, go ahead and install them. They both should be very straightforward. The sample steps below show the dialogs for the 64-bit version of Eclipse. Select Download x86_64 as shown of the download page.

On the next page, click Download.

You will see the progress on the bottom-left of the browser windows. Once completed, click
Open file.


The eclipse installer will start, displaying the installer logo page, possibly for several minutes. Be patient.

Finally代 写CSCI 201 Environment Setup Lab #1Java
代做程序编程语言, you will see a number of different selections. Select Eclipse IDE for Java Developers.

Next you will be shown the location of the Java VM and the Eclipse Installation Folder.  Do not change these folder selections. Click on INSTALL.

Next you will be shown the Eclipse Foundation Software License Agreement. Click on Accept Now.

Finally, the Launch window dialog appears. Click on LAUNCH.

Eclipse will now run.
macOS:
For Mac users, pick 64-bit since it’s the only flavor offered. Select Download x86_64 or aarc64 (for Apple Silicon) as shown of the download page. Click Download.

Once the popup shows up, click Download.

You will see the progress of the download in the macOS top bar.

After the download completes, click the .dmg file, the double-click on the Eclipse Installer.

You may see a security warning: click Open.

You will see several different selections. Select Eclipse IDE for Java Developers.

Next you will be shown the location of the Java VM and the Eclipse Installation Folder.  Do not change these folder selections. Click on INSTALL.

Next you will be shown the Eclipse Foundation Software License Agreement. Click on Accept Now.

Finally, the Launch window dialog appears. Click on LAUNCH.

Eclipse will now run.
Part 2 – Running Eclipse
Windows:
Launch Eclipse!
Pick a folder to be your ‘workspace’ . This will be the directory that contains ALL of your projects and code. Make sure to remember where you put this, but as long as you don’t check that box that says, “Use this as the default and do not ask again,” you will be prompted for the workspace directory every time you run Eclipse. The default directory will be like
‘C:\Users\username\eclipse-workspace.’ Click Launch.

You will see the Starting Eclipse IDE progress bar. Then you will be shown the Welcome
screen.

macOS:
Launch the eclipse executable!
You will be asked to pick a directory to be your ‘workspace’ . This will be the directory that contains ALL of your projects and code. Make sure to remember where you put this, but as long as you don’t check that box that says, “Use this as the default and do not ask again,” you
will be prompted for the workspace directory every time you run Eclipse. We recommend that you keep the default location for the workspace: /Users/youraccount/eclipse-
workspace. Click Launch.

You will see the Starting Eclipse IDE progress bar. Then you will be shown the Welcome screen.

Part 3 – Creating a project
This tutorial will use a Windows computer, though everything is the same for macOS or Linux. Close out of the Welcome menu, clicking on the cross.

You should see the following screen. If the workspace on top bar is not ‘eclipse-workspace’, close Eclipse and restart.

Windows

macOS
Select a wizard with  File → New → Project →Java →Java Project. Click Next >.

Windows

macOS
Make sure that JavaSE-21 is selected under the JRE → execution environment JRE. Leave all other options unmodified, except uncheck the box under Module → Create module-
info.java. For the project name, use the following convention: username_CSCI201_Assignment#.
For example, if your email iscareymd@usc.edu, you would submit your Assignment1 for grading with the project name careymd_CSCI201_Assignment1.For now, go ahead and name the project username_CSCI201_Lab1. The press Finish. If you are asked to Create module-info.java, click Don’t Create. You will see the project under the Package Explorer.

Windows

macOS
Part 4 – Hello World
The time has finally come to write a program. Go to File → New… →Class.

Windows

macOS
You can name classes anything you want for homework assignments but go ahead and make a ‘HelloWorld’ class. Just type the name and press Finish.Eclipse will generate a HelloWorld.java file for us, as well as create a package in our project. Packages just correspond to directories on your file system, but they do have some significance that you’ll learn about in class.
Now we need to make a main method. Click on HelloWorld.java to display its code.

Now, insert the following code if the main() function. If the main() function was not included in the auto-generate code, add it as seen below.

You can use System.out.print(Object); to print a String to the console. You can use System.out.println(Object); to print a String followed by a newline to the console.

Now press the ‘Run’ button to execute the program!
If you are asked to Save and Launch, just click on OK.

Wait a bit, and the Console tab should appear. You should get the output “Hello World!” in the Console tab at the bottom of the window.

Part 5 – Debugging
Type the following code into your main method:

For some reason, this code doesn’t seem to work! It will run, but it throws an exception!

Windows

macOS
Let’s see what’s happening by putting breakpoints on line 6 and 7. Do this by double clicking on the left sidebar.

Click the Debug button.
Press Yes to confirm the switch from Java to the Debug perspective or click on Switch.

You will now see the Debug perspective:

We can see that s is still ‘Hello World!’, let’s resume …

We can see that right after line 6 was executed, s turned to null! (What a surprise…)
You can stop here and go back to the normal perspective by clicking ‘Java’ in the upper-right corner. 
Note: If you have breakpoints set, pressing Run will not trigger them. You MUST use Debug for the breakpoints to cause the program to stop.



         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
