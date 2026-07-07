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
 
## Day 2: EC2 Fundamentals & Architecture Configurations

### Core Concepts Mastered

* **Network Isolation:** Regional limitations and behaviors of Elastic IPs and Elastic Network Interfaces (ENIs).
* **Launch Strategies:** Operational use cases and trade-offs of EC2 Instance Launch Types.
* **Placement Groups:** Structural and hardware distribution differences across Cluster, Spread, and Partition strategies.
* **Instance Lifecycles:** State transitions and the underlying mechanics of instance Hibernation.

---

### Practical Implementations

#### Access & Provisioning

* Enforced strict POSIX permissions on a local `.pem` file via `chmod 400` to secure a macOS-to-EC2 SSH tunnel.
* Deployed a live Amazon Linux 2023 EC2 instance within the `us-east-1` (N. Virginia) region.

#### Topology & State Testing

* Triggered an EC2 Hibernate routine to verify RAM-to-EBS data persistence and network continuity upon wakeup.
* Configured all three Placement Group types to manipulate physical underlying hardware distribution.

#### Networking & Troubleshooting

* Resolved cross-region routing conflicts by destroying an orphaned Tokyo (`ap-northeast-1`) Elastic IP and provisioning a localized N. Virginia equivalent.
* Attached multiple Elastic Network Interfaces (ENIs) to assess multi-homed networking setups using terminal diagnostics.

#### Cleanup

* Executed full cloud resource terminations and detached manual components to maintain zero-cost infrastructure compliance.
