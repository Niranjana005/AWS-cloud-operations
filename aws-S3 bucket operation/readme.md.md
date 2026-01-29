                                                              AWS S3 – Bucket, Policy & Versioning (Hands-On)

--------------------------------------------------

Overview
--------
This project documents my hands-on learning with Amazon S3.
The objective was to understand how S3 buckets work, how public
access is controlled using bucket policies, and how object
versioning behaves during overwrites.

This is a learning experiment, not a production setup.


What I Practiced
----------------

1. S3 Bucket Creation
- Created an S3 bucket using the AWS Management Console
- Used default settings to understand baseline behavior


2. Object Upload
- Uploaded an image file (Lily flower)
- Verified object storage and basic access behavior


3. Bucket Policy (Public Read Access)
- Used AWS Policy Generator
- Added a bucket policy to allow public read access (s3:GetObject)
- Used bucket ARN with /* to allow access to all objects
- Verified access using the object URL

4. Object Overwriting
- Uploaded the same object again with changes
- Observed overwrite behavior


5. Bucket Versioning
- Enabled S3 versioning
- Confirmed that each overwrite creates a new version
- Previous versions are retained automatically


6. Cleanup and Cost Awareness
- Downloaded required files and screenshots
- Deleted objects, bucket policy, and the bucket
- Purpose: avoid unnecessary AWS charges


Screenshots
-----------
Screenshots included show:
- Bucket creation
- Object upload
- Bucket policy configuration
- Versioning behavior
- Public access verification


Key Learnings
-------------
- S3 is region-based but globally accessible
- Public access is controlled via bucket policies
- Versioning protects against accidental overwrites
- AWS resources must be cleaned up properly
- Even small experiments should be documented clearly


Best Practices Observed
-----------------------
- Avoid public buckets unless required
- Enable versioning for important data
- Delete test resources after learning
- Use clear naming and documentation


Notes
-----
- This project is part of my AWS fundamentals learning journey
- All actions were performed manually via AWS Console
- No production data was used