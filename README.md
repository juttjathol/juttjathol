<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=14532d&height=160&section=header&text=JATHOL&fontSize=54&fontColor=FAF7F2&desc=Order%20Flow%20-%20Offline-first%20POS%20for%20restaurants%20and%20retail&descAlignY=75&descAlign=50" alt="JATHOL banner"/>
</p>

<h1 align="center">Hi, I'm Jutt — founder of <a href="https://jathol.org">Jathol</a> 👋</h1>
<p align="center">
  I build <b>Order Flow</b> — the offline-first, multi-device POS that keeps the shop selling even when the internet doesn't.
  <br/>
  <sub>Android + Windows Main on <code>:8787</code> · Stations on LAN or encrypted cloud relay · One Main, many floors</sub>
</p>

<p align="center">
  <a href="https://jathol.org"><img src="https://img.shields.io/badge/website-jathol.org-14532d?style=for-the-badge" alt="jathol.org"/></a>
  <a href="https://jathol.org/download"><img src="https://img.shields.io/badge/download-APK_%2B_Windows-0ea5e9?style=for-the-badge" alt="download"/></a>
  <a href="https://jathol.org/guide"><img src="https://img.shields.io/badge/guide-English_%7C_%D8%A7%D8%B1%D8%AF%D9%88-b45309?style=for-the-badge" alt="guide"/></a>
  <a href="mailto:contact@jathol.org"><img src="https://img.shields.io/badge/contact-contact%40jathol.org-FAF7F2?style=for-the-badge&color=14532d" alt="contact@jathol.org"/></a>
</p>

<p align="center">
  <a href="https://github.com/juttjathol/Order-Flow-V2/releases/latest"><img src="https://img.shields.io/github/v/release/juttjathol/Order-Flow-V2?label=latest%20release&color=14532d" alt="latest release"/></a>
  <img src="https://img.shields.io/badge/Main-Android_%7C_Windows_10--11-14532d" alt="Main"/>
  <img src="https://img.shields.io/badge/Shop%20UI-English_%7C_%D8%A7%D8%B1%D8%AF%D9%88-b45309" alt="UI"/>
  <img src="https://img.shields.io/badge/license-per%20shop%20key-FAF7F2" alt="license"/>
</p>

---

### 🚀 Flagship — Order Flow V2

> **One Main. A whole floor of stations.** Main holds the license and runs the local server. Tablets join on the same Wi-Fi — or over an encrypted cloud relay when the shop Wi-Fi dies. Your sales stay on your device.

**Live:** [jathol.org](https://jathol.org) · [User Guide](https://jathol.org/guide) · [Download](https://jathol.org/download) · [Releases](https://github.com/juttjathol/Order-Flow-V2/releases/latest)

**What it does — 15 gated extras per license key:**

| Tier | What you get |
|------|--------------|
| **Starter `RM 79/mo`** | POS billing, inventory, reports, receipt printing — core only |
| **Growth `RM 149/mo`** | + 13 extras: `multi_terminal` · `station_printers` · `qr_ordering` · `loyalty` · `split_payment` · `refunds` · `customer_display` · `reservations` · `recipe_costing` · `wastage` · `purchases` · `advanced_reports` · `eighty_six` |
| **Custom** | Hand-pick any of the 15 — you choose |
| **Full** | Everything on, always |

`cloud_sync` + `qr_branding` are **Custom/Full only** — encrypted relay (`AES-GCM`, 30m TTL, 200 rows, `1.2s` hot / `30s` idle) and a branded guest QR page. Shop data is **never** backed up to the cloud — relay is transit.

<details>
<summary><b>How the shop works (click to expand)</b></summary>

- **Main = server on `:8787`** — Android phone or Windows laptop (`order_flow.exe`). Works **offline 48h** after first activation.
- **Stations** — Order Taker / Kitchen / Cashier / Driver / etc. — join free via IP or QR. No key needed.
- **QR self-order** — guests open `http://<main-ip>:8787/order`, pick a table, send to kitchen (`channel: qr`, `24/h` per table, `900/h` shop cap).
- **LAN + Cloud** — stations ride LAN first, fall back to cloud relay on mobile data. Offline queue auto-merges.
- **License:** `POST /api/v1/license/validate { licenseKey, deviceId }` — first device binds, second rejected until **Reset device**. Dashboard propagates plan in ≤15 min or instantly via **More → License → Refresh plan & features**.

Full architecture diagram → [`Order-Flow-V2/README.md#architecture--how-it-all-connects`](https://github.com/juttjathol/Order-Flow-V2#architecture--how-it-all-connects)
</details>

---

### 🛠️ Stack

<p>
  <img src="https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter&logoColor=white" alt="Flutter"/>
  <img src="https://img.shields.io/badge/Dart-0175C2?style=flat&logo=dart&logoColor=white" alt="Dart"/>
  <img src="https://img.shields.io/badge/Cloudflare-F38020?style=flat&logo=cloudflare&logoColor=white" alt="Cloudflare"/>
  <img src="https://img.shields.io/badge/D1-SQLite-003B57?style=flat&logo=cloudflare&logoColor=white" alt="D1"/>
  <img src="https://img.shields.io/badge/Pages-Workers-F38020?style=flat" alt="Pages"/>
  <img src="https://img.shields.io/badge/ESC%2FPOS-9100-14532d?style=flat" alt="ESC/POS"/>
  <img src="https://img.shields.io/badge/Bluetooth-Classic_%7C_BLE-0082FC?style=flat&logo=bluetooth&logoColor=white" alt="Bluetooth"/>
  <img src="https://img.shields.io/badge/Windows-10%2F11-0078D4?style=flat&logo=windows&logoColor=white" alt="Windows"/>
  <img src="https://img.shields.io/badge/Android-APK-3DDC84?style=flat&logo=android&logoColor=white" alt="Android"/>
</p>

**I work with:** offline-first sync, LAN servers (`shelf`/`dart:io`), `shared_preferences` persistence, role-based access, HMAC + PBKDF2 licensing, AES-GCM relay, thermal printing (ESC/POS `9100` / Bluetooth / Windows spooler), cash drawers, QR flows.

---

### 📌 Pinned — start here

<p>
  <a href="https://github.com/juttjathol/Order-Flow-V2">
    <img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=juttjathol&repo=Order-Flow-V2&theme=transparent&title_color=14532d&icon_color=14532d&text_color=1a1a1a&border_color=14532d&hide_border=false" alt="Order-Flow-V2"/>
  </a>
  <a href="https://github.com/juttjathol/order-flow">
    <img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=juttjathol&repo=order-flow&theme=transparent&title_color=14532d&icon_color=b45309&text_color=1a1a1a&border_color=b45309&hide_border=false" alt="order-flow"/>
  </a>
</p>

> Building in public: `Order-Flow-V2` is the active repo (v1.1.84). `order-flow` is the previous generation. Website + SaaS dashboard live in the same monorepo.

---

### 📊 At a glance

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=juttjathol&show_icons=true&theme=transparent&title_color=14532d&icon_color=14532d&text_color=1a1a1a&border_color=14532d&hide_border=false&include_all_commits=true" alt="stats" height="150"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=juttjathol&layout=compact&theme=transparent&title_color=14532d&text_color=1a1a1a&border_color=14532d&hide_border=false" alt="top langs" height="150"/>
</p>
<p align="center">
  <img src="https://streak-stats.demolab.com?user=juttjathol&theme=transparent&border=14532d&ring=14532d&fire=b45309&currStreakLabel=14532d" alt="streak"/>
</p>

---

### 📫 Let's talk

- **Licences, trials, resets, printers:** [contact@jathol.org](mailto:contact@jathol.org) — replies within 24h, Mon–Sat GMT+8
- **Website:** [jathol.org](https://jathol.org) · [jathol.org/guide](https://jathol.org/guide) · [jathol.org/download](https://jathol.org/download)
- **WhatsApp (support on lock):** `@Jathol_Jutt` — shown in the app when a Main locks



<p align="center">
  <sub>Profile README lives at <code>github.com/juttjathol/juttjathol</code></sub>
  <br/>
  <img src="https://komarev.com/ghpvc/?username=juttjathol&label=Profile%20views&color=14532d&style=flat" alt="profile views"/>
</p>
