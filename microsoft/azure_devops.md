## Initial Access

### Phishing (T1566)
Phishing can be leveraged to gain initial access to Azure DevOps by enticing users to provide their credentials on a spoofed login page. Attackers may craft convincing emails targeting developers or operations teams within an organization to capture sensitive usernames and passwords, which are then used to log in to Azure DevOps services.

## Credential Access

### Credentials in Files (T1552.001)
Attackers may search for credentials stored within configuration files, scripts, or source code repositories in Azure DevOps. Often, developers inappropriately store API keys, passwords, or tokens in these files, providing a vector for attackers to gain unauthorized access to the system.

### Brute Force (T1110)
Adversaries may attempt to gain access to Azure DevOps accounts by systematically guessing passwords. This brute force attack can encompass techniques such as password spraying or exploiting weak passwords, potentially leading to unauthorized access if multi-factor authentication is not enforced.

## Persistence

### Account Manipulation (T1098)
Once access is gained, attackers may create new accounts or manipulate existing ones within Azure DevOps to ensure persistent access. They might elevate their privileges or add malicious accounts to privileged groups to maintain control over the development environment.

## Discovery

### Cloud Service Enumeration (T1526)
Adversaries may leverage various tools and techniques to discover the structure and assets within an Azure DevOps environment. This can include listing repositories, understanding project dependencies, or identifying CI/CD pipelines, all of which may reveal valuable information for further exploitation.

## Lateral Movement

### Remote Services (T1021)
Attackers may move laterally within Azure DevOps by exploiting credentials to access remote services such as SSH or the Azure Resource Manager API. This movement allows them to compromise additional cloud resources, expand control, and execute further attacks within the DevOps pipeline.

## Execution

### Command and Scripting Interpreter (T1059)
Once inside the Azure DevOps environment, adversaries may use command-line interfaces or scripting languages to execute malicious payloads or automate tasks. Exploiting build agents or CI/CD pipeline capabilities can facilitate the deployment of backdoors or the tampering of application code.

## Collection

### Data from Information Repositories (T1213)
Azure DevOps often hosts significant sensitive data, including proprietary code, intellectual property, and internal documentation. Attackers targeting these repositories may download data to exfiltrate valuable information, potentially impacting the organization’s competitive edge or security posture.

## Exfiltration

### Exfiltration Over Application Layer (T1041)
Attackers may use APIs to exfiltrate data from Azure DevOps over legitimate communication channels. By abusing existing application protocols and services, adversaries can transfer sensitive information out of the environment without raising significant suspicion.

## Impact

### Resource Hijacking (T1496)
Adversaries may hijack Azure DevOps resources to perform cryptocurrency mining or other resource-intensive activities. Leveraging unauthorized access to build agents or shared environments not only affects performance but also leads to increased infrastructure costs for the organization.

### Data Destruction (T1485)
An attacker with appropriate access might destroy data within Azure DevOps, such as wiping source code repositories or deleting CI/CD configurations. This may significantly disrupt development workflows, leading to project delays and financial losses.
