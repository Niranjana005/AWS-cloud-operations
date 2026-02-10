&nbsp;                                     **AWS Cloud Operations – CloudFormation Automation**



**📌 Overview**

This project demonstrates AWS Cloud Operations using **Infrastructure as Code (IaC)** with AWS CloudFormation.



A CloudFormation stack is used to automatically provision AWS resources, removing the need for manual setup and ensuring consistency and repeatability.



---



**🚀 Project: EC2 \& S3 Automation using CloudFormation**



**🔹 Description**

Using a single CloudFormation YAML template, the following AWS resources are created automatically:

\- An EC2 instance running Ubuntu

\- An Amazon S3 bucket



All resources are fully managed by CloudFormation and can be created or deleted through the stack lifecycle.



---



**🛠 AWS Services Used**

\- AWS CloudFormation

\- Amazon EC2

\- Amazon S3

\- AWS IAM

\- Ubuntu AMI



---



**🧩 Architecture**

AWS CloudFormation Stack

|

├── EC2 Instance (Ubuntu)

|

└── S3 Bucket





---



⚙️ How It Works

1\. A CloudFormation template is written in YAML format.

2\. The template is uploaded to AWS CloudFormation.

3\. A stack is created from the template.

4\. AWS automatically provisions the EC2 instance and S3 bucket.

4\. Delete the S3 bucket created

5\. Deleting the stack removes all associated resources automatically.



---



**🎯 Learning Outcomes**

\- Understanding Infrastructure as Code (IaC)

\- Automating AWS resource provisioning

\- Managing EC2 and S3 using CloudFormation

\- Practicing AWS Cloud Operations concepts

\- Safe resource cleanup using stack deletion



---



**💡 Why Use CloudFormation?**

\- Infrastructure is version-controlled

\- Repeatable and consistent deployments

\- Easy rollback and deletion

\- Reduced manual errors



---



**🧹 Cleanup**

To avoid unnecessary AWS charges:

1\. Go to AWS CloudFormation

2\. Select the stack

3\. Choose Delete Stack and the S3 bucket

4\. All resources created by the stack are removed



---



**🔮 Future Enhancements**

\- Add input Parameters(Instance Type, Key Pair)

\- Add Outputs(EC2 Public IP, S3 Bucket Name)

\- Add Security Groups

\- Add UserData scripts for EC2 configuration

\- Extend with IAM roles and policies



---



**👩‍💻 Author**

**Niranjana R**  

AWS Cloud \& DevOps Learner  



---



**📎 License**

This project is created for learning and educational purposes.

