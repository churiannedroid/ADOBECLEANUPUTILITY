# Adobe Utility: Cleanup & Firewall Manager

![Repository Preview](repo.png)

A standalone Windows Batch script designed to remove the **Adobe Genuine Service (AGS)** and manage Windows Defender Firewall rules for Adobe applications. 

It dynamically scans your system directories to apply inbound and outbound firewall block rules, preventing background licensing checks while preserving core offline application features.

---

> ### ⚠️ Disclaimer & Important Notice
> **Use this script at your own risk.** Modifying firewall configurations and removing software services can alter how installed applications function.
> 
> **Impact on Online Features:**
> Applying firewall connection blocks will completely isolate your Adobe applications from the internet. As a result, **all network-dependent features will be disabled**, including:
> - Creative Cloud Cloud Sync & Storage
> - Adobe Stock & Typekit / Adobe Fonts
> - Neural Filters & Cloud-based Rendering
> - Firefly AI Generative Tools
> - Online License Verification & In-App Asset Store

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
