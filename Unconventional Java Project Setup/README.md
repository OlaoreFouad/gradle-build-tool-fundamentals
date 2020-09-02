### Unconventional Java Project Setup

A common convention for the location of Java sources in a Java project. As a reminder the default format is **src/main/java** - _for source files_ and **src/test/java** - _for test sources_. Well, Gradle allows us to change this conveniently. Using a block called sourceSets, we can specify the directories gradle should look into for source files of different categories like main or tests.

```
    sourceSets {
        main {
            java {
                srcDirs 'src'
            }
        }
        test {
            java {
                srcDirs 'test/src'
            }
        }
    }
```

In the main block, we tell Gradle to look for the java sources in the **src** folder, now this would not be looking for actual java files, but for the normal package structure leading to the java files e.g com.company.companyname.

## The application Plugin

The `application` plugin is a subset of the `java` plugin and it gives one very special task to Gradle to help us run. and this is the `run` task. This task allows us run the project as a JVM project. We can get this done by running `gradle run`

## Using version numbers

We can specify the version of our projects in our build scripts by doing

```
    version = '1.0-SNAPSHOT'
```

## Using mainClassName to specify the class that should be run

```
    mainClassName = 'com.company.companyname.Main'
```

this runs this class as the Main class when the `gradle run` command is issued.
