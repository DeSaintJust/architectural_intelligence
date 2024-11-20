## T1190 - Exploit Public-Facing Application
AWS Web Application Firewall (WAF) is susceptible to threats that involve exploiting vulnerabilities in public-facing applications it is designed to protect. Attackers might identify and exploit vulnerabilities such as injection flaws (e.g., SQL injection or cross-site scripting) in the web applications behind the WAF. If the WAF is not correctly configured to block such exploits or if the exploit leverages a zero-day vulnerability unknown to the WAF rules, the security of the web applications could be compromised.

## T1531 - Account Access Removal
An adversary may perform account access removal by targeting the credentials or session tokens used by AWS WAF. If access to the WAF configuration management console is gained through compromised AWS accounts, attackers can remove legitimate administrators' access, thereby controlling WAF settings to allow malicious traffic or to hide their tracks. This technique can significantly disrupt the security posture and manageability of the AWS WAF.

## T1557.002 - Man-in-the-Middle: ARP Cache Poisoning
While AWS WAF itself may not be directly affected by ARP cache poisoning because it is a managed service, associated network infrastructure and endpoints are still vulnerable. Attackers can conduct ARP cache poisoning against systems communicating with AWS to intercept or modify data packets. This can potentially lead to the bypass of the WAF if attackers manipulate the traffic before it reaches the AWS infrastructure.

## T1036.004 - Masquerading: Masquerade Task or Service
Threat actors may attempt to masquerade legitimate traffic types and sources to bypass AWS WAF. This is achieved by manipulating headers, payloads, or using known IP addresses and patterns that are whitelisted within WAF rulesets. Such masquerading can trick a poorly configured WAF into allowing malicious traffic through, intending to reach and compromise the back-end applications.

## T1134 - Access Token Manipulation
Access token manipulation can target AWS WAF indirectly by compromising access tokens used in the applications it protects. Attackers may manipulate session tokens, JWTs, or API keys used by legitimate users to escalate privileges, inject malicious traffic, or alter WAF configurations if they have acquired the necessary permissions.

## T1595.002 - Active Scanning: Vulnerability Scanning
Adversaries conduct active scans against web applications behind AWS WAF to identify potential vulnerabilities. These scanners can probe for exposed services, unpatched software, and misconfigurations within both the WAF settings and the applications. Although WAFs are designed to detect and mitigate some of these scans, sophisticated or stealthy scanning techniques may avoid detection, aiding attackers in gathering necessary intelligence for future exploitation.

## T1640 - File and Directory Discovery
Though AWS WAF focuses primarily on web traffic filtering, successful attacks like directory traversal might bypass its protections if misconfigured or if leveraging unknown vulnerabilities. Attackers will aim to discover sensitive files and directories within the application beyond the WAF. These discoveries can then lead to further attacks like direct data exfiltration or secondary malware deployment.

## T1195.003 - Supply Chain Compromise: Compromise Software Dependencies and Development Tools
A compromise in the software supply chain that affects any component integrated with AWS WAF, such as configuration management plugins or WAF rule updates, can result in attackers gaining indirect access or influence over the WAF's operation. This could result in the insertion of malicious rules or the disabling of essential protection mechanisms.
