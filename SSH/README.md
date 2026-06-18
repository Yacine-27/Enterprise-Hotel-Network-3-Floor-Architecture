# Secure Shell (SSH) Remote Management:

This module details the security hardening implementations deployed to protect the control plane of the enterprise network infrastructure. To eliminate clear-text vulnerabilities associated with legacy protocols like Telnet, Secure Shell (SSHv2) is enforced globally across all network devices, ensuring all remote administrative sessions are encrypted and authenticated.

The implementation commands executed on the network devices are captured below:

<img width="940" height="382" alt="ssh configuration" src="https://github.com/user-attachments/assets/34f3969e-23ae-4a2a-a68b-92650844ae83" />

``ciscoIOS

hostname Floor3-Core
ip domain-name project.ccna
crypto key generate rsa
ip ssh version 2
username yacine secret strongSecret
line vty 0 4
login local
transport input ssh
