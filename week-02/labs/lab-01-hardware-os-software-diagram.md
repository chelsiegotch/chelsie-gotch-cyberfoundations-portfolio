# Week 2 Lab — Cybersecurity Landscape & Digital Infrastructure Overview

**Student Name:** Chelsie Gotch

**Date Completed:** 10/4/2026

**Module:** 1 — Digital Infrastructure & CLI | **Week:** 2  
**Submission Path:** `week-02/labs/lab-01-hardware-os-software-diagram.md`

---

## Overview

In this lab, you build a working mental model of the system you'll be securing throughout this course: the hardware, operating system, and software layers that make up every computer, and where the cybersecurity field fits around them. This lab has two parts. Part A connects this week's material to the CyberFoundations City map. Part B has you build and explain a diagram of how a computer's hardware, OS, and software layers interact.

**No terminal or command line is required this week** — that starts in Week 3.

---

## Lab Environment

| Component | Details |
|---|---|
| Environment | Browser-based Lab Portal (Module 1 orientation) |
| Required Materials | CyberFoundations City map; a diagram tool of your choice (hand-drawn and photographed, or any digital tool) |

**Prerequisite:** Portfolio repo created from the CyberFoundations student template in Week 1. This file is already in your repo at `week-02/labs/lab-01-hardware-os-software-diagram.md`, ready to fill in.

**New to the Lab Portal?** Watch this short walkthrough of how to find your Week 2 lab worksheet: [Accessing the Lab Worksheet — Step by Step](PASTE-VIDEO-LINK-HERE) *(~3 min)*.

---

## Part A — CyberFoundations City & the Cybersecurity Landscape

The CyberFoundations City map is your visual guide to the next 11 weeks. Each district represents a module of this course. This part connects this week's material to the map you were introduced to in Week 1.

### Step 1 — Open the Lab Portal Orientation Module

Log into the Lab Portal with your Microsoft account. From your Student Dashboard, open the **Module 1 orientation** module.

### Step 2 — Complete the Orientation Walkthrough

Work through the orientation content. It covers the same hardware/OS/software material as this week's lessons from a different angle — use it to check your understanding, not to replace the lessons.

### Step 3 — Locate This Week's District on the City Map

Open the CyberFoundations City map (introduced in Week 1, Lesson 6). Identify which district corresponds to Module 1 — Digital Infrastructure & CLI.

**District name:** The Foundry District

```
The Foundry District
```

**Why this district fits this week's topics (1–2 sentences):**

```
The Foundry District fits this week because just like a foundry melts down metal to mold basic parts, this module gives us the raw, foundational building blocks of hardware, the operating system, and the command line that shape our core knowledge for everything coming next.
```

---

## Part B — Hardware, OS, and Software Diagram

A computer is a stack of layers: physical hardware at the bottom, an operating system managing that hardware in the middle, and the software you actually use on top. This part has you draw that stack and explain it in your own words.

### Step 1 — Identify the Layers

Before drawing anything, list the three layers you'll diagram and one example of what lives at each layer.

**Hardware layer — one example component:** GPU

```
(e.g., CPU, RAM, storage — your choice)
```

**Operating system layer — name an OS:** Windows 11

```
(e.g., Windows, Linux, macOS)
```

**Software layer — one example application:** WireShark

```
(e.g., a web browser, a word processor)
```

### Step 2 — Sketch Your Diagram

Sketch a simple diagram (hand-drawn and photographed, or built in any digital tool) showing how the hardware, OS, and software layers stack and interact. Arrows or labels showing "what talks to what" matter more than visual polish. If you'd like a free browser-based option instead of hand-drawing, try [draw.io](https://www.drawio.com/) — no account required to get started.

### Step 3 — Upload and Embed Your Diagram

Upload your diagram image directly into your repo's assets folder — keep it there rather than pasting it loose into this file, so all of this week's images stay together and organized.

1. Go to your portfolio repository on GitHub.com and navigate to `assets/screenshots/week-02/`.
2. Click **Add file → Upload files**, then drag in your diagram image, and give it a descriptive name (lowercase, hyphens, no spaces, no timestamps — e.g. `hardware-os-software-diagram.png`).
3. Scroll down and click **Commit changes**.
4. Click on the uploaded image's filename to open it — you'll see the image itself displayed on the page.
5. Right-click directly on the image and choose **Copy image address** (Chrome/Edge) or **Copy Image Link** (Firefox).
6. Come back to this file, open the pencil (edit) icon, and paste that link into the embed line below, in place of the placeholder:

![Hardware/OS/software diagram](https://raw.githubusercontent.com/chelsiegotch/chelsie-gotch-cyberfoundations-portfolio/main/assets/screenshots/week-02/hardware-os-software-diagram.drawio.png)

**If right-click doesn't show that option:** click the small download-arrow icon in the top-right of the image preview instead, then copy the URL from your browser's address bar.

**My Diagram:** Hardware-OS-Software Diagram

### Step 4 — Explain Your Diagram

In your own words — not a copied definition — explain how the three layers interact. Reference your own diagram directly.

```
The diagram I created demonstrates how software, the operating system, and hardware all work together to form a complete process by loading a webpage with Google Chrome. Each layer handles input and output by passing requests down and data back up. First, when a URL is entered into Google Chrome, the software layer cannot touch the hardware directly. Instead, Chrome issues a system call down to the operating system requesting network data.

Next, the operating system intercepts that system call and uses network drivers to send command instructions down to the physical hardware. The network interface card (NIC) then transmits that request over the network.

Finally, once the website data packets arrive back at the machine, the NIC triggers a hardware interrupt up to the CPU and operating system to signal that data is ready. The operating system processes those packets and passes the data response back up to Chrome, allowing the browser to render the finished webpage on the screen.
```

---

## Analysis Questions

Answer each question in your own words. These questions connect what you did in Parts A and B to the bigger picture of this course.

### Analysis Question 1

If the operating system crashed on the computer you diagrammed, which layer(s) would stop working, and which (if any) would keep working? Explain your reasoning.

```
If the operating system stops working, the entire flow in my diagram breaks down because the OS is the middleman that makes everything talk to each other. Apps like Google Chrome freeze or crash immediately. They can’t run on their own because they need the OS to pass their system calls down and grab memory or internet data.

The physical parts like the CPU and network card might still have power running to them, but they just sit there idle. Without the OS and drivers telling them what to do, they can't process any tasks.
```

### Analysis Question 2

Pick one piece of software you use daily. Trace it down through the OS to the hardware it ultimately depends on. What would happen to that software if the hardware layer failed?

```
I use the Spotify Desktop app daily. When I click "Play" on a song, Spotify sends system calls to the operating system. The OS uses device drivers to tell the NIC to stream the audio packets from the internet, then sends that decoded audio data to the sound card and speakers to physically produce the sound.

If the sound card died, the Spotify app might still open and look normal, but it would throw an error like "Can't play the current song" or freeze when trying to output audio.

If core hardware like the RAM, drive, or CPU failed, Spotify wouldn't even be able to load into memory or run its basic processes at all.
```

### Analysis Question 3

Explain, in your own words, why a cybersecurity professional needs to understand all three layers — hardware, OS, and software — rather than just the software layer where most visible attacks (like phishing emails) happen.

```
A cybersecurity professional needs to understand all three layers because an attack rarely stays just where it started.

Software attacks are probably the easiest way into a system, but an attacker's real goal is usually to move past that first layer. Once they get access to an application, they will try to move deeper into the operating system and hardware to gain administrative privileges, hide their activity, and take over the machine.

All three layers carry their own unique risks. A good cybersecurity professional has to know how to protect all three parts, because security is all-or-nothing—if you leave one layer unprotected, the whole system is at risk.
```

---

## Lab Report Questions

Answer each question in complete sentences.

**1. What is the cybersecurity landscape, and why does it matter to someone starting this course?**

```
The city landscape represents what all the cyber districts look like when you zoom out to see the big picture. It is made up of many different parts that act as buildings coming together to form one giant cohesive network.

This matters because having an interconnected network means an attacker can slip in through one weak spot and spread easily across the system. If you do not secure every building in the city landscape, any exposed area becomes a security risk that lets an attacker compromise the rest of the environment.
```

**2. Which CyberFoundations City district did you identify in Part A, and how does its theme connect to the hardware/OS/software material in Part B?**

```
I identified the city district as The Foundry. It connects to Part B because a foundry is where raw materials are melted down and molded into the essential building blocks that make up a city. In the same way, hardware, the operating system, and software are the core building blocks that get shaped and layered together so the computer can function as one complete, working unit.
```

**3. Of the three layers (hardware, OS, software), which one do you think is hardest to secure, and why?**

```
I think the hardest layer to secure is the software layer. Software has the largest attack surface because systems run hundreds of different applications, third-party libraries, and web services, and any single bug in the code can become an open door.

Attackers have a massive variety of tools and entry points here, including social engineering like phishing, memory flaws like buffer overflows, and input attacks like command injection. Because software directly interacts with end users who can make mistakes and developers who write imperfect code, it creates a perfect storm of tactics and vulnerabilities that defenders must constantly patch and monitor.
```

---

## Submission Checklist

- [x] Lab Portal Module 1 orientation completed

- [x] District identified and explained

- [x] Hardware, OS, and software layer examples listed

- [x] Diagram uploaded to `assets/screenshots/week-02/` and embedded using a copied image link (not pasted loose, not a local file path)

- [x] Diagram explanation written in your own words (minimum 3 sentences)

- [x] All three Analysis Questions answered (minimum sentence counts met)

- [x] All three Lab Report Questions answered in complete sentences

- [x] This file is committed to your portfolio repo at `week-02/labs/lab-01-hardware-os-software-diagram.md`
