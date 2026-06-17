# PROGRAM - 02

## (Q) Working with Maven: Creating a Maven Project, Understanding the POM File, Dependency Management and Plugins.

### ANS:

> **Note:** Always create a separate folder to do any program.

- Open Command Prompt.

```bash
mkdir program2
```

This will create the `program2` folder.

```bash
cd program2
```

Navigate to the `program2` folder.

- After that, follow the below steps to work with a Maven project.

## STEP 1: Creating a Maven Project

```bash
mvn archetype:generate -DgroupId=com.example -DartifactId=myapp -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
```

## Step 2: Open the pom.xml File

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

        int result = app.add(2, 3);

        System.out.println("2+3=" + result);
        System.out.println("Application is running successfully.");
    }
}
```

## Step 4: Open Java Code (AppTest.java) File

```java
package com.example;

import org.junit.Assert;
import org.junit.Test;

public class AppTest {

    @Test
    public void testAdd() {
        App app = new App();

        int result = app.add(2, 3);

        System.out.println("Running test: 2 + 3 = " + result);

        Assert.assertEquals(5, result);
    }
}
```

## Step 5: Building the Project

### 1. Compile the Project

```bash
mvn compile
```

### 2. Run the Unit Tests

```bash
mvn test
```

### 3. Package the Project into a JAR

```bash
mvn package
```
