**T1190 - Exploit Public-Facing Application:** One common threat to AWS CloudFront involves exploiting vulnerabilities in the CDN service itself or misconfigured web applications behind CloudFront. Attackers can leverage common web application vulnerabilities such as SQL injection, cross-site scripting (XSS), or cross-site request forgery (CSRF) by sending malicious payloads to the edge locations of CloudFront, potentially gaining unauthorized access to backend services or data.

**T1566.001 - Phishing: Spearphishing Attachment:** Attackers may use phishing techniques to deliver malformed URLs or malicious attachments that exploit CloudFront domain configurations. By tricking users or administrators into clicking on these URLs or opening attachments, adversaries attempt to achieve unauthorized access to credentials that could allow further manipulation or malicious configuration of CloudFront distributions.

**T1078 - Valid Accounts:** Utilizing compromised credentials for valid AWS accounts poses a significant risk to AWS CloudFront. Attackers with access to CloudFront management APIs can modify distribution settings, inject malicious code, alter caching rules, or conduct other malicious actions unchecked, potentially impacting a wide range of users globally.

**T1595.003 - Active Scanning: Cloud Service:** Adversaries often perform reconnaissance by actively scanning CloudFront distributions for configurations and vulnerabilities. By detecting default error messages, analyzing custom domains, or identifying misconfigured permissions, attackers gather intelligence to craft more targeted attacks or identify weak points in the CDN architecture and associated backend services.

**T1071 - Application Layer Protocol:** Malicious actors can abuse common application layer protocols used by CloudFront, such as HTTP/HTTPS, to exfiltrate data, communicate with command and control servers, or execute binary payloads. They may disguise their traffic to blend in with legitimate CDN traffic, making detection more challenging.

**T1568.002 - Dynamic Resolution: Fast Flux DNS:** Attackers might use fast flux DNS, a technique where the IP address associated with CloudFront distributions changes rapidly, to obfuscate their malicious network infrastructure. This approach makes it difficult for defenders to track or block malicious activity effectively as it dynamically evades domain blacklisting services.

**T1600 - Weaken Encryption:** Introducing weaker encryption methods or misconfigurations into CloudFront's settings can make secure connections vulnerable to man-in-the-middle attacks. Attackers may attempt to force service downgrades for SSL/TLS or exploit improper handling of public keys and certificates to intercept or tamper with data passing through the CDN.

**T1219 - Remote Access Software:** Unauthorized remote management software might be deployed on servers behind CloudFront distributions. Malicious actors could exploit such software to gain persistent access, execute commands, or exfiltrate data, posing a threat to the overall security and integrity of services delivered through CloudFront.

**T1048 - Exfiltration Over Alternative Protocol:** In some scenarios, attackers might leverage alternative communication protocols supported by CloudFront to exfiltrate data or bypass network monitoring solutions. By encapsulating malicious data streams within common protocols as they pass through CloudFront, an adversary can obscure their actions from traditional detection mechanisms.