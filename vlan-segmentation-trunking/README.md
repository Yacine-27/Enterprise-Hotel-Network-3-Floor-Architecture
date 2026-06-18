# VLAN Segmentation & Trunking Configuration

This module details the Layer 2 configuration of the enterprise network, focused on isolating broadcast domains by department across all three physical floors using IEEE 802.1Q tagging.

## Cisco IOS Configuration Snippets

Creating VLANs 

```cisco IOS
conf t
vlan 10
name IT
vlan 20
name Admin
exit
```
Assigning access ports to VLANS:

```cisco IOS
interface fa0/1
switchport mode access
switchport access vlan 10
exit
```
Configuring 802.1Q uplink trunks:

```cisco IOS
interface gig0/1
switchport trunk encapsulation dot1q
switchport mode trunk
switchport trunk allowed vlan 60,70,80
```
## Verification

Using the "show vlan brief" and "show interfaces trunk" commands (Example shown for **Floor 1 Router**):

### Floor 1:
Showing access ports:

<img width="882" height="476" alt="SW1 vlan" src="https://github.com/user-attachments/assets/396f3e5d-6065-4d94-bc86-275e6e46e1f2" />

Showing trunk ports:

<img width="956" height="368" alt="SW1 trunk links" src="https://github.com/user-attachments/assets/304b2383-799f-4534-beff-a412258570c5" />

