# Asset-Oriented Risk Assessment Of Storage Assets In AWS And Azure
# Name: KISHORE J
# REG NO:212225240072
## Aim
To perform an asset-oriented risk assessment of cloud storage assets including:
- AWS Elastic Block Store (EBS)
- AWS Elastic File System (EFS)
- Azure Files (File Storage)



## Pre-requisites

### 1. Background
Cloud storage services offer flexible, scalable options for storing data. However, each storage type brings distinct security risks and configurations. This experiment focuses on identifying assets and performing a detailed risk assessment based on:
- Confidentiality, Integrity, and Availability (CIA)
- Access control
- Encryption
- Auditing capabilities

### 2. Tools Required
- AWS Console with EC2, EBS, and EFS access  
- Azure Portal with Storage Account access  
- IAM credentials with sufficient permissions  
- Risk Assessment Template (provided)  
- Internet browser  
- Microsoft Excel or Google Sheets for tabulating findings


## Procedure

### Part A: Identifying AWS Storage Assets

#### Step 1: Login to AWS Console
- Go to: [https://aws.amazon.com/console](https://aws.amazon.com/console)  
- Log in using IAM or root credentials

#### Step 2: Identify EBS Volumes
- Navigate to: `EC2 > Volumes (under Elastic Block Store)`
- Record the following:
  - Volume ID
  - Size and Type (e.g., gp2, io1)
  - Availability Zone
  - Attached instance (if any)
  - Encryption status
  - Tags

#### Step 3: Identify EFS File Systems
- Go to: `EFS > File systems`
- Record:
  - File system ID and name
  - Mount targets (AZs)
  - Throughput mode (bursting/provisioned)
  - Performance mode
  - Lifecycle policy
  - Encryption at rest status


### Part B: Identifying Azure File Storage Assets

#### Step 4: Login to Azure Portal
- Go to: [https://portal.azure.com](https://portal.azure.com)
- Log in using credentials with access to storage accounts

#### Step 5: View File Shares
- Navigate to: `Storage Accounts > Choose Account > File Shares`
- Record:
  - Name
  - Quota (in GB)
  - Used space
  - Protocol (SMB/NFS)
  - Authentication method (SAS Tokens, Azure AD, Shared Keys)
  - Snapshot policies


## Risk Assessment Methodology

Use the following **CIA-based asset-oriented checklist** for each asset:

| Criteria         | Description                                  |
|------------------|----------------------------------------------|
| Confidentiality  | Encryption, authentication, access control   |
| Integrity        | Data consistency, snapshot support, checksums|
| Availability     | Multi-AZ, redundancy, auto-scaling           |
| Access Control   | IAM, Security Groups, ACLs                   |
| Encryption       | At-rest and in-transit encryption            |
| Auditing         | CloudTrail, logs, alerts                     |


## Sample Output Table

| Cloud Provider | Asset Type | Asset ID  | Encrypted | Access Control  | Risk Level | Comments         |
|----------------|------------|-----------|-----------|------------------|------------|------------------|
| AWS            | EBS Volume | vol-abc   | Yes       | IAM Policy       | Medium     | Used by EC2      |
| AWS            | EFS        | fs-xyz    | Yes       | Security Group   | Low        | Multi-AZ mount   |
| Azure          | File Share | datafiles | Yes       | Shared Key       | Medium     | Quota 1TB        |

# output:
<img width="1919" height="1077" alt="Screenshot 2026-08-05 111203" src="https://github.com/user-attachments/assets/3229cffa-baa6-460f-be7b-edcf553cb7e2" />
<img width="1918" height="1079" alt="Screenshot 2026-08-21 133653" src="https://github.com/user-attachments/assets/9a01183a-aa0a-4509-81a8-083ea7657f0c" />
<img width="1919" height="1079" alt="Screenshot 2026-08-21 133919" src="https://github.com/user-attachments/assets/f67e0c6b-fac3-4f17-8fc8-74e97aec8b90" />
<img width="1919" height="1079" alt="Screenshot 2026-08-21 133951" src="https://github.com/user-attachments/assets/aa49cfc0-3cd4-455f-b9ac-de57a25aa92c" />

<img width="1919" height="1076" alt="Screenshot 2026-08-21 134119" src="https://github.com/user-attachments/assets/a7f16727-0b9b-4f5d-ae0a-a64efaf99180" />

<img width="1919" height="1079" alt="Screenshot 2026-08-21 134240" src="https://github.com/user-attachments/assets/9b3a62bc-acc5-4002-bcbd-4f5625307918" />
<img width="1919" height="1079" alt="Screenshot 2026-08-21 134311" src="https://github.com/user-attachments/assets/547dfed0-5203-41de-b4cb-2446b7e9ee9c" />
<img width="1919" height="1079" alt="Screenshot 2026-08-21 134349" src="https://github.com/user-attachments/assets/5f9e1304-06b5-4237-89dd-c32cd425afb9" />

## Result

All active cloud storage assets across AWS and Azure have been identified and assessed for security posture based on CIA principles, access control, encryption, and risk level.
