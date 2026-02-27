# Lab 4 – Working with Amazon Elastic Block Store (EBS)

## Author

* **Name**: SARAVANA KUMAR S
* **Register Number**: 212224220090
* **Date of Submission**: 27-02-2026

---

## Objective

The objective of this experiment is to understand how Amazon Elastic Block Store (EBS) provides persistent block-level storage for EC2 instances. This lab focuses on creating and attaching an EBS volume, formatting and mounting it on an EC2 instance, storing data, and verifying data persistence after instance reboot.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing EC2 instance (Amazon Linux 2 preferred)
* Basic knowledge of Linux commands

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Amazon EBS
* SSH Client (Terminal / PuTTY)

---

## Tasks Performed

### Task 1: Explore Amazon EBS

Explore the Amazon EBS service through the EC2 dashboard. Observe different volume types such as General Purpose SSD (gp2/gp3), Provisioned IOPS SSD, Throughput Optimized HDD, and Cold HDD.

---

### Task 2: Create an EBS Volume

Create a new EBS volume in the same Availability Zone as the EC2 instance. Choose an appropriate size and volume type.

---

### Task 3: Attach EBS Volume to EC2 Instance

Attach the created EBS volume to the running EC2 instance as an additional block device.

---

### Task 4: Format the EBS Volume

Connect to the EC2 instance using SSH and format the attached volume with a file system (for example, ext4).

---

### Task 5: Mount the EBS Volume

Mount the formatted volume to a directory in the EC2 instance (for example, /data or /mnt/ebs).

---

### Task 6: Store Data in EBS Volume

Create files and directories inside the mounted EBS volume and store sample data.

---

### Task 7: Verify Data Persistence

Reboot the EC2 instance and verify that the data stored in the EBS volume is still available after reboot.

---

## Workflow (Student Explanation)

(Write the steps you followed in your own words)

1. Create a New EBS Volume task provisions a 1 GiB Amazon Elastic Block Store (gp2) volume in the same Availability Zone as the existing Amazon EC2 instance and tags it for structured resource identification before attachment.

2. Attach the Volume to an Instance task attaches the newly created Amazon Elastic Block Store volume to the Lab Amazon EC2 instance using the specified device name, transitioning the volume state from Available to In-use.

3. Connect to Your Amazon EC2 Instance task establishes a browser-based terminal session to the Lab Amazon EC2 instance using EC2 Instance Connect for secure, direct command-line access.
   
4. Create and Configure Your File System task formats the attached Amazon Elastic Block Store volume with an ext3 file system, mounts it to /mnt/data-store, updates /etc/fstab for persistent mounting, and validates storage integration on the Amazon EC2 Linux instance. 

5. This step verifies snapshot lifecycle progression from Pending to Completed in Amazon Elastic Block Store, then removes and confirms deletion of the test file from the mounted volume on the Amazon EC2 instance to simulate data change after backup creation.

6. Restore the Amazon EBS Snapshot task restores a snapshot to a new Amazon Elastic Block Store volume, attaches it to the Lab Amazon EC2 instance, mounts it, and verifies successful data recovery from the previously backed-up file.

---

## Output Screenshots (Attach 3)

### Screenshot 1: EBS Volume Created

<img width="1919" height="1088" alt="Screenshot 2026-02-27 083207" src="https://github.com/user-attachments/assets/97845a60-1fb3-4250-9e9d-275726b1c491" />

---

### Screenshot 2: EBS Volume Attached to EC2

<img width="1919" height="1140" alt="Screenshot 2026-02-27 083418" src="https://github.com/user-attachments/assets/a35c9616-8bcc-4ba9-97df-286d68fc2b42" />

---

### Screenshot 3: Mounted Volume with Data

<img width="1919" height="1141" alt="Screenshot 2026-02-27 084404" src="https://github.com/user-attachments/assets/27be4305-128b-4672-ab6d-152d4c910955" />

---

## Result / Conclusion

This experiment demonstrated how Amazon EBS provides persistent storage for EC2 instances. By creating, attaching, formatting, and mounting an EBS volume, and by verifying data after reboot, the concept of durable block storage in the cloud was clearly understood.
