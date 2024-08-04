# Resolving domain names using nslookup command

nslookup stands for Name Server Lookup. It is used to query DNS server to obtain the information about domain name and its IP address.

```> nslookup google.com```

![image](https://github.com/user-attachments/assets/64be4da2-2705-4d05-9963-1d4c1a268cba)

- **Server and address:** denotes the DNS server that responded to the query and its IP address
- **Non-authoritative answer:** it means that the displayed information was obtained from the cache and not directly from authoritative DNS server.
- **Name and address:** it is the domain name and its IP address that was requested.

```> nslookup intranet.cb.amrita.edu```

![image](https://github.com/user-attachments/assets/d63d5ce9-f0cd-43bc-bda9-67fabab0809e)

The Wi-Fi is connected to Amrita network. Both the DNS server and requested domain name have IP address in the same range.

>** -type parameter**

- A – maps to IPv4 address
- AAAA – maps to IPv6 address
- CNAME – maps the subdomain to its main domain hosting
- MX – gives information about mail exchange server
- NS – gives the authoritative DNS servers for a domain
- PTR – used for reverse DNS lookup
- SOA – State of authority – gives administrative information about the domain
- TXT – stores text information like SPF records

```> nslookup -type=soa intranet.cb.amrita.edu```

![image](https://github.com/user-attachments/assets/e7fa7a22-eb69-4b82-bac3-8379a65d9989)

- **Primary name server** – primary DNS server of the domain 
- **Responsible mail addr** – email address of the domain administrator – sysadmin@amrita.edu
- **Serial** – version of the zone file in YYYYMMDDnn format where n increments with each change
- **Refresh** – the interval after which secondary DNS servers must check for updates
- **Retry** – if the last refresh fails, the DNS servers must wait for this long to retry another refresh
- **Expire** – the validity period if the secondary servers cannot access the primary server
- **Default TTL** – time taken to cache the records by the servers
