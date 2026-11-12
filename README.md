# PennyWise

### Your Money. Your Privacy. Your Power.

An AI-powered, privacy-first personal finance assistant designed to help students make smarter financial decisions through intelligent spending analysis, personalized insights, and secure financial data processing.

## Overview

PennyWise combines AI-driven financial intelligence with a **privacy-first hybrid architecture**. Instead of sending raw financial information to cloud services, it processes sensitive data locally, masks personally identifiable information (PII), and sends only anonymized transaction data for AI analysis.

The goal is to make personal finance smarter, more accessible, and more engaging without compromising user privacy.

## Key Features

- **Hybrid AI Masking Engine:** Detects and anonymizes sensitive financial information before cloud-based AI processing.
- **Encrypted Financial Vault:** Local SQLite storage with AES-256 encryption through SQLCipher.
- **Auditor Mode:** Provides visibility into local data processing, PII masking, and anonymized network payloads.
- **AI Financial Assistant:** Generates personalized spending insights and recommendations.
- **Coach & Roast Modes:** Two AI personalities that make financial feedback informative and engaging.
- **Can I Afford This?:** Evaluates purchase affordability based on available balance and upcoming expenses.
- **Financial Sandbox:** Simulates financial scenarios to help users make informed decisions.

## Architecture

PennyWise follows a local-first hybrid AI architecture:

```text
       Financial Data
             |
             v
      Local Processing
             |
             v
       PII Detection
             |
             v
     Data Anonymization
             |
             v
      Sanitized JSON
             |
             v
       FastAPI Gateway
             |
             v
       Cloud AI (Gemini)
             |
             v
      Financial Insights
             |
             v
     Local Re-hydration
             |
             v
       User Dashboard
```

**Core Principle:** Sensitive personal identifiers remain on the user's device. Only sanitized financial data is intended to leave the device for AI analysis.

## Tech Stack

| Component | Technologies |
|---|---|
| Frontend | React, TypeScript |
| Desktop Framework | Tauri |
| Styling | Tailwind CSS |
| Backend | Python, FastAPI |
| AI Integration | Google Vertex AI, Gemini |
| Database | SQLite, SQLCipher |
| Cloud Infrastructure | Google Cloud Run |
| Data Processing | pdf-parse, PapaParse |
| Visualization | Recharts |

## Project Structure

```text
PennyWise/
├── backend/
├── public/
├── src/
├── src-tauri/
├── .vscode/
├── index.html
├── package.json
├── tsconfig.json
├── vite.config.ts
└── README.md
```

## Getting Started

**Prerequisites**
- Node.js
- npm
- Python 3.10+

**1. Clone the repository**

```bash
git clone https://github.com/tiyachaudhari/Pennywise.git
```

**2. Navigate to the project**

```bash
cd Pennywise
```

**3. Install dependencies**

```bash
npm install
```

**4. Start the development server**

```bash
npm run dev
```

Refer to the backend configuration for additional setup and environment variables.

## Roadmap

- Enhanced financial statement parsing
- Scholarship and grant discovery
- Subscription detection and expense tracking
- Receipt and voice-based expense ingestion
- Portfolio analysis and financial simulations

---

*PennyWise — Making financial intelligence smarter, simpler, and more private.*
