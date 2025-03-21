# Topic outlines
- What is build tool
- Why we need build tools
- Maven vs Gradle
- Gradle Setup
- Creating gradle projects
- Gradle projects folders
- Build scripts and tasks
- Adding dependencies
- Adding repositories
- Gradle wrapper
- Building java projects
- Conclusion

# What is build tool
- Build tool is used to convert project source code into executable file

# Gradle
- Has taken advantages of both maven and ant
- Release in 2007, stable release came in 2009
- Written in groovy language
- Makes project build automation process easy
- Large projects uses Gradle such as; Hibernate and Spring because of faster builds
- in Gradle it was build.gradle and in maven it was pom.xml
- Everything is called task.

build.gradle: It is gradle build script file (groovy or kotlin)
gradlew: It is a wrapper to run Gradle in Linux & Mac OS machine
gradlew.bat: It is a wrapper to run Gradle in Windows
settings.gradle: To configure global settings of gradle project

# Project build process steps;
1. Download required dependencies
2. Add dependencies to project build path
3. Compile the project source code
4. Execute unit test cases
5. Package project as jar or war file (Executable artifact)

# Gradle commands
gradle init: initialize gradle project
gradle compileJava: compiles the project java files
gradle build: Compiles + Unit tests + Package the project
gradle run: executes the main class

# Gradle structure
====== build.gradle ======
plugins: for plugins needed for your project
dependencies:
- implementation: meaning dependencies required for compile time and runtime
- testImplementation: meaning dependencies required for testing environment

repositories: This is where gradle look, get, and download the dependencies you specify
jar: used to configure the name of your generated jar file

```
plugins {
	id 'java'
}

sourceCompatibility = 21
targetCompatibility = 21

repositories {
	mavenCentral()
}

dependencies {
	implementation 'mysql-connector-j'
	testImplementation 'junit'	
}

jar {
	archieveBaseName = 'yourJarAppName'
	archieveVersion = '1.1'
}
```