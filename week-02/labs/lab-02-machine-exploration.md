# Week 2 Lab — Explore Your Own Machine (Real Specs & Live Activity)

**Student Name:** Chelsie Gotch

**Date Completed:** 10/4/2026

**Module:** 1 — Digital Infrastructure & CLI | **Week:** 2  
**Submission Path:** `week-02/labs/lab-02-machine-exploration.md`

---

## Overview

Lab 01 got you diagramming how hardware, OS, and software interact — in theory. This lab makes it real, in one sitting. First, you'll look up your own machine's actual specs (OS version, RAM, storage) using its built-in settings screens. Then you'll open Task Manager (Windows) or Activity Monitor (Mac) and watch those same hardware and software layers working together live — CPU usage, memory usage, and real running processes — and connect what you see back to your Lab 01 diagram.

**No terminal or command line is required this week** — that starts in Week 3. Settings screens, Task Manager, and Activity Monitor are all point-and-click tools.

---

## Lab Environment

| Component | Details |
|---|---|
| Environment | Your own computer (Windows or Mac) — no VM, no cloud, no install needed |
| Required Materials | Your computer's built-in Settings/About screen; Task Manager (Windows: `Ctrl+Shift+Esc`) or Activity Monitor (Mac: `Cmd+Space`, then type "Activity Monitor") |

**Prerequisite:** Lab 01 completed — you'll reference your diagram in this lab's Analysis Questions.

---

## Part A — Find Your Real Specs

**Before you start:** here's what to expect so you don't second-guess yourself. On Windows, you're looking for a page titled **About**, reached via **Settings → System → About**, listing your device specs under "Device specifications." On Mac, you're looking for a window titled **About This Mac** (click the Apple menu, top-left corner), with an Overview tab listing your chip, memory, and macOS version. If what's on your screen doesn't roughly match that, you're in the wrong menu — try again before recording anything below.

### Step 1 — Find Your OS Version

Open your computer's system settings (Windows: **Settings → System → About**. Mac: **Apple menu → About This Mac**) and find the exact operating system name and version you're running.

**OS and version:** Windows 11 Home version 26H2

```
(e.g., "Windows 11, version 23H2" or "macOS Sonoma 14.4")
```

### Step 2 — Check Your Installed RAM

On the same settings screen, find how much RAM (memory) is installed on your computer.

**Installed RAM:** 16 GB

```
(your answer here)
```

### Step 3 — Check Your Available Storage

Find your computer's total storage capacity and how much is currently free (Windows: **Settings → System → Storage**. Mac: **About This Mac → Storage**).

**Total storage:** 477 GB

```
(your answer here)
```

**Free storage:** 429 GB

```
(your answer here)
```

---

## Part B — Watch It Live

Your Part A numbers are a snapshot. This part shows those same layers actually working, moment to moment.

### Step 1 — Open Task Manager or Activity Monitor

Windows: press `Ctrl+Shift+Esc`. Mac: press `Cmd+Space`, type "Activity Monitor," and press Enter.

### Step 2 — Find the Performance / CPU Tab

Windows: click the **Performance** tab. Mac: click the **CPU** tab.

### Step 3 — Freeze the List Before You Read It

The process list updates constantly and can be hard to read while it's jumping around. Before recording anything, click the **Name** column header (or **Memory**, if you'd rather sort by what's using the most RAM) to sort the list — this won't stop it from updating, but it keeps things from reordering under you while you read.

### Step 4 — Record CPU Usage

Look at the current CPU usage percentage.

```
Current CPU usage: ____%
```

### Step 5 — Record Memory Usage

Find how much RAM is currently in use, out of your total installed RAM (the same total you looked up in Part A).

```
RAM in use: ____   out of total: ____
```

### Step 6 — List Five Running Processes

List five processes running right now. For each, write your best guess at what it is or does — you don't need to be 100% correct, just reason it out. If you spot something on the cheat sheet below, you can use that, but try at least a couple you don't recognize.

**Cheat sheet — common processes you'll likely see (not exhaustive, just a starting reference):** 5 Running Processes  Google Chrome: A basic desktop web browser. Settings: Where you can find general computer settings. Dell Support Assist: An app used to help me with my PC issues Sticky Notes:  An app for writing quick saved memos on desktop  Task Manager: An app to keep stats on the computers performance

| Process Name | Usually Seen On | What It Generally Is |
|---|---|---|
| explorer.exe | Windows | The Windows desktop and file browser itself — normal, always running |
| svchost.exe | Windows | A generic host for background Windows services — several running at once is normal |
| Antimalware Service Executable | Windows | Windows Defender scanning files in the background — normal |
| dwm.exe | Windows | Desktop Window Manager — handles visual effects like transparency and window animations |
| System Idle Process | Windows | Not a real program — represents how much CPU is doing *nothing* right now |
| WindowServer | Mac | Manages everything drawn on your screen — always running |
| Finder | Mac | The Mac desktop and file browser itself — normal, always running |
| mdworker / mds | Mac | Spotlight's background indexing service — normal, can spike briefly after installing apps |
| launchd | Mac | The very first process Mac starts — manages and launches other background services |

```
1. Process name: __________   What I think it does: __________
2. Process name: __________   What I think it does: __________
3. Process name: __________   What I think it does: __________
4. Process name: __________   What I think it does: __________
5. Process name: __________   What I think it does: __________
```

### Step 7 — Screenshot and Embed

Take a screenshot of Task Manager or Activity Monitor showing your CPU/memory usage and process list.

1. Go to your portfolio repository on GitHub.com and navigate to `assets/screenshots/week-02/`.
2. Click **Add file → Upload files**, then drag in your screenshot, and give it a descriptive name (lowercase, hyphens, no spaces — e.g. `machine-exploration.png`).
3. Scroll down and click **Commit changes**.
4. Click on the uploaded image's filename to open it — you'll see the image itself displayed on the page.
5. Right-click directly on the image and choose **Copy image address** (Chrome/Edge) or **Copy Image Link** (Firefox).
6. Come back to this file, open the pencil (edit) icon, and paste that link into the embed line below, in place of the placeholder:

![Task Manager / Activity Monitor screenshot](https://raw.githubusercontent.com/chelsiegotch/chelsie-gotch-cyberfoundations-portfolio/refs/heads/main/assets/screenshots/week-02/machine-exploration.png)

**If right-click doesn't show that option:** click the small download-arrow icon in the top-right of the image preview instead, then copy the URL from your browser's address bar.

**My Screenshot:** This screenshot is showing the Top 5 Labor intensive processes running on my computer tonight.

### Step 8 — Connect the Numbers

In your own words, explain how the real numbers you found in Part A (OS version, RAM, storage) relate to what you just watched live in Part B. Which number describes hardware, and which describes the OS?

```
How Part A Relates to Part B:
The numbers in Part A represent the computer's physical capacity, while Part B shows the operating system managing those physical resources in real time.

The machine has 16 GB of physical RAM (hardware), and during Part B, Windows (the OS) was actively using about 10 GB to run open programs and background services. The machine also has a 477 GB hard drive (hardware), and Windows showed 429 GB of free space, which represents the remaining unused capacity after storing system files and installed applications.

Part A defined the physical limits of the system, and Part B showed the OS actively coordinating work within those limits.
```

---

## Analysis Questions

### Analysis Question 1

Pick one process from your list in Part B, Step 6. Is it "software" in the sense Lab 01 used that word? Explain how it depends on the OS and on hardware to actually run.

```
The process I picked from my list in Part B is Dell SupportAssist.

It counts as software because it is an installed application made of code that runs on the computer, rather than a physical part of the machine. It cannot talk directly to the hardware on its own.

It depends on the OS (Windows) to act as the middleman. SupportAssist has to send requests to Windows to get permission to run scans, check for driver updates, and look through system files.

It depends on the hardware because it needs physical computer parts to actually do its job. The CPU runs its code, the RAM holds it in active memory while it is open, the hard drive stores its files, and it needs physical parts like the network card or hard drive to run its diagnostic tests.
```

### Analysis Question 2

Your CPU usage number changes constantly, even when you're not doing anything. Explain, in your own words, why watching this number matters for security work — not just for performance. (Hint: think about what it might mean if a process you don't recognize suddenly spikes CPU usage.)

```
Every computer has a normal CPU baseline when it is sitting idle. Watching this number matters for security, not just performance, because an unexpected spike can be an immediate sign of unauthorized activity.

If my computer is idling and the CPU suddenly jumps to 90% or 100%, an attacker or malicious code could be running in the background. For example, malware might be encrypting files for ransomware, running unauthorized crypto-mining scripts, or scanning the network. By watching CPU usage in Task Manager, a security analyst can spot an unrecognized process eating up resources, investigate where it came from, and kill it before the attacker expands their reach across the system
```

### Analysis Question 3

Compare what you saw in Task Manager/Activity Monitor to the diagram you built in Lab 01. What's the same? What did watching your machine live show you that a static diagram couldn't?

```
What Is the Same:
The same architecture from my Lab 01 diagram is visible in Task Manager. The five main processes I tracked on my diagram are still the main software applications running in user space, and they still rely on the operating system to access physical resources like CPU and RAM. Just like the diagram showed, the software isn't running on its own—the OS is actively sitting in the middle, managing those processes and reporting their resource usage.

What Watching Live Showed That a Static Diagram Couldn't:
A static diagram makes the computer look fixed and still, but watching the machine live in Task Manager showed just how fast system resources change from second to second. I saw that even when I'm not actively doing anything, background tasks and CPU numbers constantly jump around as the OS schedules work.

It also revealed the real impact of everyday software. For example, something as routine as running Google Chrome can quickly eat up CPU and memory because having multiple tabs open spawns several separate processes in the background. The static diagram showed that Chrome talks to the OS and hardware, but the live monitor actually demonstrated how heavy and fast that resource competition is in real time.
```

---

## Submission Checklist

- [x] OS version, installed RAM, and total/free storage looked up and recorded (Part A)

- [x] Task Manager or Activity Monitor opened and list sorted before recording (Part B)

- [x] Current CPU usage recorded

- [x] Current RAM usage recorded, alongside total RAM from Part A

- [x] Five running processes listed, each with a reasoned guess at what it does

- [x] Screenshot uploaded to `assets/screenshots/week-02/` and embedded using a copied image link

- [x] Connection explanation written (Part B, Step 8 — minimum 2 sentences)

- [x] All three Analysis Questions answered (minimum sentence counts met)

- [x] This file is committed to your portfolio repo at `week-02/labs/lab-02-machine-exploration.md`

---

*CyberVisionaries Institute · Cyber Foundations · Tier I*
