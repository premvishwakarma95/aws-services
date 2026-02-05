# aws-services
- Iaas - EC2 -> this will give only an OS then we have to manage all things.
- PaaS - RDS -> This manage gives all managed thing all configuration just we need to manage our data as we want but other things will be managed automatically.
- SaaS - Email -> prem@ibrinfotech.com

# aws basic 
aws provided -> storage, networking, databases and many more services
1) scalable, security, reliable, globle reach

Popular services
EC2, S3 bucket, RDS, Lambda, CloudFront

aws IAM -> Identity and access management service -> role and permission management by this service. this give who can access what. -> This is global servie i mean no region specific.

aws CLI - search aws cli download -> download to run aws command just like we do in ubuntu.

AWS IAM Best Practices
• Avoid using root account except of account setup.
• Add user to a group and assign permission to group • Use password policy or MFA
• Use ACCESS KEYS for CLI/SDK
• Never share ACCESS KEYS or Password
• Audit the permission using IAM credential report.


# EC2
AWS EC2 
- It is region specific.
- AWS EC2 (Amazon Elastic Compute Cloud) is a cloud service that provides resizable virtual servers, called
instances, which you can use to run applications.
- this gives server to host a website.

About ec2 creation.
• Instance Type: Select the hardware capacity (e.g., CPU, memory). • AMI (Amazon Machine Image): Choose the operating system and software (linux, mac, windows).
• Storage: Configure the type and size of storage (e.g., EBS volume).
• Security Groups: Set up firewall rules to control inbound/outbound
traffic.
• Key Pair: Create or use an existing key pair for SSH access.
• Network Settings: Configure VPC, subnet, and assign public or private IP addresses.
• IAM Role: Attach an IAM role for permissions to access other AWS
resources.

• User Data: Add scripts to be executed when the instance starts.
	Userdata script to install and run Apache Webserver
	#!/bin/bash
	sudo yum update -y
	# Install Apache web server (httpd) sudo yum install -y httpd
	sudo systemctl start httpd
	sudo systemctl enable httpd
	# Create a simple HTML file to verify the web server is running
	echo "<html><h1>Welcome to Apache Web Server on Amazon Linux!</h1></html>"> 	/var/www/html/index.html

• Elastic IP: Optionally associate a static IP address for consistent
public access.
