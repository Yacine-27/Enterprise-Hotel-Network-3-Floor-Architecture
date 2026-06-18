# Switchport Port Security:

This module details the edge-layer security controls implemented to protect physical access to the enterprise network. By deploying Layer 2 MAC address filtering on the access switches, we mitigate rogue device integration, MAC flooding attacks, and unauthorized hardware attachment at the desk level.

The implementation commands executed across the edge interface blocks are captured below:

```CiscoIOS
interface fastEthernet 0/1
Switch(config-if-range)# switchport port-security
Switch(config-if-range)# switchport port-security maximum 1
Switch(config-if-range)# switchport port-security mac-address sticky
Switch(config-if-range)# switchport port-security violation shutdown
```

<img width="755" height="401" alt="port security" src="https://github.com/user-attachments/assets/28e606f9-8b8e-4966-bd83-fbda63aefb54" />


