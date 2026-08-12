## Ex--2-AWS-Account-setup-and-EC2-creation

### NAME: Kevin P
### REG NO: 212224040159

## Aim

To create and manage an Amazon EC2 instance using the AWS Management Console, configure its security settings, monitor its performance, resize its resources, and explore EC2 protection features and service limits.

## Objectives

Create an Amazon EC2 instance with termination protection enabled.

Configure security groups to allow HTTP access.

Monitor the EC2 instance using AWS monitoring tools.

Resize the EC2 instance and modify its storage volume.

Explore EC2 service quotas and test stop protection.

## Procedure
### Task 1: Launch an Amazon EC2 Instance

Log in to the AWS Management Console.

Open the EC2 service and launch a new instance.

Select the Amazon Linux 2023 AMI and t2.micro instance type.

Configure the key pair, VPC, subnet, and security group.

Enable termination protection.

Add the user data script to install the Apache web server.

Launch the instance and wait until it reaches the Running state.

### Task 2: Monitor the EC2 Instance

Open the Status Checks tab and verify the instance health.

View CloudWatch monitoring metrics.

Retrieve the system log.

View the instance screenshot for troubleshooting.

### Task 3: Configure Security Group and Access the Web Server

Copy the Public IPv4 address of the EC2 instance.

Attempt to access the web server through a browser.

Edit the inbound rules of the security group.

Add an HTTP rule allowing traffic from Anywhere (IPv4).

Save the changes and refresh the browser.

### Task 4: Resize the EC2 Instance

Stop the EC2 instance.

Change the instance type from t2.micro to t2.small.

Enable stop protection.

Increase the EBS volume size from 8 GiB to 10 GiB.

Restart the EC2 instance.

### Task 5: Explore EC2 Limits and Test Stop Protection

Open the Service Quotas service.

View Amazon EC2 resource limits.

Attempt to stop the protected EC2 instance.

Disable stop protection.

Stop the EC2 instance successfully.

## Output
Output 1: EC2 Instance Creation
<img width="1918" height="1087" alt="Screenshot 2026-07-28 135010" src="https://github.com/user-attachments/assets/a32904b6-a85f-44e1-8f3d-a242aa2c7bfa" />

Output 2: EC2 Monitoring
<img width="1915" height="1087" alt="Screenshot 2026-07-28 135723" src="https://github.com/user-attachments/assets/9bf5184f-1ce7-444f-97cf-43a70a083f7b" />

Output 3: Web Server Access
<img width="1916" height="1085" alt="Screenshot 2026-07-28 140316" src="https://github.com/user-attachments/assets/be91d8c6-b8c9-441b-8ecb-98093849d027" />

Output 4: Instance Resizing
<img width="1918" height="1133" alt="Screenshot 2026-07-29 103726" src="https://github.com/user-attachments/assets/48f7f803-01ed-4d15-864d-7a9bf1be056b" />

Output 5: EC2 Limits and Stop Protection
<img width="1918" height="1140" alt="Screenshot 2026-07-29 111148" src="https://github.com/user-attachments/assets/3a8f1fdd-19a8-4ec2-b0a4-a1c86a30a1cb" />


## Result

The Amazon EC2 instance was successfully launched, monitored, secured, resized, and managed using the AWS Management Console. Security group configuration, instance monitoring, storage modification, service quota exploration, and stop protection features were successfully demonstrated
