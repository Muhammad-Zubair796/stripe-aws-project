# 🚀 Deploying a Node Js Application on AWS EC2

### 💻 Testing the project locally

1. **Clone this project**
```bash
git clone [https://github.com/Muhammad-Zubair796/stripe-aws-project.git](https://github.com/Muhammad-Zubair796/stripe-aws-project.git)
Setup environment variables - (.env) file

Plaintext

DOMAIN="http://localhost:3000"
PORT=3000
STATIC_DIR="./client"
PUBLISHABLE_KEY="your_test_key"
SECRET_KEY="your_test_key"
Initialise and start the project

Bash

npm install
npm run start
☁️ Set up an AWS EC2 instance
Create an IAM user & login to your AWS Console

Access Type: Password

Permissions: Admin

Create an EC2 instance

OS Image: Ubuntu

Instance type: t2.micro

Key pair: Create and download Nodejs.pem

Connecting to the instance using SSH

Bash

ssh -i Nodejs.pem ubuntu@13.53.177.149
⚙️ Configuring Ubuntu on remote VM
Update packages and dependencies

Bash

sudo apt update
Install Git

DigitalOcean Installation Guide

Configure Node.js and npm

DigitalOcean Node.js Guide

🚢 Deploying the project on AWS
Clone this project in the remote VM

Bash

git clone [https://github.com/Muhammad-Zubair796/stripe-aws-project.git](https://github.com/Muhammad-Zubair796/stripe-aws-project.git)
Setup environment variables - (.env) file

Plaintext

DOMAIN="[http://13.53.177.149:3000](http://13.53.177.149:3000)"
PORT=3000
STATIC_DIR="./client"
PUBLISHABLE_KEY="your_key"
SECRET_KEY="your_key"
Note: For this project, we used an Elastic IP Address for our EC2 as our permanent DOMAIN.

Initialise and start the project

Bash

npm install
npm run start
🛡️ Network Configuration
IMPORTANT: Edit the Inbound Rules in your EC2 Security Group to allow traffic on Port 3000 (Custom TCP) from source 0.0.0.0/0.

Project is deployed on AWS 🎉
