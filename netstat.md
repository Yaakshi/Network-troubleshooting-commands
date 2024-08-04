# Checking network configuration and statistics using netstat command

Netstat means Network Statistics. It displays all the active connections of the computer.

```> netstat```

![image](https://github.com/user-attachments/assets/bbc3d7d8-a5fc-44f7-99e5-052082cdbe3f)

- **Protocol** denotes which protocol has been used for that connection. 
- **Local address** denotes the IP address at the host end and the port used to make that connection.
- **Foreign address** is the IP address with port number on the other end or the external server that the computer is connected to.
- **States –** 
	- **ESTABLISHED** – open and active connection
	- **FIN_WAIT** – termination request sent to remote server.
	- **TIME_WAIT** – local end is waiting to handle any delayed packets before closing the connection

```> netstat -a```

![image](https://github.com/user-attachments/assets/85f198e1-656f-4ba9-b8f2-2747f62a500b)

All the TCP connections and ports are displayed. The output is similar to >netstat command.

```>netstat -e```

It displays the Ethernet interface statistics.

![image](https://github.com/user-attachments/assets/2cd7a9ee-7929-43cb-aa99-3bbd90297a34)

It displays the number of bytes received and sent by the network interface, the number of packets sent and received by unicast, broadcast and multicast, number of packets discarded due to any errors and any packets received with unsupported or new protocols.

```> netstat -n```

Displays active TCP connections all expressed only as numerical numbers and not names. The output is similar to >netstat only.

![image](https://github.com/user-attachments/assets/7ff05262-6faa-4bce-92b1-897780c6d638)

```> netstat -o```

Displays TCP connections along with an additional column process ID (PID).

![image](https://github.com/user-attachments/assets/d3bf96c9-5651-44cc-ad80-e526be1b1795)

A PID is a number that uniquely identifies a running process in an OS.

```> netstat -p UDP```

It filters and displays the details of the connections based on the criteria of a specific protocol.

![image](https://github.com/user-attachments/assets/8920e4c3-db2e-43af-96a1-03f696cb0bee)

There are no active UDP connections. Hence the table is empty.

```> netstat -p tcpv6```

![image](https://github.com/user-attachments/assets/70198757-8dea-4c94-bee5-7208086165f5)

Displays active connections under TCPv6 protocol.

```> netstat -s```

S stands for statistics. Detailed information is displayed for every protocol on the system.

![image](https://github.com/user-attachments/assets/7a228567-c914-4512-8f85-46bf93811209)

It displays the number of packets received by that protocol, any errors in the header values, number of packets discarded, any new and unrecognised protocols received, packets assembled and fragmentation.

![image](https://github.com/user-attachments/assets/0775cd81-f35d-48c2-8a6f-fe98000fefa6)

- **Active opens –** connection initiations done by the host
- **Passive opens –** connections accepted by the host
- **Reset connections –** reset packets received

```> netstat -r```

This command displays all the routing table of different protocols. 

![image](https://github.com/user-attachments/assets/9640264d-1d7d-4e30-8a6d-fbabe97ddc17)

- The **interface list** denotes all the interfaces through which connections can be made. 
- **Network destination** gives the IP address of the destination computer.
- **Netmask** gives the subnet mask of the destination IP address.
- **Gateway** gives the IP address of the next-hop router.
- **Interface** is the IP address of the network interface that sends the packets.
- **Metric** is the cost of the route. It is used to determine the best routing path.

```> netstat 10```

With interval value=10, the netstat command redisplays its information every 10 seconds.  The output is same as the general netstat command.

```> netstat /?```

Acts like a manual and displays various parameters that can be used along with netstat and their usage.

![image](https://github.com/user-attachments/assets/087362b7-d966-4faf-b054-599ce19a2f16)
