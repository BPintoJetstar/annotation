# Tasks

Each project is made up of one or more tasks.
A task represents some atomic piece of work which a build performs. 
This might be compiling some classes, creating a JAR, generating Javadoc, or publishing some archives to a repository.

# Build File

Gradle’s build scripts are written in Groovy or Kotlin, not XML

# Wrapper

Gradle Wrapper allows you to execute Gradle builds on machines where Gradle is not
installed. This is useful for example for some continuous integration servers. It is also useful for
an open source project to keep the barrier low for building it. The wrapper is also very
interesting for the enterprise. It is a zero administration approach for the client machines. It also
enforces the usage of a particular Gradle version thus minimizing support issues.

# Command basics

    gradle [taskName...] [--option-name...]
    
# Demon 

A daemon is a background process used to cache information about the project, avoinding overhead.

# Migration from Maven
    
You can easily migrate from maven project just running this command from the root
    
    gradle init --type java-application
    
# Multi-Project Builds

Gradle allows multiprojects eache project with separated building file. For more hight lavel organization.

# Plugins

- Allos to extend the tool cabapilites 
- Promotes reuse and reduces the overhead of maintaining similar logic across multiple projects
- Allows a higher degree of modularization, enhancing comprehensibility and organization
- Encapsulates imperative logic and allows build scripts to be as declarative as possible

```groovy 
//Exemple of plugin declaration
plugins {
    id 'java'
    id 'java-gradle-plugin'
}
```
# Source Set

Is the process of segragationsource files, compiled files and resource  in group of same type (testing,integration and main)

# Maven, Ant and Gradel

## Ant

In many aspects, Ant is very similar to Make, and it’s simple enough so anyone can start using it without any particular prerequisites. Ant build files are written in XML, and by convention, they’re called build.xml.

Different phases of a build process are called “targets”.

Here is an example of a build.xml file for a simple Java project with the HelloWorld main class:

This will trigger target clean first which will delete the “classes” directory. After that, target compile will recreate the directory and compile src folder into it.

The main benefit of Ant is its flexibility. Ant doesn’t impose any coding conventions or project structures. Consequently, this means that Ant requires developers to write all the commands by themselves, which sometimes leads to huge XML build files which are hard to maintain.

Since there are no conventions, just knowing Ant does not mean we’ll quickly understand any Ant build file. It’ll likely take some time to get accustomed with an unfamiliar Ant file, which is a disadvantage compared the other, newer tools.

At first, Ant had no built-in support for dependency management. However, as dependency management became a must in the later years, Apache Ivy was developed as a sub-project of the Apache Ant project. It’s integrated with Apache Ant, and it follows the same design principles.

However, the initial Ant limitations due to not having built-in support for dependency management and frustrations when working with unmanagable XML build files led to the creation of Maven.

**Aint build file**
```xml
<project>
    <target name="clean">
        <delete dir="classes" />
    </target>
 
    <target name="compile" depends="clean">
        <mkdir dir="classes" />
        <javac srcdir="src" destdir="classes" />
    </target>
 
    <target name="jar" depends="compile">
        <mkdir dir="jar" />
        <jar destfile="jar/HelloWorld.jar" basedir="classes">
            <manifest>
                <attribute name="Main-Class"
                  value="antExample.HelloWorld" />
            </manifest>
        </jar>
    </target>
 
    <target name="run" depends="jar">
        <java jar="jar/HelloWorld.jar" fork="true" />
    </target>
</project>
```
## Apache Maven

Apache Maven is a dependency management and a build automation tool, primarily used for Java applications. Maven continues to use XML files just like Ant but in a much more manageable way. The name of the game here is convention over configuration.

While Ant gives the flexibility and requires everything to be written from scratch, Maven relies on conventions and provides predefined commands (goals).

Simply put, Maven allows us to focus on what our build should do, and gives us the framework to do it. Another positive aspect of Maven was that it provided built-in support for dependency management.

Maven’s configuration file, containing build and dependency management instructions, is by convention called pom.xml. Additionally, Maven also prescribes strict project structure, while Ant provides flexibility there as well.

Here’s an example of a pom.xml file for the same simple Java project with the HelloWorld main class from before:

## Gradle

Gradle is a dependency management and a build automation tool which was built upon the concepts of Ant and Maven.

One of the first things we can note about Gradle is that it’s not using XML files, unlike Ant or Maven.

Over time, developers became more and more interested in having and working with a domain specific language – which, simply put, would allow them to solve problems in a specific domain using a language tailored for that particular domain.

This was adopted by Gradle, which is using a DSL based on Groovy. This led to smaller configuration files with less clutter since the language was specifically designed to solve specific domain problems. Gradle’s configuration file is by convention called build.gradle.

Here is an example of a build.gradle file for the same simple Java project with the HelloWorld main class from befor

At its core, Gradle intentionally provides very little functionality. Plugins add all useful features. In our example, we were using java plugin which allows us to compile Java code and other valuable features.

Gradle gave its build steps name “tasks”, as opposed to Ant’s “targets” or Maven’s “phases”. With Maven, we used Apache Maven Dependency Plugin, and it’s specific goal to copy dependencies to a specified directory. With Gradle, we can do the same by using tasks:


# Reference 

[Gradle Documantation](https://docs.gradle.org/current/userguide/)
[Baedung](https://www.baeldung.com/ant-maven-gradle")

