# Rise-Internship-Project-1
# Project 1: Deploy a Website on AWS EC2

## Overview

This project demonstrates how to deploy a static HTML/CSS website on a cloud server using **Amazon EC2**.
The objective is to understand cloud hosting, Linux server configuration, and web server setup as part of my Cloud & DevOps internship.

The website is hosted on a Linux-based EC2 instance configured with a web server and made publicly accessible via the internet.

---

##  Cloud Platform

This project was implemented using **Amazon Web Services (AWS)**.

---

## Objectives

* Launch and configure a Linux EC2 instance
* Connect securely using SSH
* Install and configure a web server (Apache/Nginx)
* Deploy a responsive HTML/CSS website
* Make the website live using the public IP

---

##  Technologies Used

* AWS EC2 (Amazon Linux 2023)
* Linux Command Line
* Apache / Nginx Web Server
* HTML5 & CSS3
* Git & GitHub (for version control)

---

##  Project Architecture

User → Internet → AWS EC2 Instance → Apache/Nginx → Hosted HTML Website

---

## ⚙️ Implementation Steps

### 1 Launch EC2 Instance

* Created an EC2 instance from AWS Console
* Selected Amazon Linux 2023 AMI
* Allowed inbound rules for:

  * SSH (Port 22)
  * HTTP (Port 80)

### 2 Connect to Instance via SSH

```bash
ssh -i mykey.pem ec2-user@<Public-IP>
```

### 3️ Install Web Server

```bash
sudo dnf update -y
sudo dnf install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
```

### 4️ Deploy Website

```bash
cd /var/www/html
sudo nano index.html
```

Added custom HTML landing page.

### 5️ Access Live Website

Opened in browser:

```
http://<Public-IP>
```

---

## Live Outcome

A fully functional website hosted on an AWS EC2 Linux server and accessible over the internet.

---

##  Key Learnings

* Basics of cloud computing and EC2 provisioning
* Linux server management using SSH
* Installing and configuring Apache/Nginx
* Hosting static websites on cloud infrastructure
* Understanding security groups and public IP access

---

## Screenshots


---

## 🔮 Future Enhancements

* Attach a custom domain using Route 53
* Enable HTTPS using SSL/TLS
* Automate deployment using CI/CD pipeline
* Deploy dynamic applications (React / Node.js)

---


## 📎 Repository Purpose

This repository is created as part of my internship to showcase hands-on experience in deploying a website on AWS EC2 and understanding real-world cloud hosting workflows.
