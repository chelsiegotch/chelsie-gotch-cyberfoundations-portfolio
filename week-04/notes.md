# Week 4 Notes — Permissions, Searching, and Virtual Machines

**Student Name:** Chelsie Gotch

**Date Completed:** 11/04/2026

Summarize this week's key concepts in your own words — not copy-pasted definitions.

## Key Concepts This Week

- File permissions: read/write/execute × owner/group/other, and reading `ls -l`
- Changing permissions with `chmod` (symbolic and numeric) — and THE GATEKEEPER'S RULE
- Windows ACLs, read with `Get-Acl` (the real-world `icacls` tool does the same job, but is not available in the simulator)
- Wildcards (`*`, `?`, `[ ]`) and searching inside files with `grep`/`Select-String`
- Virtual machines: host vs. guest, the hypervisor, Type 1 vs. Type 2, isolation
- The VM lifecycle: create, start, stop (deallocate), snapshot, delete — and what each costs
- Golden snapshots — how your Weeks 6–12 lab machines are made

## In My Own Words

**Decode `-rw-r-----` audience by audience: who can do what to this file?**

```
The Owner (rw-): The person who created or owns the file has both read and write access. They can open it, view the file and make edits or save changes. They don't have execute permissions, so they can't run it as a program.
The Group (r--): Anyone belonging to the file's assigned group only has read access. They can view and read the file's contents, but they are blocked from modifying, writing, or executing it.
Others  (---): All others who are aren't the owner or part of the group have no access. They can't read it, write to it, or execute it. The file is completely locked down to anyone outside.
```

**What is a hypervisor, and what are its two jobs?**

```
A hypervisor is the software layer that lets you run multiple virtual computers on a single physical machine. Instead of buying separate computers for every OS, the hypervisor sits on the physical hardware and lets them all share it safely.

It handles two jobs:
Sharing the physical hardware. Keeping the machines separated. 
```

**A stopped VM still costs a little money. What is it paying for, and what's the only way to reach a true zero?**

```
When a VM is stopped or powered down, compute charges drop to zero because the processors aren't executing instructions for it.
It's paying for persistent storage and reserved network resources. 
The only way to stop all ongoing costs is to completely terminate or delete the VM and delete its attached storage disks.
```

---

## Submission Checklist

- [x] I summarized each concept in my own words, not copied definitions

- [x] I answered all three "In My Own Words" prompts

- [x] This file is committed to my portfolio repo at `week-04/notes.md`
