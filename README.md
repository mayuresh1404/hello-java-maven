# 🚀 Task 8 - Java Maven Build Job using Jenkins

This repository contains a simple Java application that demonstrates how to run a Maven build job using Jenkins. It is part of a DevOps internship assignment to understand the basics of CI/CD and Jenkins job creation.

---

##  Project Structure

```
hello-java-maven/
├── pom.xml
└── src/
    └── main/
        └── java/
            └── HelloWorld.java
```

- `HelloWorld.java`: A simple Java program that prints "Hello, Jenkins + Maven!" to the console.
- `pom.xml`: Maven build configuration file.

---

## ⚙️ Tools & Technologies Used

- **Jenkins** (via Docker)
- **Maven** (v3.8.6)
- **Java** (JDK 8 or 11)
- **Docker** (for containerized Jenkins)
- **GitHub** (for version control & submission)

---

##  How to Run the Project

### 1. Clone the Repo
```bash
git clone https://github.com/your-username/hello-java-maven.git
cd hello-java-maven
```

### 2. Start Jenkins (if using Docker)
```bash
docker run -p 8080:8080 -p 50000:50000 jenkins/jenkins:lts
```

### 3. Configure Maven in Jenkins
- Go to: `Manage Jenkins > Global Tool Configuration`
- Under **Maven**, add a new Maven installation (e.g., `Maven-3.8.6`)
- Check ✔️ "Install Automatically"

### 4. Create a Freestyle Job in Jenkins
- Go to Jenkins Dashboard > **New Item**
- Select **Freestyle Project** and name it `Hello-Java-Build`
- In the **Build** section:
  - Add a build step: **Invoke top-level Maven targets**
  - Set **Goals**: `clean package`
  - Select Maven version: `Maven-3.8.6`

### 5. Build the Job
- Click **Build Now**
- Go to **Console Output**
- You should see:  `BUILD SUCCESS`

