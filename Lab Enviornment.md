##### **Lab Environment**



Virtualized infrastructure built using VirtualBox (Hypervisor):

* Kali Linux (Attacker VM)
* Ubuntu Server (Monitoring VM)
* Metasploitable 2 (Target VM)





##### Network Architecture



Each VM was configured with:

* NAT Adapter (Internet access)
* Host-Only Adapter (Isolated lab network)
* Host-Only Network Range: 192.168.56.0/24



This ensured safe, isolated testing environment, no external traffic exposure, and controlled internal network simulation.





##### **Network Configuration \& Troubleshooting**



Configured Linux network interfaces using:

* ip addr
* Netplan (Ubuntu)
* /etc/network/interfaces (Metasploitable)
* DHCP lease validation
* Adapter verification in VirtualBox
* Key Networking Concepts Applied
* Static vs DHCP configuration
* Interface identification (enp0s3 vs enp0s8)
* NAT vs Host-Only networking
* IP range validation
* ICMP connectivity testing
* Packet loss troubleshooting
* Adapter misconfiguration debugging



Validated connectivity using: ping

Resolved 100% packet loss issue by identifying disabled Host-Only adapter and re-enabling VM network configuration.



##### **Reconnaissance \& Service Enumeration**



Performed full port and service scan using: nmap -sV -O -p- 192.168.56.102



* Skills Demonstrated
* Full TCP port scan
* Service version detection
* OS fingerprinting
* Attack surface identification
* Interpretation of scan results
* Identification of vulnerable services



This phase provided visibility into exposed services and mapped the internal attack surface.



##### **Exploitation Simulation (Controlled Lab)**



Used: Metasploit Framework



Configured:

* RHOSTS (Target IP)
* LHOST (Attacker Host-Only IP)
* Successfully simulated a reverse shell connection within the isolated network.
* Networking Skills Demonstrated
* Reverse shell communication flow
* TCP session establishment analysis
* Listener configuration
* Host-to-host communication validation
* Controlled exploit testing in lab environment



This validated proper network routing and host communication configuration.



##### **Packet Capture \& Traffic Analysis**



Captured live traffic using:

* Wireshark
* Zeek



Observed:

* ARP broadcasts
* ICMP traffic
* TCP handshake process
* Reverse shell traffic patterns
* Port scanning behavior
* Service enumeration signatures



Skills Demonstrated:

* TCP/IP packet inspection
* Three-way handshake analysis
* Protocol filtering
* Traffic pattern recognition
* Identifying abnormal outbound connections
* Understanding attacker behavior from packet data
* Intrusion Detection \& Monitoring



###### **Implemented detection** 

Using: Suricata



Created and tested alert rules to detect:

* Suspicious FTP behavior
* Reverse shell traffic
* Port scanning activity
* Verified detection via Suricata logs and alert output.



Defensive Skills Demonstrated:

* IDS rule configuration
* Signature-based detection
* Log validation
* Security event analysis
* Attack signature recognition
* Mitigation \& Service Hardening
* Simulated defensive response by:
* Disabling vulnerable service on target VM
* Verifying port closure
* Confirming exploit failure post-mitigation
* Validating network behavior after remediation



This demonstrated:

* Service management
* Risk reduction techniques
* Validation of mitigation effectiveness
* Secure configuration practices
* Automation \& Enterprise Scalability Concepts
* Designed conceptual extension of lab into enterprise security pipeline using:
* Automated scanning scheduling
* Centralized log aggregation
* SIEM integration
* Continuous network monitoring
* Service exposure tracking
* Configuration drift detection



Tools referenced for scalability:

* Nmap scripting
* Zeek logging
* Suricata monitoring
* Vulnerability scanners
* SOAR-style automated response workflows





Technical Skills Demonstrated

* Networking
* TCP/IP fundamentals
* Subnetting and IP addressing
* NAT vs Host-Only networking
* Interface configuration
* Packet-level analysis
* Network troubleshooting
* Service exposure analysis
* Security \& Monitoring



##### **Vulnerability assessment**



* Port scanning
* OS fingerprinting
* Intrusion detection systems
* Log analysis
* Reverse shell traffic identification
* Attack surface mapping
* Systems
* Linux CLI administration
* Network service management
* VM deployment \& configuration
* Multi-host lab design



Key Takeaways



This project demonstrates the ability to:

* Design and configure virtualized network environments
* Troubleshoot network-level connectivity issues
* Analyze packet-level network traffic
* Identify exposed services and vulnerabilities
* Implement detection mechanisms
* Validate mitigation effectiveness
* Understand attacker behavior from a network perspective
* The lab reflects real-world SOC and network operations workflows in a controlled and ethical environment.
