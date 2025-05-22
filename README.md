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
