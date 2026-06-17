# PROGRAM-06

## (Q) Experiment 6: Continuous Integration with Jenkins

### ANS:

## To Push the Maven Folder in Git Repository Follow the Steps

### 1) Go to the folder where the Maven project is present.

### 2) Then type the following commands:

```bash
git init
```

```bash
git add .
```

```bash
git commit -m "initial commit"
```

Change if present in master or get some error:

```bash
git branch -M main
```

```bash
git remote add origin <Your_repository_Url(you created in git)>
```

```bash
git push -u origin main
```

## Step 1: Create a New Jenkins Job

### 1. Log into Jenkins

- Open your web browser and navigate to your Jenkins URL (e.g., `http://localhost:8080` or your cloud instance URL).
- Log in with your admin credentials.

### 2. Create a New Job

- On the Jenkins dashboard, click on **New Item**.
- Enter an Item Name: For example, **Maven-CI** (or **Gradle-CI** if you prefer Gradle).
- Select **Freestyle project**.
- Click **OK**.

## Step 2: Configure Source Code Management (SCM)

### 1. Select SCM

- In the job configuration page, scroll down to the **Source Code Management** section.
- Select **Git** (if using Git for version control).

### 2. Enter Repository Details

- **Repository URL:** Enter the URL of your Git repository.

Example:

```text
https://github.com/yourusername/your-maven-project.git
```

- **Credentials:** If your repository is private, click **Add** to provide the necessary credentials.
- Optionally, specify the Branch Specifier:

```text
*/main
```

## Step 3: Add Build Steps

### A. For a Maven Project

#### 1. Add Maven Build Step

- Scroll down to **Build** and click on **Add build step**.
- Select **Invoke top-level Maven targets**.

**Goals:**

```text
clean package
```

This command instructs Maven to clean the previous build artifacts, compile the code, run tests, and package the application into a JAR/WAR file.

- Optionally, set the POM file location if it is not in the default location (`pom.xml`).

## Step 4: Configure Post-build Actions

### 1. Publish Test Results

- Scroll down to the **Post-build Actions** section.
- Click **Add post-build action** and select **Publish JUnit test result report**.

**Test Report XMLs:**

```text
**/target/surefire-reports/*.xml
```

## Step 5: Save and Run the Job

### 1. Save the Configuration

- Click **Save** at the bottom of the job configuration page.

### 2. Trigger a Build

- On the job's main page, click **Build Now**.
- The build will be added to the build history on the left side.

### 3. Monitor Build Output

- Click on the build number (e.g., **#1**) and then click **Console Output**.
- Verify that Jenkins successfully checks out the code, runs the build commands (Maven or Gradle), and executes tests.
- Look for:

```text
BUILD SUCCESS
```

or the equivalent output to confirm that the build and tests passed.
