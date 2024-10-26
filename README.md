# Secure VPC Setup with EC2 Instances, Load Balancer, and Auto Scaling

This project demonstrates the setup of a secure Virtual Private Cloud (VPC) with EC2 instances, an Application Load Balancer, and an Auto Scaling Group on AWS. The goal is to create a scalable and secure infrastructure for running web applications.

## Project Structure

1. **VPC Design and Configuration:**
   - Created a VPC with custom IP ranges (`10.0.0.0/16`).
   - Set up public (`10.0.1.0/24`, `10.0.2.0/24`) and private subnets (`10.0.3.0/24`, `10.0.4.0/24`).
   - Configured route tables and associated them with the subnets.

2. **Network Security:**
   - Set up Network ACLs to control inbound and outbound traffic.
   - Configured Security Groups for EC2 instances to allow specific ports and protocols.

3. **Provision EC2 Instances:**
   - Launched EC2 instances in both public and private subnets.
   - Configured Security Groups for instances to allow necessary traffic.
   - Created and assigned IAM roles to the instances with appropriate permissions.

4. **Networking and Routing:**
   - Set up an Internet Gateway to allow internet access for instances in the public subnet.
   - Configured a NAT Gateway to enable outbound internet access for instances in the private subnet.
   - Created appropriate route tables and associated them with the subnets.

5. **Application Load Balancer:**
   - Created an Application Load Balancer to distribute traffic across multiple EC2 instances.
   - Configured listeners and target groups for the load balancer.
   - Implemented path-based routing to handle traffic for different applications.

6. **Auto Scaling Group:**
   - Created an Auto Scaling Group to automatically scale the number of EC2 instances based on demand.
   - Configured scaling policies to handle increases and decreases in traffic.
   - Ensured high availability by distributing instances across multiple Availability Zones.

7. **SSH Key Pair and Access Control:**
   - Generated an SSH key pair and securely stored the private key.
   - Configured instances to allow SSH access only with the generated key pair.
   - Implemented IAM policies and roles to control access and permissions to AWS resources.

8. **Testing and Validation:**
   - SSH into EC2 instances using the private key and verified connectivity.
   - Tested network connectivity between instances in different subnets.
   - Validated Security Group rules and Network ACL settings.

## Technologies Used

- **AWS EC2**
- **AWS VPC**
- **AWS IAM**
- **AWS Load Balancer**
- **AWS Auto Scaling**
- **AWS Route 53**
- **SSH**
- **Amazon Route 53**
  
- link https://youtu.be/FZPTL_kNvXc?si=CqnoXdGwDxEaf3v0



