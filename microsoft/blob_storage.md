## T1087.002 - Cloud Account Discovery
An adversary may attempt to discover cloud account credentials associated with Azure Blob Storage. By gaining access to account credentials, attackers can enumerate storage accounts and containers. This can lead to unauthorized access or malicious use of stored data. Techniques for this might include password spraying, phishing, or searching for leaked credentials.

## T1078.003 - Valid Accounts: Cloud Accounts
Attackers may compromise legitimate accounts associated with Azure Blob Storage. Once in control, they can access or modify stored data, execute code, or launch further attacks from legitimate-looking sources. Compromised credentials may result from credential dumping, phishing campaigns, or weak password practices.

## T1558.001 - Steal or Forge Authentication Certificates: Cloud Services
Adversaries might attempt to steal or forge authentication certificates to access Azure Blob Storage environments. This can be achieved by exploiting vulnerabilities in certificate management or using tools to extract certificates from compromised servers or devices. Such access allows attackers to read, modify, or delete blob contents unnoticed.

## T1190 - Exploit Public-Facing Application
Azure Blob Storage can be vulnerable to exploits targeting internet-exposed resources. If containers or storage accounts are improperly configured to allow public access, attackers can exploit these settings to access sensitive data. Web application vulnerabilities, such as those found in web service endpoints interfacing with Blob Storage, can also be exploited.

## T1203 - Exploitation for Client Execution
When clients interact with Azure Blob Storage, attackers might exploit vulnerabilities within client applications to execute arbitrary code. This can occur when handling malformed data or metadata retrieved from blob contents, allowing an attacker to gain control over client resources utilized to access the storage.

## T1530 - Data from Cloud Storage Object
Adversaries may target Azure Blob Storage to extract sensitive data directly from storage objects. This includes files, databases, and other structured storage forms. Methods often involve direct download of data from blobs if permissions are improperly set, enabling unauthorized reads or exfiltration of sensitive information.

## T1114.002 - Email Collection: Remote Email Collection
Adversaries may utilize Azure Blob Storage as a storage location for collected emails facilitated by compromised administrative scripts or APIs. This allows them to exfiltrate sensitive email data for further exploitation, leveraging Blob Storage's scalable and persistent nature.

## T1567.002 - Exfiltration Over Web Service
Azure Blob Storage may serve as a destination for exfiltrated data using web services. Attackers may configure malware to upload sensitive information directly to blob storage containers over HTTP/HTTPS. This technique can hide data exfil under legitimate web service traffic, making it harder to detect.

## T1071.001 - Application Layer Protocol: Web Protocols
Attackers may employ web protocols to interact with Azure Blob Storage through API calls, mimicking legitimate applications. Using standard HTTP/S protocols, they can access, modify, or corrupt data, bypassing detection mechanisms that focus on typical malicious traffic or command-and-control channels. 

## T1071.004 - Application Layer Protocol: DNS
DNS tunneling techniques can be used by adversaries to exfiltrate data from Azure Blob Storage or communicate with malicious servers. By encoding data within DNS queries, attackers bypass normal network security measures, covertly transmitting sensitive information to external locations.
