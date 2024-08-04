# Tracing the route of packets using tracert command

Tracert stands for ‘trace route’. It sends ICMP packets from source to destination via several pathways containing several routers. Whenever a packet passes through a router, it is considered as a hop.

```> tracert 10.11.132.117```

This command displays the number of hops, time taken to reach the destination computer and all the intermediate router’s IP addresses.

![image](https://github.com/user-attachments/assets/9c0539f8-7e7f-4700-85db-24526fce35f4)

Here, 10.11.132.117 is the IPv4 address of Wi-Fi adapter. There is only one hop because we are tracing the same computer as the source and the destination.

```> tracert intranet.cb.amrita.edu```

![image](https://github.com/user-attachments/assets/9ca43203-05b8-4015-bce3-cc17a1db4064)

There are 2 hops to reach intranet.cb.amrita.edu. The output shows 5 columns.

- **Column1** – the hop number – increments every time it passes through a router in the network
- **Column 2, 3 and 4** – round trip time (in milliseconds) – It is the time taken for the packet to reach the next router and back to the source. Three columns denote three packets sent to the same router. Less time means the faster the connection. Each column represents various paths that lead to the same destination – hence, the time varies every time.
- **Column 5** – indicates the IP address of the router connected during each hop.

The asterisk (*) symbol denotes that there was a timeout or no response from the router back to the source.
