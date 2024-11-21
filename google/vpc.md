### T1190: Exploit Public-Facing Application
Adversaries may exploit vulnerabilities in public-facing applications deployed within a GCP Virtual Private Cloud (VPC) to achieve initial access. This could include web applications or any services exposed through the Google Cloud Load Balancer. Exploiting these vulnerabilities could allow attackers to execute unauthorized code or commands within the VPC.

## Execution

### T1059: Command and Scripting Interpreter
Once access has been gained, adversaries may use command line and scripting utilities to execute commands on virtual machines (VMs) in the GCP VPC. Scripting languages such as Python, Bash, or PowerShell could be used to automate tasks and maintain persistence.

## Persistence

### T1136.003: Create Cloud Account
Adversaries may create accounts within GCP and grant them access to the VPC to maintain persistence. These accounts could be used to regain access if initial entry points are remediated, and they often have legitimate access and roles that allow them to blend in with normal users.

## Privilege Escalation

### T1068: Exploitation for Privilege Escalation
Attackers may try to exploit software vulnerabilities within the VPC to escalate their privileges. Whether through unpatched software or configuration weaknesses, successful exploitation can lead to higher privileges on the network or within the cloud environment.

## Defense Evasion

### T1070.004: File Deletion
Adversaries may delete logs or alter audit trails in GCP environments to evade detection. GCP’s Stackdriver Logging and Cloud Audit Logs may be targeted to obfuscate the adversary's actions within the VPC settings.

## Credential Access

### T1552.001: Unsecured Credentials
Stored credentials within the cloud environment present a target for attackers. Adversaries may search for credentials improperly stored in instance metadata, hard-coded in applications, or present in source code repositories that facilitate lateral movement within or access to the GCP VPC.

## Discovery

### T1069.003: Cloud Service Discovery
Once inside the GCP environment, adversaries may perform reconnaissance to discover running services and resources within the VPC. This can include listing out Compute Engine instances, understanding network configurations, or identifying data storage services like Google Cloud Storage buckets.

## Lateral Movement

### T1534: Internal Spearphishing
Adversaries can perform lateral movement by executing internal spearphishing campaigns targeting VPC users with legitimate access. Compromised accounts can provide further access to internal resources and expand the threat actor’s footprint within the VPC.

## Collection

### T1114.002: Email Collection: Mail Client
Attackers may attempt to collect sensitive information from mail clients used by individuals accessing the VPC, particularly if the cloud environment integrates with corporate email solutions or uses cloud-native email services.

## Impact

### T1485: Data Destruction
Adversaries may seek to cause business disruption by destroying data or resources hosted within a GCP VPC. This could include deleting virtual machines, erasing storage buckets, or corrupting network configurations, leading to service downtime and potential data loss.
