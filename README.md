# OneBank — Enterprise Banking Operations Portal

[![Live Application](https://img.shields.io/badge/Live_Portal-GitHub_Pages-0A1628?style=for-the-badge&logo=react&logoColor=61DAFB)](https://ashokkumarone.github.io/OneBank/)
[![Tech Stack](https://img.shields.io/badge/Stack-React_19_|_TypeScript_|_Tailwind_|_Vite-2563EB?style=for-the-badge&logo=typescript&logoColor=white)](package.json)
[![Domain](https://img.shields.io/badge/Domain-Ex--DBS_Bank_Personal_Banker-C9A84C?style=for-the-badge&logo=shield&logoColor=white)](#why-i-built-this)
[![Author](https://img.shields.io/badge/Author-Ashokkumar_S-FBBC05?style=for-the-badge&logo=linkedin&logoColor=black)](https://linkedin.com/in/ashokkumarone)

> An internal Core Banking Solution (CBS) operations dashboard concept designed to eliminate operational tool fragmentation for branch employees by unifying account onboarding, deposits, loan origination, customer service ticketing, and branch analytics into a single cohesive workspace.

---

## Why I Built This

During my tenure as a **Personal Banker at DBS Bank**, I experienced firsthand the friction of legacy branch banking operations. A typical branch officer juggles 5 to 7 disconnected legacy software windows daily:
- One legacy green-screen terminal for Core Banking (CBS) balance enquiries
- A separate third-party portal for Aadhaar / PAN e-KYC verification
- An isolated loan origination system for underwriting and EMI generation
- Physical registers and untracked desk notes for customer callback requests

This fragmentation causes severe turnaround time (TAT) delays, customer drop-offs, and compliance oversights. **OneBank** is an enterprise operations workspace designed around the actual day-to-day journey of a branch banker — streamlining customer service, compliance adherence, and revenue-generating operations.

---

## System Architecture & Branch Workflow

```
                                      ONEBANK CBS PORTAL
                                               │
         ┌───────────────────┬─────────────────┼───────────────────┬───────────────────┐
         │                   │                 │                   │                   │
   ACCOUNTS & e-KYC       DEPOSITS      LOAN ORIGINATION      SERVICE HUB         ANALYTICS &
   (7 Account Types)      (FD & RD)      (4-Stage Pipeline)   (SLA Tracking)      BRANCH RANKING
         │                   │                 │                   │                   │
   Aadhaar & PAN       Tenure & Yield    Eligibility, CIBIL   Ticket Lifecycle,   Real-time TAT,
   Verification        Compounding       & EMI Amortization   SMS/Email Updates   CASA Growth & SLA
```

---

## Core Product Modules

### 1. Accounts & e-KYC Management
- **7 Distinct Account Types:** Prime Savings (7.2% p.a.), Joint Savings, Student Campus Account, NRI/NRE/NRO, Business Current Account (GST entity required), Corporate Executive Salary, and Senior Citizen Savings (Aged 60+).
- **7-Step Registration Wizard:** Branch allocation, personal details, permanent address, income verification, nominee declaration, and mandatory KYC uploads adhering to **RBI Domestic Guidelines**.
- **CBS Core Balance Enquiry:** Multi-parameter search across Core Banking databases (by Account Number, CIF, Mobile, Aadhaar, or PAN) returning available vs. ledger balances, active fixed deposits, and linked loan liabilities in a single view.

### 2. Term Deposit Management (FD & RD)
- **Real-Time Yield & Maturity Calculator:** Interactive calculator for lump-sum Fixed Deposits and monthly Recurring Deposits, featuring automatic senior citizen interest rate bumps (+0.50% to 7.85% p.a.).
- **Deposit Certificate Issuance:** Configurable payout options (Cumulative compounding at maturity, quarterly interest credit, or monthly income payout).
- **Branch Term Deposit Ledger:** Real-time visibility into active certificates, principal invested, accrued yields, and maturity dates.

### 3. Loan Origination & Management
- **Multi-Product Lending:** Housing Loans, Personal Credit Lines, Vehicle Loans, Business Working Capital, and Gold Loans.
- **Dynamic EMI Schedules:** Generates detailed monthly amortization schedules breaking down principal recovery, interest component, and outstanding loan balances.
- **4-Stage Approval Pipeline:** Tracking applications through Document Verification &rarr; Credit Underwriting &rarr; Sanction Approval &rarr; Fund Disbursement.

### 4. Customer Service Hub & Follow-Up System
- **Omni-Channel Ticket Intake:** Fast intake for branch service requests (Debit Card hotlisting, Chequebook issuance, Passbook updates, Address/Mobile changes).
- **Priority-Driven SLAs:** Tiered response windows: Urgent (2h for card blocking), High (12h), Medium (24h), Low (48h).
- **Closed-Loop Follow-Up Engine:** Dedicated tracking controls recording call connection status (*Connected*, *Unreachable*, *Scheduled Callback*), resolution notes, automated customer SMS/Email alerts, and an immutable audit timeline.

### 5. Operations Analytics & Branch Performance
- **Operational Metrics:** Daily account creation throughput, loan disbursal targets (e.g. ₹4.25 Cr / 106% of target), and overall service SLA compliance (97.8%).
- **Branch Ranking & Peer Comparison:** Performance leaderboard comparing Tamil Nadu regional branches (T. Nagar #2, Anna Nagar, Coimbatore, Madurai, Trichy).
- **Executive Business Insights:** Highlighting CASA growth trends, retail cross-sell conversion rates, and turnaround bottlenecks.

---

## Tech Stack & Design System

- **Frontend Framework:** React 19 with TypeScript for strong typing across complex banking entities
- **Styling & Design System:** Tailwind CSS with enterprise slate/navy banking colorways and accessible contrast ratios
- **Data Visualization:** Recharts for branch KPI monitoring, volume trends, and SLA tracking
- **Iconography:** Lucide React for consistent financial system symbols
- **Build Tooling:** Vite for lightning-fast HMR and optimized production builds

---

## Live Prototype Access

Explore the live, interactive enterprise dashboard deployed on GitHub Pages:

👉 **[https://ashokkumarone.github.io/OneBank/](https://ashokkumarone.github.io/OneBank/)**

*Tip: On the Officer Authentication login screen, click **"Click here to auto-fill Manager credentials"** to instantly access the active session for T. Nagar Branch (TN-004).*

---

## About the Author

**Ashokkumar S**  
*Associate Product Manager · Product Analyst · Ex-Personal Banker (DBS Bank)*  
Specializing in fintech operations, retail banking compliance, enterprise workflows, and digital platform design.

- **LinkedIn:** [linkedin.com/in/ashokkumarone](https://linkedin.com/in/ashokkumarone)  
- **GitHub:** [@ashokkumarone](https://github.com/ashokkumarone)  
- **Other Projects:** [Tuning Music](https://ashokkumarone.github.io/Tuning-Music/) · [Flux](https://ashokkumarone.github.io/Flux/) · [Google Product Strategy Cases](https://ashokkumarone.github.io/Google-Product-Strategy-Cases/) · [OTT India Disruption Strategy](https://ashokkumarone.github.io/OTT-India-Disruption-Strategy/)

---

*Disclaimer: OneBank is an independent product design and architecture concept built to demonstrate enterprise banking workflow modernization. It operates entirely on simulated mock data with no connection to actual banking records.*
