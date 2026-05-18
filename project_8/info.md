# BK Sports Complex — Gym Member Management System

## Overview

**Type:** Desktop Management Application  
**Status:** Completed  
**GitHub:** https://github.com/pan-k15/gym_manager

BK Sports Complex Gym Member Management System is an offline desktop application for managing gym members, check-ins, training sessions, exports, and membership card printing. It is built with Python and Tkinter and stores data locally with SQLite.

## Details

| Field | Information |
| --- | --- |
| Project name | BK Sports Complex — Gym Member Management System |
| Project type | Desktop Gym Management App |
| Main technology | Python, Tkinter, SQLite, Pillow, qrcode, openpyxl |
| Optional hardware | QR scanner, RFID reader, IDP CUBO3 card printer |
| Platform | Windows, macOS, Linux |
| Repository | https://github.com/pan-k15/gym_manager |

## Description

This project is a full-featured desktop system for running gym membership operations without requiring a web server, internet connection, or cloud account. The app manages member profiles, membership plans, expiry status, check-ins, training packages, trainer records, and export workflows.

The system is designed for real gym front-desk use. Staff can add and edit members, enroll RFID cards, scan QR codes, track daily check-ins, manage trainer sessions, export reports, and generate membership cards for printing.

## Images

Recommended screenshots to add:

- `./images/members-list.png` - Member management table
- `./images/check-in.png` - QR/RFID/manual check-in screen
- `./images/training-sessions.png` - Training package management
- `./images/card-preview.png` - Membership card print preview
- `./images/export-records.png` - Check-in or member export screen

## Features

- Add, edit, search, filter, and delete gym members
- Custom member IDs such as `MEM00001` or `VIP-001`
- Member photo upload stored directly in the database
- RFID card enrollment for physical member cards
- Membership plans with automatic expiry calculation
- Status tracking for Active, Expiring Soon, and Expired members
- QR code, RFID, and manual check-in methods
- Today's check-in log with method tracking
- Date-range filtering for check-in records
- Export records to CSV and Excel
- Trainer management with Active and Inactive status
- Training package assignment and session deduction
- Full training session history with audit logs
- Membership card generation and preview
- IDP CUBO3 card printer support

## Modules And Data

| Area | Description |
| --- | --- |
| Member management | Stores member profile, contact details, plan, status, photo, and RFID UID |
| Check-ins | Records check-in time and method: QR, RFID, or manual |
| Training packages | Tracks assigned trainer sessions and remaining session counts |
| Session logs | Stores add/deduct history for training sessions |
| Card printing | Generates CR80 membership cards with QR code and member details |
| Export | Outputs member and check-in data to CSV or Excel |

## Database

The app uses a local SQLite database named `gym_members.db`. The database is created automatically on first launch and contains tables for:

- `members`
- `checkins`
- `trainers`
- `training_packages`
- `session_logs`

## Links

- **GitHub:** https://github.com/pan-k15/gym_manager
- **Python:** https://www.python.org/
- **Tkinter:** https://docs.python.org/3/library/tkinter.html
- **SQLite:** https://www.sqlite.org/
- **Pillow:** https://python-pillow.org/
- **openpyxl:** https://openpyxl.readthedocs.io/

## Notes

The app is designed to run offline on Windows, macOS, and Linux. QR and RFID scanners can work as keyboard-wedge devices, so they do not require special drivers. For direct card printing on Windows, `pywin32` can be installed as an optional dependency.
