# Pricyfy v12.2 🏢

> **Modern, ultra-fast, offline-first Price Directory, Stock Purchase Ledger & Supplier Directory PWA** with built-in Web Bluetooth ESC/POS thermal printing for retail shops, distributors, and wholesale merchants.

## 📖 Table of Contents

* [Overview](#-overview)

* [Key Features](#-key-features)

  * [1. 🏷️ Price Directory](#1-️-price-directory)

  * [2. 📦 Purchase Ledger & Multi-Log](#2--purchase-ledger--multi-log)

  * [3. 📇 Supplier Directory](#3--supplier-directory)

  * [4. 🖨️ Thermal Receipt Printing & ESC/POS Engine](#4-️-thermal-receipt-printing--escpos-engine)

  * [5. 💾 Data Portability, Backups & Privacy](#5--data-portability-backups--privacy)

* [Tech Stack](#-tech-stack)

* [Quick Start](#-quick-start)

  * [Run Locally](#run-locally)

  * [Deploy to GitHub Pages (Recommended)](#deploy-to-github-pages-recommended)

* [Installing as a PWA (Mobile & Desktop)](#-installing-as-a-pwa-mobile--desktop)

* [Web Bluetooth Thermal Printer Setup](#-web-bluetooth-thermal-printer-setup)

* [Data Storage & Security](#-data-storage--security)

* [Contributing](#-contributing)

* [License](#-license)

## 🌟 Overview

**Pricyfy** is a self-contained, zero-backend Progressive Web Application (PWA) built specifically for retail store owners, wholesale traders, and inventory managers. It replaces clumsy paper price notebooks, chaotic stock bills, and scattered supplier contact cards with a clean, lightning-fast mobile dashboard.

* **100% Client-Side:** Operates directly inside your web browser. No databases, accounts, servers, or subscriptions required.

* **Offline First:** Works seamlessly without an internet connection using local caching and browser storage (`localStorage`).

* **Single-File Architecture:** The entire app runs out of a single HTML file (`index.html`) containing modern Tailwind CSS styling, FontAwesome icons, and lightweight vanilla JavaScript.

## ✨ Key Features

### 1. 🏷️ Price Directory

* **Instant Search**: Real-time fuzzy filtering across product names, sizes, packaging variants, and categories.

* **Dual-Price Visibility**: Displays both Cost Price and Selling Price alongside package sizes.

* **Last-Purchased Timestamps**: Automatic badges highlighting when each product was last restocked.

* **Category Badges & 2-Line Ribbon Tiles**: Interactive, color-coded category chips for one-touch category filtering.

* **Custom Category Studio**: Create, edit, recolor, and assign categories on the fly with custom hex palettes.

* **Bulk Import & Bulk Edit**:

  * Add multiple items at once using formatted comma-separated lists (`Product, Size, Cost, Sale, Category`).

  * Edit names, categories, variants, and prices across your entire inventory in a single unified editor.

### 2. 📦 Purchase Ledger & Multi-Log

* **Single Stock Inward**: Log individual stock purchases with automated unit cost and total calculations.

* **📋 Multi-Log (Batch Entry)**:

  * Log multiple supplier items on a single invoice/voucher screen.

  * Live dropdown lookup that auto-populates known unit costs and categories.

  * Automatic catalog sync: Entering a new item in Multi-Log automatically registers it in your Price Directory.

* **📜 Multilog History & Vouchers**: Complete searchable history of past purchase vouchers with itemized breakdowns and instant reprint capabilities.

* **Capital & Order Analytics**: Live summary cards showing Total Capital Investment and total order records.

* **Smart Date & Category Filters**: 1-click date presets for **Today**, **This Month**, **All Time**, or flexible **Custom Date Ranges**, paired with category filtering and voucher printing.

* **Selective Ledger Reset**: Delete purchase logs selectively by **Date**, **Category**, **Item**, or **Wipe All** with an expandable matching-records preview list.

### 3. 📇 Supplier Directory

* **Category-Based Vendor Hub**: Organizes suppliers by product line and vendor category.

* **Direct Communication**:

  * 📞 **One-Touch Calling**: Direct `tel:` link integration to dial vendors instantly.

  * 💬 **Direct WhatsApp**: Launch WhatsApp (`wa.me`) chats with preformatted phone numbers with a single click.

  * Inline phone number management to update vendor details at any time.

* **Collapsible Catalog Accordion**: Expand or collapse supplier item lists on demand.

* **Clickable Item History**: Click any product name in the supplier list to open its comprehensive purchase log, showing total units received, total expenditure, and historic average buy price.

* **Item Action Menu**: 3-dot dropdown menu on every item to **Log Stock**, **Edit Item**, **View History**, or **Delete Item** directly from the supplier view.

### 4. 🖨️ Thermal Receipt Printing & ESC/POS Engine

* **Web Bluetooth Printing (BLE / RFCOMM)**:

  * Connect directly to wireless Bluetooth thermal receipt printers without proprietary drivers or companion software.

  * Supports standard ESC/POS command sequences (`ESC @`, font sizing, bold formatting, paper feeding, and auto-cut).

* **Dual Paper Sizes**: Toggle between **58 mm (2-inch / 32 cols)** and **80 mm (3-inch / 48 cols)** layouts.

* **Customizable Voucher Options**: Toggle **Purchase Date**, **2-Line Item Names**, **Unit Cost**, **Serial Numbers**, **Store Header**, and **Voucher No**.

* **Real-Time Canvas Preview**: High-fidelity live canvas view mirroring exact thermal receipt outputs.

* **Custom Store Headers**: Personalize voucher headers with your business name, address, and GST/contact numbers.

* **System Printing**: Print 3-inch thermal catalogs or purchase bills via standard desktop/mobile system print dialogs (`Ctrl + P`).

* **Image Export & Sharing**: Export receipts as PNG images or share them natively via device share dialogs.

### 5. 💾 Data Portability, Backups & Privacy

* **Zero Data Tracking**: Your prices, purchases, and supplier lists never leave your device.

* **Smart CSV Import Wizard**: Flexible file upload with intelligent column-mapping to import data from Excel, Google Sheets, or existing POS databases.

* **1-Click CSV Exports**: Download your Price Directory or Purchase Ledger as CSV spreadsheets anytime.

* **JSON Complete Backup**: Export a full JSON archive containing all catalog items, categories, purchase ledgers, and batch vouchers, and restore it with one click.

* **📱 Download Offline App**: Download a standalone copy (`Pricyfy_v12_2.html`) directly to your device storage for offline archiving.

## 🛠️ Tech Stack

| Technology | Role | 
| ----- | ----- | 
| **HTML5 & Vanilla JS (ES6+)** | Core client-side application logic and state management | 
| **Tailwind CSS (CDN)** | Responsive, mobile-first design with built-in dark mode | 
| **Web Bluetooth API** | Direct browser-to-hardware communication with Bluetooth thermal printers | 
| **HTML5 Canvas** | Pixel-accurate real-time receipt rendering | 
| **Service Worker & Web Manifest** | Progressive Web App (PWA) installation and offline capability | 
| **FontAwesome (v6)** | Modern vector icons for buttons and interface elements | 

## 🚀 Quick Start

### Run Locally

1. Clone or download the repository:

   ```bash
   git clone https://github.com/your-username/pricyfy.git
   cd pricyfy
   ```

2. Open `index.html` in any modern web browser:

   * Double-click `index.html` to open it in Chrome, Edge, Brave, or Safari.

   * Or start a quick local server:

     ```bash
     # Python 3
     python -m http.server 8000
     ```

   * Navigate to `http://localhost:8000` in your browser.

### Deploy to GitHub Pages (Recommended)

Running Pricyfy on an HTTPS connection is **required** for Web Bluetooth printer pairing and Service Worker PWA installation.

1. Push your repository to GitHub.

2. In your repository, go to **Settings** > **Pages**.

3. Under **Build and deployment** > **Branch**, select `main` (or `master`) branch and the `/ (root)` folder.

4. Click **Save**.

5. Within 1–2 minutes, your app will be live at `https://<your-username>.github.io/<repo-name>/`.

## 📱 Installing as a PWA (Mobile & Desktop)

Pricyfy can be installed to run full-screen without address bars, just like a native Android or iOS app:

### Android (Chrome / Brave / Edge)

1. Open your hosted GitHub Pages URL in Google Chrome.

2. Tap the **⋮** menu in the browser header (or the **⋮** menu in the app bar and choose **Install App (PWA)**).

3. Tap **Install** or **Add to Home Screen**.

4. Launch Pricyfy directly from your phone's home screen or app drawer.

### iOS (Safari)

1. Open your hosted URL in Safari.

2. Tap the **Share** button (box with an upward arrow).

3. Scroll down and tap **Add to Home Screen**.

4. Tap **Add** in the top right corner.

### Desktop (Chrome / Edge)

1. Open the hosted URL on desktop.

2. Click the install icon in the URL bar (computer with down arrow) or choose **Install Pricyfy** from the menu.

## 🖨️ Web Bluetooth Thermal Printer Setup

Pricyfy uses the standard **Web Bluetooth API** to send ESC/POS bytecode to thermal printers:

### Prerequisites:

* A Bluetooth thermal receipt printer (58mm or 80mm).

* Google Chrome, Edge, or Brave on Android, Windows, macOS, or Linux.

* An HTTPS origin (GitHub Pages, Vercel, or `http://localhost`).

### Pairing Steps:

1. Turn on your thermal printer and enable Bluetooth.

2. Open Pricyfy and click **Multi Log** or the **🖨️ Printer** icon in the header.

3. In the Print Center or Receipt Modal, click **📶 Connect Bluetooth**.

4. In the browser pairing popup, select your printer (e.g., `MPT-II`, `POS-58`, `POS-80`, `RPP-02`, etc.) and tap **Pair**.

5. The badge will turn green (**Connected:** ).

6. Click **Print ESC/POS** or **⚡ Save & Print** to print vouchers instantly!

## 🔒 Data Storage & Security

* **Strictly Local**: All data (items, purchase logs, vendor contacts) is saved to your browser's `localStorage` (`pricyfy_v12_2_state`).

* **No Third-Party Trackers**: No analytics scripts, cookies, or external server pings.

* **Regular Backups**: Use the **⇄** menu > **Export JSON Backup** regularly to keep safe offline copies of your data across devices.

## 🤝 Contributing

Contributions, feedback, and feature requests are welcome!

1. Fork the Project.

2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`).

3. Commit your Changes (`git commit -m 'Add AmazingFeature'`).

4. Push to the Branch (`git push origin feature/AmazingFeature`).

5. Open a Pull Request.

## 📄 License

Distributed under the **MIT License**. See `LICENSE` for more information.