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
- Gradle task = Maven goal

# Gradle features
1. Incremental builds: meaning its reusing and optimizing the old builds compiling only changed files making it faster.
2. Gradle daemon: running process in the background making use of repeatable builds.

# Gradle advantages
1. Faster than maven
2. Concise build script
3. Easier to customize
4. Promotes build code reuse

# Gradle disadvantage
1. DSL specific (Domain Specific Languange): meaning its written in either groovy or kotlin so if you dont know these languange leads to steep learning curve.
2. 

# Gradle files
- build.gradle: It is gradle build script file (groovy or kotlin)  
- gradlew: It is a wrapper to run Gradle in Linux & Mac OS machine  
- gradlew.bat: It is a wrapper to run Gradle in Windows  
- settings.gradle: To configure global settings of gradle project  

# Project build process steps;
1. Download required dependencies
2. Add dependencies to project build path
3. Compile the project source code
4. Execute unit test cases
5. Package project as jar or war file (Executable artifact)
