### Initial Access

**Valid Accounts (T1078):** Adversaries may leverage valid account credentials to gain initial access to Microsoft Entra ID, bypassing conventional access controls. This technique often involves the use of stolen or leaked credentials, allowing attackers to authenticate as legitimate users. Once authenticated, threat actors can move laterally within the Azure environment or escalate privileges to gain further access.

### Credential Access

**Brute Force (T1110):** Attackers may employ brute force techniques to compromise user accounts in Microsoft Entra ID. This typically involves the automated guessing of passwords against Azure Active Directory (AAD) accounts. Susceptible accounts often have weak or commonly used passwords. A successful brute-force attack can lead to unauthorized access and potential lateral movement within the tenant.

**Password Spraying (T1110.003):** Similar to brute force, password spraying is a technique where attackers attempt to gain access to a large number of accounts using commonly used passwords. Unlike brute force, which targets one account with many passwords, spraying targets many accounts with a select few passwords. This technique helps avoid account lockout and remains under detection thresholds.

### Privilege Escalation

**Abuse Elevation Control Mechanism (T1548):** Adversaries might exploit legitimate elevation control mechanisms within Microsoft Entra ID to gain higher privileges. This could involve manipulating role-based access control (RBAC) settings or compromising accounts with elevated privileges to perform administrative functions, enabling further malicious activities.

### Defense Evasion

**Forge Web Credentials (T1606.002):** Attackers may forge web credentials, such as SAML tokens, to bypass security controls and impersonate legitimate users. By exploiting vulnerabilities in the authentication process, adversaries can gain unauthorized access and perform actions as an authenticated user without detection.

### Lateral Movement

**Cloud Infrastructure Discovery (T1580):** As part of lateral movement efforts, attackers may query Microsoft Entra ID to gain insights into organizational infrastructure, including virtual machines, network settings, and identity configurations. Such reconnaissance helps adversaries identify weaknesses and plan subsequent stages of an attack.

### Persistence

**Add Cloud Instance Metadata Service Account (T1689):** Attackers can establish persistence by creating or modifying service accounts within an Azure AD environment. By doing so, they ensure ongoing access even if user credentials are changed. These accounts often have elevated permissions to perform specific tasks within the cloud, making them ideal for maintaining unauthorized access.

### Collection

**Data from Cloud Storage Object (T1530):** Malicious actors may target cloud storage resources linked with Microsoft Entra ID, such as Azure Blob Storage. They can exfiltrate sensitive information, such as user data or enterprise files, directly from cloud storage services, bypassing traditional endpoint security measures.

### Impact

**Account Access Removal (T1531):** A threat actor with sufficient privileges can remove access for legitimate users within Microsoft Entra ID, effectively conducting a denial of service. By locking out key personnel or disabling critical accounts, attackers can disrupt organizational operations and potentially extort the victim into regaining access.
