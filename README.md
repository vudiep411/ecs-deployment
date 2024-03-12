# Automating Docker Image Deployment to Amazon ECR and ECS with GitHub Actions

This repository contains GitHub Actions workflows and configuration files to automate the deployment of a Docker image into Amazon ECR and ECS.

## Overview

The deployment process involves the following steps:

1. **Building Docker Image**: A Docker image is built using the provided Dockerfile.

2. **Pushing Docker Image to Amazon ECR**: The Docker image is pushed to Amazon ECR, which acts as a private Docker registry.

3. **Deploying Docker Image to Amazon ECS**: The Docker image is deployed to Amazon ECS, which manages the containerized application.

## Workflow

The deployment process is automated using GitHub Actions. When changes are pushed to the main branch of this repository, the following workflow is triggered:

1. **Build and Push Docker Image to ECR**:
   - Builds the Docker image based on the provided Dockerfile.
   - Pushes the Docker image to the specified Amazon ECR repository.

2. **Deploy Docker Image to ECS**:
   - Deploys the Docker image to the specified Amazon ECS cluster and service.

## Prerequisites

Before you can use this repository to automate your deployment process, ensure that you have the following prerequisites:

- An AWS account with permissions to create and manage resources in Amazon ECR and ECS.
- Docker installed on your local machine for building Docker images.
- AWS CLI configured with appropriate credentials to interact with your AWS account.

## Setup Instructions

Follow these steps to set up the deployment automation process:

1. **Clone Repository**: Clone this repository to your local machine.
    ```
    git clone https://github.com/your-username/your-repository.git
    ```
2. **Configure AWS Credentials**: Configure AWS credentials on your local machine using the AWS CLI. Ensure that the credentials have permissions to interact with Amazon ECR and ECS.

3. **Update Workflow Configuration**: Customize the workflow configuration files (`ecr.yml` and `ecs.yml`) to match your AWS resources, Docker image name, and other settings.

4. **Push Changes**: Push your changes to the main branch of your repository.

5. **Monitor Deployment**: Monitor the GitHub Actions workflows to ensure that the deployment process runs successfully. You can view the workflow runs in the "Actions" tab of your GitHub repository.

## Contributing

Contributions to improve the deployment process or add new features are welcome! If you encounter any issues or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.