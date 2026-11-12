\# AWS CLI \& Amazon S3 — Hands-On Project



\## Project Overview



This project demonstrates practical experience using AWS CLI to manage Amazon S3 cloud storage resources through Windows PowerShell.



\## Technologies Used



\- Amazon Web Services (AWS)

\- AWS CLI v2.40.1

\- Amazon S3

\- AWS Identity and Access Management (IAM)

\- Windows PowerShell

\- Git and GitHub



\## Project Implementation



\### 1. AWS CLI Configuration



Configured AWS CLI with IAM credentials and verified authentication.



```powershell

aws configure

aws sts get-caller-identity

```



\### 2. S3 Bucket Creation



Created an Amazon S3 bucket in the AWS Ohio region.



```powershell

aws s3 mb s3://otega-cloud-lab-2026 --region us-east-2

```



\### 3. Listing S3 Buckets



```powershell

aws s3 ls

```



\### 4. Uploading a File



```powershell

aws s3 cp test.txt s3://otega-cloud-lab-2026/

```



\### 5. Verifying the Upload



```powershell

aws s3 ls s3://otega-cloud-lab-2026/

```



\### 6. Downloading a File



```powershell

aws s3 cp s3://otega-cloud-lab-2026/test.txt downloaded-test.txt

```



\### 7. Verifying File Contents



```powershell

Get-Content downloaded-test.txt

```



\## Project Results



\- Successfully configured AWS CLI authentication.

\- Created and verified an S3 bucket.

\- Uploaded a local text file to Amazon S3.

\- Downloaded the stored object using AWS CLI.

\- Verified file contents using PowerShell.



\## Security Considerations



AWS credentials are excluded from this repository. For future projects, I plan to implement least-privilege IAM policies and further explore S3 security controls.



\## Key Skills Demonstrated



AWS CLI | Amazon S3 | IAM | PowerShell | Cloud Storage | Git



\## Author



Julius Otega



Cybersecurity | Cloud Security | DevSecOps

