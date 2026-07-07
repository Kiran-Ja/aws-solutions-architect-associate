Daily Lab Logs

Day 2: EC2 Fundamentals & Architecture Configurations

Concepts Learned: Regional isolation of AWS networking assets (Elastic IPs 
and Network Interfaces), differences between EC2 Instance Launch Types, 
operational trade-offs of the 3 Placement Group strategies (Cluster, 
Spread, and Partition), and instance state lifecycles including 
Hibernation mechanisms.
Implementations:
Configured explicit 'chmod 400' security permissions on a private '.pem' 
key file to execute a secure local SSH tunnel from a Mac environment into 
a live instance.
Provisioned and deployed an Amazon Linux 2023 EC2 instance live in the 
'us-east-1' (N. Virginia) data tier.
Executed an EC2 Hibernate routine, tracking how the instance state 
interacts with system memory and verifying storage/network continuity upon 
wakeup.
Tested network topology behaviors by configuring all 3 types of Placement 
Groups to manipulate underlying hardware distribution.
Isolated and resolved cross-region routing conflicts by destroying an 
orphaned Tokyo ('ap-northeast-1') Elastic IP and generating a localized N. 
Virginia equivalent.
Attached and managed multiple Elastic Network Interfaces (ENIs) to assess 
multi-homed networking setups directly through active SSH terminal 
diagnostics.
Executed secure cloud resource terminations and detached manual components 
to ensure zero-cost infrastructure compliance.

