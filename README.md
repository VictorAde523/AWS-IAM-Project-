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

- **Created IAM users and user groups:** Set up named user accounts for individuals and created user groups (`Admins`, `BillingAdmins`) to manage permissions collectively.
- **Attached policies:** Assigned `AdministratorAccess` to the Admin group to grant full permissions and confirmed user inheritance via group attachment.
- **Tested group/user policy application:** Verified effective permissions using the IAM Policy Simulator tool.
- **Created and applied a custom policy:** Developed `RDSLimitedAccess`, which restricted RDS actions to specific DB tags and department group. Applied this to the `DBAdmins` group and confirmed it worked with IAM user "Emily."
- **Configured AWS CLI access:** Generated and tested access keys by configuring the CLI (`aws configure`) and attempting commands like `aws s3 ls`. Adjusted credentials and paths when troubleshooting CLI access.
- **Enabled MFA and secured root user:** Enabled MFA for the root user and users with console access. Verified console activity and access key usage history.
- **Debugged permission issues:** Resolved EC2 and S3 access issues by reviewing policy statements and using the AWS Policy Generator to modify or restrict permissions.
- **Created S3 bucket policies:** Denied access to a user (`Connor`) via a custom S3 bucket policy generated from the AWS Policy Generator, and tested it through the console.
- **Created RDS instances:** Launched two RDS instances using MySQL in `us-east-1`, verified their configuration, and backed them up.
- **Deleted RDS instances:** Performed cleanup by initiating deletion of the RDS instances once lab testing was complete.
- **Set up an AWS Organization:** Created an AWS Organization and added a second AWS account under a root OU for practicing account management and central governance.

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

## 💡 Why This Repo?

This is both a **learning record** and a **personal reference** for future IAM and access control projects on AWS. I also aim to showcase practical knowledge to potential employers or collaborators.

---

## 📅 Timeline

| Date       | Task Completed                |
|------------|-------------------------------|
| 2025-04-15 | Created IAM Users & Groups    |
| 2025-04-16 | Configured RDS & Custom Policies |
| 2025-04-16 | Set Up Organizations & Denied S3 Access |

---

## 🔗 Resources

- [Udemy Course](https://www.udemy.com/)
- [AWS IAM Documentation](https://docs.aws.amazon.com/iam/)
- [AWS CLI Command Reference](https://docs.aws.amazon.com/cli/latest/index.html)
