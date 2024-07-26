# Troubleshooting-network-commands

> 1. Verifying IP configuration settings

```> ipconfig```

This command gives a brief information about the network settings of the system. It gives details about all the network interfaces connected with the system – like Ethernet, Wireless LAN, connections with virtual machines like VMware, Bluetooth and Wi-Fi.

![image](https://github.com/user-attachments/assets/bf63b708-abda-4865-bc9f-b7f3476a2f5b)

**Ethernet adapter ethernet:**

It denotes the whether a connection is made or not to an ethernet LAN which is plugged into the RJ45 connectors on the computer motherboard physically. Two possibilities – Connected/Disconnected.

**Connection-specific DNS suffix:**

It is applicable when the computer is connected to a network organisation. It is the domain name of the local network that the system is connected to. It is used at the end of DNS queries for accessing unqualified host names within the same network. Here, in our case, Wi-Fi is connected to amritanet.edu.

**Wireless LAN adapter local area connection:**

It refers to any another wireless adapter connected to the system.

**Ethernet adapter VMware network adapter:**

It refers to the virtual network interface card(NIC) used by VMware to connect to a network. It denotes the connection acquired from the physical NIC and passed to the virtual NIC. Bridges – has many ports. Some are:

**vmnet0** – connect host and virtual machine(VM)
  
  **vmnet1** – create isolated network environment (host-only mode). Connect host, virtual DHCP server and VM
  
  **vmnet8** – It performs network address translation (NAT). It helps the VM to use host IP address to connect to internet or other networks. Connect virtual NAT server, DHCP server and VM.
  
  
**Wireless LAN adapter Wi-Fi:**

It is the connection made using Wi-Fi.

**Ethernet adapter Bluetooth Network Connection:**

details about Bluetooth connection

**Link local IPv6 address:**

It is IPv6 address used to communicate between nodes within the same network like other hosts and routers. They are globally unique unicast and local address. Some prefixes are:

**fe80::** to denote local-link unicast addressing
  
**fc00::** denotes that address is locally assigned

**2000::** is global unicast addressing

**FF00::** for multicast
  
**IPv4 address:**

the address assigned to that particular adapter during the connection. They are globally unique public address used for network traffic and private addresses.

**Subnet mask:**

Subnetting means to partition a single large network into smaller sub-networks. Subnet mask is a 32-bit number(4 octets = 4*8 bits) that divides IP address into network and host portions.

**Default subnet masks:**

  **Class A:** 255.0.0.0
  
  **Class B:** 255.255.0.0
  
  **Class C:** 255.255.255.0

  
**Default gateway:**

the device that connects local network to other networks and the Internet. The address is the network router’s IP address.
