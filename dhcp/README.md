# Dynamic Host Configuration Protocol (DHCP) Services

This module details the automated IP addressing architecture implemented across the enterprise network. To eliminate manual static configuration and prevent IP conflicts, a central Cisco IOS Router serves as the dedicated DHCP Server, dynamically provisioning IP leases, subnet masks, default gateways, and DNS records to client endpoints.

## 🛠️ Cisco IOS DHCP Server Configuration

The DHCP server is built directly onto the routing tier. The implementation follows industry best practices by reserving structural space for statically assigned network infrastructure (such as switches, routers, and network printers) before defining the client assignment boundaries.



The command execution structure from the core router configuration is shown below (Example shown for **Floor 1 Router**):

```CiscoIOS
ip dhcp pool VLAN70
network 192.168.7.0 255.255.255.0
default-router 192.168.8.10
```
<img width="800" height="440" alt="Configuting DHCP on router" src="https://github.com/user-attachments/assets/6301e6dd-c6ef-4122-8e63-2465e1d09d1d" />


