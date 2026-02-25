# Cloud Infrastructure

## AWS Basics

- EC2 - Virtual machines in the cloud 
![ec2 example](https://devop-final.s3.us-east-1.amazonaws.com/Screenshot+2026-02-25+133203.png)
- Security Groups - Act as a firewall for your instance
- Inbound Rules - Control what traffic can reach your instance

## Common Steps

### Opening a port in AWS:
1. Go to EC2 dashboard
2. Click your instance → Security tab
3. Click the Security Group
4. Edit inbound rules → Add rule
5. Set port, protocol, and source
6. Save rules

### Connecting to EC2:
```bash
ssh -i your-key.pem ec2-user@<public-ip>
```

## Key Concepts
- Always use private subnets for databases
- Never expose port 3306 (MySQL) publicly
- Use IAM roles instead of hardcoding credentials
