# CSARCH2-Virtual-Exhibit-Group4-S04

# A Deep Dive Into the Bus System

---

## Overview

Modern computer systems contain multiple components that need access to a common communication channel called the **system bus**. The CPU, memory controller, DMA controller, storage devices, and peripherals may all attempt to use the bus simultaneously. Without a mechanism to control access, data collisions and system instability would occur.

This project is an **interactive virtual exhibit** that explains and simulates how **bus arbitration** works, the mechanism that decides which device gets control of the bus when multiple devices request access at the same time.


---

## The Simulator

The centerpiece of this exhibit is an **interactive bus arbitration simulator** with three devices:

- **CPU**
- **DMA Controller**
- **Disk I/O**

### Features
- Select an arbitration mode (Fixed Priority, Round-Robin, or Daisy Chain)
- Click **"Request Bus"** on any device to queue it
- Watch the arbiter decide who gets the bus in real time
- Visual feedback:
  - **Yellow** — device is requesting
  - **Green** — device is granted the bus (pulse travels along the bus)
  - **Red** — device is denied and queued
- A **transaction log** records every cycle's events (e.g., `Cycle 6: Arbiter granted bus to CPU (fixed priority)`)

---

## Getting Started

> **Prerequisites:** Node.js 26+

```bash
# Clone the repository
git clone https://github.com/<your-repo>/bus-arbitration-exhibit.git
cd bus-arbitration-exhibit

# Install dependencies
npm install

# Start the development server
npm run dev
```

Then open your browser at `http://localhost:4321`.

```bash
# Build for production
npm run build

# Preview the production build
npm run preview
```

---

*CSARCH2 Group 4 Project — Bus Arbitration Virtual Exhibit*
