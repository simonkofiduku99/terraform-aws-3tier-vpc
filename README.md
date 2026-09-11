# Terraform AWS 3-Tier VPC - Project 3

Built a production-grade, highly available VPC in `us-east-1` using Terraform.

### Architecture
- **VPC:** `10.0.0.0/16`
- **6 Subnets across 2 AZs:**
    - Public: `10.0.1.0/24` (1a), `10.0.2.0/24` (1b) -> IGW
    - App Private: `10.0.3.0/24` (1a), `10.0.4.0/24` (1b) -> NAT
    - DB Private: `10.0.5.0/24` (1a), `10.0.6.0/24` (1b) -> isolated
- **Gateways:** `project3-igw` + `project3-nat` (with EIP)
- **Security Groups:** App SG + DB SG (MySQL 3306 only from App SG)

### Tech Stack
Terraform, AWS VPC, Kali Linux on VirtualBox, GitHub

### Lessons Learned
- NAT Gateway is $0.05/hr - always destroy after demo
- Fix Kali time with `timedatectl set-ntp true` for AWS auth errors
- Use .gitignore for tfstate

Built by Simon Kofi Duku - Aspiring Cloud Engineer | Accra, GH
