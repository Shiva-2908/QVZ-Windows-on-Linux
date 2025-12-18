# QVZ Linux Subsystem for Windows (QVZ-LSW)

> **An independent, low-level systems project exploring how Windows binaries run on Linux**

---

## Overview

**QVZ Linux Subsystem for Windows (QVZ-LSW)** is an **experimental, ground-up systems project** focused on running **Windows PE binaries on Linux** by re-implementing key parts of the Windows execution and loading model.

This project is built for **deep technical understanding**, not for end-user compatibility or production use.

It is **not**:

* ❌ a Wine fork
* ❌ an emulator
* ❌ a virtual machine

Instead, QVZ-LSW studies how Windows programs *actually start and execute*, and reproduces that behavior using native Linux mechanisms.

---

## What I Am Working On

Current development focuses on the **core Windows loader pipeline**, including:

* **PE (Portable Executable) parsing**
* **Image mapping** into Linux process memory
* **Base relocations**
* **MinGW pseudo-relocations**
* Windows **ABI and calling convention behavior**
* Early subsystem design for Windows-style execution

The emphasis is on correctness, clarity, and learning — not speed or feature completeness.

---

## Project Goals

* Understand Windows execution internals at a low level
* Build a minimal Windows-style loader on Linux
* Replicate Windows loader behavior through experimentation
* Keep the codebase small, readable, and educational

---

## Current Status

* ✅ PE header and section parsing
* ✅ Image loading and memory mapping
* ⚠️ Relocation handling (actively being worked on)
* ⛔ Import resolution (planned)
* ⛔ Windows API / syscall layer (future work)

---

## Important Disclaimer

**This project is completely independent.**

QVZ Linux Subsystem for Windows:

* Has **no affiliation** with Microsoft
* Is **not endorsed** by Microsoft or any other company
* Does **not use proprietary Windows source code**
* Is **not related** to Windows Subsystem for Linux (WSL)

This is a **personal research and learning project** developed independently.

All trademarks belong to their respective owners.

---

## Motivation

Most compatibility layers hide the loader behind large abstractions.

This project does the opposite.

QVZ-LSW exists to answer one question:

> *What actually happens when a Windows executable starts running?*

---

## License

This project is released under the **MIT License**.
