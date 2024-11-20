## T1190: Exploit Public-Facing Application
AWS Direct Connect can be exploited if associated network management applications are exposed to the public without adequate security controls. Attackers may search for vulnerabilities in configurations or software bugs in applications managing Direct Connect services. Exploiting these weaknesses can provide unauthorized access to send or intercept traffic over Direct Connect, potentially leading to data breaches or disruptions in service.

## T1078: Valid Accounts
Compromise of valid account credentials allowing access to AWS Management Console or API can lead to unauthorized changes to the Direct Connect configuration. If attackers obtain such credentials through phishing campaigns or credential stuffing attacks, they can potentially modify or disconnect virtual private interfaces (VIFs), enabling data exfiltration or denial of service (DoS) attacks.

## T1046: Network Service Scanning
Adversaries may conduct network service scanning techniques to identify Direct Connect configurations and associated resources. By using scanning tools to map out network attributes, attackers can ascertain the existence of Direct Connect connections, which can aid in subsequent efforts to disrupt or intercept network traffic, thereby posing a significant threat to data integrity and service availability.

## T1071: Application Layer Protocol
Adversaries might exploit application layer protocols to communicate with compromised or misconfigured network devices within an AWS Direct Connect setup. By utilizing usual communication protocols or encrypted traffic, attackers can hide the exfiltration of data or command and control (C2) activities, thus going undetected by security monitoring tools focused on typical network protocol anomalies.

## T1568.002: Dynamic Data Exchange
While not specific to AWS Direct Connect, adversaries might use dynamic data exchange mechanisms to influence processes handling Direct Connect network traffic. Manipulating interfaces or administrative services that utilize dynamic data exchange protocols can enable attackers to reroute data streams, disrupt network services, or covertly monitor communications over Direct Connect connections.

## T1529: System Shutdown/Reboot
Attackers with access to management consoles or APIs may attempt to shut down or reboot network infrastructure relevant to AWS Direct Connect. By causing targeted systems to restart or go offline, adversaries can disrupt connectivity and availability, leading to a denial of service condition that affects business operations relying on seamless Direct Connect services.
