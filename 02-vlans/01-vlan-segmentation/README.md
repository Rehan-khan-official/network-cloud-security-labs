# Lab 2 — VLAN Segmentation & Inter-VLAN Routing

## Objective

Design and configure a segmented enterprise network using Cisco Packet Tracer.

The lab implements multiple VLANs, access ports, an 802.1Q trunk, and Router-on-a-Stick inter-VLAN routing.

## Network Topology

The network consists of:

- 1 Cisco 2911 Router
- 1 Cisco 2960 Switch
- 6 PCs
- 3 VLANs

## VLAN Design

| VLAN | Department | Network |
|---|---|---|
| 10 | IT | 192.168.10.0/24 |
| 20 | HR | 192.168.20.0/24 |
| 30 | ADMIN | 192.168.30.0/24 |

## Port Assignment

| Switch Port | Device | VLAN |
|---|---|---|
| Fa0/2 | IT-PC1 | VLAN 10 |
| Fa0/3 | IT-PC2 | VLAN 10 |
| Fa0/4 | HR-PC1 | VLAN 20 |
| Fa0/5 | HR-PC2 | VLAN 20 |
| Fa0/6 | ADMIN-PC1 | VLAN 30 |
| Fa0/7 | ADMIN-PC2 | VLAN 30 |
| Gi0/1 | Router R1 | Trunk |

## IP Addressing

| Device | IP Address | Gateway |
|---|---|---|
| IT-PC1 | 192.168.10.10 | 192.168.10.1 |
| IT-PC2 | 192.168.10.11 | 192.168.10.1 |
| HR-PC1 | 192.168.20.10 | 192.168.20.1 |
| HR-PC2 | 192.168.20.11 | 192.168.20.1 |
| ADMIN-PC1 | 192.168.30.10 | 192.168.30.1 |
| ADMIN-PC2 | 192.168.30.11 | 192.168.30.1 |

## Router-on-a-Stick Configuration

The router uses subinterfaces to provide gateways for each VLAN.

```text
G0/0.10 → VLAN 10 → 192.168.10.1
G0/0.20 → VLAN 20 → 192.168.20.1
G0/0.30 → VLAN 30 → 192.168.30.1

show vlan brief
show interfaces trunk
show ip interface brief


---

# 4. GitHub commit

When you upload it, use a meaningful commit message:

```text
Add VLAN segmentation and inter-VLAN routing lab
