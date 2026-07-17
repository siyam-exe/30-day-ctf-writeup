<h1 align="center">30-Day CTF Writeup Challenge</h1>

<h3 align="center">Expanded into a 32-day CTF writeup series</h3>

<p align="center">
  A public record of my 30 days CTF learning sprint, later expanded into 32 days to finish the final reverse engineering section properly.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/30%20Days-expanded%20to%2032-111827" alt="30 days expanded to 32">
  <img src="https://img.shields.io/badge/Writeups-32-111827" alt="32 writeups">
  <img src="https://img.shields.io/badge/Completed-30-16A34A" alt="30 completed">
  <img src="https://img.shields.io/badge/Placeholders-2-F59E0B" alt="2 placeholders">
  <img src="https://img.shields.io/badge/Images-local-2563EB" alt="local images">
  <img src="https://img.shields.io/badge/Format-Markdown-0F172A" alt="Markdown">
</p>

## Overview

This repository started as my 30-day CTF writeup challenge. The original goal was simple: solve and document one challenge each day for 30 days to build consistency and public technical evidence.

I later expanded it from 30 days to 32 days because the final reverse engineering section felt incomplete if I stopped exactly at Day 30. Instead of ending the series at an arbitrary number, I added two more reversing writeups so the challenge ended with a cleaner progression through GDB, packed binaries, and runtime flag reconstruction.

So the project is still kept under the 30-day CTF writeup idea because that is how the challenge started, and because many people search for 30 days CTF writeup, 30 day CTF challenge, or 30 days cybersecurity challenge. The final version is a 32-day series.

The writeups are written for beginners who want to follow the reasoning, not only copy the final answer. Each completed entry focuses on the path from first clue to final flag, including mistakes, tool usage, and the lesson from the challenge.

## Current Status

| Metric | Count |
|---|---:|
| Total days | 32 |
| Completed writeups | 30 |
| Placeholder writeups | 2 |
| Local image assets | 285 |

Day 17 and Day 19 are placeholders. I will add those writeups after finishing the rooms.

## Categories

| Category | Days | Focus |
|---|---:|---|
| Cryptography | 1 to 7 | Encoding, classical crypto, RSA, CBC, ECB, oracle-style attacks |
| OSINT | 8 to 10 | Username reuse, public clues, social platforms, geolocation, investigation flow |
| Forensics | 11 to 14 | File carving, disk images, packet analysis, hidden data, Sleuth Kit |
| Linux privilege escalation | 15 to 18 | Permissions, sudo abuse, enumeration, shell upgrade, root paths |
| Web exploitation | 20 to 24 | Cookies, SQL injection, uploads, XSS, JWT, browser behavior |
| Binary exploitation | 25 to 29 | Buffer overflow basics, PIE, ROP, ret2win, split |
| Reverse engineering | 30 to 32 | GDB, Ghidra, packing, string reconstruction, runtime analysis |

## Repository Layout

```text
.
|-- README.md
|-- writeups/
|   |-- day-01-introduction-to-cryptohack-writeup.md
|   |-- day-02-picoctf-2019-easy1-writeup.md
|   |-- day-03-ecb-oracle-writeup.md
|   `-- ...
`-- assets/
    |-- day-08-sakura-tryhackme-osint-writeup/
    |-- day-09-kaffeesec-someint-tryhackme-osint-writeup/
    |-- day-10-cache-me-outside-tryhackme-osint-writeup/
    `-- ...
```

All screenshots are stored locally in `assets/`, grouped by writeup. The Markdown files use relative paths, so the repo should render correctly on GitHub without relying on external image hosting.

## Writeup List

| Day | Writeup | Short Description | Status |
|---:|---|---|---|
| 1 | [Introduction to CryptoHack Writeup](writeups/day-01-introduction-to-cryptohack-writeup.md) | Beginner CryptoHack challenges covering basic encodings, XOR, and early crypto warmups. | Complete |
| 2 | [picoCTF 2019 Easy1 Writeup](writeups/day-02-picoctf-2019-easy1-writeup.md) | A Vigenere cipher solve using the provided key and CyberChef-style reasoning. | Complete |
| 3 | [ECB Oracle Writeup](writeups/day-03-ecb-oracle-writeup.md) | A CryptoHack ECB oracle challenge showing why deterministic block encryption leaks structure. | Complete |
| 4 | [Lazy CBC Writeup](writeups/day-04-lazy-cbc-writeup.md) | A CBC challenge where error output and IV misuse lead to key recovery. | Complete |
| 5 | [ALEXCTF CR2: Many Time Secrets Writeup](writeups/day-05-alexctf-cr2-many-time-secrets-writeup.md) | A many-time pad style crypto challenge focused on reused keystream weakness. | Complete |
| 6 | [Mind Your Ps and Qs Writeup](writeups/day-06-mind-your-ps-and-qs-writeup.md) | A picoCTF RSA challenge where weak public parameters make decryption possible. | Complete |
| 7 | [Dancing Queen CTF Writeup](writeups/day-07-dancing-queen-ctf-writeup.md) | A CryptoHack challenge involving stream cipher behavior and careful byte-level recovery. | Complete |
| 8 | [Sakura TryHackMe OSINT Writeup](writeups/day-08-sakura-tryhackme-osint-writeup.md) | An OSINT trail through usernames, GitHub, PGP, crypto wallets, WiFi clues, and travel evidence. | Complete |
| 9 | [KaffeeSec SomeINT TryHackMe OSINT Writeup](writeups/day-09-kaffeesec-someint-tryhackme-osint-writeup.md) | An OSINT investigation using public profiles, Reddit clues, and automated recon tools. | Complete |
| 10 | [Cache Me Outside TryHackMe OSINT Writeup](writeups/day-10-cache-me-outside-tryhackme-osint-writeup.md) | An OSINT room built around public activity, platform clues, and identity correlation. | Complete |
| 11 | [Matryoshka Dolls picoCTF Forensics Writeup](writeups/day-11-matryoshka-dolls-picoctf-forensics-writeup.md) | A nested image forensics challenge where each extracted file reveals the next layer. | Complete |
| 12 | [tunn3l v1s10n picoCTF Forensics Writeup](writeups/day-12-tunn3l-v1s10n-picoctf-forensics-writeup.md) | A broken BMP header challenge where repairing image metadata reveals the real flag. | Complete |
| 13 | [Carnage TryHackMe Network Forensics Writeup](writeups/day-13-carnage-tryhackme-network-forensics-writeup.md) | A Wireshark-focused network forensics investigation through suspicious traffic and artifacts. | Complete |
| 14 | [Sleuthkit Apprentice picoCTF Forensics Writeup](writeups/day-14-sleuthkit-apprentice-picoctf-forensics-writeup.md) | A disk image forensics challenge solved with Sleuth Kit command-line tools. | Complete |
| 15 | [Permissions picoCTF Writeup](writeups/day-15-permissions-picoctf-writeup.md) | A Linux permissions challenge where one sudo rule provides the privilege escalation path. | Complete |
| 16 | [TryHackMe Linux Privilege Escalation Writeup](writeups/day-16-tryhackme-linux-privilege-escalation-writeup.md) | A practical Linux privilege escalation walkthrough covering enumeration and multiple root paths. | Complete |
| 17 | [Linux PrivEsc TryHackMe Writeup](writeups/day-17-linux-privesc-tryhackme-writeup.md) | Placeholder for a future Linux privilege escalation room writeup. | Placeholder |
| 18 | [RootMe TryHackMe Writeup](writeups/day-18-rootme-tryhackme-writeup.md) | A beginner web-to-root room using directory discovery, upload abuse, shell access, and privesc. | Complete |
| 19 | [Wonderland TryHackMe Writeup](writeups/day-19-wonderland-tryhackme-writeup.md) | Placeholder for the future Wonderland TryHackMe writeup. | Placeholder |
| 20 | [Power Cookie picoCTF Web Exploitation Writeup](writeups/day-20-power-cookie-picoctf-web-exploitation-writeup.md) | A web challenge where modifying a trusted browser cookie unlocks access. | Complete |
| 21 | [SQLiLite picoCTF Web Exploitation Writeup](writeups/day-21-sqlilite-picoctf-web-exploitation-writeup.md) | A SQL injection challenge where the login query exposes exactly where to attack. | Complete |
| 22 | [n0s4n1ty 1 picoCTF Web Exploitation Writeup](writeups/day-22-n0s4n1ty-1-picoctf-web-exploitation-writeup.md) | A file upload challenge that turns profile picture handling into command execution. | Complete |
| 23 | [Noted picoCTF Web Exploitation Writeup](writeups/day-23-noted-picoctf-web-exploitation-writeup.md) | A notes app challenge involving XSS behavior, browser state, and report-flow abuse. | Complete |
| 24 | [JaWT Scratchpad picoCTF Web Exploitation Writeup](writeups/day-24-jawt-scratchpad-picoctf-web-exploitation-writeup.md) | A JWT challenge where a weak secret allows token tampering and admin access. | Complete |
| 25 | [buffer overflow 0 picoCTF Binary Exploitation Writeup](writeups/day-25-buffer-overflow-0-picoctf-binary-exploitation-writeup.md) | A first binary exploitation step showing how crashing input can trigger the win condition. | Complete |
| 26 | [picoCTF Buffer Overflow 1 Writeup](writeups/day-26-picoctf-buffer-overflow-1-writeup.md) | A buffer overflow challenge focused on controlling EIP and redirecting execution. | Complete |
| 27 | [PIE TIME picoCTF Binary Exploitation Writeup](writeups/day-27-pie-time-picoctf-binary-exploitation-writeup.md) | A PIE bypass challenge using leaked addresses and offset calculation. | Complete |
| 28 | [ROP Emporium ret2win x86_64 Writeup](writeups/day-28-rop-emporium-ret2win-x86-64-writeup.md) | A beginner ROP Emporium challenge using stack control to call an existing win function. | Complete |
| 29 | [ROP Emporium split x86_64 Writeup](writeups/day-29-rop-emporium-split-x86-64-writeup.md) | A ROP challenge using useful strings and function calls to print the flag. | Complete |
| 30 | [GDB Test Drive picoCTF Reverse Engineering Writeup](writeups/day-30-gdb-test-drive-picoctf-reverse-engineering-writeup.md) | A reversing challenge where GDB helps skip unnecessary execution and reach the flag. | Complete |
| 31 | [Packer picoCTF Reverse Engineering Writeup](writeups/day-31-packer-picoctf-reverse-engineering-writeup.md) | A packed binary challenge where identifying and unpacking UPX reveals the real program. | Complete |
| 32 | [FactCheck picoCTF Reverse Engineering Writeup](writeups/day-32-factcheck-picoctf-reverse-engineering-writeup.md) | A reverse engineering challenge using Ghidra and GDB to catch the flag being built. | Complete |

## What This Repository Shows

- Consistent technical writing across multiple CTF categories.
- Beginner-friendly explanations instead of only final commands.
- Practical tool usage across CyberChef, Wireshark, Sleuth Kit, Burp Suite, GDB, Ghidra, Python, and Linux utilities.
- A public learning trail that connects CTF practice to offensive security fundamentals.

## Notes

- Day 17 and Day 19 are intentionally kept as placeholders to preserve the 32-day sequence.
- Screenshots were converted from my Obsidian notes into GitHub-ready local assets.
- A small amount of payload text may be redacted where needed to keep the exported Markdown friendly to local antivirus scanning.

## Disclaimer

These writeups are for legal CTF practice, education, and personal documentation. Do not use any technique from this repository against systems you do not own or do not have explicit permission to test.
