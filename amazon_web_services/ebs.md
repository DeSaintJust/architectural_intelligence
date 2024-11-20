**Initial Access - Phishing: Spearphishing Link (T1566.002)**  
Threat actors may target specific individuals within an organization to gain access to AWS credentials that can be used to manipulate Amazon Elastic Block Store (EBS) volumes. Spearphishing attacks often involve emails that appear to be from trusted sources, leading users to malicious websites where their AWS credentials can be harvested.

**Initial Access - Exploit Public-Facing Application (T1190)**  
Compromising a publicly accessible application that has permissions to manage Amazon EBS resources can allow attackers unauthorized access to EBS volumes. Attackers may leverage vulnerabilities in applications running on EC2 instances to gain control over EBS volumes attached to those instances.

**Defense Evasion - Virtualization/Sandbox Evasion (T1497)**  
Adversaries may attempt to evade defenses by detecting the virtualized environment in which EBS operates and then altering their behavior to avoid detection. This can involve manipulating aspects of the environment in which EC2 instances and EBS volumes run or using legitimate access to change security configurations to avoid alerting monitoring systems.

**Credential Access - Valid Accounts (T1078)**  
Attackers might gain access to a victim’s AWS account using stolen credentials. Once access is obtained, adversaries can control various aspects of EBS, such as creating snapshots, attaching or detaching volumes to instances, or deleting volumes – leading to potential data loss or service disruption.

**Discovery - Cloud Service Discovery (T1580)**  
Once attackers have compromised an account, they might attempt to enumerate EBS volumes as part of a broader effort to map out resources in the AWS cloud environment. This can include querying and listing available EBS volumes and snapshots, which can be leveraged for further attacks or data exfiltration.

**Impact - Data Destruction (T1485)**  
Adversaries with sufficient permissions might threaten an organization by destroying data stored within Amazon EBS. This can involve deleting EBS snapshots or volumes, thereby causing data loss and potential downtime, critical for business continuity.

**Impact - Resource Hijacking (T1496)**  
After gaining access to AWS resources, attackers could exploit EBS for illicit purposes, such as using storage for unauthorized applications or processes. Such actions can incur unexpected costs and impact the performance of legitimate applications utilizing EBS resources.
