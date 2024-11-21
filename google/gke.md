## Initial Access: Phishing (T1566)
Phishing remains a significant threat vector wherein attackers craft deceptive emails to lure GKE administrators into revealing credentials or unknowingly executing malicious code. This technique is often used as an entry point to gain unauthorized access to Kubernetes infrastructure by compromising user accounts with elevated permissions.

## Initial Access: Exploit Public-Facing Application (T1190)
Attackers may exploit vulnerabilities in public-facing applications or APIs exposed by GKE clusters. Such vulnerabilities can allow remote code execution or unauthorized access, granting attackers footholds within the Kubernetes environment, which they can then leverage to execute further attacks.

## Persistence: Account Manipulation (T1098)
To maintain persistence in a compromised GKE environment, attackers may manipulate existing user or service accounts. This can include inserting SSH keys, altering permissions, or creating rogue accounts to ensure continued access even after a security incident is discovered and remediated.

## Persistence: Container File System Injection (T1564.004)
Attackers might inject malicious code or executables directly into the file system of running containers in GKE. This technique allows persistence by ensuring that malicious activity resumes within compromised containers upon their restart or upon loading essential files during container operations.

## Privilege Escalation: Container Escape (T1611)
Once inside a GKE pod, adversaries may attempt a container escape by exploiting vulnerabilities in the container runtime. The goal is to gain more extensive privileges on the underlying host node, thereby potentially securing root access over the Kubernetes node or affecting other containers running therein.

## Defense Evasion: Obfuscated Files or Information (T1027)
Adversaries often obfuscate their malware or scripts in a GKE environment to avoid detection by monitoring tools. This can include encoding binaries or scripts and using packers or encryption to disguise malicious payloads, making it difficult for signature-based security solutions to detect these threats.

## Credential Access: Credentials in Files (T1552.001)
GKE environments are susceptible to credential theft when they are inadvertently stored in files within containers or nodes. Attackers can scan the file system to extract credentials for GCP services, Kubernetes API servers, or other applications to escalate privileges or move laterally.

## Discovery: Cluster and Service Discovery (T1687)
Attackers perform discovery actions to map the GKE cluster environment, identifying running pods, nodes, services, and their respective configurations. This reconnaissance is crucial for adversaries to understand how to navigate the environment and plan subsequent attack strategies.

## Lateral Movement: Internal Spearphishing (T1593)
With knowledge of the cluster's operational dynamics, attackers may engage in internal spear-phishing within the compromised GKE environment. By sending credibly crafted messages to users with legitimate-looking requests, they aim to trick additional personnel into revealing secrets or executing malicious commands, facilitating lateral movement.

## Collection: Data from Information Repositories (T1213)
Adversaries targeting GKE often aim to exfiltrate sensitive data by accessing information repositories associated with the cluster. They may target databases, object storage (e.g., Google Cloud Storage buckets), or any service storing valuable information, facilitated by compromised access credentials.

## Impact: Data Destruction (T1485)
An adversary with access to a GKE cluster might execute destructive commands to wipe data or disrupt Kubernetes services critically. This could involve deleting compute instances, instance groups, or entire Kubernetes namespaces, rendering essential components of an organization’s service architecture unusable.
