### Initial Access: Exploit Public-Facing Application (T1190)
Attackers can exploit vulnerabilities in the Kubernetes API server or exposed applications running on EKS clusters to gain unauthorized access. Outdated or misconfigured components may present an attack surface for exploiting these public-facing services, leading to execution of malicious code or unauthorized data access.

### Execution: Command and Scripting Interpreter (T1059)
Once access is achieved, adversaries may use Kubernetes API commands to execute arbitrary commands within containers. Attackers may leverage scripting interpreters available within the container environment to perform post-exploitation activities like installing malware or pivoting within the network.

### Persistence: Container-Orchestration Job (T1078)
Attackers could create or modify kube-controller jobs or cronjobs within EKS to maintain persistence. By scheduling the execution of malicious workloads, adversaries ensure that their presence persists through automated, recurring tasks or jobs within the Kubernetes environment.

### Privilege Escalation: Container in Container (T1611)
An adversary with access to a compromised container within EKS may attempt privilege escalation by exploiting vulnerabilities allowing running a new, nested container. This nested container might be configured to run with elevated privileges or capabilities, enabling broader control over the target environment.

### Defense Evasion: Impair Defenses (T1562)
Attackers may disable or modify logging and monitoring services in EKS to conceal their activities. This could involve tampering with AWS CloudTrail or disabling Kubernetes native logging to reduce visibility into malicious operations carried out within the cluster.

### Credential Access: Application Access Token (T1550.001)
EKS workloads may involve the use of API tokens or service account credentials that attackers can steal to perform lateral movement or elevate privileges. Harvesting these credentials from within pods allows attackers to escalate their privileges or access additional resources unauthorizedly.

### Discovery: Network Service Discovery (T1046)
Attackers could perform network service discovery within the Kubernetes environment to enumerate running services and connections in EKS. This technique helps identify potential targets for lateral movement or further exploitation within the cluster's network topology.

### Lateral Movement: Exploitation of Remote Services (T1210)
An attacker may exploit vulnerabilities in adjacent services or nodes within the EKS environment for lateral movement. This involves leveraging known or unknown vulnerabilities in interlinked services to propagate malicious payloads across the Kubernetes cluster.

### Impact: Resource Hijacking (T1496)
EKS clusters may fall victim to resource hijacking, where attackers deploy malicious workloads to leverage compute resources for cryptocurrency mining or fraudulent activities. This affects the availability and performance of legitimate applications running in the EKS environment, leading to increased operational costs.
