# Enterprise-Scale Hierarchical Network Design and Implementation

## Project Overview
This repository contains the complete documentation, architectural design, and verification evidence for a secure three-tier hierarchical network. The project was developed to simulate a resilient corporate infrastructure, utilizing industry-standard protocols to ensure high availability, scalability, and security.

## Project Documentation
The following documents provide the technical specifications and presentation for the implementation:
* [View Technical Report (PDF)](./Documentation/Enterprise%20Network%20Project%20Report.pdf)
* [View Presentation Slides (PPTX)](./Documentation/Enterprise%20Network%20Project%20Report.pptx)

## Technical Architecture
The infrastructure is modeled on the Cisco Three-Tier Hierarchical Model:
* Core Layer: Redundant routing fabric utilizing OSPF for dynamic path selection and NAT/PAT for secure internet egress.
* Distribution Layer: Multilayer switches managing Inter-VLAN routing and LACP (802.3ad) link aggregation.
* Access Layer: Layer 2 switches providing end-host connectivity with STP PortFast optimization.

## Protocols and Configurations
* Virtual LANs (VLANs): Segmentation of Management, Finance, IT, and Native traffic.
* Redundancy: Link Aggregation Control Protocol (LACP) for multi-gigabit backbone reliability.
* Dynamic Routing: OSPF (Open Shortest Path First) for internal route propagation.
* Security: RSA-2048 SSH hardening, Extended Access Control Lists (ACLs), and Port Security.
* Address Translation: NAT/PAT Overload for internal-to-external communication.

## Troubleshooting and Resolution Logic
A primary focus of this project was the documentation of resolution logic for complex configuration conflicts:
* LACP Interface Synchronization: Resolved port-channel suspension by defaulting physical member interfaces.
* OSPF Adjacency Stability: Corrected neighbor state failures by assigning explicit Router-IDs.
* NAT Scope Expansion: Resolved internet reachability issues by re-configuring NAT ACLs to encompass all internal subnets.

## Technical Verification Directory
The Verification folder contains the following evidentiary screenshots:
* [Network Topology Diagram](./Verification/Network%20Topology%20Diagram.png)
* [NAT Translation Tables](./Verification/NAT%20Translation%20Tables.png)
* [ACL Match Counts](./Verification/ACL%20Match%20Counts.png)
* [Connectivity Success (Pings)](./Verification/Connectivity%20Success.png)
* [VLAN Status Verification](./Verification/VLAN%20Status%20Verification.png)
