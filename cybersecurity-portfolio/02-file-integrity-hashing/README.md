# Lab 02 — Create Hash Values

**Provider:** Google Skills training activity  
**Category:** Cryptography / File Integrity  
**Status:** Completed  
**Provider duration/level:** 1 hour / Introductory

## Objective
Generate SHA-256 digests for files and compare saved hash outputs to understand how hashes can support file-integrity checking.

## Tools
Linux shell, `ls`, `cat`, `sha256sum`, shell output redirection and `cmp`.

## Work performed
- Listed and inspected `file1.txt` and `file2.txt`.
- Generated SHA-256 hashes for both files.
- Appended hash command output to `file1hash` and `file2hash`.
- Viewed the saved outputs and compared them with `cmp`.
- Observed that the files appeared similar when printed but produced different hash values, indicating their contents were not identical.

## Commands

```bash
ls
cat file1.txt
cat file2.txt
sha256sum file1.txt
sha256sum file2.txt
sha256sum file1.txt >> file1hash
sha256sum file2.txt >> file2hash
cat file1hash
cat file2hash
cmp file1hash file2hash
```

## Command explanations
- `sha256sum`: calculates a SHA-256 digest for a file.
- `>>`: appends standard output to a file, creating it if needed.
- `cmp`: compares two files byte by byte.
- `cat`: displays file contents.

## Skills demonstrated
SHA-256 hashing, Linux command-line use, output redirection, file comparison and basic integrity verification.

## Key learning
A cryptographic hash can reveal that two files differ even when their contents look similar during casual inspection. A hash alone does not prove the identity or trustworthiness of a file; comparison requires a trusted reference value.

## Evidence to add
Screenshots showing the hash commands, saved outputs and `cmp` result. Do not upload sensitive source files.
