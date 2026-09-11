# virtual-cybersecurity-lab-NETWORKWALKS-B083-WK1
VirtualBox and Kali Linux lab environment for penetration testing, vulnerability assessment, and cybersecurity practice.
## Project Overview
This project focuses on setting up a virtual cybersecurity and penetration-testing lab using VirtualBox and Kali Linux.
## Objectives
- Install virtual box and Kali Linux
- Configure NAT Network
- Assign static IP address on Kali Linux VM
- Test network connectivity and DNS resolution
- Take a snapshot of the VM
- Document the process
## Purpose of Lab
The lab provides a safe, isolated, and controlled environment for learning cybersecurity concepts and carrying out authorized security testing. It can be used to practice network reconnaissance, port scanning, vulnerability assessment, packet analysis, web security testing, exploitation techniques, and experimenting with different cybersecurity tools.
## Lab Architecture
![image alt](https://github.com/benjamin-ngandwe/virtual-cybersecurity-lab-NETWORKWALKS-B083-WK1/blob/main/lab.jpg?raw=true)
## Lab Configuration
![image alt](https://github.com/benjamin-ngandwe/virtual-cybersecurity-lab-NETWORKWALKS-B083-WK1/blob/main/lab%20config.png?raw=true)
## Lab Setup Procedure
## Step 1. Install 7-Zip
7-Zip was installed to extract the Kali Linux virtual-machine package, which may be distributed as a .7z archive.
Tool: 7-Zip
## Step 2. Step 2. Install VirtualBox
A dedicated NAT Network was created in VirtualBox.
Configuration: Network Name: NatNetwork IPv4 Prefix: 10.0.0.0/24 

![image alt](https://github.com/benjamin-ngandwe/virtual-cybersecurity-lab-NETWORKWALKS-B083-WK1/blob/d6f9ff699484c745d8dedca87dc60a254c4bff17/nat.png)

## Step 4. Import Kali Linux
The Kali Linux virtual machine was downloaded from the official Kali Linux website and imported into VirtualBox.
The VM network adapter was configured as follows:
Adapter 1
Attached to: NAT Network
Network:     NatNetwork
Adapter Type: Intel PRO/1000 MT Desktop

![image alt](https://github.com/benjamin-ngandwe/virtual-cybersecurity-lab-NETWORKWALKS-B083-WK1/blob/main/kali.png?raw=true)

## Step 5. Configure the Kali Linux Network
The Kali Linux network configuration was checked and configured with a static IPv4 address.

![image alt](https://github.com/benjamin-ngandwe/virtual-cybersecurity-lab-NETWORKWALKS-B083-WK1/blob/main/ip.png?raw=true)

## Step 6. Create a Clean VM Snapshot
After completing the initial configuration, a VirtualBox snapshot (Backup) was created.

## Problems Encountered

## Problem 1. Internet Connectivity After Static IP Configuration
After manual configuration of the IPv4 settings, Internet connectivity may fail depending on the Kali/NetworkManager configuration, the command "sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0" sorts out this issue

## What I learned
Through this project, I learned how to create and configure a virtual environment for cybersecurity practice.

## NAT Vs NAT Network
A NAT Network allows multiple virtual machines to communicate with each other while also providing internet access through network address translation, making it ideal for building a multi-machine cybersecurity lab.

## Virtual Machine Networking
I learned how VirtualBox network adapters connect virtual machines to different network environments and how network settings influence communication between the virtual machines.

## VM Snapshots
I learned the importance of creating a clean snapshot before carrying out risky or experimental activities, providing a reliable recovery point that can be restored during future cybersecurity exercises.
