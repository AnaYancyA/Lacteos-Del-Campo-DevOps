# Lácteos del Campo — DevOps Task 2

## Overview

This project demonstrates a basic CI/CD pipeline using Jenkins and Docker for a Python application.

The pipeline automates the process of building a Docker image, checking Python syntax, and running the application container.

## Technologies

- Python 3.12
- Docker
- Jenkins
- Git and GitHub

## Project Structure

- `DevOpsTask2.py` — Python application.
- `Dockerfile` — Instructions to build the Docker image.
- `Jenkinsfile` — Jenkins pipeline configuration.
- `requirements.txt` — Python dependencies.
- `datos.json` — Application data.
- `.gitignore` — Files excluded from version control.

## CI/CD Pipeline

The Jenkins pipeline includes three stages:

1. **Build:** Builds the Docker image named `lacteos-del-campo`.
2. **Test:** Checks the Python syntax using `py_compile`.
3. **Deploy:** Runs the application container as a deployment demonstration.

The pipeline also displays a success message when all stages complete successfully.

## Jenkins Configuration

The Jenkins job uses **Pipeline script from SCM** to retrieve the `Jenkinsfile` from this GitHub repository.

SCM polling is configured with the schedule:

`H/5 * * * *`

This checks the repository approximately every five minutes for changes.

## How to Run

Build the Docker image:

```bash
docker build -t lacteos-del-campo .
```

Check Python syntax inside the container:

```bash
docker run --rm --entrypoint python lacteos-del-campo -m py_compile DevOpsTask2.py
```

Run the application container:

```bash
docker run --rm lacteos-del-campo
```

## Test Results

The pipeline completed successfully in Jenkins, with the Build, Test, and Deploy stages passing.

**Note:** The Deploy stage is a demonstration. It runs the container and removes it when execution finishes; it does not configure a permanent production deployment.

## Author

Ana Yancy Aguilar Prado

DevOps Task 2 — Jenkins and Docker
