# Pi-hole Homelab Installation Guide

This document explains how to set up Pi-hole on a Raspberry Pi 4 with a WD Elements external HDD for log storage.

---

## Prerequisites

- Raspberry Pi 4 Model B
- MicroSD card (8 GB or larger)
- MicroSD card reader (USB or built-in)
- WD Elements portable HDD (or similar)
- Internet connection for the Pi
- A computer to flash Raspberry Pi OS Lite onto the SD card

---

## Step 1: Flash Raspberry Pi OS Lite

1. Download **Raspberry Pi Imager** from [https://www.raspberrypi.com/software/](https://www.raspberrypi.com/software/)
2. Insert your SD card into your computer
3. Open Raspberry Pi Imager:
   - **Choose OS:** Raspberry Pi OS Lite (64-bit)
   - **Choose Storage:** your SD card
   - **Advanced Options (gear icon):**
     - Set hostname: `pihole`
     - Enable SSH
     - Set username & password
     - Configure Wi-Fi (optional)
     - Set locale/timezone
4. Click **Write** and wait for completion
5. Safely eject the SD card

> **Note:** If you don’t have an SD card reader yet, skip to Step 2 and prepare scripts and configs.

---

## Step 2: Boot Raspberry Pi

1. Insert the flashed SD card into the Pi
2. Connect Pi to network (Ethernet recommended) and power
3. Find Pi IP address:
   - On router device list
   - Or use `ping pihole.local` if mDNS is enabled

---

## Step 3: SSH into Pi

```bash
ssh pi@<pi-ip-address>
# default username/password from imaging step
