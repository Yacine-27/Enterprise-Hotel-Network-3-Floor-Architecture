# Core Routing Matrix & Topology Verification

## 🛠️ Cisco IOS Routing Protocols

The system utilizes dynamic routing to automatically distribute internal subnets across the infrastructure. Below are the structural configuration commands used to establish core connectivity:

```CiscoIOS
router ospf 1
network 10.10.10.4 0.0.0.3 area 0
network 10.10.10.8 0.0.0.3 area 0
network 192.168.6.0 0.0.0.255 area 0
network 192.168.7.0 0.0.0.255 area 0
network 192.168.8.0 0.0.0.255 area 0
```
## Routers & Endpoint Connectivity Verification:

### 1. Point-to-Point Core Link Pings (Example: Router 1)
This screenshot confirms that Layer 3 serial links between adjacent routers are up and operational. Direct ICMP traffic reaches neighbor interfaces seamlessly with a 100% success rate.

<img width="950" height="460" alt="Pinging between routers - 1" src="https://github.com/user-attachments/assets/f72f6f44-89f9-4835-bf6f-a1f0a2fcc933" />

### 2. End-to-End Cross-Floor Communication (Example: Floor 1 Node)
To verify that traffic successfully traverses the routing core from an end-user perspective, we test connectivity from a workstation on Floor 1 (`Reception-PC`) to the default gateways of remote floors.
The initial drop corresponds to standard ARP resolution, immediately followed by successful multi-hop delivery across the WAN backbones:

<img width="855" height="370" alt="pining floor 1to floors 2 and 3" src="https://github.com/user-attachments/assets/e0e051cd-5b8a-4944-bae3-64dc43d242fb" />


