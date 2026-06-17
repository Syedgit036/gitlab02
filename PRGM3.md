# PROGRAM 3

## (Q) Working with Gradle Project (Groovy DSL)

### ANS:

## Step 1: Create a New Project

```bash
gradle init --type java-application
```

## Step 2: build.gradle (Groovy DSL)

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

## Step 3: App.java

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

## Step 4: AppTest.java (JUnit Test)

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

## Step 5: Run Gradle Commands

### Build the Project

```bash
gradle build
```

### Run the Application

```bash
gradle run
```

### Run the Tests

```bash
gradle test
```
