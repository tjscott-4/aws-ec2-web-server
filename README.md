# AWS EC2 Web Server Project (Apache + Monitoring + Troubleshooting)

## Overview

This project demonstrates how to deploy, monitor, and troubleshoot a web server using **Amazon EC2** and **CloudWatch**.

The project includes launching an EC2 instance, installing Apache, hosting a website, simulating a failure, and configuring monitoring with CloudWatch alarms.

---

## AWS Services Used

* Amazon EC2
* Security Groups (Firewall)
* Amazon Linux 2023
* Amazon CloudWatch

---

## Project Architecture

User Browser
⬇
Public IP Address
⬇
EC2 Instance (Linux)
⬇
Apache Web Server
⬇
CloudWatch Monitoring & Alerts

---

## 1. Launch EC2 Instance

A Linux-based EC2 instance was launched using Amazon Linux 2023.

![EC2 Instance Running](screenshots/01-ec2-instance-running.png)

---

## 2. Configure Security Group

Inbound rules were configured to allow:

* SSH (Port 22)
* HTTP (Port 80)

![Security Group Rules](screenshots/02-security-group-rules.png)

---

## 3. Connect to EC2 Instance

Connected to the EC2 instance using EC2 Instance Connect and executed Linux commands.

![Terminal Connection](screenshots/03-ec2-terminal-connection.png)

---

## 4. Install and Start Apache

Installed Apache (httpd) and verified that the service was running.

![Apache Running](screenshots/04-apache-running.png)

---

## 5. Deploy Website

Created an `index.html` file and verified the website was accessible via the public IP address.

![Live Website](screenshots/05-ec2-live-website.png)

---

## 6. Simulate Failure (Website Down)

Stopped the Apache service to simulate a real-world outage.

This caused the website to become unreachable.

![Website Down](screenshots/06-ec2-website-down.png)

---

## 7. Restore Service (Website Fixed)

Restarted the Apache service to restore website functionality.

![Website Restored](screenshots/07-ec2-website-restored.png)

---

## 8. CloudWatch Monitoring (CPU Tracking)

Configured Amazon CloudWatch to monitor EC2 CPU utilization.

Simulated CPU load to observe how the system responds under stress.

![CPU Spike](screenshots/08-cloudwatch-cpu-spike.png)

---

## 9. CloudWatch Alarm Configuration

Created an alarm that triggers when CPU utilization exceeds 10%.

![Alarm Created](screenshots/09-cloudwatch-alarm-created.png)

---

## 10. Alarm Recovery (Back to Normal)

Stopped the CPU load and verified that the alarm returned to a healthy state.

![Alarm OK](screenshots/10-cloudwatch-alarm-ok.png)

---

## Key Skills Demonstrated

* EC2 instance deployment and configuration
* Linux command-line usage
* Apache web server installation and management
* Security group (firewall) configuration
* Troubleshooting service outages
* Diagnosing connection issues
* CloudWatch monitoring and metrics analysis
* Alarm configuration and alerting
* Simulating system load for testing
* Observing and validating system recovery

---

## Website Access

http://3.87.123.197

---

## Author

**Tedarrell Scott Jr**
Aspiring Cloud Support / Cloud Operations Engineer
