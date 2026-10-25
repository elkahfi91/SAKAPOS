# OmniPOS

A modern, lightweight point-of-sale (POS) web application built for small businesses and micro-retail operations in Indonesia. OmniPOS is designed to run as a static web app, works well on desktop and mobile devices, and can be installed as a progressive web app (PWA) for faster access and offline use after the first load.

[![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-blue)](https://github.com/elkahfi91/SAKAPOS)
[![PWA](https://img.shields.io/badge/Type-PWA-orange)](https://github.com/elkahfi91/SAKAPOS)
[![Status](https://img.shields.io/badge/Status-Operational-success)](https://github.com/elkahfi91/SAKAPOS)

## Overview

OmniPOS helps store owners manage sales transactions, track incoming stock, monitor inventory, and generate daily reports without requiring a backend server or complex infrastructure. The app stores data in browser localStorage, making it easy to deploy, test, and operate in low-cost environments.

This project is ideal for:
- coffee shops and beverage stalls
- small retail counters
- neighborhood stores
- daily product sales workflows

## Core Features

### Product Management
- Add, edit, and archive products
- Set selling price per item
- Manage catalog directly from the browser

### Daily Stock Intake
- Record incoming inventory per date
- Compare received stock with sold stock
- Validate whether stock is sufficient before sale

### Cashier & Sales Workflow
- Search products quickly
- Add items to cart
- Apply discount
- Choose payment method: cash, transfer, or other
- Auto-calculate total, tax, and change
- Print or preview receipt in a new browser tab

### Daily Reporting
- Summary of revenue, transactions, incoming stock, and sold items
- Transaction history by date
- Refund support for voided transactions
- CSV export for stock and sales data
- Share report via WhatsApp or copy text

### Store Settings
- Store name and cashier name
- Merchant location and contact details
- Instagram and TikTok profile fields
- Tax configuration
- Light/dark/system theme toggle
- Backup and restore with JSON export

### PWA Support
- Installable on supported devices
- Offline support after initial load
- Fast local access via browser home screen or app install flow

## Project Structure

```text
SAKAPOS/
├── index.html              # Root entry page for GitHub Pages
├── omnipos.html            # Main POS application
├── manifest.webmanifest    # PWA metadata
├── sw.js                   # Service worker for offline caching
├── icon.svg                # App icon
├── README.md               # Documentation
└── .gitignore              # Optional repo ignore rules
```

## How It Works

OmniPOS is a client-side application with no backend database. Data is saved in the browser using `localStorage`, which means:

- the app is fast and simple to deploy
- no server setup is required for basic usage
- all data stays in the browser on the device used by the store

For operational safety, the app includes JSON backup and restore functions in the settings menu.

## Quick Start

### Option 1: Open directly in the browser
Open `omnipos.html` in a browser.

### Option 2: Run a local web server
From the project directory, run:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## GitHub Pages Deployment

1. Push this repository to GitHub.
2. Open the repository on GitHub.
3. Go to Settings → Pages.
4. Set the source to:
   - Source: Deploy from a branch
   - Branch: `main`
   - Folder: `/root`
5. Save the settings.
6. The app will be available at:

```text
https://<username>.github.io/<repository-name>/
```

Example:

```text
https://elkahfi91.github.io/SAKAPOS/
```

## Data Safety Notes

- Data is stored in browser `localStorage`, not on a cloud server.
- Clearing browser data may delete stored sales and product data.
- Use the backup feature regularly in the Settings page.
- For production use, combine this with a safer backup routine and device management policy.

## Why This Project Exists

OmniPOS was created to give small businesses a practical, low-cost sales system without the burden of full-stack infrastructure. It focuses on the essentials that matter most in daily retail operations:

- moving products quickly
- monitoring stock accurately
- calculating revenue cleanly
- generating a daily operational overview

## Roadmap

Future improvements may include:
- multi-user support with cloud sync
- category and inventory history
- barcode scanning
- printable branded receipts
- authentication and admin roles
- database-backed deployment options

## License

This project is intended for operational use by small businesses and can be adapted or extended according to business needs.

## Maintainer

OmniPOS is maintained as a lightweight operational tool for local retail workflows and continues to evolve based on real usage needs.

## Powered Development by :
SAKA OMNI. 
