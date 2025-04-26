# lamp-ansible-deploy

# Automated LAMP Stack Deployment using Ansible on AWS EC2

![LAMP Stack](https://via.placeholder.com/800x400?text=LAMP+Stack+Deployment)

## Overview

This project implements a highly available LAMP (Linux, Apache, MySQL, PHP) stack on AWS EC2 instances using Ansible for automation and Git for version control. The infrastructure is designed for scalability and reproducibility, making it easy to deploy and manage multiple environments.

## Key Features

- **AWS EC2 Provisioning**: Automated provisioning of EC2 instances with Ubuntu using AWS CLI and SSH key management
- **Configuration Management**: Ansible playbooks to install and configure Apache, MySQL, and PHP components
- **Security**: Configured virtual hosts and firewall rules with ufw for enhanced security
- **Version Control**: Used Git to version control all infrastructure code for better collaboration and tracking
- **Monitoring**: Enabled log rotation and basic monitoring with logrotate and cron jobs
- **Validation**: Deployed a sample PHP website to validate functionality and demonstrate the stack

## Technologies Used

- **Infrastructure**: AWS EC2, Ubuntu Linux
- **Automation**: Ansible, Bash scripting
- **Web Stack**: Apache, MySQL, PHP
- **Version Control**: Git
- **Security**: UFW (Uncomplicated Firewall)
- **Monitoring**: Logrotate, Cron

## Project Structure

```
ansible-lamp-deployment/
├── ansible/
│   ├── inventory/
│   │   └── hosts.ini
│   ├── playbooks/
│   │   ├── main.yml
│   │   ├── apache.yml
│   │   ├── mysql.yml
│   │   ├── php.yml
│   │   └── security.yml
│   └── roles/
│       ├── apache/
│       ├── mysql/
│       ├── php/
│       └── common/
├── scripts/
│   ├── provision-ec2.sh
│   └── setup-ssh-keys.sh
├── sample-app/
│   ├── index.php
│   └── assets/
└── docs/
    ├── architecture.md
    └── setup-guide.md
```

## Setup Instructions

### Prerequisites

- AWS CLI configured with appropriate permissions
- Ansible installed on your local machine
- SSH key pair for EC2 access
- Git installed

### Deployment Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/caugustine2022/ansible-lamp-deployment.git
   cd ansible-lamp-deployment
