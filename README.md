# AWS Certified Solutions Architect Associate (SAA-C03) Labs

Welcome to my technical proof-of-work repository. Here, I log my daily terminal configurations, architecture implementations, and foundational cloud design labs.

## 🚀 Daily Lab Logs

### Day 1: Identity & Access Management (IAM) & AWS CLI Setup
- **Concepts Learned:** Principal of Least Privilege, Root vs. IAM administrative users, and policy assignment via User Groups.
- **Implementations:** 
  - Configured a secure `admin` IAM group with `AdministratorAccess`.
  - Created a dedicated IAM user profile and locked down the root account.
  - Successfully connected local Windows environment to the AWS cloud infrastructure via Git Bash using the AWS CLI engine.
  - Explored serverless CLI interactions using AWS CloudShell.
 
### Day 2: EC2 Fundamentals & Security Controls
**Concepts Mastered**

Compute Sizing & Use Cases: Categorized EC2 instance families (General Purpose, Compute, Memory, and Storage Optimized) and decoded AWS naming conventions (m5.2xlarge).

Security Group Mechanics: Understood stateful firewall rules (ports 22, 80, 443, 3389), inbound blocking defaults, outbound allowance, and troubleshooting connection timeouts vs. application errors.

Cost Optimization & Purchasing Models: Evaluated trade-offs between On-Demand, Reserved Instances, Savings Plans, Dedicated Hosts/Instances, and Spot Fleets.

**Practical Implementations**

Automated Instance Provisioning: Launched an Amazon Linux EC2 instance in us-east-1 and executed an EC2 User Data bootstrap script during initial launch to automate web server setup.

Network Security Configuration: Built custom Security Groups to regulate HTTP (80) and SSH (22) traffic, testing rule updates to confirm immediate propagation.

Remote Terminal Access: Established secure command-line connections via standard SSH using key pairs, as well as browser-based management via EC2 Instance Connect.

Purchasing & Fleet Exploration: Experimented with instance lifecycle configurations, comparing On-Demand vs. Spot Instance request behaviors and launching options directly within the console.

### Day 3: Advanced EC2 Architecture & Networking

**Concepts Mastered**

IP Addressing Dynamics: Differentiated between Private IPs (internal VPC routing), Public IPs (ephemeral internet access), and Elastic IPs (static IPv4 mapping), recognizing why Elastic IPs should generally be avoided in favor of DNS.

Placement Group Strategies: Evaluated hardware distribution models—Cluster (low-latency, single AZ), Spread (isolated hardware, max 7 instances per AZ for high availability), and Partition (rack-isolated clusters for large-scale distributed workloads like Kafka).

Elastic Network Interfaces (ENIs): Understood virtual network cards (Layer 2) bound to specific Availability Zones, used to detach and reattach secondary private IPs for fast failover.

EC2 Hibernation Mechanics: Analyzed state persistence by saving instance RAM directly to an encrypted root EBS volume for rapid boot times without re-initializing the OS or application cache.

**Practical Implementations**

IP Address & Lifecycle Testing: Observed Public IP address re-assignment upon restarting an EC2 instance, and assigned a static Elastic IP to maintain a persistent address across state changes.

Network Interface Management: Created and attached a secondary Elastic Network Interface (ENI) to a running instance, testing live failover by moving the network card to another EC2 machine within the same Availability Zone.

Hardware Placement Configuration: Created and deployed EC2 instances into custom Placement Groups (Cluster, Spread, and Partition) to manipulate physical underlying hardware distribution.

State Persistence & Hibernation: Provisioned an EC2 instance with an encrypted EBS root volume, enabled hibernation support, and triggered a full RAM-to-EBS dump to verify fast restoration upon startup.
