# Enterprise Network – Cisco Packet Tracer

![Status](https://img.shields.io/badge/Status-Completed-green)
![Tool](https://img.shields.io/badge/Tool-Cisco%20Packet%20Tracer-blue)
![Network](https://img.shields.io/badge/Type-Enterprise%20Network-orange)

This project implements a small enterprise network with two departments—**Accounts** and **Delivery**—each containing 2 PCs and 1 printer, connected through switches and a router. The given network `192.168.40.0` is subnetted into two /25 subnets for departmental separation.

## Network Topology

            +----------------------+
            |        Router        |
            |  G0/0/1   G0/0/2     |
            +----------+-----------+
                       |
       ---------------------------------------
       |                                     |
+------------------+                +------------------+
|  Accounts Dept   |                |  Delivery Dept   |
+------------------+                +------------------+
| PC0  PC1 Printer |                | PC2 PC3 Printer  |
|   Switch_1       |                |   Switch_2       |
+------------------+                +------------------+


## Screenshots

### Topology Overview
![Network Topology](./screenshots/1.png)

### IP Configuration
![IP Configuration](./screenshots/2.png)

## Project Structure
.
├── README.md
├── enterprise-network.pkt        # Packet Tracer file
└── screenshots/
    ├── topology.png
    └── ip-config.png
## Subnetting Summary
- Network: `192.168.40.0`
- Subnets Needed: `2`
- Borrowed Bits: `1`
- Subnet Mask: `255.255.255.128 (/25)`

## Subnet Details
**Accounts Subnet**  
- Network ID: `192.168.40.0`  
- Host Range: `192.168.40.1 – 192.168.40.126`  
- Gateway: `192.168.40.1`  

**Delivery Subnet**  
- Network ID: `192.168.40.128`  
- Host Range: `192.168.40.129 – 192.168.40.254`  
- Gateway: `192.168.40.129`

## IP Assignments
- Accounts: PC0 `192.168.40.2`, PC1 `192.168.40.3`, Printer `192.168.40.4`  
- Delivery: PC2 `192.168.40.130`, PC3 `192.168.40.131`, Printer `192.168.40.132`

## Testing
Connectivity between both departments verified via `ping`.

