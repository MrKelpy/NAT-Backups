# 🗄️ NAS Integration with ESP32-S3  
**Cold-Storage Backup Automation with USB-C OTG**

Automated cold-storage data backup between a NAS and a USB external hard drive using the ESP32-S3 microcontroller. Fully offline, backups on-demand with the press of a button.

---

## 📦 Overview

This project enables seamless, automated file backups from a **NAS** to a **USB-C external hard drive**, leveraging the **ESP32-S3**'s dual USB capabilities.

- 💻 No need for additional computers or scripts.
- 🔌 Runs directly from USB-C power.
- 🔒 Preserves existing backups (never deletes).
- 🧊 Optional active cooling with 3D printed case.

---

## 🔧 Hardware Architecture

```text
+------------------------+
|       NAS (Ubuntu)     |
|  - Shared Folder (SMB) |
+-----------+------------+
            | USB (mass storage mode)
            ▼
+------------------------+
|      ESP32-S3          |
|  - Parses spec file    |
|  - USB OTG to HDD      |
+-----------+------------+
            | USB-C OTG
            ▼
+------------------------+
|  External HDD (1TB)    |
+------------------------+
