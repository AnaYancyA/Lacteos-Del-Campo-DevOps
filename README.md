# DevOps Task 2: Jenkins CI/CD Pipeline

## Project Overview

This project demonstrates a basic Continuous Integration and Continuous Deployment (CI/CD) pipeline using Jenkins and Docker. The pipeline automates the process of building a Docker image, testing Python code syntax, and running the application container.

## Technologies Used

- **Jenkins:** Automates the CI/CD pipeline.
- **Docker:** Builds and runs the application container.
- **Python:** Programming language used by the application.
- **Git and GitHub:** Version control and source code repository.

## Project Structure

```text
Lacteos-Del-Campo-DevOps/
├── DevOpsTask2.py
├── Dockerfile
├── Jenkinsfile
├── requirements.txt
├── datos.json
├── .gitignore
└── README.md
```

## Pipeline Stages

The Jenkins pipeline contains three stages:

### 1. Build
Builds a Docker image named `lacteos-del-campo` using the project's Dockerfile.

### 2. Test
Checks the Python syntax of `DevOpsTask2.py` using Python's `py_compile` module inside the Docker container.

### 3. Deploy
Runs the application container as a demonstration of the deployment stage. The container is automatically removed after execution.

## How to Run the Pipeline

1. Start Docker and Jenkins.
2. Open the Jenkins dashboard.
3. Open the `Lacteos-Del-Campo-DevOps` pipeline.
4. Click **Build Now**.
5. Open **Console Output** to review the execution of each stage.
6. Confirm that the build finishes with `Finished: SUCCESS`.

## CI/CD Workflow

```text
GitHub Repository
        |
        v
      Jenkins
        |
        v
   Build Docker Image
        |
        v
     Test Python
        |
        v
   Run Docker Container
        |
        v
   Pipeline Result
```

## Expected Result

The pipeline should complete the Build, Test, and Deploy stages successfully.

## Learning Objectives

- Understand the fundamentals of CI/CD.
- Create and configure a declarative Jenkins pipeline.
- Build and run Docker containers.
- Automate basic application validation and execution.

## Repository

GitHub: https://github.com/AnaYancyA/Lacteos-Del-Campo-DevOps.git
