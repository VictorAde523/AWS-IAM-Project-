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
![Screenshot 2025-04-29 101749](https://github.com/user-attachments/assets/f1d4422c-f46e-4dbf-b247-21ff539d8614)
![Screenshot 2025-04-29 101901](https://github.com/user-attachments/assets/39513ecf-116f-47c5-a10b-778f56db49fb)
![Screenshot 2025-04-29 102101](https://github.com/user-attachments/assets/50e648ef-456c-4714-aaf4-29bb0f4d11dd)
![Screenshot 2025-04-29 102146](https://github.com/user-attachments/assets/67b1dde9-94b2-477d-b023-392360716682)
![Screenshot 2025-04-29 102210](https://github.com/user-attachments/assets/ef124f17-a972-4db3-b799-2566c4d54b21)
![Screenshot 2025-04-29 102253](https://github.com/user-attachments/assets/92b9183b-760d-4b4d-b035-5fdc1e4ae85e)
![Screenshot 2025-04-29 102345](https://github.com/user-attachments/assets/24f203d2-12eb-40dd-bb26-ea06893b6735)
![Screenshot 2025-04-29 102428](https://github.com/user-attachments/assets/b66582d5-cd6d-4c68-aaad-b17b5f46f5a0)
![Screenshot 2025-04-29 102512](https://github.com/user-attachments/assets/6bcd94c4-646d-41f6-803e-5c131bc19de7)
![Screenshot 2025-04-29 102530](https://github.com/user-attachments/assets/f5f7363d-22f1-4ba3-ad8f-557b8302807f)
![Screenshot 2025-04-29 102549](https://github.com/user-attachments/assets/ebf78816-99d5-48a2-8eeb-d20b00293bd8)
![Screenshot 2025-04-29 102605](https://github.com/user-attachments/assets/37845229-daad-4278-aeb4-7c646d27f48c)
![Screenshot 2025-04-29 102627](https://github.com/user-attachments/assets/d5288af4-d9e2-48b2-a1fe-4cfc8b4cc7f6)
![Screenshot 2025-04-29 102636](https://github.com/user-attachments/assets/f97a0896-77d7-431e-84bb-b05d855c491c)
![Screenshot 2025-04-29 105549](https://github.com/user-attachments/assets/787767cb-1cd2-48fe-ac0f-e85024c6f20d)
![Screenshot 2025-04-29 105620](https://github.com/user-attachments/assets/b6805020-7e3f-4efa-8f59-1ab0886fe36b)
![Screenshot 2025-04-29 105642](https://github.com/user-attachments/assets/348bffc1-d42f-481f-913c-75201963f734)
![Screenshot 2025-04-29 105727](https://github.com/user-attachments/assets/06d32104-1067-4c77-8192-1a1fca3a051c)
![Screenshot 2025-04-29 105816](https://github.com/user-attachments/assets/de890122-4025-440b-9486-696f2eddc7ed)
![Screenshot 2025-04-29 105828](https://github.com/user-attachments/assets/47af7885-eee1-4090-bf2c-f72bbff00183)
![Screenshot 2025-04-29 110135](https://github.com/user-attachments/assets/c5d3eb83-2c14-4666-9cff-d44cd39fafbb)
![Screenshot 2025-04-29 110315](https://github.com/user-attachments/assets/75e59608-3bd8-4893-a7d0-75ce75cefcb0)
![Screenshot 2025-04-29 110718](https://github.com/user-attachments/assets/dc523a75-8d9c-4bb7-805a-34769d29f329)
![Screenshot 2025-04-29 110734](https://github.com/user-attachments/assets/1be55806-f3a1-4cdd-a6af-f1d6d75ec8ea)
![Screenshot 2025-04-29 111013](https://github.com/user-attachments/assets/b91c7a70-f268-47e4-acb9-dabf5b6615da)
![Screenshot 2025-04-29 124039](https://github.com/user-attachments/assets/a47b0bfe-a2de-4da5-aa47-eddfe80fb9de)
![Screenshot 2025-04-29 124120](https://github.com/user-attachments/assets/b6737f29-43d4-4b81-920f-4095f9b4e054)
![Screenshot 2025-04-29 124131](https://github.com/user-attachments/assets/138b1db3-6c53-4c2c-b102-a518fdd5a0e3)
![Screenshot 2025-04-29 124213](https://github.com/user-attachments/assets/eeed778e-db67-46ac-8755-28b633a97a9e)
![Screenshot 2025-04-29 124243](https://github.com/user-attachments/assets/deb705b5-d7fa-4800-a8a3-dc99daf971a8)
![Screenshot 2025-04-29 124407](https://github.com/user-attachments/assets/1271ddb1-3872-4b47-84a3-3d34874960b2)
![Screenshot 2025-04-29 124725](https://github.com/user-attachments/assets/1ce12aa2-f63d-4282-b562-cee0291f11a5)
![Screenshot 2025-04-29 124759](https://github.com/user-attachments/assets/8d817781-d94f-4127-8709-22ee3b574048)
![Screenshot 2025-04-29 101722](https://github.com/user-attachments/assets/1385dc90-cb13-4479-a748-b45829e87d41)


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
