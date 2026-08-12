# Crew Attendance & Location Billing Tracker

A simple, offline-friendly attendance and site tracking tool built for small concrete and construction crews (up to ~15 workers). This app is self-contained in a single HTML file—requiring no server, no installation, and no internet login.

## Features

- **Mark Daily Attendance**: Mark crew members as **Present** or **Absent** on any selected date.
- **Site Assignment**: Assign working crew members to specific job sites/clients for the day.
- **Crew Management**: Add, edit, or archive/delete crew members from your roster.
- **Location Directory**: Add and manage job sites/clients. Archiving keeps histories while cleaning today's dropdowns.
- **Interactive History**: Review attendance logs by **Date**, by **Worker** profile (presence rate and historical timelines), or by **Location** (deployment dates and worker lists).
- **Weekly Billing Summary**: Select any billing week to view client summaries:
  - Total active days at that site.
  - Total worker-days (distinct workers × active days) to invoice the client.
  - List of workers deployed and how many days each worked there.
  - **Export Billing CSV**: Download weekly breakdowns ready to email or import into Excel/Sheets.
- **Manual Salary Ledger**: Track payments worker-by-worker manually:
  - **Total Salary Agreed**: Manually enter the agreed total pay for the worker.
  - **Payment Logs**: Log individual payments given with dates.
  - **Running Balance**: Automatically computes total given and the remaining unpaid balance.
  - **Export Salary Slip**: Download the chronological payment log as a CSV receipt for the worker's records.
- **Offline & Local Storage**: Data is saved on the device using browser local storage (`localStorage`).
- **Data Portability**: Full database backups via JSON import/export, and complete master report exports to CSV.
- **Installable (PWA)**: Add the app to your phone's home screen or desktop to open it instantly offline.

## Project Structure

```text
attendance-tracker/
├── index.html        # Entire web application (markup, styles, and logic)
├── manifest.json     # PWA configurations for home-screen installations
├── sw.js             # Service Worker for local caching and offline operations
└── icons/            # App icons (192px and 512px)
```

## How to Use It

1. **Setup Directory**:
   - Open **Crew** tab -> Add your crew member names.
   - Open **Sites** tab -> Add your active job locations or clients.
2. **Track Attendance**:
   - Go to **Today** tab -> Select a default location for today (optional, fills worker dropdowns).
   - Toggle **Present** or **Absent** for each worker.
   - Adjust site selections in the dropdowns next to present workers.
3. **Manage Salaries**:
   - Go to **Salary** tab -> Select a worker from the sidebar list.
   - Click **Edit** next to "Total Salary Agreed/Due" to input the target amount.
   - Fill in the "Log Payment Given" form to record payments with amounts and dates.
   - Inspect the payment log list and the computed unpaid balance card.
   - Click **Export Slip** to download their payment ledger as a CSV.
4. **Review Invoices**:
   - Go to **Summary** tab -> Check the client summary for the week.
   - Click **Export Weekly CSV** to download the invoice records.
5. **Data Backups**:
   - Go to **Settings** -> Export JSON files occasionally to safeguard your database from manual browser cache cleans.

## Installation (PWA)

- **Chrome / Android**: Tap the three-dot menu and select **"Install app"** or **"Add to Home screen"**.
- **Safari / iOS**: Tap the Share button and select **"Add to Home Screen"**.
- **Desktop (Chrome / Edge)**: Click the Install icon in the URL bar (computer screen icon with down arrow).

---

*Note: Since all data lives in your browser's site cache, avoid clearing site cookies/storage unless you have exported a JSON backup.*
