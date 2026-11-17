# Lab 04 — Capture Your First Packet with tcpdump

**Provider:** Google Skills training activity  
**Category:** Network Traffic Capture  
**Status:** Completed — 4 of 4 tasks reported completed

## Objective
Use tcpdump to identify network interfaces, capture packets, apply capture filters, save packet data to a PCAP file and inspect captured traffic.

## Tools
Linux command line, `ifconfig`, `tcpdump`.

## Work performed
- Inspected network interface configuration.
- Listed interfaces available for packet capture.
- Captured a limited number of packets on `eth0` with verbose output.
- Captured traffic associated with port 80.
- Saved captured packets to `capture.pcap`.
- Read the saved capture back with tcpdump.
- Used hexadecimal/ASCII output to inspect packet contents.
- Observed TCP connection setup (SYN, SYN-ACK, ACK), an HTTP GET request to `opensource.google.com`, a 301 redirect toward HTTPS, connection teardown (FIN) and DNS reverse-lookup activity.

## Commands

```bash
ifconfig
tcpdump -D
tcpdump -i eth0 -v -c 5
```

The exercise also used a port-80 capture and saved it to `capture.pcap`. Common command patterns for the documented readback and packet-content inspection were:

```bash
tcpdump -r capture.pcap
tcpdump -X -r capture.pcap
```

## Command explanations
- `ifconfig`: displays network-interface configuration (availability depends on the system).
- `tcpdump -D`: lists interfaces available to tcpdump.
- `-i eth0`: selects interface `eth0`.
- `-v`: enables verbose packet output.
- `-c 5`: stops after capturing five packets.
- `-r capture.pcap`: reads packets from a saved capture file instead of capturing live traffic.
- `-X`: displays packet contents in hexadecimal and ASCII.

## Skills demonstrated
Interface inspection, packet capture, capture filtering, PCAP creation/readback, verbose output and introductory TCP/HTTP/DNS traffic interpretation.

## Evidence to add
Screenshots of interface listing, capture command, saved PCAP readback and packet output. Do not upload captures containing private or unauthorized traffic.

## Scope and safety
This was a guided lab. Capture traffic only on systems and networks where you have explicit authorization.
