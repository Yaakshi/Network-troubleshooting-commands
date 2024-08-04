# Checking IP level connectivity using Ping command

Ping stands for Packet Internet or Internetwork Groper. This command is used to test and verify the connection between computer and another computer or server using IP address or even hostname. 

```> ping 192.168.7.51```

![image](https://github.com/user-attachments/assets/397da4ef-2421-438b-a5e6-8adc3fab1e95)

192.168.7.51 is the IPv4 address of Wi-Fi adapter. The above result is when Wi-Fi is off.

![image](https://github.com/user-attachments/assets/19370106-f19e-4f7b-92cb-0e444a07ef58)

The ping to same address when Wi-Fi is on yields the above output. Here both sender and receiver is same address.

```> ping google.com```

![image](https://github.com/user-attachments/assets/49dc9fa5-e6e2-46fa-85df-4f25b284904a)

Pinging google.com: Totally 4 packets are sent and received. Nothing is lost. Each ICMP packet is 32 bytes.

- **Time** denotes the time taken to reply. 
- **Time to live (TTL)** shows number of hops that the packet can travel before discarding.
- **Round trip times** – the maximum, minimum and average of time of each packet taken to reply.

![image](https://github.com/user-attachments/assets/203124a1-63ef-4533-beb7-a5946a432b3e)

Options:
- -n : number of packets to be sent. 4 is default
- -w : timeout – reply must be within the timeframe (in milliseconds). 1000ms is default.
- -l : size of packet. 32 bytes is default.
- -f : do not fragment the packet. It is fragmented by default.
- -t : ping continues until stopped using Ctrl + C.
- -4: ping using IPv4
- -6 : ping using IPv6
