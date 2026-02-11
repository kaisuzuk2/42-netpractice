*This project has been created as part of the 42 curriculum by kaisuzuk*

# Description
NetPractice is an exercise designed to help you understand the inner workings of networking.
The goal of this project is to establish successful communication between hosts by appropriately configuring IP addresses, subnet masks, and routing tables.

The project consists of 10 levels (Level 1 to Level 10).
As you progress, the configurations become more complex, involving the connection of multiple different networks. In every level, you are required to set the correct IP addresses and subnet masks to ensure connectivity.

# Instructions

## How to Run

1. Download [net_practice.1.9.tgz](https://cdn.intra.42.fr/document/document/46101/net_practice.1.9.tgz) from the project page.

2. Extract the downloaded file

3. Execute run.sh located inside the folder.

4. A page will open in your browser. Enter your 42 ID.
- Selecting "Training" will present the problems from Level 1 to Level 10 in order.
- Selecting "Evaluation" will present random problems chosen from Levels 6 to 10.

5. Check the network configuration of each level and set the IP addresses and routing so that communication is established.
Press "Check again" to verify if your settings are correct. Once a level is cleared, a "Next" button will appear, allowing you to proceed to the next level.

## Exxporting Configrations
After completing each level, you can download your current network settings by clicking the "Get my config" button. A separate configuration file will be generated for each level.

## Submission Requirements
Submit a total of 10 config files (one for each level from 1 to 10).
Place these files in the root of your repository. Additionally, submit this README.md file.

# Resources

## OSI Reference Model and TCP/IP

The OSI Reference Model is a guideline for designing communication protocols, established by the ISO. It simplifies complex network protocols by dividing the necessary communication functions into [7 layers](https://learningnetwork.cisco.com/s/article/osi-model-reference-chart). A protocol is a set of rules for communication; devices with different protocols cannot communicate with each other.

TCP/IP is the suite of protocols actually used on the internet. Unlike the OSI model, it is divided into [4 layers](TCP/IP is the suite of protocols actually used on the internet. Unlike the OSI model, it is divided into 4 layers. TCP/IP became the dominant model largely due to its early support by UNIX systems.). TCP/IP became the dominant model largely due to its early support by UNIX systems.

When data is sent, encapsulation occurs. Each layer adds information necessary for transmission in the form of a "header." For example:
- The Network Layer adds the destination IP address.
- The Transport Layer adds control information to ensure communication reliability.
- The Data Link Layer adds MAC addresses.
On the receiving side, decapsulation occurs. Each layer removes its respective header until the data is finally delivered to the application.

In NetPractice, you will primarily focus on the 3rd layer of the OSI model (Network Layer) and learn concepts from the Internet Layer of the TCP/IP model, such as IP addressing, subnet masks, routing, and default gateways. Additionally, the behavior of Switches (corresponding to Layer 2/Data Link Layer) and the logic of communication within the same network are vital elements.

## TCP/IP Addressing

TCP/IP addressing is a system used to identify the network and the specific host of a communication partner using IP addresses and subnet masks. An IP address is divided into a Network Portion and a Host Portion, with the boundary defined by the Subnet Mask.

In communication within the same network, the device determines via bitwise operations whether the destination shares the same network portion. If it does, communication happens directly without a router. For communication to a different network, packets are forwarded to the Default Gateway for routing.

## Subnet Mask

A subnet mask is a 32-bit value that determines the boundary between the network portion and the host portion of an IP address. It is always used in conjunction with an IP address. It is essential for dividing and managing networks and for a computer to determine if another device belongs to the same network.

## Default Gateway

The default gateway is the IP address of the device (router) that serves as the access point for a network. If a destination does not exist within the local network, the device sends the data to the router in its own network. The router then forwards the data toward the destination network.

## LAN and WAN

Computer networks can be categorized into two types based on their scale: LAN (Local Area Network) and WAN (Wide Area Network).

- LAN: A private network constructed within a single building or site.
- WAN: A network constructed over a wide geographical area, generally using lines provided by telecommunications carriers.

## Routers and Switches

### Switch

A switch connects multiple devices (PCs, printers, etc.) within a LAN and efficiently transmits data only to the intended destination node. It maintains a MAC Address Table to track which MAC address is connected to which port. If a destination MAC address is not in the table, the switch performs "flooding," sending the data to all ports except the one it arrived on.

### Router

A router is a device that enables communication between nodes on different networks. It maintains a Routing Table. The router checks the destination IP address of incoming data and forwards it to the appropriate location based on the table.
Routing is performed using Longest Prefix Match. If no specific route matches, the Default Route (0.0.0.0/0) is used as a "path of last resort."


# References

- Mastering TCP/IP: Introductory Level
- Isshuukande CCNA no kiso ga manaberu hon 
- [Network(CCNA) Learning for Aspiring Infrastructure Engineers(Youtube)] (https://www.youtube.com/playlist?list=PLXXalsdlzX-J7AUuw2zSHit5nRUZ3eDdz)


# AI
- Used as a self-check to test my understanding.
- Used for text translation.