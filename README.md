# ADOBECLEANUPUTILITY
A lightweight Windows Batch utility to safely uninstall Adobe Genuine Service and dynamically block/unblock internet connections for Adobe Creative Cloud applications using Windows Firewall.

# Adobe Utility: Cleanup & Firewall Manager

A standalone Windows Batch script designed to remove the **Adobe Genuine Service (AGS)** and manage Windows Defender Firewall rules for Adobe applications. 

It dynamically scans your system directories to apply inbound and outbound firewall block rules, preventing background licensing checks while preserving core offline application features.

---

## Features

- **Interactive Menu:** Run individual tasks or perform a full cleanup in one click.
- **Adobe Genuine Service Removal:** Stops background processes (`AGSService.exe`, `AdobeGCClient.exe`, `AdobeGenuineValidator.exe`) and uninstalls AGS via official cleanup utilities, `winget`, and `wmic`.
- **Dynamic Application Scanning:** Automatically searches `Program Files` and `Common Files` for installed Adobe `.exe` binaries—no hardcoded file paths needed.
- **Bi-Directional Blocking:** Creates both Inbound and Outbound block rules for every detected Adobe executable.
- **Complete Revert/Unblock Option:** Instantly scans and removes all script-generated firewall rules to restore default internet access.
- **Safety Checks:** Requires Administrator privileges and prompts for user confirmation before executing changes.

---

## Interactive Menu Overview

```text
========================================================
        ADOBE UTILITY: CLEANUP & FIREWALL MANAGER
========================================================

 [1] Uninstall Adobe Genuine Service ONLY
 [2] Apply Firewall Connection Blocks ONLY
 [3] Run BOTH (Uninstall AGS & Apply Firewall Blocks)
 [4] UNBLOCK / REVERT All Adobe Firewall Rules
 [5] Exit
========================================================
