# CFSI Temporary Visitor QR System - QR Code Maker

A minimal, installable visitor QR code maker for Children of Fatima School of Mabalacat, Inc.

This version contains only the QR code maker. It does not include the admin dashboard or the scanner.

## What it does
- Visitors request a temporary visitor pass.
- The system creates a unique temporary code and generates a QR code for the pass.
- The QR code is time-limited based on the selected purpose.
- The visitor sees the QR code and temporary code on their phone.

## Runs without Python
- This is a fully static web app. No backend server and no Python required.

## Phone app (PWA)
- Open the app in Chrome (Android) or Safari (iOS).
- Use "Add to Home Screen" / "Install App" from the browser menu.
- The app launches standalone with the QR code maker.

## Included
- `index.html` - Single-file visitor QR pass maker interface (client-side QR + in-browser SQLite).
- `manifest.json` - Web app manifest for installability.
- `icon-192.png`, `icon-512.png` - App icons.
- In-browser SQL database: SQLite via WebAssembly (sql.js).

## Usage
- Open `index.html` in a modern browser.
- Request a temporary visitor pass.
- Show the QR code / temporary code at the gate.

## Phone usage
- Serve the folder with any static web server (for example `npx serve` or a static host).
- Open the app URL on the phone via the same network.
- Install via browser "Add to Home Screen" / "Install App".

## QR download
- The pass screen includes a "Download QR" button that saves the QR code as a PNG image.

## Database
- SQLite database runs in the browser via WebAssembly (sql.js).
- Tables: `purposes`, `visitors`.
