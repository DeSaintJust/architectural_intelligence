### Initial Access
Azure Lighthouse allows service providers to manage customer environments, and it's susceptible to initial access threats involving compromised accounts. Attackers may leverage targeted phishing campaigns (T1566) to obtain credentials of administrators with delegated access. This initial breach can allow them to infiltrate one or more managed tenants.

### Execution
Once access is gained, adversaries can execute unwanted scripts or automate tasks within Azure environments. Through the use of Command and Scripting Interpreter (T1059), attackers might employ PowerShell scripts or Azure CLI to execute commands that open further attack vectors or maintain persistence.

### Persistence
Adversaries may establish persistence by abusing Azure Active Directory service principals (T1098), which allows them to maintain uninterrupted access. These principals can be configured to have broad permissions and can be difficult for humans to monitor due to their automated nature.

### Privilege Escalation
Privilege escalation could be executed through exploitation of valid accounts (T1078). An attacker with initial low-privilege access could potentially escalate privileges by using accounts with higher levels of access within Azure Lighthouse, potentially leveraging available permissions to make unauthorized changes.

### Defense Evasion
Azure environments are typically monitored, so attackers might leverage technique T1562, Impair Defenses, to evade detection. By altering logging settings or administrative alerts, they can reduce the likelihood of being discovered in managed environments.

### Credential Access
Adversaries could aim to extract valid credentials through spear phishing, or by accessing credential stores and secrets within Azure Key Vault (T1555). Compromising these credentials can further their infiltration into Azure Lighthouse-managed environments.

### Discovery
An integral step for attackers is horizontal and vertical discovery (T1087) within the tenant environments managed by Azure Lighthouse. They may employ native Azure capabilities or custom scripting to map out resources, sensitive data, and access permissions across multiple customer environments.

### Lateral Movement
Having discovered accounts and systems, attackers could use the technique T1550, Use Alternate Authentication Material. They might duplicate access tokens or hijack sessions to move laterally across Azure services, gaining access to additional managed customer tenancies without triggering fresh authentication processes.

### Collection
Data from customer environments is a lucrative target, and attackers might employ data from information repositories (T1213). Using Azure's APIs, they could extract sensitive organizational data hosted across different customer tenants as managed by Azure Lighthouse.

### Exfiltration
Exfiltration over cloud storage (T1567) is a prevalent technique wherein the adversary moves data from compromised environments into external locations like third-party cloud storage services. Azure APIs can facilitate the exfiltration of considerable data volumes.

### Impact
Finally, for operations aiming to disrupt services, adversaries might target aspects of resource deletion (T1485) across managed tenants, altering configurations or deleting essential components in Azure environments. This could result in significant service outages or loss of critical customer data managed through Azure Lighthouse.
