# PROGRAM – 10

## Creating Build Pipelines using Azure DevOps

## Step 1: Open Azure DevOps

Open browser and visit:

```text
Azure DevOps Official Website
```

Login using Microsoft account.

## Step 2: Create Azure DevOps Project

### 1. Click:

```text
New Project
```

### 2. Enter:

- Project Name
- Description

### 3. Select:

```text
Private / Public
```

### 4. Click:

```text
Create
```

## Step 3: Prepare Maven/Gradle Project

## Step 4: Push Project to GitHub

## Step 5: Create Pipeline

Go to:

```text
Pipelines → Create Pipeline
```

## Step 6: Select Repository Source

Choose repository source:

```text
✔ GitHub
```

OR

```text
✔ Azure Repos Git
```

Authorize access if prompted.

## Step 7: Select Repository

- Choose your project repository from GitHub/Azure Repos.
- Click:

```text
Select
```

## Step 9: Configure Pipeline

Choose:

```text
Starter Pipeline
```

Azure DevOps automatically detects:

- Maven project

OR

- Gradle project

## Step 10: Add YAML Pipeline Configuration

In the steps change the following:

```yaml
task: Maven@3
jdkVersionOption: '1.17'
goals: 'clean package'
```

## Step 11: Save Pipeline

Click:

```text
Save and Run
```

## Step 12: Execute Pipeline

Azure Pipeline automatically starts:

- ✔ Download source code
- ✔ Build project
- ✔ Execute tests

## Step 13: Run Unit Tests

Pipeline automatically executes unit tests.

Example output:

```text
Tests Run: 5
Failures: 0
BUILD SUCCESS
```

## Step 14: Verify Build Status

If successful:

```text
Pipeline Status: SUCCESS
```
