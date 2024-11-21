### Initial Access: Exploit Public-Facing Application (T1190)
Attackers may acquire access to a Kubernetes environment by exploiting unpatched vulnerabilities in applications exposed to the internet. For example, flaws in the Kubernetes API server or dashboard can allow unauthorized access if not properly secured.

### Initial Access: External Remote Services (T1133)
Unauthorized access may be gained by exploiting exposed remote services. This can include gaining access to management interfaces or services running inside Kubernetes that are not properly secured or configured.

### Initial Access: Valid Accounts (T1078)
Attackers might use compromised credentials to gain access to the Kubernetes environment. Various phishing or credential-stuffing techniques may be employed to obtain these credentials, giving adversaries a foothold within the cluster.

### Execution: Command and Scripting Interpreter (T1059)
Once inside a Kubernetes environment, attackers might leverage execution through command-line interfaces such as `kubectl`. They may run malicious scripts or commands directly within containers to execute further attacks or maintain presence.

### Persistence: Account Manipulation (T1098)
Adversaries might create new accounts or modify existing ones within the Kubernetes environment to ensure ongoing access. This might involve adjusting role-based access control (RBAC) to give themselves more privileges than they should have.

### Persistence: Container Image (T1610)
Attackers may build and deploy their own container images, which might include malicious software or backdoors. These images can be used to gain persistent access to the environment and remain undetected within legitimate operations.

### Privilege Escalation: Container to Host (T1611)
An attacker can attempt to exploit weaknesses in the containerization layer to move from the Kubernetes environment onto the host machine. Successful exploitation would allow full control over the host and potentially the entire cluster.

### Defense Evasion: Masquerading (T1036)
Attackers might rename or alter their scripts, images, or other artifacts to resemble benign or expected ones in the Kubernetes environment, thus avoiding detection by standard security measures or human oversight.

### Credential Access: Credential Dumping (T1003)
Within a compromised container, an adversary might attempt to extract credentials available in the environment. These credentials can include Kubernetes service account tokens or other secrets stored improperly, providing broader access.

### Discovery: System Information Discovery (T1082)
Attackers who gain initial access might enumerate system information within the Kubernetes environment. This could include details about nodes, services, deployments, or resource configurations, which could aid in planning further attacks.

### Lateral Movement: Container Administration Command (T1612)
Adversaries might use legitimate administrative commands to move laterally across the Kubernetes environment, accessing multiple containers or nodes by leveraging Kubernetes management capabilities.

### Collection: Data Staged (T1074)
Attackers might collect and stage collected data in volumes or exports within the Kubernetes environment, making it easier to exfiltrate all at once. This data can include sensitive files or application output that was processed within compromised pods.

### Exfiltration: Transfer Data to Cloud Account (T1537)
Adversaries may exploit cloud storage services for data exfiltration due to their accessibility and scalability. They might transfer collected data from within a Kubernetes environment to an account controlled by the attacker on a cloud provider.

### Impact: Resource Hijacking (T1496)
Attackers may leverage Kubernetes environments to hijack resources for undesirable purposes like cryptomining. This misuse of compute capacity can lead to increased operational costs and reduced performance for legitimate tasks.
