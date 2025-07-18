# Aws-projects
Automated AWS infrastructure using Terraform with EC2 + EFS
## 🛠️ Tools Used

- AWS EC2, EFS, VPC, Subnet, Internet Gateway
- Terraform (Infrastructure as Code)
- PowerShell (for Windows SSH)
- IAM, Key Pairs
- ## ✅ Why Use Amazon EFS Instead of S3?

Although **Amazon S3** is an excellent service for object storage, this project required:

- **File-level access** (read/write like a normal Linux file system)
- The ability to **mount the same filesystem across multiple EC2 instances**
- **Low-latency**, POSIX-compliant access using standard Linux tools (`cat`, `echo`, etc.)

These are features **S3 does not provide**, as it’s not mountable or usable like a traditional file system.

That’s why I used **Amazon EFS** — it’s perfect for applications where EC2 instances need to **share files in real time**, such as:
- CMS platforms (like WordPress)
- Web server clusters
- Log processing pipelines
