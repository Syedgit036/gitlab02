# PROGRAM – 01

## (Q1) 1. Introduction to Maven and Gradle: Overview of Build Automation Tools, Key Differences Between Maven and Gradle, Installation and Setup.

### ANS:

- **What is Maven?** Maven is a build automation tool primarily used for Java projects. It uses an XML configuration file called `pom.xml` (Project Object Model) to define project settings, dependencies, and build steps.

- **What is Gradle?** Gradle is a more modern and versatile build tool that supports multiple programming languages, including Java, Groovy, and Kotlin. It uses a domain-specific language (DSL) for build scripts, written in Groovy or Kotlin.

### Key Differences Between Maven and Gradle

| Aspect | Maven | Gradle |
|----------|----------|----------|
| Configuration | XML (`pom.xml`) | Groovy or Kotlin DSL |
| Performance | Slower | Faster due to caching |
| Flexibility | Less flexible | Highly customizable |
| Learning Curve | Easier to pick up | Slightly steeper |
| Script Size | Verbose | More concise |
| Dependency Management | Uses Maven Central | Compatible with Maven too |
| Plugin Support | Large ecosystem | Extensible and versatile |

# How to Install Maven

## 1. Download Maven

- Go to the Maven Download Page and download the latest binary ZIP file.

## 2. Extract the ZIP File

- Right-click the downloaded ZIP file and select **Extract All...** or use any extraction tool like WinRAR or 7-Zip.

## 3. Move the Folder

- After extraction, move the extracted Maven folder (usually named `apache-maven-x.x.x`) to a convenient directory like:

```text
C:\Program Files\
```

## 4. Navigate to the bin Folder

- Open the Maven folder, then navigate to the `bin` folder inside.
- Copy the path from the File Explorer address bar.

Example:

```text
C:\Program Files\apache-maven-x.x.x\bin
```

## 5. Set Environment Variables

- Open the Start Menu, search for **Environment Variables**, and select **Edit the system environment variables**.
- Click **Environment Variables**.
- Under **System Variables**:
  - Find the **Path** variable.
  - Double-click on it and click **New**.
  - Paste the full path to the `bin` folder of your Maven directory.

Example:

```text
C:\Program Files\apache-maven-x.x.x\bin
```

## 6. Save the Changes

- Click **OK** to close the windows and save your changes.

## 7. Verify the Installation

- Open Command Prompt and run:

```bash
mvn -v
```

If Maven is correctly installed, it will display the version number.

# How to Install Gradle

## 1. Download Gradle

- Visit the Gradle Downloads Page and download the latest binary ZIP file.

## 2. Extract the ZIP File

- Right-click the downloaded ZIP file and select **Extract All...** or use any extraction tool like WinRAR or 7-Zip.

## 3. Move the Folder

- After extraction, move the extracted Gradle folder (usually named `gradle-x.x.x`) to a convenient directory like:

```text
C:\Program Files\
```

## 4. Navigate to the bin Folder

- Open the Gradle folder, then navigate to the `bin` folder inside.
- Copy the path from the File Explorer address bar.

Example:

```text
C:\Program Files\gradle-x.x.x\bin
```

## 5. Set Environment Variables

- Open the Start Menu, search for **Environment Variables**, and select **Edit the system environment variables**.
- Click **Environment Variables**.
- Under **System Variables**:
  - Find the **Path** variable.
  - Double-click on it and click **New**.
  - Paste the full path to the `bin` folder of your Gradle directory.

Example:

```text
C:\Program Files\gradle-x.x.x\bin
```

## 6. Save the Changes

- Click **OK** to close the windows and save your changes.

## 7. Verify the Installation

- Open a terminal or Command Prompt and run:

```bash
gradle -v
```

If it shows the Gradle version, the setup is complete.
