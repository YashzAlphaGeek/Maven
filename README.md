# Maven

## Maven Project
+ Maven has the ability to download dependencies automatically based on the dependencies block you put in respective maven project’s pom.xml file.Maven is a powerful project management tool that is based on POM (project object model). It is used for projects build, dependency and documentation.POM is an acronym for Project Object Model. It contains information about project and configuration of the project such as dependencies, build directory, source directory, test source directory, plugins, goal, etc. Maven reads pom.xml and then executes goal.
+ Open Source Build Tool developed by the Apache Group
+ Take cares of the Builds, Dependencies, Reports, Distribution, Releases & Mailing List
+ Helps in getting the right JAR files for each project from (mvnrespository.com)

## Maven Core Concepts:

### Project Object Model
The Project Object Model File(also called as pom.xml) contains the meta-data of the project and is also responsible to manage dependencies and to configure plugins which helps us in automating many repetitive tasks.

### Maven Advantages

![](https://github.com/YashzAlphaGeek/Maven/blob/master/Maven%20Pics/Maven%20Advantages.png)

### Maven Architecture

![](https://github.com/YashzAlphaGeek/Maven/blob/master/Maven%20Pics/Maven%20Architecture.png)

### Maven Plugins
+	Plugins enable us to run the lifecycle phases in our Maven Project
+	Each Plugin is associated with a GOAL, which is linked to the lifecycle phase
+	Plugins can be defined inside <plugin> section, under the <build> tag

### Maven Compiler Plugin
+	Compiles out java files, similar to running javac <java-class-name>

<pre><code>
groupId = org.apache.maven.plugins
artifactId = maven-compiler-plugin
</pre></code>

<pre><code>
mvn compiler: compile
mvn compiler: testCompile
</pre></code>

![](https://github.com/YashzAlphaGeek/Maven/blob/master/Maven%20Pics/Compiler%20Plugin.png)


### Maven Surefire Plugin
+ Runs Unit Test inside our Project and also generates Test Reports

<pre><code>
groupId = org.apache.maven.plugins
artifactId = maven-surefire-plugin
</pre></code>

<pre><code>
mvn clean test
</pre></code>

![](https://github.com/YashzAlphaGeek/Maven/blob/master/Maven%20Pics/SurfirePlugin.png)

### Maven Install Plugin
+ Packages source code into an artifact and installs it into the Local Repository

<pre><code>
groupId = org.apache.maven.plugins
artifactId = maven-install-plugin
</pre></code>

<pre><code>
mvn clean install
</pre></code>

![](https://github.com/YashzAlphaGeek/Maven/blob/master/Maven%20Pics/Installer%20Plugin.png)

 
### Maven Deploy Plugin
+ Deploys the created Artifact into the Remote Repository

<pre><code>
mvn clean deploy
</pre></code>

### Maven Multi-Module Project
We have a parent project (parent POM) that contains different sub-projects (sub-modules), each of which is again a normal Maven Project.

![](https://github.com/YashzAlphaGeek/Maven/blob/master/Maven%20Pics/MultiModuleProjects.png)

The parent POM usually encapsulates the other child’s and that’s why it is packaged as a POM instead usual packaging format of JAR.
 
### Profiles
Profiles can be used in Maven to create customized build configurations. This means customizing the behavior of our builds based on specific conditions.

<pre><code>
mvn -Pskip-test clean install
</pre></code>

![](https://github.com/YashzAlphaGeek/Maven/blob/master/Maven%20Pics/Profiles.png)
