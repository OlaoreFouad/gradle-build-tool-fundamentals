### Building Java Projects

When we want to build Java projects, Gradle provides a `JAVA` plugin that provides a lot of infrastructure to help compile, test, execute and package our java sources. To add this plugin we have several options. But the most recent is:

```
    plugins {
        id 'java'
    }
```

After adding this `plugins` block, Gradle understands that this project would at some point build some Java sources. Generally, gradle seeks to find the Java files that are to be built and this follows a general convention of **src/main/java** - _for source files_ and **src/test/java** - _for test sources_. In the final _java_ folders, the package containing the code can be in the form on _com.company.companyname_.

Running `gradle build` at this point allows us compile sources and test sources, execute and package our files appropriately. The aftermath of these process can be located in the **build/classes** - _for class files_ and the **build/libs** - _for the jar files_