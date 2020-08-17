# Gradle Plugins

At this point, I had created my <a href="https://github.com/OlaoreFouad/gradle-build-tool-fundamentals/tree/master/First%20Steps%20with%20Gradle">first task</a> with gradle, I ran the task and also issued the build command to build my file. I then took a look at the concept of _Plugins_. Gradle allows usage of plugins to define custom behaviour to our build system and provide support for external entities. In this case, I made use of the _java_ plugin.

## Using the Java Plugin

At the top of your _build.gradle_ file, add:

```
    apply plugin: 'java'
```

By doing this, we are telling gradle to apply the Java plugin and consider it when building our project (a java-based project). If we have a java project, and this plugin is applied, when we issue our `gradle build` command, Gradle automatically kick-starts the build process by generating class files, running unit tests and among others.

An updated way of applying plugins in written as such:

```
    plugins {
        id 'java'
    }
```
