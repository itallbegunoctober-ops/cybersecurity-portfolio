# Lab 06 — Install Software in a Linux Distribution

**Provider:** Google Skills training activity  
**Category:** Linux Administration  
**Status:** Completed — 5 of 5 tasks reported completed  
**Provider duration/level:** 1 hour / Introductory

## Objective
Practise managing software packages on a Debian-based Linux distribution using APT.

## Tools
Debian-based Linux environment, APT, Nload and tcpdump.

## Work performed
- Confirmed APT was available in the Linux environment.
- Installed Nload.
- Used Nload's help option to verify the command was available.
- Removed Nload and reinstalled it.
- Installed tcpdump.
- Used APT package listing to inspect installed packages.

## Commands

```bash
sudo apt install nload
nload -h
sudo apt remove nload
sudo apt install tcpdump
apt list --installed
```

The lab also included reinstalling Nload after removal.

## Command explanations
- `sudo`: runs a command with elevated privileges.
- `apt install`: installs a package and its dependencies.
- `nload -h`: displays Nload help information.
- `apt remove`: removes a package while generally retaining configuration files.
- `apt list --installed`: lists packages currently installed.

## Skills demonstrated
Linux package management, APT, installing/removing/reinstalling software and verifying package availability.

## Evidence to add
Screenshots of successful installation, help output, removal/reinstallation and installed-package listing.

## Scope
A guided Linux administration exercise. Installing tcpdump in this lab is distinct from the separate tcpdump packet-capture lab.
