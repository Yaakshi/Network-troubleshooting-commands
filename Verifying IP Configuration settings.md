# Troubleshooting-network-commands

# 1. Verifying IP configuration settings

```> ipconfig```

This command gives a brief information about the network settings of the system. It gives details about all the network interfaces connected with the system – like Ethernet, Wireless LAN, connections with virtual machines like VMware, Bluetooth and Wi-Fi.

![image](https://github.com/user-attachments/assets/bf63b708-abda-4865-bc9f-b7f3476a2f5b)

>**Ethernet adapter ethernet:**

It denotes the whether a connection is made or not to an ethernet LAN which is plugged into the RJ45 connectors on the computer motherboard physically. Two possibilities – Connected/Disconnected.

>**Connection-specific DNS suffix:**

It is applicable when the computer is connected to a network organisation. It is the domain name of the local network that the system is connected to. It is used at the end of DNS queries for accessing unqualified host names within the same network. Here, in our case, Wi-Fi is connected to amritanet.edu.

>**Wireless LAN adapter local area connection:**

It refers to any another wireless adapter connected to the system.

>**Ethernet adapter VMware network adapter:**

It refers to the virtual network interface card(NIC) used by VMware to connect to a network. It denotes the connection acquired from the physical NIC and passed to the virtual NIC. Bridges – has many ports. Some are:

- **vmnet0** – connect host and virtual machine(VM)
  
- **vmnet1** – create isolated network environment (host-only mode). Connect host, virtual DHCP server and VM
  
- **vmnet8** – It performs network address translation (NAT). It helps the VM to use host IP address to connect to internet or other networks. Connect virtual NAT server, DHCP server and VM.
  
>**Wireless LAN adapter Wi-Fi:**

It is the connection made using Wi-Fi.

>**Ethernet adapter Bluetooth Network Connection:**

details about Bluetooth connection

>**Link local IPv6 address:**

It is IPv6 address used to communicate between nodes within the same network like other hosts and routers. They are globally unique unicast and local address. Some prefixes are:

- **fe80::** to denote local-link unicast addressing
  
- **fc00::** denotes that address is locally assigned

- **2000::** is global unicast addressing

- **FF00::** for multicast
  
>**IPv4 address:**

the address assigned to that particular adapter during the connection. They are globally unique public address used for network traffic and private addresses.

>**Subnet mask:**

Subnetting means to partition a single large network into smaller sub-networks. Subnet mask is a 32-bit number(4 octets = 4*8 bits) that divides IP address into network and host portions.

>**Default subnet masks:**

- **Class A:** 255.0.0.0

- **Class B:** 255.255.0.0
  
- **Class C:** 255.255.255.0
  
>**Default gateway:**

the device that connects local network to other networks and the Internet. The address is the network router’s IP address.


```> ipconfig/all```

Displays detailed information about network configurations of the computer.

![image](https://github.com/user-attachments/assets/bf90035e-e555-46e7-888b-2045246219f0)

>**Primary DNS suffix:**

It is the domain name when attached to a network organisation.

>**Node type:**

It denotes the how the computer communicates with other computers in the network. The four types: 
- Broadcast – B node
- Peer to peer – P node
- Mixed – M node (B+P)
- Hybrid – H node (B+P in reverse)

>**IP routing:**

Enabled/Disabled shows if routing the IP packets between different network segments is allowed or not.

>**WINS proxy:**

It is used to resolve the names of hosts to IP addresses in intranets. WINS stands for Windows Internet Name Service.

>**Description:**

Description of an adapter describes the type, name and brand of the physical driver or hardware adapter in the computer.

>**Physical address:**

Physical address is the unique MAC address provided by the manufacturer for that particular adapter.

>**DHCP:**

Dynamic Host Configuration Protocol is used to automatically assign IP address to devices on a network. If enabled, DHCP server allocates the address. Else, static IP address is used.

>**Autoconfiguration:**

Even if DHCP is unavailable, IP address is configured automatically by the network adapter when enabled. If disabled, the adapter cannot assign address to itself. Lease obtained and expires denotes the validity period of the IP address assigned by the DHCP server.

>**DHCP server:**

The IP address of the DHCP server that provided the IP configuration for that adapter.

>**DHCPv6 IAID:**

Identity Association Identifier: the unique ID that identifies the network interface on the client system.

>**DHCPv6 Client DUID:**

DHCP Unique Identifier. ID used to identify the client system across all networks.

>**NetBIOS over TCP/IP:**

NetBIOS allows different computers to communicate and access shared resources.

```> ipconfig/renew```

This command refreshes the IP address configuration. Current IP address is dropped and a new one is requested from the DHCP server.

![image](https://github.com/user-attachments/assets/cc0d3d16-c046-4358-bc5e-27254dd3d6f0)

Since Ethernet adapter, local connections and Bluetooth are not connected, renew operation cannot be performed. 

```> ipconfig/release```

It will discard all the IP addresses of all the adapters.

![image](https://github.com/user-attachments/assets/95f2b025-71f2-48a2-8763-9dfacf0b1e36)

There is no IPv4 address associated with the adapters.

```> ipconfig/flushdns```

Flushdns is used to clear the DNS cache on the computer.

![image](https://github.com/user-attachments/assets/f6e4d32c-67ac-4a79-bd8d-22e70dff1e4e)

DNS cache stores recently accessed domain names for quickly resolving domain names to IP addresses. It is cleared completely and successfully.

``` > ipconfig/displaydns```

It is used to view the DNS cache.

![image](https://github.com/user-attachments/assets/2b8af8f5-0152-4f9a-be0a-9054cee0e610)

Since DNS was flushed, the records are less. It displays:
- domain name
- the type of record – 1 maps domain name to IPv4 address, 2 maps to IPv6 address, 15 specifies mail servers, etc. 
- The time to live (in seconds) is the validity of the record in the cache. 
- Section denotes where the record was found.
	- Answer – actual answer to query
	- Authority – information about authoritative DNS servers
	- Additional – extra information
- A (host) record denotes the actual IPv4 address it resolves to.
- PTR record – for reverse DNS lookup – map IP address to domain name

```> ipconfig/registerdns```

It is used to manually register DNS names and IP addresses of a computer in DNS server.

![image](https://github.com/user-attachments/assets/78eb0266-15e8-4592-8a2e-68b502c7c4b1)

It can be verified using nslookup or dig commands.

```> ipconfig/showclassid```

It will display the DHCP class ID for the adapter. This command works on networks with a DHCP server. This command works mostly in a business or organisational network and not a home network.

![image](https://github.com/user-attachments/assets/7c688807-15ab-4dc6-a0cf-1d3766e74ac0)

Currently, we are connected to a home network, hence, there is no DHCP server in the network.

```> ipconfig/setclassid```

It is used to set the DHCP class ID for the adapter.

![image](https://github.com/user-attachments/assets/2ec56ce2-6944-4c20-b5e4-e05581fda7db)

The ID helps to distinguish between DHCP clients in the same network.

```> ipconfig/?```

It acts like a manual for the command entered. displays all the possible options that can be along with the ipconfig command and a brief description about their usage.

![Uploading image.png…]()







