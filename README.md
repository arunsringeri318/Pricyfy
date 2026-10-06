# Pricyfy v12.1 🏢

> **Modern, Offline-First Price Directory, Stock Purchase Ledger & Supplier Directory PWA** with built-in Web Bluetooth ESC/POS Thermal Printing.

[![Version](https://img.shields.io/badge/version-12.1-amber.svg)](https://github.com)
[![PWA](https://img.shields.io/badge/PWA-Installable-blue.svg)](https://github.com)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Zero-Dependencies](https://img.shields.io/badge/dependencies-0%20runtime%20build-success.svg)](https://github)

---

## 🌟 Overview

**Pricyfy** is a single-file, zero-backend Progressive Web Application (PWA) tailored for retail stores, wholesale merchants, distributors, and shopkeepers. It streamlines price lookups, stock purchase ledgering, supplier communication, and on-the-spot thermal receipt generation directly from mobile devices or desktop browsers.

Everything runs **100% client-side** using your browser's local storage (`localStorage`). No servers, no subscriptions, and no database configuration required.

---

## ✨ Key Features

### 🏷️ 1. Price Directory
- **Instant Search**: Real-time filtering by item name, package variant, or size.
- **Categorization**: Visual color-coded category tags with 2-line quick-toggle category ribbon tiles.
- **Smart Catalog View**: Clean tabular layout showcasing Cost Price, Selling Price, package sizes, and last-purchased timestamps.
- **Bulk Operations**: Bulk Add products via formatted text or CSV, and Bulk Edit existing items in a unified panel.

### 📦 2. Stock Purchase Ledger & Multi-Log
- **Single & Multi-Entry Logging**: Log individual stock receipts or use **Multi-Log** to log entire batches of products on a single invoice.
- **Auto-Catalog Sync**: Unlisted items entered in Multi-Log can be auto-registered into your catalog on the fly.
- **Voucher History**: Complete audit trail of past batches with instant breakdown modals.
- **Financial Analytics**: Total capital investment metrics and date range filtering (Today, All Time, This Month, or Custom Date Ranges).

### 📇 3. Supplier Directory
- **Vendor Organization**: Categorized supplier directory with direct phone number management.
- **1-Click Call & WhatsApp**: Direct dialing (`tel:`) and instant WhatsApp chat (`wa.me`) integration.
- **Collapsible Catalog Accordion**: Expand or collapse supplier item lists on demand.
- **Item History Integration**: Click any product in the supplier list to immediately view its detailed purchase history, average buy price, and logs.
- **Quick Actions Menu**: 3-dots menu on each item to Log Stock, Edit, or Delete without switching views.

### 🖨️ 4. ESC/POS Thermal Printing & Receipt Center
- **Web Bluetooth Printing**: Pair directly with portable 58mm or 80mm wireless Bluetooth thermal printers from Chrome (Android / Desktop).
- **Live Canvas Preview**: Real-time paper preview matching ESC/POS layout formatting.
- **Custom Voucher Headers**: Customizable shop name, address, and contact headers.
- **System Printing**: Print 3-inch thermal catalogs and purchase vouchers via system print dialogs.
- **Image Sharing**: Export vouchers as high-resolution PNG images or share them natively.

### 💾 5. Data Privacy & Portability
- **100% Offline & Private**: All data resides safely inside your browser.
- **Smart CSV Import**: Flexible column-mapping wizard for importing from Excel, Google Sheets, or custom POS exports.
- **Exports**: 1-click export to CSV (Directory or Purchase Ledger) and full JSON backup files.
- **1-Click Offline App Download**: Save `Pricyfy_v12_1.html` directly to your device for offline storage and backups.

---

## 🛠️ Tech Stack

- **HTML5 & Vanilla JavaScript**: Pure client-side logic with zero framework overhead.
- **Tailwind CSS**: Utility-first responsive styling via CDN.
- **Web Bluetooth API**: Direct wireless hardware integration for thermal receipt printers.
- **Progressive Web App (PWA)**: Standalone desktop & mobile installation via Service Worker and Web App Manifest.
- **HTML5 Canvas**: Dynamic receipt rendering and export.

---

## 🚀 Getting Started

### Option 1: Run Locally
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/pricyfy.git
   cd pricyfy
   ```
2. Open `index.html` in any modern web browser (Google Chrome, Microsoft Edge, or Safari).

### Option 2: Deploy to GitHub Pages (Recommended)
1. Push the code to your GitHub repository.
2. Go to **Settings** > **Pages**.
3. Under **Branch**, select `main` (or `master`) and save.
4. Open the hosted URL on your mobile phone or PC to install it as an app!

> ⚠️ **Note for Bluetooth Printing**: The Web Bluetooth API requires an **HTTPS** connection (such as GitHub Pages or `localhost`) to communicate with wireless printers.

---

## 📱 Installing as a PWA

1. Open the hosted app in Google Chrome on Android or Desktop.
2. Tap the **⋮** menu in the app header and choose **Install App (PWA)**, or use your browser's **Install / Add to Home screen** prompt.
3. Pricyfy will launch full-screen as a native app with offline capabilities.

---

## ⌨️ Thermal Printer Compatibility

Pricyfy's print engine is optimized for standard **ESC/POS** Bluetooth receipt printers:
- **Paper Sizes**: 58mm (2-inch / 32 columns) & 80mm (3-inch / 48 columns).
- **Supported Connection**: Wireless Web Bluetooth (GATT profile).
- **Tested Hardware**: Epson, Star Micronics, Rongta, POS-5802, PT-210, MPT-II, and generic 58mm/80mm Bluetooth thermal POS printers