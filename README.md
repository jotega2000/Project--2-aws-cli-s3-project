
# AWS CLI & Amazon S3 — Hands-On Project

## Project Overview

This project demonstrates hands-on experience managing Amazon S3 object storage using AWS CLI and Windows PowerShell.

The project covers AWS CLI configuration, IAM authentication, S3 bucket creation, file uploads, downloads, and verification.

## Technologies Used

- AWS CLI v2.40.1
- Amazon S3
- AWS IAM
- Windows 11 PowerShell
- Git and GitHub

## Project Implementation

### 1. AWS CLI Configuration

Configured AWS CLI using IAM credentials and verified authentication.

```powershell
aws --version
aws configure
aws sts get-caller-identity
```

### 2. Create an S3 Bucket

Created an S3 bucket in the AWS Ohio region.

```powershell
aws s3 mb s3://otega-cloud-lab-2026 --region us-east-2
```

### 3. List S3 Buckets

```powershell
aws s3 ls
```

Verified that the bucket was successfully created.

### 4. Upload a File

Created a local text file using PowerShell.

```powershell
Set-Content -Path test.txt -Value "This is my AWS S3 project using AWS CLI"
```

Uploaded the file to Amazon S3.

```powershell
aws s3 cp test.txt s3://otega-cloud-lab-2026/
```

### 5. Verify Uploaded Object

```powershell
aws s3 ls s3://otega-cloud-lab-2026/
```

**Verification result:**

```text
2026-11-12 12:12:33         41 test.txt
```

### 6. Download the File

```powershell
aws s3 cp s3://otega-cloud-lab-2026/test.txt downloaded-test.txt
```

### 7. Verify Downloaded Contents

```powershell
Get-Content downloaded-test.txt
```

**Result:**

```text
This is my AWS S3 project using AWS CLI
```

## Project Results

- Successfully configured AWS CLI authentication.
- Created an Amazon S3 bucket.
- Uploaded a 41-byte text file to S3.
- Verified the uploaded object using AWS CLI.
- Downloaded the object to Windows.
- Verified the downloaded file contents.

## Security Considerations

- AWS access credentials are not included in the repository.
- Sensitive local files are excluded using `.gitignore`.
- Least-privilege IAM permissions are recommended.
- S3 Block Public Access should remain enabled unless required otherwise.

## Key Skills Demonstrated

`AWS CLI` `Amazon S3` `IAM` `PowerShell` `Cloud Storage` `Git`

## Future Improvements

- Implement least-privilege IAM policies.
- Enable S3 versioning and explore encryption controls.
- Automate S3 operations using PowerShell.
- Provision cloud resources using Terraform.

## Author

**Julius Otega**

Cybersecurity | Cloud Security | DevSecOps
