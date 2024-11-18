#### Initial Access - Phishing (T1566)
Adversaries may employ phishing techniques to gain initial access to credentials associated with Azure Policy resources. These attacks often involve crafting convincing emails that trick users into divulging confidential information, such as Azure account credentials. With these credentials, attackers can potentially alter or disable existing Azure Policies or create new policies with malicious intent, such as reducing security controls.

#### Execution - Scripting (T1059)
Scripts can be utilized to automate interactions with Azure Policy. Adversaries could execute scripts to systematically modify, create, or delete Azure Policies. This technique facilitates large-scale policy alterations that can degrade security posture across the cloud environment, allowing other malicious actions to be executed undetected.

#### Persistence - Account Manipulation (T1098)
Attackers might attempt to achieve persistence by creating or modifying Azure accounts with elevated privileges. By elevating or adding permissions to these accounts, they can ensure ongoing control over Azure Policies, permitting repeated access to modify or disable them even if initial access methods are discovered and removed.

#### Privilege Escalation - Privileged Account Management (T1078)
Through the acquisition or misuse of privileged Azure accounts, attackers can gain elevated permissions necessary to modify Azure Policy settings. Privileged account theft or misuse allows adversaries to change policy definitions and assignments, which can weaken security controls across Azure resources.

#### Defense Evasion - Valid Accounts (T1078)
Using valid account credentials, adversaries can evade detection while interacting with Azure Policies. By using existing user accounts, attackers blend their actions with legitimate activities, making it challenging to detect policy changes made with malicious intent.

#### Credential Access - Credential Dumping (T1003)
Adversaries may gather account credentials that are stored in Azure environments to gain access to Azure Policy resources. Credential dumping allows actors to capture necessary credentials from Azure Key Vaults or storage accounts, potentially leading to hostile policy alterations if administrative credentials are accessed.

#### Discovery - Cloud Service Discovery (T1526)
Attackers may perform discovery actions within Azure to identify and understand the current landscape of Azure Policies in place. By listing and analyzing policy assignments, policy definitions, and compliance states, adversaries can determine which policies to target or disable for further malicious activity.

#### Lateral Movement - Cloud Services (T1534)
Exploiting credentials or permissions of Azure accounts can allow lateral movement between different Azure services, potentially extending control to Azure Policies. Once moved laterally to a higher privilege account or service, an adversary can manipulate policies to weaken the security of the entire cloud environment.

#### Impact - Resource Hijacking (T1496)
Attackers may seek to modify Azure Policies to facilitate resource hijacking, redirecting or consuming Azure resources for unauthorized purposes, such as mining cryptocurrency. By manipulating policies to reduce auditing and monitoring, adversaries can exploit resources without immediate detection, resulting in increased costs and resource consumption for the organization.
