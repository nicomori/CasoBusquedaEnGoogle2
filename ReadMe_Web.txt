fffffvvvffffffbbbllllbbbbnnnnnnvvvvvvvvvvvvccccccfffffffffffffdddddffff
asdsdsdsdsssfffjjdddddfffffff33332222erfergefgergergsdsdsddedwdedhhhasdasdasdasfffdddsssssdsdasdasdasd
sssssd
sssssss
d
bbbd
asdasd
asdcytvubbjinjhvgcg222222sdfsdfsdfsdfsdfsdmmmmmmhgfdsdfghg
xs
asdasd

sxsx

I decide to use the pattern design DSL because this pattern help to us for reuse all the methods for all the pages, this us the principal different with the page object page where you need to include all the methods in all the different pages.

For this example I use cucumber framework, maven, junit, appium, and testng.

The best idea for use all this convination of framework is create just one framework for the different platforms, Android, IOS and Web.

With that I can include of course parallel executions in real devices, in the same type of mobile real devices, this is very important for us, because we need execute the same test in different mobiles in parallel at the same time, from Jenkins and take all the reports from cucumber reports.

The architecture of the framework is very interesting. The test execute from maven calling to the POM file, this execute the testng.xml file, this call to AppTest.java class who call the Cucumber files. In the cucumber feature files you can read all the steps included in the test case, after that cucumber execute all the steps.java files where you can read all the pages called there. This pages call to all the methods stored in the DSL.java, inside of this class you can see all the methods for all the pages of all the applications in all the different platforms.

For understand better the execution is that,

POM.xml - testng.xml - AppTest.java - cucumber.feature - steps.java - pages - DSL.java 

Example of execution:
For a better understand I make a little video, in youtube of the execution of this project, please press click in the next link:

https://youtu.be/LGcwmnvWVCw

Reports:
In relation with the reports I use Cucumber plug in for Jenkins, there I can see all the steps with all the times and all the builds with error too. In Jenkins I can see too the monitors where I can see the semaphores lights for a permanent control.

Pre-Requisites:
_install JDK 8.
_install Maven.
_Setup the environments variables, this depend of your OS. 
_Firefox for execute Selenium automations, example of that is version 39. For check that, just execute the project, and if you see the Firefox don't start, you have a problem with the version of Firefox.

Setup:
_Download the project.
_from the command line, go to folder of the project.
_type "mvn clean compile" and press enter. This make the download of all the dependencies.

Execution:
_from the command line, go to folder of the project.
_type "mvn package", and press enter. Should start.
_I expect you can see in your terminal console the text "BUILD SUCCESS".

Nicolas Mori.
