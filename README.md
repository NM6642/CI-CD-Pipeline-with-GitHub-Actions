# CI/CD Pipeline with GitHub Actions 

This project demonstrates how to automate the **Continuous Integration (CI)** and **Continuous Deployment (CD)** processes using **GitHub Actions** and **Docker**. The application is a simple **Flask** web app that gets containerized and deployed using Docker. The CI/CD pipeline builds the Docker image and pushes it to **DockerHub** automatically every time you push new changes to the `main` branch.


## Project Overview

This project is designed to help automate the process of deploying a Flask application using **GitHub Actions** and **Docker**. Once the code is pushed to the GitHub repository, the following happens automatically:
1. The code is built into a Docker image.
2. The Docker image is pushed to **DockerHub**.
3. The app is ready to be deployed anywhere from the DockerHub repository.

## Tech Stack

- **GitHub Actions**: For automating the CI/CD pipeline.
- **Docker**: For containerizing the Flask application.
- **Flask**: A lightweight Python web framework to build the app.
- **DockerHub**: For hosting and storing the Docker image.

## Setup Instructions

### 1. Create a Flask App
   Create a simple `Flask` app and save it as `app.py`.

### 2. Dockerize the Flask App

Create a **Dockerfile** to containerize the Flask app.

### 3. Requirements File
Create a **requirements.txt** to list the dependencies:
- flask

### 4. Docker Build and Run

Build and run the Docker image locally.

### 5. Set Up GitHub Actions for CI/CD
1. Create a repository on GitHub and push your project code there.
2. Set up GitHub Actions:
   - Create a `.github/workflows` folder and add a workflow file (`ci-cd.yml`).
   - Define a CI/CD pipeline that triggers on `push` events to the `main` branch.
   - The workflow installs dependencies, builds the Docker image, and optionally pushes it to DockerHub.

## How the CI/CD Pipeline Works

The CI/CD pipeline is defined using **GitHub Actions** in the `.github/workflows/ci-cd.yml` file. Here’s what happens:

1. **Trigger**: The workflow is triggered every time code is pushed to the `main` branch.
2. **Setup Python Environment**: The pipeline sets up a Python environment and installs dependencies from the `requirements.txt`.
3. **Docker Build**: It builds the Docker image using the `Dockerfile` provided in the repository.
4. **Push to DockerHub**: The image is tagged with your DockerHub username and pushed to DockerHub for easy access and deployment.

## Testing the Project

### 1. Push Code to GitHub
   Make a change to your `app.py` or any file in your repository and push it to GitHub.

### 2. Check GitHub Actions
   Go to the **Actions** tab in your GitHub repository to check the status of the pipeline.

### 3. Verify the Docker Image in DockerHub
   After the pipeline completes, check if the Docker image has been pushed to your DockerHub account.

### 4. Run the Docker Image Locally (Optional)
   You can pull the Docker image from DockerHub and run it locally to verify the application is working.
   
   ## What Does This Project Do?
- **Automation**: It automates building and deploying a Flask app using GitHub Actions, a widely used CI/CD tool.
- **Dockerization**: The app is containerized with Docker to ensure consistency across different environments.
- **CI/CD Pipeline**: It sets up a GitHub Actions pipeline that builds the app, runs tests (optional), and deploys the Docker image to DockerHub automatically when code changes are pushed to the `main` branch.

## Deployment (Optional)

If you wish to deploy the Flask app to a production server or cloud service, you can pull the image from DockerHub and run it on the desired infrastructure.


