# OneBank — Enterprise Banking Operations Portal

[![Live Application](https://img.shields.io/badge/Live_Portal-GitHub_Pages-0A1628?style=for-the-badge&logo=react&logoColor=61DAFB)](https://ashokkumarone.github.io/OneBank/)
[![Tech Stack](https://img.shields.io/badge/Stack-React_19_|_TypeScript_|_Tailwind_|_Vite-2563EB?style=for-the-badge&logo=typescript&logoColor=white)](package.json)
[![Domain](https://img.shields.io/badge/Domain-Ex--DBS_Bank_Personal_Banker-C9A84C?style=for-the-badge&logo=shield&logoColor=white)](#why-i-built-this)
[![Author](https://img.shields.io/badge/Author-Ashokkumar_S-FBBC05?style=for-the-badge&logo=linkedin&logoColor=black)](https://linkedin.com/in/ashokkumarone)

> An internal Core Banking Solution (CBS) operations portal concept for branch employees, designed around real-world retail banking workflows to eliminate tool fragmentation and introduce a **proprietary closed-loop Request Tracker** that solves the classic *"Please come tomorrow"* customer drop-off problem.

---

## Why I Built This

During my tenure as a **Personal Banker at DBS Bank**, I experienced firsthand the friction of legacy branch banking operations. A typical branch officer juggles 5 to 7 disconnected software windows daily:
- One legacy terminal for Core Banking (CBS) balance enquiries
- A separate third-party portal for Aadhaar / PAN e-KYC verification
- An isolated loan origination system for underwriting and EMI calculations
- Physical registers and sticky notes for customer service requests

This fragmentation causes severe turnaround time (TAT) delays, customer drop-offs, and compliance oversights. **OneBank** is an enterprise operations workspace designed around the actual day-to-day journey of a branch banker — streamlining customer service, compliance adherence, and revenue-generating operations.

---

## ⭐ The Flagship Innovation: Closed-Loop Request Tracker

While account onboarding, deposits, and lending are standard table stakes in any bank, the **Request Tracker** is the original product innovation at the heart of OneBank.

```
                  THE "COME TOMORROW" PROBLEM vs ONEBANK SOLUTION
┌────────────────────────────────────────┐      ┌────────────────────────────────────────┐
│     TRADITIONAL BANKING FAILURE        │      │       ONEBANK CLOSED-LOOP ENGINE       │
├────────────────────────────────────────┤      ├────────────────────────────────────────┤
│ Customer visits branch with query      │      │ Customer visits branch with query      │
│ "System is down, please come tomorrow" │ ───► │ Officer logs request in 30 seconds     │
│ No digital record; written on notepad  │      │ Instant SMS / Email token to customer  │
│ Customer leaves; request is forgotten  │      │ Banker gets scheduled callback queue   │
│ Customer loses trust & churns          │      │ Resolution recorded with audit trail   │
└────────────────────────────────────────┘      └────────────────────────────────────────┘
```

### Why Core Banking Systems Fail at Customer Follow-up
Traditional core banking engines (such as Finacle, Flexcube, or BaNCS) are built as accounting ledgers: they process debits and credits with high precision, but have zero native awareness of informal customer interactions at the welcome desk. When a customer walks in for a chequebook, debit card block, or address update and cannot be serviced immediately, the interaction falls into an operational black hole.

### The 4-Pillar Request Tracker Architecture
1. **30-Second Fast Intake with SLA Tiering:**
   - Pre-configured service request categories (Debit Card Block, Chequebook, Passbook, Address Change, Mobile/Email Update, NetBanking Reset).
   - Built-in SLA thresholds based on urgency:
     - **Urgent (2 Hours):** Hotlisting stolen cards & fraud security freezes.
     - **High (12 Hours):** Time-sensitive account and netbanking locks.
     - **Medium (24 Hours):** Chequebooks and deliverable dispatches.
     - **Low (48 Hours):** General address updates and re-KYC documentation.
2. **Instant Customer Transparency (Tokenization):**
   - Automatically generates a unique tracking ticket (e.g. `SR-88201`) and triggers an automated SMS and Email confirmation directly to the customer's mobile number, ending customer anxiety.
3. **Dedicated Banker Follow-Up Controls:**
   - Real-time call disposition capture: *Connected with Customer*, *Unreachable / Ringing*, *Scheduled Callback*, or *Not Initiated*.
   - Next-day follow-up date picker ensuring no ticket is orphaned.
   - Structured resolution notes box capturing the exact outcome of the conversation.
4. **Immutable Audit Timeline:**
   - Comprehensive chronological timeline recording:
     `Ticket Created` &rarr; `Assigned to Officer` &rarr; `Customer Follow-up Call Logged` &rarr; `Resolved / Closed`.
   - Ensures branch managers have complete visibility into team responsiveness and compliance.

---

## System Architecture & Branch Workflow

```
                                      ONEBANK CBS PORTAL
                                               │
         ┌───────────────────┬─────────────────┼───────────────────┬───────────────────┐
         │                   │                 │                   │                   │
   ACCOUNTS & e-KYC       DEPOSITS      LOAN ORIGINATION      REQUEST TRACKER     ANALYTICS &
   (7 Account Types)      (FD & RD)      (4-Stage Pipeline)   (Flagship Module)   BRANCH RANKING
         │                   │                 │                   │                   │
   Aadhaar & PAN       Tenure & Yield    Eligibility, CIBIL   Closed-Loop SLA,    Real-time TAT,
   Verification        Compounding       & EMI Amortization   SMS/Email Updates   CASA Growth & SLA
```

---

## Core Banking Modules (Operational Table Stakes)

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

### 4. Operations Analytics & Branch Performance
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
- **CI/CD:** Automated GitHub Actions pipeline deploying directly to GitHub Pages

---

## Live Prototype Access

Explore the live, interactive enterprise dashboard deployed on GitHub Pages:

👉 **[https://ashokkumarone.github.io/OneBank/](https://ashokkumarone.github.io/OneBank/)**

*Tip: On the Officer Authentication login screen, click **"Click here to auto-fill Manager credentials"** and **"Sign In To Portal"** to instantly access the active session for T. Nagar Branch (TN-004). Navigate to **Customer Service Hub &rarr; Request Tracker** to inspect the flagship follow-up controls.*

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
