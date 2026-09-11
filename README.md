# 🏗️ Terraform AWS 3-Tier VPC - Production Grade

Production-ready Highly Available VPC architecture built with Terraform.

## Architecture
- **VPC:** 10.0.0.0/16
- **6 Subnets across 2 AZs (eu-north-1a, 1b):**
    - 2x Public (Web Tier) - with IGW
    - 2x Private App Tier - with NAT
    - 2x Private DB Tier - isolated
- **Components:** IGW, NAT Gateway, 3 Route Tables

## Diagram
