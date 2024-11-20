## T1531 - Account Access Removal
Adversaries may remove legitimate administrative access to AWS Route 53, effectively tampering with DNS configurations. This could prevent authorized users from making critical DNS changes or remediating DNS hijacks. Once access is removed, attackers can maintain control over Route 53 resources and intercept or reroute traffic intended for legitimate applications.

## T1501 - Hijack Execution Flow
Attackers may manipulate DNS queries handled through AWS Route 53 by setting malicious or incorrect DNS records. By altering the execution flow, they can redirect traffic to malicious sites or disrupt service availability for users depending on the impacted DNS records.

## T1071.004 - Application Layer Protocol: DNS
Adversaries could abuse Route 53 DNS resolution for data exfiltration or command-and-control communication. By exploiting DNS as a transport mechanism, attackers can obfuscate their activities and potentially hide in the noise of legitimate DNS traffic, making detection more challenging.

## T1592 - Gather Victim Network Information: DNS
Reconnaissance on AWS Route 53 configurations may be performed to gather information on DNS records. This knowledge can help attackers map out the victim's network architecture, identify critical services, and pinpoint potential targets for further attacks. Knowledge of DNS records and zones may also inform attackers about subdomains and external dependencies.

## T1565.001 - Data Manipulation: Stored Data
Attackers may manipulate data stored within Route 53 by altering DNS zone files or record sets. This could lead to traffic being rerouted to attacker-controlled resources, causing service disruption, data interception, and unauthorized access to sensitive information—turning trusted applications or services into adversarial conduits.

## T1078 - Valid Accounts
Compromised AWS credentials can allow attackers unauthorized access to Route 53 services. With valid account access, attackers can alter DNS configurations, delete records, or introduce malicious entries, enabling phishing attacks, data exfiltration, or denial-of-service.

## T1557.002 - Adversary-in-the-Middle: DNS Spoofing
Attackers can conduct DNS spoofing by altering AWS Route 53 configurations to return false IP addresses for legitimate domain requests. This misdirection can facilitate man-in-the-middle attacks, allowing adversaries to intercept and modify data in transit, lead users to phishing sites, or disrupt services.

## T1518.001 - Software Discovery: Web Services
Adversaries may leverage knowledge of AWS Route 53 setups to learn more about the victim's cloud service implementations. Discovering the use of Route 53 can provide insights into the DNS services used, helping inform additional exploit strategies against the network, such as targeting specific services or exploiting known vulnerabilities in AWS services.

## T1574.010 - Hijack Execution Flow: DNS Hijacking
DNS hijacking can be used to redirect traffic that should reach its destination via AWS Route 53. By hijacking DNS queries, adversaries can point users to malicious sites, facilitating phishing attacks or malware distribution and undermining trust in the service's integrity.

## T1036 - Masquerading
Attackers may utilize subdomain masquerading by creating lookalike domain names via AWS Route 53. These can be used for phishing attacks or fraudulent activities, with the goal of deceiving users or automated processes into thinking they're interacting with legitimate services.

## T1040 - Network Sniffing
In the context of intercepting DNS traffic intended for AWS Route 53, network sniffing could be abused to capture sensitive data, such as DNS query patterns or other metadata that may reveal organizational behaviors or trends. Attackers can leverage this information for subsequent attacks or targeted intrusions.
