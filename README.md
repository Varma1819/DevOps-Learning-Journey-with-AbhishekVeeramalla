# DevOps-Learning-Journey-with-AbhishekVeeramalla
Welcome to my public learning journal! I'm Jaya Rakesh Varma M, an aspiring DevOps Engineer and M.Tech Cloud Computing student. I'm following a structured DevOps learning path curated by [Abhishek Veeramalla](https://in.linkedin.com/in/abhishek-veeramalla), documenting each day's learning here.

# DevOps with Abhishek Veeramalla - Day 1
##### 21-05-2025
Today, I covered the following foundational topics:

### Core Concepts of DevOps: 
- Definition and cultural aspects of DevOps.
- The importance of DevOps in modern software delivery.
- How to articulate one's role and experience as a DevOps engineer.

### The Software Development Life Cycle (SDLC) and DevOps: 
- Understanding the various phases of the SDLC (Planning, Defining, Designing, Building, Testing, Deploying).
- How DevOps practices and automation optimize and improve the efficiency of the SDLC.
- Brief overview of project management methodologies like Agile.

### Prerequisites and Context for Learning DevOps: 
- The different roles within a software development organization and how DevOps interacts with them.
- The practical application of project management tools like Jira for tracking DevOps tasks.
- The proactive nature of DevOps in identifying and addressing inefficiencies in the development pipeline.

# DevOps with Abhishek Veeramalla - Day 2
##### 22-05-2025
Today's focus was on understanding Virtual Machines (VMs) and how they are foundational to cloud computing and DevOps practices.

### What are Virtual Machines?
- Learned that VMs are logical, isolated computer systems created within a single physical server. They allow for efficient use of hardware resources by running multiple independent operating systems and applications on one machine.
- The hypervisor is the key software layer that enables virtualization, managing and creating these VMs (e.g., VMware, Zen).
- Understood how virtualization addresses the inefficiency of underutilized physical servers.
- Cloud platforms (AWS, Azure, GCP) heavily rely on VMs to provide scalable compute resources (like EC2 instances in AWS).

### Creating Virtual Machines in AWS & Azure:
#### Manual Creation:
- AWS: Walked through the steps of launching an EC2 instance via the AWS Management Console, including selecting an AMI (like Ubuntu, Free tier), instance type (e.g., t2.micro), creating a key pair for SSH access, and basic network configuration.
- Azure: Explored the process of creating a VM through the Azure Portal, noting its similarity to the AWS process, involving selecting an OS, size, and other configurations.
- Instance - Creation_Stopping_Termination(Deletion).
- ![Screenshot 2025-05-22 233519](https://github.com/user-attachments/assets/7bb61dc7-2af0-499b-a4ad-18dab17447e1)
- ![Screenshot 2025-05-22 233549](https://github.com/user-attachments/assets/65d48ead-da3a-42d6-b91b-9fc9b3fa3ab2)
- ![Screenshot 2025-05-22 233627](https://github.com/user-attachments/assets/85ddebe3-2798-42fb-a41c-69c55e09be00)

#### Automation Concepts (Crucial for DevOps):
- Recognized that manual creation isn't scalable for multiple VMs.
- Introduced to automation tools for AWS, such as: AWS CLI; AWS API (using SDKs like Boto3 for Python); AWS CloudFormation Templates (CFT) for Infrastructure as Code (IaC); AWS CDK (Cloud Development Kit).
- Terraform was highlighted as a multi-cloud IaC tool for managing resources across different providers.
- The core idea is that automation relies on making authenticated and authorized API calls to the cloud provider.
- While less detailed for Azure in the video, the same principles of API-driven automation apply, with tools like Azure Resource Manager (ARM) templates being relevant.

##### Gained a solid understanding of what VMs are, why they are important, and the basic methods (manual and automated) for provisioning them on major cloud platforms like AWS and Azure. This is a critical building block for further DevOps learning.

# DevOps with Abhishek Veeramalla - Day 3

#### 23-05-2025

Today's session was a deep dive into interacting with AWS services, particularly EC2 instances, using the AWS Command Line Interface (CLI) and various terminal tools.

### Connecting to EC2 Instances

- **AWS Management Console (UI)**: Revisited connecting to EC2 instances directly through the web console for quick access.
- **Terminal (CLI/SSH)**: Focused on the more common and automatable method of connecting via SSH from a local terminal.
  - Requires the EC2 instance's **public IP address** and the correct **username** (e.g., `ubuntu`).
  - Authentication uses a **private key file (.pem)** specified with the `-i` flag (e.g., `ssh -i yourkey.pem ubuntu@public_ip`).
  - Set proper file permissions using:  
    ```bash
    chmod 600 yourkey.pem
    ```
    to avoid "permission denied" errors.

### Terminal Software

- Discussed terminal options:
  - `iTerm2` for macOS.
  - `PuTTY`, `NoMachine`, and notably `MobaXterm` for Windows.
- MobaXterm was highlighted for its **user-friendly interface** and **session management** features.

### AWS CLI (Command Line Interface)

- **Purpose**: A powerful tool to interact with and manage AWS services directly from the terminal.
- **Installation & Verification**:
  - Install via AWS docs.
  - Verify using:
    ```bash
    aws --version
    ```
- **Configuration**:
  - Use `aws configure` to set:
    - Access Key ID
    - Secret Access Key
    - Default Region
    - Output Format
    - ![image](https://github.com/user-attachments/assets/4bae5cba-acd2-4507-afbf-bc70d0eac9c8)

  - Access keys are created via the **IAM** section in the AWS Console.
- **Basic Usage**:
  - Example: List S3 buckets:
    ```bash
    aws s3 ls
    ```

- **Managing EC2 with CLI**:
  - EC2 instances can be created and managed using:
    ```bash
    aws ec2 run-instances
    ```
  - Parameters are referenced from AWS documentation.

### Brief Introduction to Other Automation Methods

- **AWS CloudFormation**: Infrastructure as Code (IaC) service using templates.
- **AWS API (Boto3 for Python)**: Programmatic interaction using Python SDK.

##### Gained practical knowledge on connecting to EC2 instances via different methods and configuring AWS CLI. These are fundamental skills for automating AWS tasks and essential for any DevOps role in an AWS environment.
