Certainly, let's rewrite the README.md file in a more professional and layman-friendly manner:

---

# Chicken Disease Classification - End-to-End

## Workflows

1. Update Configuration: Make necessary changes to the configuration file (config.yaml).
2. (Optional) Update Secrets: If needed, update sensitive information in the secrets file (secrets.yaml).
3. Update Parameters: Modify parameters in the params file (params.yaml).
4. Update the Entity: Update the return type of a function in your code.
5. Update Configuration Manager: Make changes to the configuration manager located in the 'src/config' folder.
6. Update Components: Modify and enhance the components of your project.
7. Update the Pipeline: Make updates to the project's data processing pipeline.
8. Update Main.py: Enhance the main Python script.
9. Update DVC Configuration: Update the DVC (Data Version Control) configuration for data tracking.

# How to Run?

### Steps:

1. Clone the Repository:
   - Copy the URL of the repository and use the following command to clone it to your local machine:

```bash
git clone https://github.com/harshit-sharma1256/Chicken-disease-calssification-end-to-end.git
```

### Step 01 - Create a Conda Environment:

1. After opening the repository, create a Conda environment using the following commands:

```bash
conda create -n chicken python=3.8 -y
```

   - Note: You can replace "chicken" with any desired environment name.

```bash
conda activate chicken
```

   - Note: If you are using the latest version of Anaconda, use the following command:

```bash
activate chicken/
```

### Step 02 - Install Requirements:

Install the required Python packages by running:

```bash
pip install -r requirements.txt
```

### Running the Application:

To run the application, execute the following command:

```bash
python app.py
```

Afterward, open your web browser and navigate to your local host and port to access the application.

### DVC Commands:

1. Initialize DVC:

```bash
dvc init
```

2. Reproduce DVC Pipeline:

```bash
dvc repro
```

3. Visualize DVC Pipeline:

```bash
dvc dag
```

# AWS CI/CD Deployment with GitHub Actions

## 1. Login to AWS Console:

Access your AWS account and log in to the AWS Management Console.

## 2. Create IAM User for Deployment:

Create an IAM user in AWS with specific access permissions, including EC2 and ECR.

- EC2 Access: This provides access to virtual machines.
- ECR: Elastic Container Registry, used to store Docker images in AWS.

## 3. Create ECR Repository:

Create an Elastic Container Registry repository to store and manage Docker images. Save the repository URI for later use.

## 4. Create an EC2 Machine:

Set up an EC2 instance with the Ubuntu operating system.

## 5. Install Docker on the EC2 Machine:

Optionally, update and upgrade the EC2 instance and install Docker to manage containers.

```bash
# Optional
sudo apt-get update -y
sudo apt-get upgrade

# Required
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker ubuntu
newgrp docker
```

## 6. Configure EC2 as Self-Hosted Runner:

Configure the EC2 instance as a self-hosted runner for GitHub Actions. This is done by following the settings in the GitHub repository under "Actions."

## 7. Setup GitHub Secrets:

In the GitHub repository settings, set up secrets for AWS credentials, ECR URI, and other necessary information.

- `AWS_ACCESS_KEY_ID`: Your AWS access key.
- `AWS_SECRET_ACCESS_KEY`: Your AWS secret access key.
- `AWS_REGION`: Your AWS region (e.g., us-east-1).
- `AWS_ECR_LOGIN_URI`: The ECR login URI.
- `ECR_REPOSITORY_NAME`: The name of your ECR repository.

---

This revised README.md provides a more professional and easy-to-follow guide for both setting up your project and deploying it to AWS using GitHub Actions.
