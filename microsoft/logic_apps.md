### Execution: User Execution (T1204)

Azure Logic Apps are susceptible to threats arising from compromised user accounts, where unauthorized individuals may execute logic apps by tricking legitimate users into executing malicious instructions or modifying existing logic apps. Phishing attacks or other social engineering techniques can lure users into performing unintended actions that could compromise the logic apps, thereby allowing attackers to modify workflows or inject malicious payloads that could subsequently trigger during regular execution.

### Initial Access: Valid Accounts (T1078)

Attackers may gain initial access to Azure Logic Apps by compromising valid user accounts. This can occur through techniques such as credential stuffing, where attackers use credential dumps from other sites, or by exploiting weak or reused passwords. Once access to valid accounts is established, attackers can potentially access, modify, or create logic apps, gaining further insight into an organization's business processes and potentially manipulating them for malicious purposes.

### Persistence: Create or Modify System Process (T1543.003)

Persistence in Azure Logic Apps could be maintained by attackers who create or modify system processes. An attacker with sufficient privileges might create a new logic app or modify an existing app to include malicious processes, ensuring they have ongoing access to orchestrate or exfiltrate data or manipulate the logic app to perform unintended actions during its execution. This manipulation might go undetected if not properly monitored.

### Privilege Escalation: Hijack Execution Flow (T1574)

Privilege escalation can be achieved by hijacking the execution flow within Azure Logic Apps. If an attacker has limited access to the Azure environment, they may attempt to escalate their privileges by exploiting misconfigurations or injecting malicious steps into the execution pipeline of a logic app. This could allow them to manipulate app operations, access sensitive data, or pivot to other resources within the Azure environment.

### Credential Access: Input Capture (T1056)

Azure Logic Apps might be targets for credential capturing by attackers if sensitive information like API keys or plain-text passwords are used within the app workflows. Attackers could capture input credentials by gaining access to debugging and execution logs where these sensitive details might be inadvertently logged or by deliberately injecting steps that capture and forward such information to an attacker-controlled endpoint.

### Lateral Movement: Use Alternate Authentication Material (T1550)

Lateral movement can occur if an attacker uses alternate authentication materials, such as OAuth tokens or API keys stored within Azure Logic Apps, to access other services tied to the app. Mismanagement or exposure of such authentication materials can allow an attacker to freely move laterally within the Azure environment without needing additional credentials, thus increasing the attack radius.

### Collection: Automated Collection (T1119)

Attackers can exploit Azure Logic Apps for automated data collection by creating apps that automatically gather, aggregate, and export sensitive business data. Once an attacker gains the ability to modify or create logic apps, they may set up processes to siphon off sensitive information frequently or at particular events, sending this data to attacker-controlled destinations without raising immediate suspicion.

### Command and Control: Application Layer Protocol (T1071)

Logic Apps might be manipulated by attackers to use application layer protocols as a covert command and control channel. Azure Logic Apps that interact with web services or APIs can be exploited such that communications to these services are manipulated to include commands or data exfiltration tasks using normal application layer protocols, masking malicious activities as regular web traffic.

### Impact: Data Manipulation (T1565)

Attackers can introduce data manipulation threats within Azure Logic Apps by altering data that flows through the app or automating processes that modify data to benefit the attacker. This includes subtler forms of manipulation such as altering transaction amounts or birth dates within records, which may go unnoticed but produce detrimental long-term effects on business operations or reputational damage if confidentiality or integrity breaches result.
