CI/CD Pipeline Documentation

This document provides an overview of the CI/CD pipeline setup, configuration, and how it works in a GitHub Actions environment. The pipeline is designed to automatically lint, build, and deploy your application to a staging environment whenever code changes are pushed to the main branch.

---
1. Pipeline Overview
The pipeline automates the following tasks:
- Running lint checks to ensure code quality.
- Building the project using Vite.
- Deploying the application to a staging environment after successful testing and build.

---

2. CI/CD Setup

Step 1: Create a GitHub Repository
Start by creating a GitHub repository for your project. This repository will hold both your code and the CI/CD configuration. 

Step 2: Configure GitHub Actions
You will need to set up GitHub Actions in your repository to define the steps the pipeline should follow. This involves creating a workflow file inside the repository that will run specific tasks on certain events, such as when code is pushed to the main branch.

---

3. Workflow Configuration

Triggering the Pipeline
The pipeline is set to trigger automatically whenever code is pushed to the main branch. It can also be configured to run on pull requests or other branches as needed.

Environment Setup
The pipeline runs on a virtual machine that uses the Ubuntu operating system. Node.js is installed as part of the setup to ensure the project dependencies can be installed and the build process can run.

Key Steps in the Pipeline
1. Checkout Code: The pipeline starts by retrieving the latest code from the repository.
   
2. Install Dependencies: All necessary project dependencies are installed automatically. This ensures that the build process has everything it needs to complete successfully.

3. Linting: A linting step is included to check the code quality. This ensures that all code adheres to the defined style guide and quality rules before it can proceed to the build step.

4. Build Process: The pipeline builds the project using Vite. This step ensures that the application compiles correctly and is ready for deployment.

5. Deploy to Staging: Once the build and lint checks pass, the application is deployed to a staging environment. Deployment commands and configurations for the staging environment should be defined based on the specific needs of the project.

---

 4. How to Trigger the Pipeline

Push Events
Whenever code changes are pushed to the main branch, the pipeline is triggered automatically. This means that any new code updates are automatically built, tested, and deployed to staging without any manual intervention.

---

The site is a react + Vite with Nodejs as well

# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh
