# Secure Docker Image Build and Vulnerability Scanning Pipeline Using GitHub Actions

## 1. Project Overview

This project implements a Continuous Integration (CI) pipeline using GitHub Actions to automate application testing, Docker image building, and security vulnerability scanning.

Whenever code is pushed to the `main` branch or a pull request is created, the pipeline automatically runs tests, builds a Docker image, and scans the image using Trivy.

The main objective is to identify potential security vulnerabilities early in the development process and improve application reliability.

## 2. Objectives

- Automate application testing using GitHub Actions.
- Build a Docker image for a Python Flask application.
- Scan the Docker image for operating-system and Python package vulnerabilities.
- Integrate security scanning into the CI workflow.
- Improve software quality and security through automation.

## 3. Technologies Used

- **Python:** Application development.
- **Flask:** Lightweight web framework.
- **Pytest:** Automated application testing.
- **Docker:** Application containerization.
- **Git and GitHub:** Source code management.
- **GitHub Actions:** CI workflow automation.
- **Trivy:** Docker image vulnerability scanning.

## 4. Project Workflow

1. A developer pushes code to GitHub or creates a pull request.
2. GitHub Actions checks out the source code.
3. Python is configured and project dependencies are installed.
4. Automated tests are executed using Pytest.
5. A Docker image is built.
6. Trivy scans the image for security vulnerabilities.
7. The workflow displays the execution status and scan results.

## 5. Application Features

- Flask application with a home endpoint.
- Health-check endpoint at `/health`.
- Automated tests for application endpoints.
- Docker-based application packaging.
- Automated CI workflow.
- Security scanning for operating-system and Python package vulnerabilities.

## 6. Security Scanning Results

The successful GitHub Actions run completed the Docker image build and Trivy scan.

In the recorded scan:
- Operating-system vulnerabilities detected: 0
- Python package vulnerabilities detected: 0

These results apply to the scanned image and packages at the time of execution. They do not guarantee that every possible security issue is absent.

## 7. How to Run the Project Locally

### Prerequisites

Install Python, Docker, and Git.

### Install dependencies

```bash
pip install -r requirements.txt
```

### Run automated tests

```bash
python -m pytest -v
```

### Build the Docker image

```bash
docker build -t secure-docker-pipeline:latest .
```

### Run the Docker container

```bash
docker run -p 5000:5000 secure-docker-pipeline:latest
```

Open the following URLs in your browser:

- Home: http://localhost:5000/
- Health check: http://localhost:5000/health

## 8. GitHub Actions Workflow

The workflow configuration is located at:

`.github/workflows/ci-cd-security.yml`

It automates testing, Docker image building, and Trivy security scanning on configured GitHub events.

## 9. Expected Outcome

The pipeline automatically validates the application, builds the Docker image, and reports detected vulnerabilities. This demonstrates how testing and security checks can be incorporated into a DevOps workflow.

## 10. Future Enhancements

- Fail the pipeline when configured severity thresholds are exceeded.
- Generate and publish security scan reports.
- Add Docker image publishing to a container registry.
- Add a deployment stage.
- Introduce additional security checks.

## 11. Repository

GitHub: https://github.com/Thejshri-sush/SecureDockerPipeline

## 12. Conclusion

This project demonstrates a basic automated CI pipeline that combines Python application testing, Docker image building, and vulnerability scanning using GitHub Actions and Trivy. It helps introduce security checks earlier in the software development lifecycle.
