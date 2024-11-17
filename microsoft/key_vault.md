### Initial Access - Valid Accounts (T1078)
Attackers may gain access to Azure Key Vault by compromising valid cloud accounts. This can occur through credential theft, such as phishing attacks, brute force attacks, or through the exploitation of weak passwords. Once access to an Azure Key Vault account is achieved, attackers can potentially list, retrieve, and decrypt sensitive data stored within the Key Vault.

### Persistence - Application Access Token (T1527)
Compromised applications with valid access tokens can be manipulated by attackers to maintain persistence in accessing Azure Key Vault. If the application’s credentials or tokens are captured, an adversary can use them to continually access the Key Vault unless the tokens are revoked. This technique allows attackers to persistently interact with the Key Vault without needing to re-authenticate directly.

### Credential Access - Unsecured Credentials (T1552)
Azure Key Vault may store credentials or secrets that, if improperly configured or unsecured, can be accessed by malicious actors. This can occur if environment variables, script files, or default read permissions are not adequately secured, leading to unauthorized access to sensitive data in Key Vault.

### Lateral Movement - Cloud Storage Object (T1530)
Attackers who have gained control of a compromised account can leverage misconfigured permissions to move laterally by accessing linked cloud storage objects. This access might allow an adversary to execute operations that utilize stored secrets or keys in different cloud services linked to Azure Key Vault, broadening their attack surface within the cloud environment.

### Discovery - Cloud Service Dashboard (T1538)
An attacker with access to a compromised Azure account can use the cloud service dashboard to gain insights into the configuration and logs of Azure Key Vault. This discovery technique enables adversaries to gather information on IAM roles, permissions, and access history, which can be leveraged for further attack planning and execution.

### Collection - Data from Cloud Storage (T1539)
Azure Key Vault’s data can be exfiltrated if an adversary gains access to stored secrets, certificates, or keys. Attackers may use scripted or manual processes to extract this data from Key Vault and utilize it for decrypting confidential information, conducting identity attacks, or accessing other cloud services.

### Exfiltration - Transfer Data to Cloud Account (T1567)
Exfiltration of data via Azure Key Vault may involve transferring the sensitive information to an external cloud account controlled by the attacker. This can include moving secrets, keys, or certificates to cloud storage services that provide the attacker with unmonitored and discreet access to the sensitive information extracted from Azure Key Vault.

### Defense Evasion - Access Token Manipulation (T1602)
An attacker can manipulate access tokens to bypass certain security measures set in Azure Key Vault. Access token manipulation includes altering token data to extend the token’s validity or to escalate privileges. Such evasion tactics enable attackers to surmount security controls and maintain lengthy access to the Key Vault resources.
