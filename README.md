📌 Project Overview
This project demonstrates how to deploy a Virtual Machine (VM) on Google Cloud Platform (GCP), configure auto-scaling based on CPU utilization, and implement security measures like IAM roles and firewall rules.

🚀 Features Implemented
✔️ VM Deployment – Created a VM instance on GCP
✔️ Auto-Scaling – Configured a Managed Instance Group (MIG)
✔️ Scaling Policy – Set auto-scaling based on CPU utilization
✔️ IAM Roles – Defined access control policies
✔️ Firewall Rules – Configured secure traffic flow

🔧 Step-by-Step Implementation
1️⃣ Create a VM Instance
Open Google Cloud Console.
Navigate to Compute Engine → VM Instances.
Click Create Instance and configure:
Name: my-instance
Machine Type: e2-micro (free-tier eligible)
Boot Disk: Ubuntu 20.04
Networking: Allow HTTP & HTTPS traffic
Click Create to launch the VM.
2️⃣ Configure Auto-Scaling
Go to Compute Engine → Instance Templates.
Click Create Instance Template, set VM specs.
Navigate to Instance Groups → Create Instance Group.
Choose Managed Instance Group (MIG), select your template.
Enable Auto-Scaling with:
CPU Utilization Target: 70%
Min Instances: 1
Max Instances: 3
Click Create to enable auto-scaling.
3️⃣ Implement Security Measures
(a) Configure IAM Roles
Go to IAM & Admin → IAM.
Click Add and assign roles:
Viewer: Read-only access
Editor: Limited modification access
Owner: Full control
(b) Set Firewall Rules
Navigate to VPC Network → Firewall.
Click Create Rule and configure:
Allow HTTP (80) & HTTPS (443) traffic
Restrict SSH access to specific IP addresses
