### T1190 - Exploit Public-Facing Application
Azure Web Application Firewall can be targeted by adversaries aiming to exploit vulnerabilities in internet-facing applications. These attacks might leverage vulnerabilities in the application itself, in the web server, or in the web framework. An attacker could exploit these vulnerabilities to bypass WAF controls or gain unauthorized access to systems behind the WAF. Common methods include SQL injection, Cross-Site Scripting (XSS), and various forms of remote code execution.

### T1566.002 - Phishing: Spearphishing Link
Although Azure WAF itself is not directly susceptible to phishing attacks, attackers may use spearphishing to entice internal users into visiting compromised websites or clicking malicious links that allow attackers to bypass security controls indirectly. If users within the network configuration of Azure WAF are compromised, they could potentially manipulate or reconfigure firewall settings.

### T1195.002 - Supply Chain Compromise: Compromise Software Dependencies and Development Tools
Adversaries may exploit weaknesses in the supply chain to introduce malicious code or vulnerabilities into web applications protected by Azure WAF. This could occur through compromised third-party libraries, dependencies, or development tools used during application development, potentially undermining the integrity of the application and evading WAF's protections.

### T1078 - Valid Accounts
An attacker with valid credentials can bypass Azure WAF protections entirely. By obtaining legitimate access credentials through techniques such as credential dumping or brute force attacks, adversaries can carry out unauthorized activities under the guise of an authorized user, thereby sidestepping the security measures enforced by WAF.

### T1046 - Network Service Scanning
Adversaries may perform network service scanning to identify open ports, services, and other information about the network that could reveal weaknesses in Azure WAF's configuration. By gaining insights into network topology and services, attackers can better plan their exploitation strategies to evade detection or compromise protected applications.

### T1203 - Exploitation for Client Execution
If an attacker identifies a vulnerability in client-side components that interact with Azure WAF, such as a browser-based interface for WAF management, they might exploit these vulnerabilities to execute unauthorized client-side code. This could lead to the manipulation of WAF settings or extraction of sensitive configuration data.
