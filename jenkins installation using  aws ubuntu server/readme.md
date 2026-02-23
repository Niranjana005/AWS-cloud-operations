###              **Jenkins Installation on AWS EC2 (Manual Setup)**





**📌 Overview**



This demonstrates the manual installation and configuration of Jenkins (LTS) on an AWS EC2 Ubuntu server.

It includes security group configuration, Java installation, Jenkins setup, and web-based initialization.



**🏗️ Architecture**



AWS EC2 Instance (Ubuntu)



Security Group (Port 22 \& 8080 enabled)



Java (JDK 17/21/25)



Jenkins LTS



Web Browser Access via Public IP



**⚙️ Step-by-Step Implementation**



1️⃣ **Launch EC2 Instance**



AMI: Ubuntu



Instance Type: t3.micro (Free Tier)



Key Pair: Created/Selected



**Security Group:**



SSH → Port 22



HTTPS -> Port 443



HTTP -> Port 80



Custom TCP → Port 8080 → Anywhere (0.0.0.0/0)



2️⃣ **Connect to EC2**

   instance created ->connect



3️⃣ **Update Server**

sudo su

apt update



4️⃣ **Install Java (Jenkins Requirement)**

sudo apt install openjdk-25-jdk (Debian/Ubuntu)



**5️⃣ Install Jenkins (LTS)**



**Add Jenkins repository:**



sudo wget -O /etc/apt/keyrings/jenkins-keyring.asc \\

&nbsp; https://pkg.jenkins.io/debian-stable/jenkins.io-2026.key

echo "deb \[signed-by=/etc/apt/keyrings/jenkins-keyring.asc]" \\

&nbsp; https://pkg.jenkins.io/debian-stable binary/ | sudo tee \\

&nbsp; /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt update

sudo apt install Jenkins 



**6️⃣ Enable \& Start Jenkins Service**

sudo systemctl enable jenkins

sudo systemctl start jenkins

sudo systemctl status jenkins



**Expected Output:**



Active: active (running)



7️⃣ **Access Jenkins in Browser**



Open:



http://(Public-IP):8080



**8️⃣ Unlock Jenkins**



Retrieve initial admin password:



sudo cat /var/lib/jenkins/secrets/initialAdminPassword



Copy and paste into the browser.



9️⃣ **Complete Setup**



Install Suggested Plugins



**Create Admin User**



Set Username, Password, Full Name, Email



Confirm Jenkins URL



🎉 Jenkins is successfully configured!





💡 **Key Learnings**



EC2 Instance provisioning



Security Group configuration



Linux package management



Service management using systemctl



Jenkins manual installation process



🔐 **Security Note**



**For production:**



Restrict Port 8080 access



Use HTTPS



Use IAM roles instead of access keys



👩‍💻 Author



Niranjana R

AWS \& DevOps Learner

