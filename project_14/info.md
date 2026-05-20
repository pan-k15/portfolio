# Dogcare Management App

## Overview

**Type:** Web Management Application  
**Status:** In Progress  
**GitHub:** https://github.com/pan-k15/dogcare-management-app

Dogcare Management App is a Vue.js web application for managing a dogcare facility with multiple services, including dog run, cafe, wash and dry, grooming and bath, and a dog snack shop.

## Details

| Field | Information |
| --- | --- |
| Project name | Dogcare Management App |
| Project type | Web Management Application |
| Main technology | Vue 3, Vite, Vue Router, TailwindCSS, FullCalendar |
| Optional backend | Firebase, Supabase, or Node.js/Express |
| State management | Pinia planned / optional |
| Repository | https://github.com/pan-k15/dogcare-management-app |

## Description

This project is designed as an internal management system for dogcare operations. It provides the structure for service booking, scheduling, member management, service operation pages, inventory tracking, reporting, staff roles, and settings.

The app uses Vue Router to organize the system into separate pages for login, dashboard, bookings, booking form, calendar, members, wash and dry, grooming, dog run and cafe, inventory, reports, logs, profile, staff roles, and settings. It can be extended with Firebase, Supabase, or a Node.js backend for real data storage and authentication.

## Images

Recommended screenshots to add:

- `./images/login.png` - Staff login page
- `./images/dashboard.png` - Home or admin dashboard
- `./images/bookings.png` - Booking management page
- `./images/calendar.png` - Calendar schedule view
- `./images/members.png` - Customer and dog member profiles
- `./images/inventory.png` - Snack and product inventory page
- `./images/reports.png` - Daily or weekly report view

## Features

- Customer service booking workflow
- Admin dashboard for service overview
- Booking form for creating new bookings
- Calendar page for schedule management
- Customer profile and member management
- Wash and dry service management
- Grooming and bath service management
- Dog run and cafe usage page
- Snack and product inventory page
- Reports page for operational summaries
- Logs page for activity tracking
- Staff profile, roles, and settings pages
- Real-time availability tracking planned
- Optional QR code check-in/check-out planned

## Pages

| Route | Purpose |
| --- | --- |
| `/login` | Staff login page |
| `/home` | Main dashboard or home page |
| `/bookings` | Booking list and management |
| `/bookings/new` | New booking form |
| `/calendar` | Schedule calendar |
| `/members` | Member and customer profile management |
| `/wash-dry` | Wash and dry operations |
| `/grooming` | Grooming and bath operations |
| `/dog-run-cafe` | Dog run and cafe service usage |
| `/inventory` | Snack and product stock management |
| `/reports` | Daily and weekly reports |
| `/logs` | Staff or system activity logs |
| `/profile` | Staff profile |
| `/staff-roles` | Staff account and role management |
| `/settings` | Service pricing, hours, and configuration |

## Planned Management Features

| Area | Planned capability |
| --- | --- |
| Service scheduling | Internal staff booking and calendar management |
| Availability | Real-time zone and service status |
| Authentication | Secure login and role-based access control |
| Operations | Wash, grooming, dog run, and cafe usage tracking |
| Inventory | Snack stock tracking and low-stock alerts |
| Reports | Daily and weekly report downloads |
| Notifications | Staff task reminders and alerts |
| Settings | Pricing, staff accounts, and operating hours |

## Links

- **GitHub:** https://github.com/pan-k15/dogcare-management-app
- **Vue:** https://vuejs.org/
- **Vite:** https://vite.dev/
- **Vue Router:** https://router.vuejs.org/
- **TailwindCSS:** https://tailwindcss.com/
- **FullCalendar:** https://fullcalendar.io/

## Notes

The project currently includes a Vue 3 and Vite frontend structure. Backend services such as Firebase, Supabase, or Node.js/Express are listed as optional extension paths for authentication, real-time status, and persistent data storage.
