# GymFlow Pro

## Overview

**Type:** Desktop Fitness Management Application  
**Status:** Completed  
**GitHub:** https://github.com/pan-k15/gymflow-pro

GymFlow Pro is a desktop fitness management system for BK Sports Complex. It manages gym members, check-ins, training sessions, trainers, and ID card printing from a single customtkinter application. The app connects to Firebase Firestore for cloud-backed data and can also run with local mock data when Firebase credentials are not available.

## Details

| Field | Information |
| --- | --- |
| Project name | GymFlow Pro |
| Project type | Desktop Fitness Management App |
| Main technology | Python, customtkinter, Firebase Firestore, Pillow, qrcode, openpyxl |
| Hardware support | USB QR scanner, serial scanner, IDP CUBO3 card printer |
| Platform | Windows, macOS, Linux |
| Repository | https://github.com/pan-k15/gymflow-pro |

## Description

This project is a modern desktop application for managing fitness center operations. It provides member management, QR/manual check-in, check-in records, training package tracking, trainer management, and membership card printing in one interface.

GymFlow Pro is designed to work with Firebase Firestore for shared cloud data, but it includes a mock-data fallback so the app can be developed, tested, and demonstrated without live Firebase credentials. This makes it useful both as a production-style gym management app and as a polished desktop application example.

## Images

Recommended screenshots to add:

- `./images/dashboard.png` - GymFlow Pro dashboard
- `./images/members.png` - Member management page
- `./images/check-in.png` - QR/manual check-in page
- `./images/records.png` - Check-in records and export page
- `./images/training.png` - Training session management page
- `./images/card-print.png` - ID card preview and print page

## Features

- Dashboard with member, check-in, expiry, and training session stats
- Add, edit, delete, search, and filter members
- Auto-generated member IDs in `MEM00001` format
- Member photo upload stored as base64 in Firestore
- Membership plans with automatic expiry and live status tracking
- QR code check-in using USB keyboard-wedge scanner
- Manual member ID check-in fallback
- Today's check-in log with method tracking
- Date range filters and quick presets for check-in records
- Export check-in records to CSV and Excel
- Assign training packages to members
- FIFO session deduction from oldest active package
- Trainer management with active/inactive status
- IDP CUBO3 CR-80 card printing workflow
- Live card preview and save-card-as-PNG support
- Firebase Firestore data layer with mock fallback

## Pages And Modules

| File / Folder | Purpose |
| --- | --- |
| `main.py` | App entry point, sidebar shell, dashboard, and navigation |
| `firebase_db.py` | Firebase Firestore data layer with mock fallback |
| `theme.py` | Shared colors, fonts, and reusable UI widgets |
| `pages/members.py` | Member CRUD, photo upload, and membership extension |
| `pages/checkin.py` | QR/manual check-in and live result card |
| `pages/records.py` | Check-in history, filters, CSV and Excel export |
| `pages/training.py` | Training packages, FIFO deduction, and session logs |
| `pages/trainers.py` | Trainer management |
| `pages/card_print.py` | CUBO3 card generation, preview, and printing |
| `hardware/scanner.py` | USB-HID and serial QR scanner integration |
| `hardware/cubo3.py` | IDP CUBO3 printer integration |

## Data And Hardware

| Area | Description |
| --- | --- |
| Database | Firebase Firestore with optional mock data fallback |
| Member photos | Stored as base64 data |
| QR scanner | USB-HID keyboard-wedge scanner or serial scanner |
| Card printer | IDP CUBO3 CR-80 PVC card printer |
| Card output | Member name, member ID, QR code, plan, and expiry date |
| Exports | CSV and Excel records |

## Links

- **GitHub:** https://github.com/pan-k15/gymflow-pro
- **customtkinter:** https://github.com/TomSchimansky/CustomTkinter
- **Firebase Firestore:** https://firebase.google.com/docs/firestore
- **Pillow:** https://python-pillow.org/
- **qrcode:** https://github.com/lincolnloop/python-qrcode
- **openpyxl:** https://openpyxl.readthedocs.io/

## Notes

The app can run immediately with mock data by starting `python main.py`. For live data, a Firebase service account file named `serviceAccountKey.json` is placed in the project root. The file is intentionally ignored by Git so credentials are not committed.
