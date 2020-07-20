# Advanced Routing with Centos8

In this toturial we are going to create a wide area network betwen three data centers
at diffirent physical locations.

## Scenario
A startup or enthusiastic organization with more than one virtual Data Centers is 
in need to interconnect the networks and enable direct access between the nodes.
The virtual machine instances are spread across multiple virtual networks in each
of the data centers.

## Assumptions
- esxi visualization platform, utilizing free esxi hypervisior from VMware 
- All the concepts would fully apply to vCenter / vSphere based installations
- Each of the networks has a mixture of the Windows and Linux nodes
- DHCP and DNS services (if not already present) would be provided by routers

## Prerequisites

1. VMware esxi servers or Hyper-V housing the VM instances at each location
1. Existing VM instances to interconnect (LANs and WAN)

## Implenemtation Plan
### Steps
1. Build and configure Virtual Network Router at each Data Center
1. Connect the Virtual Router to all the Virtual Networks and configure proper
local rouring
1. Install a central routing hub
1. Congigure VPN service at the Central routing hub
1. Configure VPN service at each Data Center to connect to the entral routing hub
1. Configure routes at the central routing hub to correctly deliver IP traffic

### Operatung Systems

Role| OS
:--- |:---
|Virtual Routers    | CentOS 8 |
|Nodes              | Windows Server 2019<br/>  Ubuntu Linux |
|Central Routing hub| CentOS 8 |
