# Lab 6 – Scale and Load Balance Your Architecture

## Title

## Scale and Load Balance Your Architecture

## Author : SARAVANA KUMAR S
## Reg no : 212224220090
## Date : 19.03.2026

---

## Objective

The objective of this lab is to understand how to design a scalable and highly available architecture on AWS using Auto Scaling and Elastic Load Balancing. This experiment focuses on distributing incoming traffic across multiple EC2 instances, automatically scaling resources based on demand, and validating fault tolerance.

---

## Prerequisites

* Basic knowledge of Amazon EC2 and VPC
* Completion of previous labs (IAM, EC2, EBS, Database Server)
* AWS Academy Lab access
* Stable internet connection

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Elastic Load Balancer (ELB / ALB)
* Auto Scaling Groups (ASG)
* Amazon CloudWatch

---

## Tasks Performed

### Task 1: Review Existing Architecture

Students review the existing EC2-based application architecture created in previous experiments.

### Task 2: Create a Launch Template

Students create a launch template that defines the EC2 instance configuration including AMI, instance type, security group, and user data.

### Task 3: Create an Auto Scaling Group

Students create an Auto Scaling Group using the launch template and configure minimum, maximum, and desired instance capacity.

### Task 4: Configure an Application Load Balancer

Students create an Application Load Balancer and configure target groups for routing traffic to EC2 instances.

### Task 5: Register Auto Scaling Group with Load Balancer

Students attach the Auto Scaling Group to the target group of the load balancer.

### Task 6: Configure Scaling Policies

Students configure scaling policies based on CPU utilization using Amazon CloudWatch alarms.

### Task 7: Test Load Balancing and Scaling

Students test the setup by generating traffic and observing automatic scaling and load distribution.

---

## Workflow

1. Launch the AWS lab environment and open the AWS Management Console.

2. Navigate to **Amazon EC2**, select **Web Server 1**, and create an **Amazon Machine Image (AMI)** named `WebServerAMI`.

3. Go to **Target Groups** and create a new target group named `LabGroup`, selecting **Instances** as the target type and choosing **Lab VPC**.

4. Create an **Application Load Balancer** named `LabELB`, select **Lab VPC**, and configure **Public Subnet 1** and **Public Subnet 2**.

5. Attach the **Web Security Group** and configure the **HTTP:80 listener** to forward traffic to the `LabGroup` target group.

6. Navigate to **Launch Templates** and create a launch template named `LabConfig` using the `WebServerAMI`, instance type `t2.micro`, key pair `vockey`, and **Web Security Group**.

7. Enable **Detailed Monitoring** through **Amazon CloudWatch** in the advanced settings of the launch template.

8. Create an **Auto Scaling Group** named `Lab Auto Scaling Group` using the launch template and select **Private Subnet 1** and **Private Subnet 2**.

9. Configure scaling settings:
   - Desired capacity: `2`
   - Minimum capacity: `2`
   - Maximum capacity: `6`
   - Scaling policy: Target tracking with **Average CPU Utilization = 60%**.

10. Verify the setup by accessing the application using the **Load Balancer DNS name**, perform a **Load Test**, monitor alarms in **CloudWatch**, observe new instances launched by **Auto Scaling**, and finally **terminate Web Server 1**.
---

## Output Screenshots 
<img width="1920" height="1200" alt="Screenshot 2026-03-11 105918" src="https://github.com/user-attachments/assets/e953948d-4439-42e4-80e4-6f3ad0646e3f" />
<img width="960" height="1200" alt="Screenshot 2026-03-11 114716" src="https://github.com/user-attachments/assets/7986afa9-c1fd-4150-b99e-be9c9354d3c5" />
<img width="1920" height="1200" alt="Screenshot 2026-03-11 105948" src="https://github.com/user-attachments/assets/6405e654-7b3f-4ce6-b135-3591dbd9eb2e" />
<img width="1920" height="1200" alt="Screenshot 2026-03-11 103437" src="https://github.com/user-attachments/assets/d2ffc100-c4cf-4dda-8069-5a6bfd57dcbe" />
<img width="1920" height="1200" alt="Screenshot 2026-03-11 103149" src="https://github.com/user-attachments/assets/a15d6f5a-01ef-414d-a85c-c2f29b56ec2d" />
<img width="1920" height="1200" alt="Screenshot 2026-03-11 104319" src="https://github.com/user-attachments/assets/dd95cdbd-903e-4141-8110-5f7320bb04cc" />


---


## Result

This experiment demonstrated how to build a scalable and fault-tolerant cloud architecture using Auto Scaling Groups and Elastic Load Balancing. The system automatically adjusted resources based on workload and ensured continuous service availability by distributing traffic across multiple instances.
