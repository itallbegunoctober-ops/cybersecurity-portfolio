# Lab 03 — Analyze Your First Packet with Wireshark

**Provider:** Google Skills training activity  
**Category:** Network Analysis  
**Status:** Completed  
**Provider duration/level:** 1 hour / Advanced

## Objective
Open a sample PCAP in Wireshark, review packet metadata and use display filters to inspect selected traffic and protocol fields.

## Environment and tools
Windows virtual machine, Wireshark and a sample PCAP supplied by the training activity.

## Work performed
- Opened the sample PCAP and reviewed packet list columns including source, destination, protocol, length, info and timestamps.
- Filtered traffic by IP address and inspected Frame, Ethernet II, IPv4 and TCP details.
- Applied source-IP, destination-IP and MAC-address filters.
- Used a UDP port 53 filter to inspect DNS query/response traffic, including a query involving `opensource.google.com`.
- Used a TCP port 80 filter to inspect web traffic and packet/header details.
- Used a TCP content filter to locate packets containing the string `curl`.

## Display filters

```wireshark
ip.addr == 142.250.1.139
ip.src == 142.250.1.139
ip.dst == 142.250.1.139
eth.addr == 42:01:ac:15:e0:02
udp.port == 53
tcp.port == 80
tcp contains "curl"
```

## Filter explanations
- `ip.addr`: matches packets where the specified IPv4 address is source or destination.
- `ip.src` / `ip.dst`: narrows traffic to a source or destination IP.
- `eth.addr`: matches frames containing the specified MAC address.
- `udp.port == 53`: filters UDP traffic on the commonly used DNS port.
- `tcp.port == 80`: filters TCP traffic on the commonly used HTTP port.
- `tcp contains "curl"`: searches TCP packet content for the specified string.

## Skills demonstrated
Wireshark navigation, PCAP inspection, display filters, IPv4/Ethernet/TCP fields, DNS traffic inspection and packet-content filtering.

## Evidence to add
Sanitized screenshots of the packet list, packet-details pane, representative IP/MAC filters and DNS/TCP filters. Only share the training PCAP itself if its terms permit redistribution.

## Scope
A guided exercise using a sample capture, not live enterprise network monitoring or a real incident investigation.
