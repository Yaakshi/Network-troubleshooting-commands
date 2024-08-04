# Displaying Address Resolution Protocol (ARP) cache using arp command

ARP is used to map IP address to MAC address in a local network.

```> arp -a```

It displays all the current ARP cache on the system.

![image](https://github.com/user-attachments/assets/9cfb6f89-b45b-49ea-b596-d6dd4780f465)

It shows the IP address of the network interface.

- **Internet address** displays IP address of device on the network. Physical address is the corresponding MAC address.
- **Dynamic type** means ARP resolution was temporary and will expire after some time.
- **Static type** means the address is permanent.
