<img width="1862" height="800" alt="image" src="https://github.com/user-attachments/assets/8142d17e-0da6-4537-9d1a-158e46fe6d46" />

# MedTrace — Digital Medicine Authentication & Traceability Framework

### Manufacturer → Distributor → Retailer → Consumer. One platform. Zero counterfeits.

### &nbsp;

[![License](https://img.shields.io/badge/license-MIT-green?style=flat)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Web%20%7C%20Mobile-blue?style=flat)](https://github.com/your-username/medtrace)
[![Stack](https://img.shields.io/badge/Stack-React%20%7C%20Node%20%7C%20Firebase-orange?style=flat)](https://github.com/your-username/medtrace)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat)](https://github.com/your-username/medtrace/pulls)

---

🧪 MedTrace is an end-to-end pharmaceutical supply chain traceability platform. Every medicine unit gets a unique QR identity at manufacture, travels through distributor and retailer with full digital custody, and can be verified by any consumer in real time.

💊 Built to solve a WHO-documented global crisis: falsified medicines containing wrong ingredients, incorrect dosages, or harmful substances — reaching patients every day due to weak supply chain monitoring.

|  | Sproxil | mPedigree | EMVS | **MedTrace** |
|---|---|---|---|---|
| **End-to-End Chain** | ❌ | ❌ | ❌ | ✅ |
| **Parent–Child Packaging** | ❌ | ❌ | ❌ | ✅ |
| **Real-Time Recall** | ❌ | ❌ | Partial | ✅ |
| **Platform Independent** | ❌ | ❌ | ❌ | ✅ |
| **Open Source** | ❌ | ❌ | ❌ | ✅ |
| **Offline Mode** | ❌ | ✅ | ❌ | ✅ |
| **B2B Marketplace** | ❌ | ❌ | ❌ | ✅ |

---

## 📢 News

`2026-01-31` 🎉 **MedTrace v1.0 Launched!** Full supply chain platform live — Manufacturer, Distributor, Retailer, and Consumer modules all connected. Zero counterfeit rate achieved in pilot testing.

---

## ✨ Features

🔐 **Unique Digital Identity** — Every medicine unit gets a QR-based UDI at manufacture, linked to batch, strength, expiry, and manufacturer.

📦 **Parent–Child Packaging Model** — One scan of a carton auto-updates all linked boxes and strips. Bulk logistics at zero extra effort.

⚡️ **Real-Time Verification** — Any stakeholder can verify medicine authenticity instantly via web portal or mobile scan.

🚨 **Instant Digital Recall** — Manufacturer triggers recall → entire network flagged within seconds → distributors, retailers, and consumers all alerted.

🏭 **Production Floor Security** — Time-limited operator job codes. One-time use, 8-hour expiry. Every printed QR is authorized and auditable.

🛒 **B2B Marketplace** — Retailers compare medicine offers across multiple distributors by price, stock, and expiry — all in one place.

🧾 **Automated Invoicing** — GST-compliant invoices auto-generated on every dispatch. Print or download as PDF.

📴 **Offline Support** — Mobile scans queued locally and synced to server on reconnect.

---

## 🖥️ Demonstration

### 🏭 Manufacturer Workflows

| 🧬 Batch Creation & QR Generation | 📦 Dispatch & Invoice | 🚨 Quality Recall |
|:---:|:---:|:---:|
| 📦 Dispatch & Invoice |
 | ![Recall](assets/demo/recall.png) |
| Create → Hierarchy → Print QR | Select Distributor → GST Invoice → Confirm | Trigger → Reason → Network Flagged |

### 🚚 Distributor & Retailer Workflows

| 📥 Incoming Shipments | 🏪 POS Terminal | 📊 Live Inventory |
|:---:|:---:|:---:|
| ![Incoming](assets/demo/incoming.png) | ![POS](assets/demo/pos.png) | ![Inventory](assets/demo/inventory.png) |
| Receive → Scan → Stock Updated | Search → Bill → Confirm Sale | Batch · Stock · Expiry · Alerts |

### 📱 Consumer Verification

| ✅ Genuine | 🚨 Recalled | ❓ Invalid |
|:---:|:---:|:---:|
| ![Genuine](assets/demo/genuine.png) | ![Recalled](assets/demo/recalled.png) | ![Invalid](assets/demo/invalid.png) |
| Safe to consume | Do NOT consume | Unknown product |

---

## 📦 Install

### From prebuilt release

Download the latest build from the [Releases](https://github.com/your-username/medtrace/releases) page.

### From source (recommended for development)

```bash
git clone https://github.com/your-username/medtrace.git
cd medtrace

# Install dependencies
npm install

# Start development server
npm run dev

# Production build
npm run build && npm start
```

---

## 🚀 Quick Start

> **Tip:** You need a Firebase project. Get one free at [firebase.google.com](https://firebase.google.com)

**1. Clone & install**

```bash
git clone https://github.com/your-username/medtrace.git
cd medtrace && npm install
```

**2. Configure** (`.env.local`)

```env
NEXT_PUBLIC_FIREBASE_API_KEY=your_api_key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_project_id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
NEXT_PUBLIC_FIREBASE_APP_ID=your_app_id
JWT_SECRET=your_jwt_secret
```

**3. Initialize Firebase**

```bash
firebase login
firebase init firestore functions
firebase deploy --only firestore:rules
```

**4. Run**

```bash
npm run dev
# → http://localhost:3000
```

That's it. Open the browser, register as a Manufacturer, and create your first batch in 2 minutes.

---

## 🧩 Stakeholder Modules

<details>
<summary><b>🏭 Manufacturer</b></summary>

### Manufacturer Portal

The root of the traceability chain. Every medicine's digital life begins here.

**Product Catalog**
Register any medicine type — Tablet, Syrup, Injection, Spray, Drops, Cream, Capsule — with brand name, generic name, strength, pack size, storage temperature, and base distributor price.

**Advanced Production Line**
```
Select Product → Set Packaging Hierarchy → Confirm → All QRs Generated
└─ Carton (N)
   └─ Box (N per Carton)
      └─ Strip (N per Box)
         └─ Unit (N per Strip)
```

**Team Management**
Register floor operators with 4–6 digit PINs. Assign time-limited production jobs (default 8 hours). Job codes are single-use — printing auto-locks when target quantity is reached.

**Dispatch & Logistics**
Select distributor → add batches to shipment → preview GST invoice → confirm. Stock and ownership transfer happen automatically.

**Quality Control & Recall**
Monitor all batch statuses. One click to trigger emergency recall with reason:
- Quality Check Failed
- Contamination Suspected
- Packaging Defect
- Regulatory Order

Recall propagates to every distributor and retailer holding the batch — instantly.

</details>

<details>
<summary><b>🚚 Distributor</b></summary>

### Distributor Portal

**B2B Marketplace** — Browse verified manufacturer catalogs, compare prices, place restocking orders.

**Incoming Shipments** — Review shipment contents (medicine, batch, quantity, price). Click "Receive & Add to Stock" — inventory auto-updates.

**My Inventory** — Real-time stock with:
- Total inventory value
- Expiry risk analysis (Safe / Warning / Critical)
- Adjustable retailer selling prices

**Order Management** — Review incoming retailer orders. Approve → auto-dispatch. Reject → retailer notified.

**Dispatch Stock** — Select retailer → add medicines → auto-calculate GST → generate invoice → confirm dispatch.

**Quality Alerts & Recalls** — Any recalled batch in stock is flagged in real time with affected batch number, manufacturer, severity, and required action.

</details>

<details>
<summary><b>🏪 Retailer</b></summary>

### Retailer Portal

**POS Terminal** — Quick billing for full strips or loose tablets. Supports Cash and UPI. Stock updates on sale confirmation. Print receipt or proceed to next sale.

**Medicine Marketplace** — Compare the same medicine across multiple distributors by price, available stock, and expiry. One-click "Buy Now".

**Shelf Inventory** — Live per-batch stock view. Low stock alerts. Expiry date warnings per batch.

**Incoming Stock** — Track dispatched orders. Accept delivery → shelf inventory auto-updated.

**Sales History** — Full transaction log: date, time, medicine, batch, quantity, amount, payment mode.

**Critical Medicine Alerts** — Recalled batch in stock? System immediately instructs: stop selling, remove from shelf, return to distributor.

</details>

<details>
<summary><b>📱 Consumer</b></summary>

### Consumer Interface

**Scan any medicine QR code** — get a result in under a second.

| Status | Meaning | Display |
|---|---|---|
| ✅ Genuine | Verified authentic, safe to consume | Green shield |
| ⚠️ Expired | Past expiry date | Orange warning |
| 🚨 Recalled | Do NOT consume | Red danger alert |
| ❓ Invalid | Unknown / potentially fake | Grey question |

**Result screen shows:** Medicine name · Generic name · Dosage form · Batch number · Strip ID · MFG date · EXP date · Manufacturer · MRP

**Quick Services:** Pharmacy Locator · Report Fake Medicine · Safety Score (0–100)

**Offline Mode:** Scans queued and synced when connection restores.

</details>

---

## ⚙️ Configuration

Config file: `.env.local`

### Services

| Service | Purpose | Get Access |
|---|---|---|
| `Firebase Firestore` | Medicine records, inventory, user data | [firebase.google.com](https://firebase.google.com) |
| `Firebase Auth` | Role-based login | Included with Firebase |
| `Firebase Functions` | QR generation, recall propagation | Included with Firebase |
| `JWT` | Secure API session tokens | Self-generated secret |

### Role Setup (Firestore)

```javascript
// Each user document in /users/{uid}
{
  uid: "...",
  role: "manufacturer" | "distributor" | "retailer" | "consumer",
  licenseNumber: "...",
  companyName: "...",
  verified: true | false
}
```

### Example `config.example.json`

```json
{
  "firebase": {
    "apiKey": "YOUR_API_KEY",
    "authDomain": "YOUR_PROJECT.firebaseapp.com",
    "projectId": "YOUR_PROJECT_ID"
  },
  "jwt": {
    "secret": "YOUR_JWT_SECRET",
    "expiresIn": "7d"
  },
  "qr": {
    "baseVerifyUrl": "https://your-domain.com/verify/",
    "errorCorrectionLevel": "H"
  }
}
```

---

## 🖥️ API Reference

| Method | Route | Description |
|---|---|---|
| `POST` | `/api/auth/login` | Login and receive JWT |
| `POST` | `/api/auth/register` | Register new organization |
| `GET` | `/api/medicine/verify/:uid` | Verify medicine by UDI |
| `POST` | `/api/batch/create` | Create production batch + generate QRs |
| `POST` | `/api/batch/recall` | Trigger emergency recall |
| `POST` | `/api/shipment/dispatch` | Dispatch to distributor or retailer |
| `POST` | `/api/shipment/receive/:id` | Confirm receipt of shipment |
| `GET` | `/api/inventory` | Get live inventory |
| `POST` | `/api/orders/place` | Place B2B order |
| `PUT` | `/api/orders/:id/approve` | Approve an order |

---

## 🔒 Security

- **Role-Based Access Control** — Manufacturer, Distributor, Retailer, Consumer each have scoped permissions.
- **JWT Authentication** — All API routes require signed tokens. Configurable expiry.
- **Operator Job Codes** — One-time use. Auto-expire after 8h. Batch printing locks after target quantity.
- **Replay Protection** — Verification sessions protected against duplication and replay attacks.
- **Audit Logs** — Every QR print, scan, dispatch, and recall permanently logged.
- **OWASP Compliant** — Built against [OWASP API Security Top 10](https://owasp.org/www-project-api-security/).

---

## 🤝 Contribute & Roadmap

PRs welcome! The codebase is modular and well-commented. 🤗

**Upcoming:**
- [ ] Regulator dashboard (cross-manufacturer audit view)
- [ ] WhatsApp verification bot
- [ ] Analytics heatmap for supply chain anomalies
- [ ] Multi-language consumer interface (Hindi, Bengali, Tamil)
- [ ] Aadhaar / digital signature integration for manufacturer KYC

---

## 🐛 Troubleshooting

### QR scan returns "Invalid" for a newly printed batch

The QR may have been scanned before the Firestore write completed. Wait 2–3 seconds and retry. If the issue persists, check Firebase Function logs for write errors.

### Recall not showing in distributor/retailer portal

The distributor must have clicked "Receive & Add to Stock" for the recall to appear in their alerts. Units never scanned into a distributor's inventory will not trigger their recall dashboard.

### Batch QR generation times out for large batches

Increase the Firebase Function timeout in `firebase.json`:

```json
{
  "functions": {
    "timeoutSeconds": 300
  }
}
```

### Login succeeds but dashboard is blank

Check that your Firestore security rules allow reads for the authenticated user's role. See [`firestore.rules`](firestore.rules) for the reference config.

### Invoice PDF not downloading

PDF generation runs client-side. Ensure your browser allows popups from the domain. Alternatively, use browser Print → Save as PDF.

---

## 📝 Free Tier Limits

| Service | Free Tier | Used For |
|---|---|---|
| **Firebase Firestore** | 1 GB storage · 50K reads/day | Medicine records, inventory, users |
| **Firebase Functions** | 2M invocations/month | QR generation, recall, invoicing |
| **Firebase Auth** | Unlimited | Role-based login |
| **Vercel** | Unlimited hobby deployments | Frontend hosting |

---

## 📚 References

1. WHO — [Substandard and Falsified Medical Products](https://www.who.int/publications/i/item/9789241513425)
2. GS1 — [Global Traceability Standard for Healthcare](https://www.gs1.org/standards/traceability/healthcare)
3. FDA — [Drug Supply Chain Security Act (DSCSA)](https://www.fda.gov/drugs/drug-supply-chain-security-act-dscsa)
4. EU — [Falsified Medicines Directive](https://health.ec.europa.eu/medicinal-products/pharmaceutical-strategy-europe/falsified-medicines-directive_en)
5. IEEE — [IoT Medicine Authentication via QR Codes](https://ieeexplore.ieee.org/document/9104512)

---

**Authors:** [Your Name] · [Team Member 2] · [Team Member 3]  
**Guide:** [Professor/Mentor Name] · [Institution Name]

<p align="center">Built with ❤️ to protect patients from counterfeit medicines.</p>

