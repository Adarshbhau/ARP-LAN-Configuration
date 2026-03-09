Configuration of Address Resolution Protocol (ARP)
Aim

The aim of this project is to construct a simple Local Area Network (LAN) and understand the concept and operation of the Address Resolution Protocol (ARP) using Cisco Packet Tracer.
The project demonstrates how devices communicate in a LAN by translating IP addresses into MAC addresses using ARP before data transmission occurs.

Project Statement

In computer networks, communication between devices requires both logical addressing (IP address) and physical addressing (MAC address).
While IP addresses are used to identify devices in a network, the actual delivery of data frames inside a LAN occurs using MAC addresses.

When a device wants to send data to another device using its IP address, it must first determine the destination device’s MAC address. Without a mechanism to perform this translation, communication between devices within a LAN would not be possible.

The Address Resolution Protocol (ARP) is used to dynamically map an IP address to its corresponding MAC address.

This project simulates a simple LAN using Cisco Packet Tracer to demonstrate how ARP requests and replies occur when devices communicate with each other.

What is an IP Address

An Internet Protocol (IP) address is a unique logical identifier assigned to each device connected to a network. It allows devices to identify and communicate with each other across a network.

IP addresses operate at the Network Layer (Layer 3) of the OSI model and are essential for routing data packets between devices.

Example of an IPv4 address:

192.168.1.1

IPv4 addresses consist of 32 bits divided into four octets separated by dots. Each octet can have a value between 0 and 255.

Example:

11000000.10101000.00000001.00000001

There are two main types of IP addresses:

IPv4

32-bit address

Most commonly used

Example: 192.168.1.10

IPv6

128-bit address

Developed to overcome IPv4 limitations

Example:

2001:0db8:85a3:0000:0000:8a2e:0370:7334
What is a MAC Address

A MAC Address (Media Access Control Address) is a unique hardware address assigned to a network interface card (NIC) by the manufacturer.

Unlike IP addresses, MAC addresses are permanent physical addresses used for communication within a local network.

Example:

00:1A:2B:3C:4D:5E

A MAC address consists of 48 bits (6 bytes) written in hexadecimal format.

Structure of a MAC address:

00-1A-2B | 3C-4D-5E

First 24 bits → Manufacturer ID (OUI)
Last 24 bits → Device Identifier

MAC addresses operate at the Data Link Layer (Layer 2) of the OSI model.

Address Resolution Protocol (ARP)

ARP (Address Resolution Protocol) is used to map an IP address to a MAC address in a local network.

When a device wants to communicate with another device in the same LAN, it must know the destination device's MAC address.

Working of ARP

Device A wants to send data to Device B.

Device A knows the IP address of Device B.

Device A checks its ARP cache table.

If the MAC address is not found, it sends an ARP Request (broadcast).

All devices receive the request.

Device B responds with an ARP Reply containing its MAC address.

Device A stores the MAC address in its ARP table.

Data transmission begins.

Example ARP command:

arp -a

This command displays the ARP table of the system.

Reverse Address Resolution Protocol (RARP)

Reverse Address Resolution Protocol (RARP) performs the opposite function of ARP.

Instead of mapping:

IP Address → MAC Address

RARP maps:

MAC Address → IP Address

RARP was used in diskless workstations that did not have storage to store IP configurations.

Working of RARP

The device sends a RARP Request containing its MAC address.

The RARP server receives the request.

The server searches its database for the MAC address.

The server replies with the corresponding IP address.

Limitations of RARP

Requires a dedicated RARP server

Works only inside LAN

Cannot provide subnet mask or gateway

Because of these limitations, RARP was replaced by:

BOOTP

DHCP

Scope of the Solution

The scope of this project includes:

Understanding LAN communication

Learning how ARP resolves IP addresses into MAC addresses

Designing a simple LAN using Cisco Packet Tracer

Assigning IP addresses to devices

Observing ARP request and ARP reply packets

Viewing ARP tables of devices

Testing connectivity using the ping command

This project provides a basic understanding of network addressing and protocol communication.

Required Components
Hardware

Personal Computers (2 or more)

8 Port Ethernet Switch

LAN Cables

Network Interface Cards

Software

Cisco Packet Tracer

Operating System (Windows / Linux)

Command Prompt / Terminal

Simulated Circuit (Cisco Packet Tracer)

Network Topology:

PC1  --------\
               SWITCH
PC2  --------/

Configuration:

PC1

IP Address : 192.168.1.1
Subnet Mask: 255.255.255.0

PC2

IP Address : 192.168.1.2
Subnet Mask: 255.255.255.0

Test connectivity using:

ping 192.168.1.2

Observe ARP packets in Simulation Mode in Cisco Packet Tracer.

Demo Video / Screenshots

Include the following in the repository:

Network topology screenshot

IP configuration screenshot

Ping command output

ARP table output

Simulation mode showing ARP packets

Example command:

arp -a

Added ARP project documentation


