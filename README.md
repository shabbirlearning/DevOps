# 🚀 Enterprise Apache Web Server Deployment on AWS (Production-Style)

## 📖 Project Overview

This project demonstrates how to deploy, configure, secure, monitor, and automate an **Enterprise Apache Web Server** on AWS EC2 using production best practices.

The project starts with a basic Apache installation and gradually evolves into a complete enterprise-ready infrastructure including:

- Apache Installation
- Virtual Hosting
- HTTPS (SSL/TLS)
- Security Hardening
- Authentication
- Logging
- Performance Tuning
- Reverse Proxy
- Load Balancer
- Database Integration
- Backup & Disaster Recovery
- Monitoring
- Ansible Automation

---

# 🏢 Real-Time Business Use Case

ABC Technologies Pvt. Ltd. is migrating its on-premises web applications to AWS Cloud.

The company needs a secure, scalable, and highly available Apache infrastructure capable of hosting multiple business applications on a single EC2 instance.

As a Linux System Administrator, your responsibilities include:

- Deploy Apache Web Server
- Configure Multiple Virtual Hosts
- Secure websites using HTTPS
- Protect server from common attacks
- Configure logging & monitoring
- Perform daily backups
- Integrate applications with databases
- Configure Reverse Proxy
- Configure Load Balancing
- Automate infrastructure using Ansible

---

# 🏗 Project Architecture

```
                    Internet
                         │
                  Route53 DNS
                         │
                  HTTPS (443)
                         │
          AWS Application Load Balancer
                         │
                 Apache Web Server
                         │
      ---------------------------------------
      │                                     │
 HR Portal                           CRM Portal
      │                                     │
 Reverse Proxy                      Static Website
      │
 Application Server
      │
 Amazon RDS / MySQL
      │
 Daily Backup → Amazon S3
```

---

# 🖥 Environment

| Component | Details |
|------------|----------|
| Cloud | AWS EC2 |
| Operating System | Amazon Linux 2023 / RHEL 9 |
| Web Server | Apache HTTP Server |
| Firewall | firewalld |
| Security | SELinux |
| Automation | Ansible |
| Database | MySQL / MariaDB / Amazon RDS |
| Monitoring | systemd, journalctl |
| Backup | Shell Script + Cron + Amazon S3 |

---

# 📂 Project Phases

---

# ✅ Phase 1 - Apache Installation & Virtual Hosting

### Business Requirement

Deploy Apache Web Server to host multiple business applications using Name-Based Virtual Hosting.

### Features

- Install Apache
- Enable Service
- Configure Firewall
- Create DocumentRoot
- Configure Virtual Hosts
- Configure SELinux
- Website Testing

### Skills Learned

- Apache Installation
- Virtual Hosts
- SELinux
- firewalld
- systemctl

---

# 🔐 Phase 2 - HTTPS (SSL/TLS)

### Business Requirement

Encrypt all employee and customer traffic using HTTPS.

### Features

- Install mod_ssl
- Create SSL Certificate
- Configure HTTPS
- Redirect HTTP → HTTPS
- TLS 1.2 / TLS 1.3

### Skills Learned

- SSL
- TLS
- OpenSSL
- Apache HTTPS

---

# 🛡 Phase 3 - Apache Security Hardening

### Business Requirement

Security Audit identified vulnerabilities.

### Implemented

- Disable Apache Version Disclosure
- Disable Directory Listing
- Configure Security Headers
- Disable Weak SSL Protocols
- Secure Cipher Suites

### Skills Learned

- Apache Hardening
- Security Headers
- TLS Hardening

---

# 🔑 Phase 4 - Authentication

### Business Requirement

Restrict HR Portal access to HR Employees only.

### Features

- Basic Authentication
- htpasswd
- Authorization

---

# 🚫 Phase 5 - Custom Error Pages

### Business Requirement

Display company branded error pages.

Configured

- 403
- 404
- 500

---

# 📜 Phase 6 - Apache Logging

### Business Requirement

Maintain separate logs for each application.

Configured

- HR Access Log
- HR Error Log
- CRM Access Log
- CRM Error Log

---

# 🔄 Phase 7 - Log Rotation

### Business Requirement

Automatically rotate logs to save disk space.

Configured

- logrotate
- Compression
- Automatic cleanup

---

# ⚡ Phase 8 - Performance Tuning

### Business Requirement

Improve website performance during high traffic.

Configured

- KeepAlive
- mod_deflate
- mod_expires
- MaxRequestWorkers
- Timeout Optimization

---

# 🔀 Phase 9 - Reverse Proxy

### Business Requirement

CRM application moved to Tomcat.

Apache forwards traffic to backend application server.

Modules

- mod_proxy
- mod_proxy_http

---

# ⚖ Phase 10 - Load Balancer

### Business Requirement

Distribute traffic across multiple backend web servers.

Configured

- mod_proxy_balancer
- Health Check
- Session Persistence

---

# 🗄 Phase 11 - Database Integration

### Business Requirement

Store employee and customer information securely.

Integrated

- MySQL
- MariaDB
- Amazon RDS

Concepts

- Database Connectivity
- CRUD Operations
- Backup

---

# 💾 Phase 12 - Backup & Disaster Recovery

### Business Requirement

Daily automated backup of Apache Server.

Backups Included

- Website Files
- Apache Configuration
- SSL Certificates
- Database Dump

Automation

- Shell Script
- Cron Job
- Amazon S3 Upload

Restore Procedure Included

---

# 📊 Phase 13 - Monitoring

### Business Requirement

Monitor Apache health and troubleshoot failures.

Commands Used

- systemctl
- journalctl
- ss
- top
- vmstat
- iostat

---

# 🤖 Phase 14 - Ansible Automation

### Business Requirement

Deploy Apache infrastructure across multiple Linux servers.

Automated

- Apache Installation
- Virtual Hosts
- SSL
- Security
- Logging
- Backup

Using

- Ansible Roles
- Templates
- Handlers
- Variables

---

# 📁 Project Directory Structure

```
enterprise-apache-project/

├── 01-apache-installation
├── 02-virtual-hosting
├── 03-https
├── 04-security-hardening
├── 05-authentication
├── 06-custom-error-pages
├── 07-logging
├── 08-logrotate
├── 09-performance
├── 10-reverse-proxy
├── 11-load-balancer
├── 12-database
├── 13-backup
├── 14-monitoring
├── 15-ansible
├── architecture
├── screenshots
├── scripts
├── configs
└── README.md
```

---

# 🔧 Technologies Used

- AWS EC2
- Apache HTTP Server
- Linux
- RHEL 9 / Amazon Linux
- SELinux
- firewalld
- OpenSSL
- Let's Encrypt
- MySQL
- MariaDB
- Amazon RDS
- Route53
- Shell Scripting
- Cron
- Amazon S3
- Ansible

---

# 🧪 Validation Checklist

- Apache Service Running
- Virtual Hosts Working
- HTTP Redirect to HTTPS
- SSL Certificate Valid
- Security Headers Enabled
- Authentication Working
- Logs Generated
- Log Rotation Verified
- Reverse Proxy Working
- Load Balancer Tested
- Database Connectivity Verified
- Backup & Restore Tested
- Monitoring Commands Verified
- Ansible Playbook Executed Successfully

---

# 🎯 Skills Demonstrated

- Linux Administration
- Apache HTTP Server
- Virtual Hosting
- HTTPS
- SSL/TLS
- Security Hardening
- SELinux
- firewalld
- Logging & Monitoring
- Performance Optimization
- Reverse Proxy
- Load Balancing
- MySQL Administration
- Backup & Disaster Recovery
- Shell Scripting
- AWS EC2
- Amazon S3
- Route53
- Ansible Automation

---

# 📚 Interview Topics Covered

- Apache Architecture
- Virtual Hosts
- SSL/TLS
- HTTP vs HTTPS
- Apache Security
- Reverse Proxy
- Load Balancer
- Apache Performance Tuning
- Apache Logging
- SELinux
- firewalld
- MySQL Integration
- Backup Strategy
- Disaster Recovery
- Route53
- Ansible Roles
- Troubleshooting Apache

---

# 👨‍💻 Author

**Shabbir Ahmad**

Linux System Administration | AWS | Apache | Nginx | Ansible | DevOps Learning
