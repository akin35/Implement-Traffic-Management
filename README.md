# Implement-Traffic-Management
### This repo is created to demo implementation of traffic management on azure.
### You can follow coming steps to complate all tasks.

## Tasks: 
1.	Provision the environment
2.	Configure hub and spoke network topology
3.	Test transitivity of virtual networking peering
4.	Configure routing in the hub and spoke topology
5.	Implement Azure Load Balancer
6.	Implement Azure Application Gateway

## Solution of Implement Traffic Management step by step:

## Step 1:
Created 4 virtual machines from azure portal according to the Topology 1.0 ; 
* be careful vnets and subnets configurations
* there is no public ip on the vm’s 
* don’t forget to save-download your json files
* all vm’s will be in the same rg
*	NEXT 6 pictures (1A…1F) show VMs, VNETs and RG configuration.
*	On the file storage(go to file)part on GitHub, you can see-download ARM templates as a separate file.
## Step 2-3:
Created 2 VNET peering between vnet01-vnet2 and vnet01-vnet3 like on the Topology 1.0 ; 
* After setting up 2 peering check the connectivity between them.
*	To check the connectivity is used Network Watcher (after altering the NW on the left pane use connection troubleshooting)
*	Next 2 pictures (2A-2B) demonstrated the connectivity, all details on it
## Step 4:
Created 2 route table which are route_from_vnet2-to-vnet3 and from_vnet3_to_vnet2.
Topology 1.0 ; 
*	Configuration, Next hop type and Next hop IP address is shown on the pictures (3A-3B)
## Step 5:
Implemented Azure Load Balancer on vm0 and vm1 and named az104-06-lb4 like on the Topology 1.0 ; 
*	Implementation take placed on the resource group 4 (rg4)
*	Public ip assigned to the Load balancer which is called az104-06-pip4
*	Configuration is shown on the picture(4A…4D)
*	There is no NAT rules
Step 6:
Implemented Azure Application Gateway on vm0 and vm1 and named az104-06-lb4 like on the Topology 1.0 ; 
*	Implementation take placed on the resource group 5 (rg5)
*	Public ip assigned to the Load balancer which is called az104-06-pip5
*	Configuration is shown on the picture(5A…5D)
*	There is no NAT rules

## Thanks

