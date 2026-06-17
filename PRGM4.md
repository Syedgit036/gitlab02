# PROGRAM 4

## (Q) Practical Exercise: Build and Run a Java Application with Maven, Migrate the Same Application to Gradle.

## Step 1: Creating a Maven Project

```bash
mvn archetype:generate -DgroupId=com.example -DartifactId=myapp -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
```

## Step 2: Open The pom.xml File

```xml
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0
         http://maven.apache.org/maven-v4_0_0.xsd">

    <modelVersion>4.0.0</modelVersion>

    <groupId>com.example</groupId>
    <artifactId>myapp</artifactId>
    <packaging>jar</packaging>
    <version>1.0-SNAPSHOT</version>

    <name>myapp</name>
    <url>http://maven.apache.org</url>

    <dependencies>
        <dependency>
            <groupId>junit</groupId>
            <artifactId>junit</artifactId>
            <version>3.8.1</version>
            <scope>test</scope>
        </dependency>
    </dependencies>

    <build>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-surefire-plugin</artifactId>
                <version>2.22.2</version>
            </plugin>
        </plugins>
    </build>

</project>
```

## Step 3: Open Java Code (App.java) File

```java
package com.example;

public class App {

    public int add(int a, int b) {
        return a + b;
    }

    public static void main(String[] args) {

        App app = new App();

        int result = app.add(5, 3);

        System.out.println("The result of adding 5 and 3 is: " + result);
        System.out.println("Application is running successfully!");
    }
}
```

## Step 4: Run the Project (go to myapp and run)

```bash
mvn clean install
```

```bash
mvn exec:java -Dexec.mainClass="com.example.App"
```

## Step 5: Migrate the Maven Project to Gradle

### 1. Initialize Gradle

Navigate to the project directory (`gradle-example`) and run:

```bash
gradle init
```

### 2. Navigate the project folder and open build.gradle file then add the below code and save it.

```gradle
plugins {
    id 'application'
}

application {
    mainClass = 'com.example.App'
}

repositories {
    mavenCentral()
}

dependencies {
    testImplementation 'junit:junit:4.13.2'
}

test {
    outputs.upToDateWhen { false }

    testLogging {
        events "passed", "failed", "skipped"
        exceptionFormat "full"
        showStandardStreams = true
    }
}
```

## Step 6: Run the Gradle Project

### Build the Project

In the project directory (`gradle-example`), run the below command to build the project:

```bash
gradlew build
```

### Run the Application

Once the build is successful, run the application using below command:

```bash
gradlew run
```

## Step 7: Verify the Migration
