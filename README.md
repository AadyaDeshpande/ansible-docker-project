AUTOMATED AND REPRODUCIBLE DEVELOPMENT ENVIRONMENT SETUP

PROJECT OVERVIEW

This project demonstrates how to deploy a simple Flask application using Ansible and Docker. The goal is to make application deployment repeatable and easier to reproduce across compatible development environments.

TOOLS USED

- Git and GitHub: Version control and project hosting
- Ansible: Automates the deployment workflow
- Docker: Packages the application into a container
- Docker Compose: Builds and runs the application
- Python Flask: Provides the web application

PROJECT STRUCTURE

app/
  app.py
  requirements.txt

ansible/
  inventory.ini
  setup.yml

docker/
  Dockerfile
  docker-compose.yml

HOW IT WORKS

1. Application code and configuration are maintained in Git.
2. Ansible executes the deployment playbook.
3. Docker Compose builds the Docker image and starts the container.
4. The Flask application becomes accessible on port 5000.

PREREQUISITES

- Git
- Ansible
- Docker Desktop with WSL integration, or a compatible Docker Engine
- Docker Compose

HOW TO RUN

From the project root, run the following command:

ansible-playbook -i ansible/inventory.ini ansible/setup.yml

Open the following address in your browser:

http://localhost:5000

Expected output: DevOps Environment Setup Successful!

VERIFICATION

Check whether the container is running:

docker ps

Test the application:

curl http://localhost:5000

LEARNING OUTCOMES

- Using Git for version control
- Writing and executing Ansible playbooks
- Containerizing a Python application with Docker
- Deploying an application using Docker Compose
- Reproducing a deployment using version-controlled configuration
