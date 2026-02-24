###                              **Jenkins Master–Agent Setup on AWS EC2**





**📌 Overview**



This demonstrates the setup of a Jenkins Master–Agent (Distributed Build) Architecture on AWS EC2 instances using SSH authentication.



The goal of this setup is to enable distributed builds where Jenkins Master delegates build tasks to connected Agent nodes for better scalability and performance.



**🛠 Technologies Used**



* Amazon EC2 (Ubuntu)



* Amazon Web Services



* Jenkins



* OpenSSH



* Linux (Ubuntu)



**🏗 Architecture**



Jenkins Master → Connects via SSH → Jenkins Agent (Node)



Master manages jobs and scheduling



Agent executes build tasks



Communication secured using SSH key authentication



**🚀 Implementation Steps**



**1. Launch EC2 Instances**



Created two Ubuntu EC2 instances:



Jenkins Master



Jenkins Agent



**2. Install Java (Both Servers)**



Jenkins requires Java to run.



sudo apt update

sudo apt install openjdk-25-jdk -y



**3. Install Jenkins (Master Only)**



sudo wget -O /etc/apt/keyrings/jenkins-keyring.asc \\

https://pkg.jenkins.io/debian-stable/jenkins.io-2026.key

echo "deb \[signed-by=/etc/apt/keyrings/jenkins-keyring.asc]" \\

https://pkg.jenkins.io/debian-stable binary/ | sudo tee \\

/etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt update

sudo apt install Jenkins





**4. Start Jenkins:**



sudo systemctl enable jenkins

sudo systemctl start Jenkins



**5. Open jenkins in the browser**



* master server's public ip(noted)
* (public ip):8080
* copy the path at the jenkins
* in the master server \[ cat (path)]
* copy the password and paste it at the password column



**6. setup jenkins account**



* and then choose install suggested plugins
* setup the username,password,email and save
* the ip for the jenkins will appear so save and proceed and then its downloaded soo click start using jenkins





**7. Configure SSH Authentication**



**On Jenkins Master:**



**Switch to Jenkins user:**



sudo su - jenkins



Generate SSH key:



ssh-keygen (press enter for all details to have a default settings)



**View public key:**



ls ~/.ssh (copy the id name)

cat ~/.ssh/(id)

(copy the passkey which will be used later at the slave)



**8. Configure Agent Server**



**On Agent:**



as the java is already installed,then



mkdir -p ~/.ssh

nano ~/.ssh/authorized\_keys



Paste the public key from Master into authorized\_keys.



**Set permissions:**



chmod 700 ~/.ssh

chmod 600 ~/.ssh/authorized\_keys





**9. Add Agent in Jenkins UI**



**In Jenkins Dashboard:**



Manage Jenkins → Nodes → New Node



fill node name, type(permanent agent) ->create



**Configure:**



**Remote root directory:** /home/ubuntu



**Launch method:** Launch agent via SSH



**Host:** slave-private ip



**Credentials:** Add SSH private key ->next ->id ->description ->username(ubuntu) ->private key->enter directly ->key(add) -> select the saved key.pem file from the explorer and copy that passkey and paste here ->create -> select that in the credentials created now



Save and connect.



**✅ Result**



Jenkins Master successfully connected to Agent.



Distributed build environment configured.



Master can delegate build tasks to Agent securely via SSH.



**This can be verified from nodes -> created node -> log ->agent successfully connected and online (connection successful)**



**📚 Concepts Learned**



Jenkins Distributed Architecture



SSH Key-based Authentication



Linux file permissions



EC2 instance configuration



DevOps infrastructure setup



**🎯 Future Improvements**



Connect GitHub repository



Create CI/CD pipeline



Automate application deployment



Integrate with Docker or Kubernetes



**🏁 Conclusion**



This sets up a foundational CI/CD infrastructure using Jenkins Master–Agent architecture on AWS. It demonstrates practical understanding of DevOps automation, secure server communication, and distributed build systems.



**AUTHOR**



**Niranjana. R**



Cloud-AWS and devOps learner

