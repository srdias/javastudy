# First test with Gradle

## Commands to install/upgrade Gradle to version 6.6 (Ubuntu 20):

```
sudo apt -y install vim apt-transport-https dirmngr wget software-properties-common
sudo add-apt-repository ppa:cwchien/gradle
sudo apt-get update
sudo apt -y install gradle
gradle -v
```
Output of command "gradle -v":
```
------------------------------------------------------------
Gradle 6.6
------------------------------------------------------------

Build time:   2020-08-10 22:06:19 UTC
Revision:     d119144684a0c301aea027b79857815659e431b9

Kotlin:       1.3.72
Groovy:       2.5.12
Ant:          Apache Ant(TM) version 1.10.8 compiled on May 10 2020
JVM:          11.0.8 (Ubuntu 11.0.8+10-post-Ubuntu-0ubuntu120.04)
OS:           Linux 4.19.104-microsoft-standard amd64
```

## Commands to start the a new application with Gradle
```
/javastudy$ mkdir gradle-fist-test
/javastudy$ cd gradle-fist-test
/javastudy/gradle-fist-test$ gradle init
```
Console output:
```
Starting a Gradle Daemon, 1 incompatible and 1 stopped Daemons could not be reused, use --status for details

Select type of project to generate:
  1: basic
  2: application
  3: library
  4: Gradle plugin
Enter selection (default: basic) [1..4] 2

Select implementation language:
  1: C++
  2: Groovy
  3: Java
  4: Kotlin
  5: Swift
Enter selection (default: Java) [1..5] 3

Select build script DSL:
  1: Groovy
  2: Kotlin
Enter selection (default: Groovy) [1..2] 1

Select test framework:
  1: JUnit 4
  2: TestNG
  3: Spock
  4: JUnit Jupiter
Enter selection (default: JUnit 4) [1..4] 1

Project name (default: gradle-fist-test): GradleFirstTest
Source package (default: GradleFirstTest):
```

After execute the commands, we will have a Java project configuration. 
You can look de Jaca class with the code in /javastudy/gradle-fist-test/src/main/java/GradleFirstTest/App.java

Command to build the project and download the dependencies:
```
gradle build
```

To run de application:
```
gradle run
```
Output:
```
> Task :run
Hello world. settingsITIALIZING [30ms]

BUILD SUCCESSFUL in 769ms
2 actionable tasks: 1 executed, 1 up-to-date
```
The text "Hello world." is implemented in the source file /javastudy/gradle-fist-test/src/main/java/GradleFirstTest/App.java
