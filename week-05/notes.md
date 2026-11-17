# Week 5 Notes — The Grid: Addresses, Names, Ports, and Diagnostics

**Student Name:** Chelsie Gotch

**Date Completed:** 11/17/2026

Summarize this week's key concepts in your own words — not copy-pasted definitions.

## Key Concepts This Week

- IP addresses — the dotted-quad number every device on a network needs (`10.20.5.42` on The Grid)
- The subnet mask — the answer to "which addresses are my neighbours?" (`/24` = `255.255.255.0`)
- The default gateway — the door out of your neighbourhood (`10.20.5.1` on The Grid)
- Private vs public addresses — `10.x`, `172.16–31.x`, and `192.168.x` are *inside* addresses
- DNS — the Grid's Directory Board: a name goes in, an IP address comes out
- NXDOMAIN vs a host that resolves but doesn't answer — two different failures with two different causes
- DHCP — the Address Office: leases, why addresses change, why a laptop "just works" on a new network
- Ports — the numbered doors on a building: 22 SSH, 53 DNS, 80 HTTP, 443 HTTPS, 3389 RDP, 25 SMTP
- TCP vs UDP — a confirmed conversation vs a shout across the room
- The TCP handshake — SYN → SYN-ACK → ACK (packets 7, 8 and 9 in Lab 03)
- The diagnostic toolkit — `ping` (does it answer this test?), `traceroute` (which hops answer?), `dig` (what number is behind that name?). Evidence limits: no ping reply doesn't prove a host is off, and `* * *` means no reply came back, not proof of the exact fault
- **THE LADDER RULE** — check yourself → check your gateway → check the target by NAME → check the target by IP → trace the path. *Work outward, one rung at a time, and let the evidence pick the culprit.*

## My Command Table

You learned the same five jobs twice this week — once in bash, once in PowerShell. Fill the pairs in from memory if you can, and check them afterwards. Type straight into the box below — one job per line, e.g. `show my address: ip addr | ipconfig`. This table is worth keeping.

The bash command and its PowerShell equivalent for each job — show my own address, show my default gateway, test reachability, trace the path, look up a name:

```
show my own address: ip addr | ipconfig
show my default gateway: ip route | ipconfig
test reachability: ping | Test-Connection
trace the path: traceroute | tracert
look up a name: dig | Resolve-DnsName
```

## In My Own Words

Your machine has three numbers: an address, a subnet mask, and a default gateway. Explain what each one is for, the way you'd explain it to someone who has never heard those words.

```
An IP address is like your personal house number on a street so other devices know exactly where to send data (or a package) back to you. The subnet mask is like the street name or neighborhood boundary that helps your computer figure out which devices are right next door on the same local network (neighbors) vs who lives somewhere else. Finally, your default gateway is the front door or exit route out of your neighborhood, meaning any traffic headed outside your local network gets handed off to that router to send out into the wider world.
```

What does DNS actually do? Include the difference between a name that comes back "Name or service not known" (NXDOMAIN) and a name that resolves perfectly well to a host that never answers.

```
DNS works like the phonebook of the internet by translating website names into the actual numerical IP addresses computers use to find each other. When a lookup comes back as "Name or service not known" (NXDOMAIN), it means that particular name isn't listed in the phonebook at all, so your computer doesn't even know what IP address to send traffic to. When a name resolves fine to a host that never answers, the phonebook found the right IP address without any issues, but nobody is answering the door at that address because it maybe turned off, unplugged, or blocking your connection.
```

An IP address gets your traffic to the right building. What does a port number add to that, and why would a defender care how many doors are open?

```
Even though a IP address gets your traffic to the right building, a port number acts like the specific apartment or office door inside that building so the data reaches the exact app or service it needs, like a web server or email. A defender cares a lot about how many doors are open because every open port is another possible entry point where an attacker can poke and prod your network by testing for weak spots or try to break in. Closing any ports you don't actually need shrinks your attack surface and gives intruders way fewer ways to interact with the machine.
```

Write out THE LADDER RULE — all five rungs, in order — and say why running them in that order matters more than running them fast.

```
Check your own interface and IP address (ip addr or ipconfig)

Check your local route and default gateway (ip route or ipconfig)

Ping your default gateway to test your local network connection

Ping an external IP address to test if traffic can actually get out past your router

Test DNS resolution by looking up or pinging a domain name (dig, Resolve-DnsName, or ping by name)
```

What is DHCP, and why does your laptop get an address automatically on a network it has never joined before, while a server like `grid-dns` keeps the same address permanently?

```
DHCP is the automated system on a network that hands out temp. IP addresses, subnet masks, and default gateways to devices as soon as they connect. Your laptop gets an address automatically on a brand new network because portable devices constantly move around from home to public places, so DHCP lends it a temporary lease that expires when you leave that place so that address can be recycled. On the other hand, a server like grid-dns keeps the exact same permanent IP address because other machines and services rely on finding it at that exact same location every single time without having to guess where it moved, as it would cause great chaos for all the clients that rely on always finding that machine at that number. 
```

---

## Submission Checklist

- [x] I summarized each concept in my own words, not copied definitions

- [x] I completed the bash-to-PowerShell command table

- [x] I answered all five "In My Own Words" prompts

- [x] This file is committed to my portfolio repo at `week-05/notes.md`

---

*CyberVisionaries Institute — Cyber Foundations, Tier I*
