# pihole-homelab
Raspberry Pi 4 homelab running Pi-hole for network-wide ad blocking and DNS privacy.

**What this project is:** A network-wide ad-blocking DNS server built with Pi-hole on a Raspberry Pi 4. This repo stores installation steps, configs, helper scripts, and troubleshooting notes — useful as a portfolio piece for system administration and networking.

## Features
- Pi-hole DNS/optional DHCP for local network ad/tracker blocking
- External HDD for persistent logs and backups
- Static IP + documented network configuration
- Optional Unbound recursive DNS for privacy
- Scripts for automated mounting & log backup

## Quick start
1. Flash Raspberry Pi OS (Lite) to your SD card. See `docs/INSTALL.md` for full commands.
2. Boot the Pi, enable SSH, and SSH into it.
3. Run `scripts/setup-pihole.sh` (review before running).
4. Configure your router to use the Pi's IP as DNS.

## Files
See `/configs` for example config files you can adapt.

## License
MIT
