# PROGRAM – 05

## (Q) Introduction to Jenkins

### What is Jenkins?

Jenkins is an open-source automation server widely used in the field of Continuous Integration (CI) and Continuous Delivery (CD). It allows developers to automate the building, testing, and deployment of software projects, making the development process more efficient and reliable.

## 1. Installing Jenkins Locally

### Prerequisites

- Ensure that Java (JDK) is installed on your system.
- Jenkins requires Java 21.

## 2. Install Jenkins on Window System

Download the Jenkins Windows installer from the official Jenkins website.

- Run the installer and follow the on-screen instructions.
- While installing choose login system: **run service as LocalSystem (not recommended)**.
- After then use default port or you can configure your own port like using port **3030**, then click on **Test** and **Next**.
- After then change the directory and choose Java JDK-21 path like:

```text
C:\Program Files\Java\jdk-21\
```

- After then click **Next**, **Next** and then it will ask permission, click **Yes** and it will start installing.
- After successfully installed, Jenkins will be running on either the default port or the chosen port.
- You can access it in your browser at:

```text
http://localhost:8080
```

or

```text
http://localhost:3030
```

## 3. Jenkins Setup in Browser

After opening browser by visiting your local address:

- It will ask for the administrator password, so you have to navigate the above highlighted path and open the `initialAdminPassword` file in Notepad or any software to see the password.
- Just copy that password and paste it and click on **Continue**.
- It will ask to customize Jenkins, so click on **Install Suggested Plugins**. It will automatically install all required plugins.
- After that create an admin profile by filling all details, then click on **Save and Continue**.
- After then click **Save and Finish**.
- After that click on **Start using Jenkins**.
