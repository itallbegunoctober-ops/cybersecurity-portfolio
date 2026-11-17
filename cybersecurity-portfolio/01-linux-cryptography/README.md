# Lab 01 — Decrypt an Encrypted Message

**Provider:** Google Skills training activity  
**Category:** Linux / Cryptography  
**Status:** Completed  
**Provider duration/level:** 1 hour / Introductory

## Objective
Use Linux Bash to inspect files, locate a hidden file, decode a Caesar-shifted message and decrypt an AES-256-CBC encrypted file with OpenSSL.

## Tools
Linux Bash, `ls`, `cd`, `cat`, `tr`, OpenSSL.

## Work performed
- Navigated directories and inspected files from the terminal.
- Used `ls -a` to reveal the hidden file `.leftShift3`.
- Applied a character translation to decode a Caesar-shifted message.
- Used OpenSSL to decrypt `Q1.encrypted` into `Q1.recovered`, using AES-256-CBC, PBKDF2 and the lab-provided password.
- Read the recovered message.

## Commands

```bash
ls
cd ~
ls -a
cat .leftShift3
cat .leftShift3 | tr "d-za-cD-ZA-C" "a-zA-Z"
```

```bash
openssl aes-256-cbc -pbkdf2 -a -d -in Q1.encrypted -out Q1.recovered
```

The training command used a lab-provided password. Do not publish passwords or secret material in this repository. OpenSSL prompts for a password when one is not supplied as an option.

## Command explanations
- `ls`: lists visible files and directories.
- `cd ~`: changes to the user's home directory.
- `ls -a`: includes hidden files.
- `cat`: prints file contents.
- `tr`: translates characters; the mapping above reverses the Caesar shift used in the exercise.
- `openssl aes-256-cbc`: invokes AES-256-CBC decryption; `-d` selects decryption, `-a` handles Base64-encoded input, and `-pbkdf2` enables PBKDF2 key derivation.

## Skills demonstrated
Linux navigation, hidden-file discovery, text transformation, OpenSSL, AES-256-CBC, PBKDF2 and basic cryptographic data recovery.

## Evidence to add
Sanitized screenshots of the hidden-file listing, decoding command and successful decryption. Hide passwords and any sensitive recovered content.

## Scope
A guided training lab, not a production cryptography engagement.
