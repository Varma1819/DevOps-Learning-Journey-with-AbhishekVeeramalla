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

# DevOps with Abhishek Veeramalla - Day 4

#### 25-05-2025

Today I focus on diving deep into **Linux fundamentals and Shell Scripting**, which are crucial for automation and efficient system management in DevOps.

### 1. Linux Fundamentals ("Linux & Shell Scripting")

#### What is an Operating System?
- Learned that an OS, like Linux, acts as the intermediary between software applications and hardware (CPU, RAM, I/O).

#### Why Linux is Popular in DevOps
- **Free and Open Source**: No licensing costs.
- **Secure**: Generally robust security, often not needing extra antivirus software.
- **Fast and Efficient**: Ideal for production environments.

#### Distributions
- Understood that Linux has various versions like **Ubuntu**, **CentOS**, offering flexibility.

#### Linux OS Architecture (Simplified)
- **Kernel**: The core of the OS, managing hardware, memory, processes, and system calls.
- **System Libraries**: Provide functions for user tasks, interfacing with the kernel.

#### Introduction to Shell & Basic Commands
- **Shell**: A command-line interface (CLI) to interact with the OS, with **Bash** being a popular choice.
- Essential commands covered:
  - `pwd`: Present working directory  
  - `ls`, `ls -ltr`: List files/directories (long format, sorted by modified time)  
  - `cd`, `cd ..`: Change directory, move up  
  - `touch`: Create an empty file  
  - `vi`: Text editor  
    - Insert mode: `i`, Save & Quit: `Esc + :wq`  
  - `cat`: Display file content  
  - `mkdir`: Create a directory  
  - `rm`, `rm -r`: Remove file or directory (recursively)  
  - `free -m`: Memory usage  
  - `nproc`: Number of CPUs  
  - `df -h`: Disk space  
  - `top`: System processes overview  

---

### 2. Shell Scripting for DevOps ("Shell Scripting for DevOps")

#### What is Automation & Shell Scripting?
- **Automation** aims to reduce manual tasks.  
- **Shell scripting** in Linux helps automate routine activities on a Linux machine.

#### Writing Your First Shell Script
- **Shebang**: Importance of `#!/bin/bash` to define the script interpreter.  
  - Discussed the difference with `#!/bin/sh`.
- **echo**: Command used for printing output.
- **Comments**: Use `#` for writing comments in scripts.

#### File Permissions and Execution
- **Understanding Permissions**: Owner, group, and others.
- **chmod**: Used to grant execute permissions (e.g., `chmod 777 script.sh`)
  - Permission values: Read (4), Write (2), Execute (1).
  - ![Screenshot 2025-05-25 181731](https://github.com/user-attachments/assets/78f67ecc-10a6-44b0-b855-dc4b1c194ce0)

- **Running Scripts**:
  - `sh script.sh`
  - `./script.sh`

#### More Useful Commands & Concepts
- `man`: Accessing manual pages for commands.
- `history`: Viewing command history.
- **Example Script**: Creating a directory, navigating into it, and creating files.
- ![Screenshot 2025-05-25 191339](https://github.com/user-attachments/assets/a86c5b54-4a52-4aeb-af60-cc09369cb722)


#### Role of Shell Scripting in DevOps
- Automating:
  - Infrastructure maintenance
  - Configuration management
  - Code management (e.g., Git interactions)
- Monitoring node health (CPU, memory, processes) using:
  - `top`, `nproc`, `free`
  - Automating health checks via scripting

Gained a **foundational understanding** of the Linux operating system, its architecture, and its importance in DevOps. Learned **essential command-line navigation and file manipulation**. Got introduced to the **power of shell scripting** for automating tasks—from simple file operations to complex system monitoring. This forms a **critical skill set for any DevOps professional**, laying the groundwork for advanced automation techniques and infrastructure management.

# DevOps with Abhishek Veeramalla - Day 5

#### 26-05-2025

Today, I continued my deep dive into **Shell Scripting for DevOps**, building on what I learned previously. This session focused on more advanced techniques and best practices to write robust and effective scripts.

### 1. Shell Scripting Best Practices

- **Script Metadata**: Adding author, date, purpose, and version info at the beginning using comments helps with script maintenance.
- **Debugging with `set -x`**: Displays each command and its arguments as they are executed. Very useful during development.
- **Error Handling**:
  - `set -e`: Script exits immediately if any command fails.
  - `set -o pipefail`: Ensures failure in any command within a pipeline causes the whole pipeline to fail.
  - ![image](https://github.com/user-attachments/assets/6d82e4ff-817f-42dc-b10f-c5edb173ba90)


### 2. Essential Linux Commands for DevOps Scenarios

- `ps -ef` / `ps aux`: View all running processes.
- ![Screenshot 2025-05-26 182433](https://github.com/user-attachments/assets/3978e687-a23e-4e05-aac8-9e47f5be248a)

- `grep`: Filter command output (e.g., `ps -ef | grep Amazon`).
- `|` (Pipe): Redirects output of one command to another.
- ![Screenshot 2025-05-26 184835](https://github.com/user-attachments/assets/fe9dbc0f-37a5-4623-92cc-7846dd6f1765)

- `awk`: Extract and format text (e.g., extract Process ID).
- ![Screenshot 2025-05-26 184857](https://github.com/user-attachments/assets/f94db750-ad6f-45f6-8dad-ad9ee6ec4979)

- `curl`: Transfer data from URLs or interact with APIs.
- ![Screenshot 2025-05-26 191447](https://github.com/user-attachments/assets/e2b39965-44d6-4447-addf-f79e02e0fefd)

- `wget`: Download files from URLs.
- ![Screenshot 2025-05-26 192245](https://github.com/user-attachments/assets/8fdf8a2c-57f7-4196-920f-b6c7ac6640fb)
- ![Screenshot 2025-05-26 193941](https://github.com/user-attachments/assets/679da6b6-8c55-40d2-b2f5-6d4312b01213)

- `find`: Search for files and directories with conditions.
- `sudo`: Run commands with elevated privileges.
- `su`: Switch user accounts.

### 3. Control Flow in Scripts

- **Conditional Statements**: `if`, `else`, `fi` for making decisions.
- **Loops**: `for`, `do`, `done` for iterating through items or commands.

### 4. Handling Signals

- **trap**: Intercept and handle signals like `SIGINT` (Ctrl+C) for cleanup tasks before exiting scripts.
- **kill**: Send signals to processes, typically used to terminate a process by its PID (e.g., `kill <pid>`).
- **killall**: Send signals to all processes matching a name, useful to terminate all instances of a program (e.g., `killall nginx`).

Today's session emphasized writing **professional and resilient shell scripts**. Best practices like metadata, debugging with `set -x`, and strict error handling (`set -e`, `set -o pipefail`) greatly enhance script quality. Mastering key Linux utilities such as `grep`, `awk`, `curl`, and `find` has boosted my ability to automate real-world DevOps tasks. Control structures (`if`, `for`) and signal handling (`trap`) are crucial for scripting smarter, interactive, and safer workflows.

Certainly! Here's the complete content you provided, formatted in Markdown for your GitHub README. This structure is optimized for clarity, and you can insert your screenshots where indicated.

---

# DevOps with Abhishek Veeramalla - Day 5 
###### (Shell Scripting Project)
#### 30-05-2025

# ShellSentinel: GitHub Access Audit & Compliance Automation

 - This project provides an automated audit system to check and validate the list of collaborators (users) with access to a specific GitHub repository against a **pre-approved whitelist**. The tool logs unauthorized access and can be integrated with email alerts using Postfix +
 - Gmail SMTP and Cron automation on an Ubuntu server.

## Use Case
Organizations often need to **track external/internal contributors** with repository access and ensure that **only approved users** have permissions like `read`, `write`, or `admin`. This tool automates that auditing process and sends a periodic report.

## Features

* Fetches all collaborators using GitHub API (with permission levels).
* Validates each user against a custom whitelist.
* Flags unauthorized users.
* Generates an audit report.
* Sends audit results to email via Postfix.
* Supports daily automation via Cron job.
* Lightweight Bash implementation.

## Phase-wise Setup Instructions

### Phase 1: EC2 & Environment Setup

1. Launch an Ubuntu-based EC2 instance.

2. SSH into the instance:

   ```bash
   ssh -i *.pem ubuntu@<your-ec2-ip>
   ```

3. Install required tools:

   ```bash
   sudo apt update
   sudo apt install -y jq curl mailutils
   ```

### Phase 2: Prepare Files

1. **Create Whitelist File**

   Open `nano` to create the whitelist file:

   ```bash
   nano whitelist.txt
   ```

   Paste your approved GitHub usernames, one per line.

   **Sample `whitelist.txt`:**

   ```text
   vasanthk77
   Varma1819
   ```

   Save and exit (`Ctrl+X`, then `Y`, then `Enter`).

2. **Create Audit Script**

   Open `nano` to create the audit script:

   ```bash
   nano github_audit.sh
   ```

   Paste the full script content provided in the [github\_audit.sh](#github_auditsh) section below.

   Save and exit.

3. Make the script executable:

   ```bash
   chmod +x github_audit.sh
   ```

### Phase 3: GitHub Access Token

1. Generate a GitHub personal access token.

   * You can use a "classic" token or a "fine-grained" token.
   * Ensure the token has the `repo` scope (or more specifically, `repo:read` for public and private repositories, or `public_repo` for public repositories if that's sufficient for your needs).

2. Export the token as an environment variable in your shell session. **Important:** For persistent storage across sessions or in scripts, consider more secure methods, but for this guide, we'll export it temporarily.

   ```bash
   export GITHUB_TOKEN='your_token_here'
   ```

   Replace `your_token_here` with your actual GitHub token.

   *Note: This token will only be available in the current terminal session. For the cron job, you'll need to ensure the token is available in its environment (see Phase 7).*

### Phase 4: Run Audit Script

Execute the script to audit a specific repository. Replace `Varma-Org` with your GitHub organisation name and `DLPAV` with your repository name.

```bash
./github_audit.sh Varma-Org DLPAV $GITHUB_TOKEN > report.txt
```

This command will run the audit and save its output to `report.txt`.

**Expected Output (content of `report.txt`):**

```text
Checking GitHub access for Varma-Org/DLPAV on 2025-05-30
-----------------------------------------------
[OK] vasanthk77 is authorized with read access.
[OK] Varma1819 is authorized with admin access.
```

### Phase 5: Configure Gmail SMTP via Postfix

This phase configures Postfix to relay emails through your Gmail account using an App Password.

1. Edit the Postfix main configuration file:

   ```bash
   sudo nano /etc/postfix/main.cf
   ```

2. Add the following lines at the end of the file:

   ```ini
   relayhost = [smtp.gmail.com]:587
   smtp_use_tls = yes
   smtp_sasl_auth_enable = yes
   smtp_sasl_password_maps = hash:/etc/postfix/sasl_passwd
   smtp_sasl_security_options = noanonymous
   smtp_tls_CAfile = /etc/ssl/certs/ca-certificates.crt
   ```

   Save and exit.

3. Create the Gmail credentials file:

   ```bash
   sudo nano /etc/postfix/sasl_passwd
   ```

4. Add your Gmail email address and App Password in the following format:

   ```text
   [smtp.gmail.com]:587 your_email@gmail.com:your_app_password
   ```

   Replace `your_email@gmail.com` with your Gmail address and `your_app_password` with a [Google App Password](https://support.google.com/accounts/answer/185833) you generated for Postfix. **Do not use your regular Gmail password.**

   Save and exit.

5. Set appropriate permissions and update Postfix maps:

   ```bash
   sudo chmod 600 /etc/postfix/sasl_passwd /etc/postfix/sasl_passwd.db
   sudo postmap /etc/postfix/sasl_passwd
   ```

6. Restart Postfix to apply the changes:

   ```bash
   sudo systemctl restart postfix
   ```

### Phase 6: Send Email Report Manually

After running the audit and generating `report.txt`, you can test the email setup:

```bash
mail -s "GitHub Audit Report - $(date '+%Y-%m-%d')" your_email@gmail.com < report.txt
```

Replace `your_email@gmail.com` with the email address where you want to receive the report.

You should receive an email.
![Screenshot 2025-05-30 181105](https://github.com/user-attachments/assets/7ed80df8-a434-4bf2-b9e4-29414fbca82c)



### Phase 7: Automate with Cron

Set up a cron job to run the audit script automatically.

1. Open your user's crontab for editing:

   ```bash
   crontab -e
   ```

   (Select an editor if prompted; `nano` is usually the easiest).

2. Add the following line to schedule the script. This example runs it daily at 8 AM UTC:

   ```cron
   0 8 * * * /home/ubuntu/github_audit.sh Varma-Org DLPAV 'your_actual_github_token' > /home/ubuntu/report.txt && mail -s "GitHub Audit Report - $(date '+\%Y-\%m-\%d')" your_recipient_email@example.com < /home/ubuntu/report.txt 2>&1
   ```

   **Important considerations for the cron job:**

   * Replace `/home/ubuntu/github_audit.sh` with the correct full path to your script.
   * Replace `Varma-Org` and `DLPAV` with your target organization and repository.
   * **Crucially, replace `'your_actual_github_token'` with your actual GitHub Personal Access Token.** Storing tokens directly in crontab is a security risk. For better security, consider:

     * Storing the token in a secured file and having the script read it.
     * Using EC2 instance roles and AWS Secrets Manager if running in AWS.
   * Replace `your_recipient_email@example.com` with the email address for the report.
   * The `$(date '+\%Y-\%m-\%d')` part needs the percent signs to be escaped with backslashes (`\%`) in cron.
   * The `&& mail ...` part ensures the email is sent only if the script execution is successful.
   * `2>&1` redirects both standard output and standard error from the script execution to the `report.txt` file, which is then emailed.

   Save and exit.

3. Verify the cron job is listed:

   ```bash
   crontab -l
   ```

