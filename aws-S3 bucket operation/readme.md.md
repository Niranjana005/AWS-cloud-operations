##### **# AWS S3 Bucket Experiment – Lily Flower Image**



\## Overview



This repository demonstrates a practical experiment with AWS S3, including bucket creation, file upload, bucket policy configuration, object overwriting, and versioning. The project includes screenshots of each step for clear reference.



This is intended as a learning exercise to understand S3 permissions, public access, and versioning.



---

\## Experiment Steps



\### 1. Bucket Creation



\* Created a new S3 bucket using the AWS Management Console.

\* Configured bucket settings and enabled versioning to track object changes automatically.



\### 2. File Upload



\* Uploaded a sample image of a Lily flower to the bucket.

\* Verified the object exists and tested basic S3 object retrieval.



\### 3. Bucket Policy



\* Used the AWS Policy Generator to create a policy allowing public read access.

\* Copied the bucket ARN and applied the generated policy in the bucket policy editor.

\* Tested the public URL — the image loaded successfully.



\### 4. Object Overwriting



\* Uploaded a new version of the Lily image to test S3 versioning.

\* Confirmed that old versions were retained automatically.



\### 5. Cleanup



\* Downloaded all files and screenshots locally.

\* Deleted the bucket to avoid any unnecessary AWS charges.



---



\## Screenshots



The following screenshots document the experiment workflow:



\* \*\*Bucket Creation \& Settings: execution screenshots/bucket creation.PNG

\* \*\* AWS policy generation: execution screenshots/aws policy generator.PNG

\* \*\*bucket arn check:execution screenshots/bucket arn.PNG

\* \*\*Object Versioning:execution screenshots/bucket overwriting and their versions.PNG

\* \*\*json policy:execution screenshots/json policy generation.PNG

\* \*\*public access:execution screenshots/public access check.PNG

\* \*\*status of file in bucket:execution screenshots/upload status of file(image).PNG

\* \*\*before overwriting output:execution screenshots/output obtained!!.PNG

\* \*\*after overwritten output:execution screenshots/overwritten output.PNG



---



\## Key Learnings



\* How to create and configure S3 buckets.

\* How to upload objects and make them publicly accessible.

\* Understanding bucket policies and ARNs.

\* How versioning works for overwritten objects.

\* Best practices for managing AWS resources efficiently to avoid costs.



---



\## Best Practices



\* Always enable versioning for important buckets.

\* Test object URLs before sharing publicly.

\* Delete test buckets to avoid incurring charges.

\* Use organized folder structures for files and screenshots in GitHub.



---



\## Notes



\* This repo serves as a learning and documentation exercise.

\* All AWS services used were free-tier or small-scale testing.

\* The images and screenshots are for educational purposes only.





