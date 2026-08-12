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
<img width="1919" height="1070" alt="Screenshot 2026-08-02 114516" src="https://github.com/user-attachments/assets/416fdf26-220b-4518-aa91-301877bc1cf8" />

Output 2: EC2 Monitoring
<img width="1919" height="1076" alt="Screenshot 2026-08-02 115033" src="https://github.com/user-attachments/assets/91dc2560-15e7-43b1-a906-f7dc8022c7f4" />

Output 3: Web Server Access
<img width="1919" height="1073" alt="Screenshot 2026-08-02 115224" src="https://github.com/user-attachments/assets/44098a2c-a332-40fa-bba7-1f693f25ed72" />

Output 4: Instance Resizing
<img width="1919" height="1080" alt="Screenshot 2026-08-02 115800" src="https://github.com/user-attachments/assets/0d3cb01d-d9b5-4b1d-9b42-023d6f3e530d" />

Output 5: EC2 Limits and Stop Protection
<img width="1919" height="1070" alt="Screenshot 2026-08-02 115821" src="https://github.com/user-attachments/assets/b6d13674-e07d-406f-b5c7-0f1d775a94c4" />

## Result

The Amazon EC2 instance was successfully launched, monitored, secured, resized, and managed using the AWS Management Console. Security group configuration, instance monitoring, storage modification, service quota exploration, and stop protection features were successfully demonstrated
