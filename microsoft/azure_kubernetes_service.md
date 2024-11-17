## Initial Access

### Valid Accounts (T1078)
Attackers may gain access to an Azure Kubernetes Service (AKS) cluster by exploiting valid accounts. This could happen if credentials are leaked, phished, or guessed using credential stuffing or brute force attacks. With valid credentials, adversaries can authenticate and interact with the cluster’s API server to perform malicious actions or exfiltrate data.

## Execution

### Command and Scripting Interpreter (T1059)
Adversaries may execute arbitrary commands on AKS nodes using command and scripting interpreters such as bash or PowerShell. They may exploit container escape vulnerabilities or leverage misconfigured or exposed API endpoints to run scripts. This can allow them to install malware, extract data, or further pivot within the organization’s network.

### Exploitation for Client Execution (T1203)
Exploitation of vulnerabilities in container images or the Kubernetes orchestrator itself can allow attackers to execute code. This might be delivered through image pulls from compromised or malicious registries. Exploit payloads can enable attackers to control the execution environment, escalate privileges, or conduct lateral movements.

## Persistence

### Container Orchestration Job (T1053.005)
Adversaries may use the Kubernetes Job or CronJob resources to maintain persistence within the cluster. By deploying a cron job, malicious scripts or binaries can be re-executed at scheduled intervals, aiding in maintaining a foothold in a compromised environment despite other defensive measures or container restarts.

## Privilege Escalation

### Container Admin Privileges (T1078.004)
Escalation could be achieved by acquiring administrative privileges within a container. This could result from insufficient credential policies or escaping from a container to gain host-level permissions. Such elevated privileges enable attackers to control processes, access sensitive data, or move laterally within the environment.

## Defense Evasion

### Obfuscated Files or Information (T1027)
Attackers may obfuscate scripts or binaries within AKS deployments to evade detection. This can involve encoding payloads or using polymorphic techniques to conceal malicious activities. Obfuscation can occur at various stages of an attack, such as during the transmission, storage, or execution of payloads.

## Credential Access

### Unsecured Credentials (T1552)
Credentials in AKS misconfigurations or improper secrets management practices may be targeted by adversaries. This includes API keys, tokens, or passwords hardcoded in scripts or stored in unsecured Kubernetes ConfigMaps. Exploiting these can facilitate further unauthorized access or lateral movement.

## Discovery

### Cloud Service Discovery (T1580)
An adversary may perform discovery actions to understand the capabilities of the cloud environment. Azure Resource Manager (ARM) APIs can be queried to enumerate Kubernetes services, pods, nodes, and associated resource configurations, which may inform subsequent attack stages such as privilege escalation or data exfiltration.

### Network Service Scanning (T1046)
Attackers could perform network scanning within the AKS environment to discover accessible services and open ports. This includes enumerating Kubernetes service endpoints that are inadvertently exposed to the internet or conduct internal scans to understand the cluster’s network topology.

## Lateral Movement

### Internal Spearphishing (T1534)
Malicious actors may use internal spearphishing tactics within an exploited AKS cluster to compromise additional accounts or services. They might leverage trustworthy channels to deliver phishing content designed to collect credentials or deploy malicious software within the organization’s internal environment.

## Impact

### Data Destruction (T1485)
An adversary may leverage AKS to destroy data within a cluster or across associated storage services. This might be achieved through direct deletion of Kubernetes resources or leveraging compromised credentials to affect Azure storage services, causing application downtime and data loss.

### Resource Hijacking (T1532)
Attackers may hijack computing resources within an AKS cluster for purposes such as cryptocurrency mining. This abuse consumes CPU, memory, or other computational resources, impacting the performance and availability of legitimate applications while incurring unexpected cloud usage costs.
