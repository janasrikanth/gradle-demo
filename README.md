##### https://spring.io/guides/gs/gradle/ #####
Gradle: Gradle is a build automation tool for multi-language software development. It controls the development process in the tasks of compilation and packaging to testing, deployment, and publishing. Supported languages include Java, C/C++, JavaScript

Gradle Tasks:
test: The test task automatically detects and executes all the unit tests in the test source set., Once the test execution is complete, it also generates a report. JUnit and TestNG are the supported APIs. The test task provides a Test.
$ gradle test
$ gradle myTask
Executing Multiple Tasks:

You can also specify multiple tasks. For example, the following will execute the test and deploy tasks in the order thatthey are listed on the command-line and will also execute the dependencies for each task.

$ gradle test deploy

Gradle Wrapper:

The vast majority of developers using Gradle use the Gradle Wrapper. This is great because using the Gradle Wrapper means that developers working on the project don’t need to manage their own Gradle installations.

First install Gradle on your machine, then open up your project directory via the command line. Run gradle wrapper and you are done! You can add the --gradle-version X.Yargument to specify which version of Gradle to use.

Command:
$ gradle wrapper --gradle-version 6.0.1

Now you can run any Gradle task in your project using the gradlew shell script or bat file located in your project’s root directory.

The Gradle Wrapper consists of a few files in your project directory:

gradlew: The shell script Unix users can run to execute Gradle tasks
gradlew.bat: The bat script Windows users can run to execute Gradle tasks
gradle/wrapper/gradle-wrapper.jar The wrapper’s executable JAR; this is where the wrapper code resides
gradle/wrapper/gradle-wrapper.properties A properties file for configuring the wrapper

You should make sure all these are committed to version control. They are all small, system-independent, and critical tousing the Gradle Wrapper.

