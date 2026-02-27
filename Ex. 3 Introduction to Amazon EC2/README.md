# Lab 3 – Introduction to Amazon Elastic Compute Cloud (EC2)

## Author

* **Name**: SARAVANA KUMAR S
* **Register Number**: 212224220090
* **Date of Submission**: 27.02.2026

---

## Objective

The objective of this experiment is to understand the fundamentals of Amazon Elastic Compute Cloud (EC2). This lab focuses on launching and managing a virtual server, understanding instance types and AMIs, connecting to an EC2 instance, monitoring its status, and performing basic instance operations such as start, stop, and terminate.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity
* Basic knowledge of Linux commands (optional)

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Key Pair
* Security Group
* SSH Client (PuTTY / Terminal)

---

## Tasks Performed

### Task 1: Explore Amazon EC2 Dashboard

Explore the EC2 service dashboard in the AWS Management Console. Observe the different sections such as Instances, AMIs, Instance Types, Key Pairs, Security Groups, and Elastic IPs.

---

### Task 2: Launch an EC2 Instance

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type (t2.micro) under the free tier. Configure basic settings such as instance name, key pair, and security group.

---

### Task 3: Configure Security Group

Configure a security group to allow inbound access:

* SSH (Port 22) from your IP address
* HTTP (Port 80) from anywhere (0.0.0.0/0)

This security group acts as a firewall for the instance.

---

### Task 4: Connect to EC2 Instance

Connect to the running EC2 instance using SSH. Use the downloaded key pair and connect via terminal or PuTTY.

For Amazon Linux:

```
ssh -i "keyname.pem" ec2-user@<Public-IP>
```



### Task 5: Perform Basic Instance Operations

Perform the following operations from the EC2 console:

* Stop the instance
* Start the instance
* Reboot the instance

Observe the state changes of the instance.

---

### Task 6: Monitor EC2 Instance

Monitor the EC2 instance using the Monitoring tab. Observe metrics such as CPU utilization, network in/out, and instance status checks.

---

### Task 7: Terminate EC2 Instance

Terminate the EC2 instance after completing the experiment to avoid unnecessary AWS charges.

---

## Workflow (Student Explanation)

1. Launch Your Amazon EC2 Instance task provisions a Amazon EC2 instance in the N. Virginia region with termination and stop protection enabled, configured inside a Lab VPC with a custom security group, and bootstrapped via user data to automatically deploy an Apache web server on Amazon Linux 2023.
2. Monitor Your Instance task focuses on monitoring your Amazon EC2 instance using status checks, logs, screenshots, and performance metrics through Amazon CloudWatch to ensure reliability and troubleshoot issues proactively.
3. Update Your Security Group and Access the Web Server task updates the security group of your Amazon EC2 instance to allow inbound HTTP (port 80) traffic, enabling external access to the deployed web server via its public IPv4 address.
4. Resize Your Instance task stops your Amazon EC2 instance to upgrade its instance type from t2.micro to t2.small, enables stop protection, and increases the attached Amazon Elastic Block Store volume size from 8 GiB to 10 GiB before restarting it.
5. Explore EC2 Limits task involves reviewing regional resource quotas for Amazon Elastic Compute Cloud through the Service Quotas console to understand default limits on running on-demand instances and other EC2 resources, and how they govern deployment capacity.
6.Test Stop Protection task validates stop protection on your Amazon EC2 instance by attempting to stop it, confirming the safeguard blocks the action, then disabling the protection to successfully stop the instance.

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Dashboard / Instance List
<img width="1919" height="1091" alt="Screenshot 2026-02-26 105810" src="https://github.com/user-attachments/assets/fbbbb691-6639-46d9-9614-7c51f7ff551f" />
<img width="1913" height="1017" alt="Screenshot 2026-02-27 090545" src="https://github.com/user-attachments/assets/e5194bda-90c8-405b-82ba-e72d889a88e7" />
<img width="1908" height="1017" alt="Screenshot 2026-02-27 090525" src="https://github.com/user-attachments/assets/45eda811-dc31-4686-a894-00af7af0a881" />



### Screenshot 2: SSH Connection to Instance
<img width="1919" height="1086" alt="Screenshot 2026-02-26 112408" src="https://github.com/user-attachments/assets/c8998d98-cd7a-4dd9-a902-6cd9715f3dab" />


### Screenshot 3: Instance Monitoring / Status

<img width="1914" height="1021" alt="Screenshot 2026-02-27 083223" src="https://github.com/user-attachments/assets/e4202d43-85a3-4fd1-ac10-c4baec27fa82" />
<img width="1890" height="916" alt="Screenshot 2026-02-27 085915" src="https://github.com/user-attachments/assets/d15855d3-e10b-4941-ab4b-021019831ed0" />

<img width="842" height="1004" alt="Screenshot 2026-02-27 083653" src="https://github.com/user-attachments/assets/a31f6af4-ce95-4870-a433-257a961ee40d" />
<img width="933" height="954" alt="Screenshot 2026-02-27 084126" src="https://github.com/user-attachments/assets/e5447e5e-2796-4491-b7f1-898c4ba22114" />


## Result 

This experiment provided hands-on experience with Amazon EC2 by demonstrating how to launch, connect, manage, and monitor a virtual server in AWS. It helped in understanding the concept of Infrastructure as a Service (IaaS) and how compute resources can be provisioned and controlled on demand in the cloud.
