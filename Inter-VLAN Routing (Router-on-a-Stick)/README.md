# Inter-VLAN Routing (Router-on-a-Stick) Configuration

This module details the Layer 3 infrastructure configurations that enable secure, routed communication between isolated broadcast domains (VLANs) across all floors of the enterprise network using Cisco Router-on-a-Stick (ROAS).

## Cisco IOS Configuration Snippets:

```ios
interface GigabitEthernet0/0
no shutdown
interface GigabitEthernet0/0.30
encapsulation dot1Q 30
ip address 192.168.3.1 255.255.255.0
interface GigabitEthernet0/0.40
encapsulation dot1Q 40
ip address 192.168.4.1 255.255.255.0
Configure Sub-interface for Finance (VLAN 50)
interface GigabitEthernet0/0.50
encapsulation dot1Q 50
ip address 192.168.5.1 255.255.255.0
```
## Verification

Using the "show ip int br" and "ping" commands (Example shown for **Floor 2 Router**):

<img width="1883" height="690" alt="router-2 interfaces" src="https://github.com/user-attachments/assets/0f6b6fb6-22bb-4e42-a5d4-41000ba6514e" />

<img width="1918" height="1080" alt="pinging Vlan 30 to 40 and 50" src="https://github.com/user-attachments/assets/c4a73c8f-bfcf-4918-8981-57be910bdb4b" />

