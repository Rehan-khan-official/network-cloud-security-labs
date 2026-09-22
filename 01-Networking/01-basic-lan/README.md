\# Lab 01 — Basic LAN Configuration



\## Objective



Build and configure a basic LAN using Cisco Packet Tracer and verify connectivity between network devices.



\## Tools



\- Cisco Packet Tracer

\- Cisco 2911 Router

\- Cisco 2960 Switch

\- PC-PT



\## Network Topology



The network consists of one router, one switch and three PCs.



\## IP Addressing



| Device | IP Address | Subnet Mask | Default Gateway |

|---|---|---|---|

| Router G0/0 | 192.168.1.1 | 255.255.255.0 | — |

| PC0 | 192.168.1.10 | 255.255.255.0 | 192.168.1.1 |

| PC1 | 192.168.1.11 | 255.255.255.0 | 192.168.1.1 |

| PC2 | 192.168.1.12 | 255.255.255.0 | 192.168.1.1 |



\## Configuration



The router interface was configured with:



```text

interface gigabitEthernet 0/0

ip address 192.168.1.1 255.255.255.0

no shutdown

