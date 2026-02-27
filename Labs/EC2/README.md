Here’s a **README.md tailored specifically for your EC2 hands-on lab** with the tasks and steps you completed. You can paste this into your GitHub repo:

---

# Amazon EC2 Hands-On Lab

## **Overview**

This repository documents a hands-on lab for deploying and managing an **Amazon EC2 web server** using AWS. The lab covers launching an EC2 instance, configuring security, monitoring performance, and resizing resources. This practical exercise provides real-world experience for cloud computing and AWS EC2 fundamentals.

---

## **Lab Objectives**

* Launch an EC2 instance with **Amazon Linux 2023 AMI**.
* Deploy a **web server** automatically using a User Data script.
* Configure **security groups** to allow HTTP traffic.
* Monitor instance health and metrics with **CloudWatch**.
* Resize **instance type** and **EBS volume** to handle changing workloads.
* Enable **termination** and **stop protection** to prevent accidental shutdowns or deletion.

---

## **Tasks Performed**

### **Task 1 — Launch EC2 Web Server Instance**

1. Navigated to **AWS Management Console → EC2 Dashboard** in **N. Virginia (us-east-1)**.
2. Launched a new instance and assigned the name **Web Server**.
3. Selected **Amazon Linux 2023 AMI** and **t2.micro** instance type.
4. Configured key pair **vockey** and selected **Lab VPC** with default subnet.
5. Created **Web Server security group** and removed default inbound rules.
6. Enabled **Termination Protection**.
7. Added a **User Data script** to install Apache and deploy a simple web page.
8. Launched the instance and verified status: **Pending → Initializing → Running** with **2/2 status checks passed**.

---

### **Task 2 — Monitor the EC2 Instance**

1. Verified system and instance reachability under **Status Checks**.
2. Viewed **CloudWatch metrics** in the Monitoring tab.
3. Retrieved **System Log** to confirm web server installation.
4. Captured an **Instance Screenshot** for console visibility and troubleshooting.

---

### **Task 3 — Update Security Group and Access Web Server**

1. Copied the **Public IPv4 address** from the instance Details tab.
2. Accessed the address in a web browser and confirmed access was blocked.
3. Updated **Web Server security group** to allow **HTTP traffic (port 80)** from Anywhere (IPv4).
4. Refreshed the browser and verified the webpage:

```
Hello From Your Web Server!
```

---

### **Task 4 — Resize Instance and EBS Volume**

1. Stopped the **Web Server** instance.
2. Changed instance type from **t2.micro → t2.small**.
3. Enabled **Stop Protection**.
4. Resized root **EBS volume** from 8 GiB → 10 GiB.
5. Restarted the instance and verified updated compute and storage resources.

---

## **Lab Outcomes**

* Successfully deployed a functional EC2 web server.
* Automated setup using **User Data scripts**.
* Applied network security through **security groups**.
* Monitored instance health via **CloudWatch and System Logs**.
* Performed vertical scaling of instance type and storage.

---

## **Repository Structure**

```text
EC2-Lab/
│
├─ images/                  # Screenshots for each task
├─ scripts/                 # User Data scripts used in the lab
├─ python-for-cybersecurity/ # Lab notes and related content
├─ README.md                # This file
```

---

## **Accessing the Web Server**

1. Copy the **Public IPv4 address** from the EC2 instance Details tab.
2. Open the address in a web browser.
3. Confirm the message:

```
Hello From Your Web Server!
```


