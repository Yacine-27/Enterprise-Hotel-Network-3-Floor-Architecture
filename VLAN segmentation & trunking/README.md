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

Using the show vlan brief and show interfaces trunk commands:

### Floor 1:
Showing access ports:

<img width="1764" height="934" alt="SW1 vlan" src="https://github.com/user-attachments/assets/396f3e5d-6065-4d94-bc86-275e6e46e1f2" />

Showing trunk ports:

<img width="1912" height="737" alt="SW1 trunk links" src="https://github.com/user-attachments/assets/304b2383-799f-4534-beff-a412258570c5" />

### Floor 2:

Showing access ports:

<img width="1788" height="948" alt="SW2 vlan" src="https://github.com/user-attachments/assets/50d4cc03-360a-4c12-b316-698192ec874a" />

Showing trunk ports:

<img width="1543" height="767" alt="SW2 trunk links" src="https://github.com/user-attachments/assets/cff59cbd-2eb5-4d18-bda2-3c46037364a2" />

### Floor 3:

Showing access ports:

<img width="1779" height="929" alt="SW3 vlan" src="https://github.com/user-attachments/assets/68993dc7-3ea6-4b52-b582-2e6785eca52a" />

Showing trunk ports:

<img width="1680" height="722" alt="SW3 trunk links" src="https://github.com/user-attachments/assets/d5568238-904e-4a56-9dd6-d93e46f78098" />

