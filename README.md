# AWS Access Management Learning Journey

This repository documents my hands-on work and learning notes from the Udemy course:  
**“Learn AWS Access Management [AWS IAM], AWS Organizations, Directory Service, SSO and Federation”**

---

## 📚 Course Overview

The course covers the core components of identity and access management in AWS, including:

- AWS Identity and Access Management (IAM)
- AWS Organizations
- AWS Single Sign-On (SSO)
- Directory Services
- Federation and Cross-account Access

---

## ✅ What I've Done So Far

### IAM Fundamentals (Sections 1–6)

Here’s a breakdown of the hands-on work I’ve completed so far:

### 1. IAM Users and Groups
- ✅ **Created IAM users** and user groups (`Admins`, `BillingAdmins`):
  - Set up named user accounts for individuals and created user groups to manage permissions collectively.

- ✅ **Attached policies** to user groups:
  - Assigned `AdministratorAccess` to the `Admins` group for full access, simplifying permission management for multiple users.

- ✅ **Tested group/user policy application**:
  - Used the IAM Policy Simulator tool to verify effective permissions for users and groups.

- ✅ **Created and applied a custom policy** (`RDSLimitedAccess`):
  - Developed a custom policy restricting RDS actions based on DB tags and department groups. Applied it to the `DBAdmins` group and tested it with the IAM user "Emily."

- ✅ **Configured AWS CLI access**:
  - Generated access keys and tested access via the AWS CLI with commands like `aws s3 ls`.

- ✅ **Enabled MFA** for root and console users:
  - Secured the root user and console users by enabling MFA, enhancing security.

- ✅ **Debugged permission issues**:
  - Resolved EC2 and S3 access issues by reviewing IAM policy statements and using the AWS Policy Generator.

- ✅ **Created S3 bucket policies**:
  - Generated a custom S3 bucket policy to deny access to a user (`Connor`) and tested it.

- ✅ **Created RDS instances**:
  - Launched two MySQL RDS instances in the `us-east-1` region, verified their configuration, and backed them up.

- ✅ **Deleted RDS instances**:
  - Performed cleanup by deleting the RDS instances after testing was completed.

- ✅ **Set up an AWS Organization**:
  - Created an AWS Organization and added a second account under a root OU for practicing account management.

> These tasks allowed me to practice and solidify the concepts of managing IAM users, creating custom policies, troubleshooting access issues, and setting up cloud resources such as RDS and S3.

### 2. Working with IAM Roles
- ✅ **Created IAM roles** for AWS services such as EC2 and Lambda:
  - Defined roles to grant EC2 instances permissions to access AWS resources like S3 without needing AWS credentials stored locally.
  
- ✅ **Assigned trust relationships** to define which entities can assume the roles:
  - Configured trust relationships to allow EC2 instances and other services to assume specific roles based on defined policies.

- ✅ **Attached permission policies** to roles:
  - Added policies such as `AmazonS3ReadOnlyAccess` to roles to allow EC2 instances to interact with resources securely.

- ✅ **Launched an EC2 instance** with an assigned IAM role:
  - Verified that EC2 could access S3 without storing AWS credentials locally by associating the IAM role with the instance.

- ✅ **Verified EC2 access to S3**:
  - Confirmed that the EC2 instance could securely access S3 resources without local credential management, using the permissions attached to the IAM role.

- ✅ **Used AWS CLI to assume roles with `sts:AssumeRole`**:
  - Practiced using the `sts:AssumeRole` command to temporarily assume roles and test cross-account access scenarios.

- ✅ **Reviewed role usage via CloudTrail**:
  - Explored CloudTrail to monitor IAM role usage and track the activities associated with role assumptions.

- ✅ **Practiced cross-account role creation and trust configuration**:
  - Created cross-account roles and configured trust policies to allow secure access between AWS accounts.

> These tasks helped develop a deeper understanding of how to configure, manage, and monitor IAM roles in AWS, which are critical for securely managing access to AWS resources.


### 3. Directory Services and Federation
- ✅ **Created a Microsoft AD directory** in the AWS Directory Service.  
  - Configured the directory with necessary parameters like **directory name**, **DNS name**, **NetBIOS name**, and **admin password**.  
  - Waited for the directory to become **Active** before proceeding with further steps.
  
- ✅ **Created IAM roles for the directory** to provide the required permissions for EC2 instances and administrative users:  
  - **EC2Domain** role:  
    - Attached the following permissions:
      - `AmazonSSMManagedInstanceCore`: For enabling Systems Manager to interact with EC2 instances.
      - `AmazonSSMDirectoryServiceAccess`: For enabling EC2 instances to join the domain.
  
  - **AD-PowerUser** role:
    - Attached the `PowerAccess` policy to grant elevated privileges for domain management.

- ✅ **Created an Application Access URL** for accessing domain-integrated applications.

> These steps help to integrate Microsoft AD into AWS, configure roles with necessary permissions for EC2 instances and admins, and set up access for applications linked to the AD directory.

---

## 🛠️ Tools Used

- **AWS Management Console**
- **AWS CLI**
- **Visual Studio Code** (for notes and version control)
- **Git & GitHub** (for tracking progress)

---

## 📌 Next Steps

- Explore and configure AWS Organizations further
- Practice Delegated Admin and Service Control Policies (SCPs)
- Set up AWS SSO for centralized access
- Learn about Directory Services and Federated Identity
- Automate IAM setup using CLI and CloudFormation

---

## 📝 Notes

> I will continue updating this repo with:
> - Step-by-step task breakdowns
> - Command-line examples
> - Screenshots
> - Key takeaways and gotchas

---

## 📸 Screenshots

![IAM User Permissions](https://github.com/user-attachments/assets/5aef8004-5f14-4aec-a961-469dc5230b36)
![Admin Group Members](https://github.com/user-attachments/assets/55ba5b41-27c9-4050-9387-cf3ba1aef5ad)
![IAM Groups Overview](https://github.com/user-attachments/assets/4b43ad08-1885-4d12-b0a3-c37565f0ab16)
![AWS CLI Configuration](https://github.com/user-attachments/assets/2f7c8917-ea88-40c9-bdd2-ec56290e146d)
![IAM Dashboard](https://github.com/user-attachments/assets/7a762407-9157-4a55-83b5-3c4dc844e9a4)
![S3 Bucket Policy Applied](https://github.com/user-attachments/assets/73e90592-7182-431b-bc2e-59b9d950c376)
![Policy Generator](https://github.com/user-attachments/assets/7390a37d-4a1f-4673-932a-2eed86478fba)
![IAM Policy Simulator Results](https://github.com/user-attachments/assets/f526934e-16f6-475c-8bde-aa16579f11a2)
![AWS Organizations Setup](https://github.com/user-attachments/assets/a43c9b28-4b82-431e-be9a-86b97ed41d94)
![RDS Monitoring](https://github.com/user-attachments/assets/60741c7d-a010-4ca0-b9e4-8af11a5b4360)
![RDS Instances](https://github.com/user-attachments/assets/5932f1ae-ba48-477f-b80e-e0918c4c8884)
![Custom RDS Policy](https://github.com/user-attachments/assets/2fb9768c-6849-4f02-a276-a9cccb18963b)
![Emily IAM Permissions](https://github.com/user-attachments/assets/c13fd17a-5a70-4a99-82e6-846b93c33803)
![MySQL Engine Selection](https://github.com/user-attachments/assets/b2e0bee6-2d4b-46f5-8ebf-3e0a624761b1)
![RDS Deleting State](https://github.com/user-attachments/assets/0f3af26d-4e92-40bc-bba5-a7a1a3b234d8)
![EC2 API Error Due to Permissions](https://github.com/user-attachments/assets/cd9c2e92-dd15-4d88-8d5b-cbd2389b428a)
![S3 Access Denied](https://github.com/user-attachments/assets/ad62a91a-e2dc-47cc-bf56-95b27e685aa3)

---


## 📅 Timeline

| Date       | Task Completed                |
|------------|-------------------------------|
| 2025-04-15 | Created IAM Users & Groups    |
| 2025-04-16 | Configured RDS & Custom Policies |
| 2025-04-16 | Set Up Organizations & Denied S3 Access |
| 2025-04-29 | Worked with IAM Roles (created EC2Domain & Lambda roles, configured trust policies, launched EC2 with role, assumed roles via CLI, tested cross-account access, audited via CloudTrail) |
| 2025-04-29 | Configured Directory Services & Federation (provisioned Microsoft AD, created EC2Domain & AD-PowerUser roles, set up Application Access URL) |

---

## 🔗 Resources

- [Udemy Course](https://www.udemy.com/)
- [AWS IAM Documentation](https://docs.aws.amazon.com/iam/)
- [AWS CLI Command Reference](https://docs.aws.amazon.com/cli/latest/index.html)
