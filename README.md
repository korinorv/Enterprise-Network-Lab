# Enterprise-Scale Hierarchical Network Design and Implementation

## Project Overview
This repository contains the complete documentation, architectural design, and verification evidence for a secure three-tier hierarchical network. The project was developed to simulate a resilient corporate infrastructure, utilizing industry-standard protocols to ensure high availability, scalability, and security.

## Project Documentation
The following documents provide the technical specifications and presentation for the implementation:
* [View Technical Report (PDF)](./Documentation/Enterprise%20Network%20Project%20Report.pdf)
* [View Presentation Slides (PPTX)](./Documentation/Network_Project_Final_Slides.pptx)

## Technical Architecture
The infrastructure is modeled on the Cisco Three-Tier Hierarchical Model:
* Core Layer: Redundant routing fabric utilizing OSPF for dynamic path selection and NAT/PAT for secure internet egress.
* Distribution Layer: Multilayer switches managing Inter-VLAN routing and LACP (802.3ad) link aggregation.
* Access Layer: Layer 2 switches providing end-host connectivity with STP PortFast optimization.

## Protocols and Configurations
* Virtual LANs (VLANs): Segmentation of Management, Finance, IT, and Guest traffic.
* Redundancy: Link Aggregation Control Protocol (LACP) for multi-gigabit backbone reliability.
* Dynamic Routing: OSPF (Open Shortest Path First) for internal route propagation.
* Security: RSA-2048 SSH hardening, Extended Access Control Lists (ACLs), and Port Security.
* Address Translation: NAT/PAT Overload for internal-to-external communication.

## Troubleshooting and Resolution Logic
A primary focus of this project was the documentation of "Challenge vs. Resolution" logs to demonstrate technical problem-solving:
* LACP Interface Synchronization: Resolved port-channel suspension by defaulting physical member interfaces and re-initializing trunking parameters.
* OSPF Adjacency Stability: Corrected neighbor state failures by assigning explicit Router-IDs and verifying physical cabling logic.
* NAT Scope Expansion: Resolved internet reachability issues by re-configuring NAT ACLs to encompass all internal subnets.

## Technical Verification Directory
The Verification folder contains the following evidentiary screenshots:
* [Network Topology Diagram](./Verification/topology_logical_view.png)
* [NAT Translation Tables](./Verification/verification_nat_translations.png)
* [ACL Match Counts](./Verification/verification_acl_matches.png)
* [Connectivity Success (Pings)](./Verification/verification_ping_success.png)
