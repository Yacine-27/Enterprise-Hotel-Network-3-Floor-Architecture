# Mulit-Floor Network Architecture

The project demonstrates advanced networking concepts including VLAN segmentation, Router-on-a-Stick (ROAS) inter-VLAN routing, dynamic/static routing between core routers, and endpoint infrastructure services like DHCP, SSH management, and Port Security.

## Architecture

The infrastructure isolates department traffic across three distinct physical floors while maintaining secure inter-departmental communication through a triangular core routing matrix.

    Floor 1 (Operations): Reception, Store, Logistics, and localized Guest/Staff Wi-Fi.
    Floor 2 (Corporate): Finance, HR, Sales, and Corporate Wi-Fi.
    Floor 3 (Management & Infrastructure): Administration, IT Operations, and Executive Wi-Fi.

<img width="1536" height="1024" alt="thumbnail" src="https://github.com/user-attachments/assets/2ae71348-c6dc-4ee9-8ade-6303b666b947" />

## Key Features

- VLAN Segmentation & Trunking.
- Inter-VLAN Routing (Router-on-a-Stick).
- Core Routing Matrix
- Network Automation & Security: DHCP, SSH Secure Management, Switchport Port Security.
