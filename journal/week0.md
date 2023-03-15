# Week 0 — Billing and Architecture

##Synopsis

This journal consists of the tasks completed in week-0 of AWS Free Bootcamp 2023 organized by Andrew Brown and his Team. In this week, we started with setting up the requirements that are needed to start the ‘Cruddur Project’.

##Pre-Requisites: 

Before starting this Cloud Project Bootcamp we have to ready with some requirements. 
For detailed explanation check the playlist by Andrew Brown and his team here : youtube.com/playlist?list=PLBfufR7vyJJ7k25byhRXJldB5AiwgNnWv

Now, Let's talk about the services we're going to work in this bootcamp!

we have to register for the following services:

- Create a Github Account, Copy Andrew's repository with the right formatting of the repo and make it as Public.
- Create a Gitpod account and install the extension for your browser.
- Create Github CodeSpace
- Create an AWS account ( Whether it is Free tier or premium, it's upto user)
- Create Lucidchart ( Hint - In this week, we're going to work here)
- Create Honeycomb.io account
- Create Rollbar account


## Week-0 Billing, Architecture & Security


Week-0 Live Session conducted By AWS Cloud project Bootcamp Organizer Andrew, and his guest lecturers -  Shala Warner, Chris Williams and Margaret Veltierra.

***What are they discussed in this Live Session ?***

This was mainly focused on ***Billing and Architecture***

- We learnt how to understand the client’s requirements,  how to segregate tasks and gather the requirements for the project. 
- Different architectures – monolithic and microservice architecture. 
- Introduction to AWS console, Gitpod console, GitHub repositories.  
- Understanding about Conceptual, Logical and Physical Diagrams. 
- Got to know about TOGAF Architecture.
- C4 models. 
- How to create diagrams in Lucid Charts. 
- Hands on example for Napkin Diagram. 

##Tasks/Challenges to be Completed for week-0

**1. Create an IAM user,role, add mfa.**

Steps to be followed inorder to create an IAM user, add multi-factor authentication.
 Login as a **root user** into AWS account.
- Search for **IAM service** and go to **Users**.
- **Create a new User** by giving the appropriate **(Admin)** permissions.
After that to set MFA you can go to particular **User -> Security Credentials -> Enable MFA**.
- Fill the required details and **Scan QR code** from the authentication app in your mobile. (Here you **need to install authentication application in your mobile** to connect it with your IAM User).
- **Enter two MFA Codes** when asked and your MFA is set.

***Creat an IAM Role***

- From IAM click on **Roles -> Create role**.
- Choose **Entity Type** as per your project, I personally chose **AWS Services for EC2 Use case.**
- Added permission policy as **Security Audit**.
- Then give **role name** and **Tags** and click on **Create role**. 
If you're getting any error or facing any challenges while creating user or role, it means your'e not authorized to create a user/role with your credentials.Upgrade to root account or get permission from root user to create a role/user.

**2. Install AWS CLI in GitPod**

Command to Install AWS CLI:

curl -fSsl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"

unzip -qq awscliv2.zip

sudo ./aws/install --update

rm awscliv2.zip
       
 In this command we're using "sudo". If you're a root user you don't need to add sudo. it is used to run the command with elevated privileges.
      
      
**3. Create a Billing Alarm**

There are 2 ways to set the billing alerts.
- Using Budget.
- Using Cloudwatch Alarm. In this case, you need to create an alarm on us-east-1 region (since it is the only region you can create an alarm for free-tier). You can create up to 10 free cloudwatch alarms with free-tier.

Those 2 alarms will be helpful to identify if you are underspending/overspending. 
Also we will receive an e-mail whenever the limit(We can mention as much as we want) exceeds. 

AWS Calculator : https://calculator.aws/#/

This is a tool where you can estimate the cost of any service based on the client requirements without actually using it. 