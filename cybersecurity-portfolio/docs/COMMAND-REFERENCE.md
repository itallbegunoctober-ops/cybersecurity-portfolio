# Command and Filter Reference

This quick reference consolidates commands and filters from the completed training labs. Use them only in systems, files and networks you are authorized to access.

## Linux navigation and files

| Command | Purpose |
|---|---|
| `ls` | List visible files and directories |
| `ls -a` | Include hidden entries |
| `cd ~` | Change to the home directory |
| `cat <file>` | Display file contents |
| `tr "d-za-cD-ZA-C" "a-zA-Z"` | Reverse the Caesar shift used in the lab |

## OpenSSL decryption

```bash
openssl aes-256-cbc -pbkdf2 -a -d -in <encrypted_file> -out <decrypted_file>
```

AES-256-CBC decryption with PBKDF2 and Base64 input handling. Never commit passwords or keys.

## Hashing and comparison

```bash
sha256sum <file>
sha256sum <file> >> <hash_output_file>
cmp <first_file> <second_file>
```

Generate a SHA-256 digest, append output to a file and compare two files byte by byte.

## tcpdump

```bash
ifconfig
tcpdump -D
tcpdump -i eth0 -v -c 5
tcpdump -r capture.pcap
tcpdump -X -r capture.pcap
```

Inspect interfaces, list capture interfaces, capture a limited number of packets, read a saved PCAP and display packet bytes in hex/ASCII.

## Wireshark display filters

| Filter | Purpose |
|---|---|
| `ip.addr == 142.250.1.139` | Source or destination IP |
| `ip.src == 142.250.1.139` | Source IP |
| `ip.dst == 142.250.1.139` | Destination IP |
| `eth.addr == 42:01:ac:15:e0:02` | Source or destination MAC |
| `udp.port == 53` | UDP port 53 / DNS-related traffic |
| `tcp.port == 80` | TCP port 80 / HTTP-related traffic |
| `tcp contains "curl"` | TCP payload/content search for a string |

## Suricata and JSON logs

```bash
cat custom.rules
sudo suricata -r sample.pcap -S custom.rules -k none
cat /var/log/suricata/fast.log
cat /var/log/suricata/eve.json | jq .
```

Inspect custom rules, run offline PCAP analysis, review concise alerts and format structured JSON event data.

## APT package management

```bash
sudo apt install nload
nload -h
sudo apt remove nload
sudo apt install tcpdump
apt list --installed
```

Install, verify, remove and inspect packages on a Debian-based distribution.

## Python concepts

- `sorted(values)`: returns a sorted list.
- `max(values)`: returns the largest value.
- `.append(value)` / `.remove(value)`: add/remove list items.
- `value in collection`: membership test.
- `collection.index(value)`: locate an item's index.
- `with open(path, "r")`: open a file for reading.
- `with open(path, "a")`: open a file for appending.
- `with open(path, "w")`: open a file for writing (overwrites existing content).
- `.read()`, `.split()`, `.write()`: read, split and write text.

Placeholders such as `<file>` must be replaced with the actual paths used in your own environment.
