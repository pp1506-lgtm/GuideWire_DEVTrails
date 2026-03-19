# GuideWire_DEVTrails
# GigShield — AI-Powered Parametric Income Protection for India's Delivery Workers

---

## Table of Contents

1. [Problem Understanding](#1-problem-understanding)
2. [Persona Definition](#2-persona-definition)
3. [Real-World Scenarios of Income Loss](#3-real-world-scenarios-of-income-loss)
4. [End-to-End System Workflow](#4-end-to-end-system-workflow)
5. [Weekly Premium Model](#5-weekly-premium-model)
6. [Parametric Trigger Design](#6-parametric-trigger-design)
7. [AI/ML Integration Plan](#7-aiml-integration-plan)
8. [Tech Stack](#8-tech-stack)
9. [System Architecture](#9-system-architecture)
10. [Dashboard Design](#10-dashboard-design)
11. [Adversarial Defense & Anti-Spoofing Strategy](#11-adversarial-defense--anti-spoofing-strategy)
12. [Future Scalability Ideas](#12-future-scalability-ideas)
13. [Business Viability](#13-business-viability)
14. [Platform Choice Justification](#14-platform-choice-justification)

---

## 1. Problem Understanding

### The Ground Reality

India has over **12 million platform-based gig delivery workers** — the unsung engines powering Zomato, Swiggy, Amazon, Flipkart, Zepto, Blinkit, and Dunzo. These workers earn approximately **₹15,000–₹25,000/month** and operate entirely on a piece-rate model: no deliveries = no income.

When a disruption strikes — a sudden thunderstorm, a red-alert AQI day, a Section 144 curfew, a communal flash strike — these workers face **immediate, total income stoppage**. There is no paid leave. No employer safety net. No financial cushion.

**The core financial injury:** A food delivery partner in Mumbai loses ₹600–₹900 on a heavy rain day. That single day can represent 3–5% of their monthly income. In a month with multiple disruption events (e.g., monsoon season in Chennai or Delhi's November smog), cumulative losses can reach **₹3,000–₹5,000 per worker per month**.

### Why Existing Insurance Fails Them

| Existing Product | Why It Fails |
|---|---|
| Traditional term insurance | Only covers death/disability, not income disruption |
| Micro-health insurance | Covers hospitalisation, not lost wages |
| Vehicle insurance | Covers repair costs, not income |
| Government welfare schemes | Require paperwork, long wait times, not real-time |
| Employer-provided cover | Platforms classify them as "partners" not employees — no obligation |

### The Opportunity

**GigShield** bridges this gap with a purely **parametric, income-protection** product: pre-defined external disruption thresholds automatically trigger a payout to the worker's UPI — no paperwork, no claim filing, nothing to fill out. If the IMD data crosses the agreed threshold, the money moves. That's the whole promise, and it's one the existing insurance market has completely failed to make.

---

## 2. Persona Definition

### Chosen Persona: Food Delivery Partner (Zomato / Swiggy)

**Why this persona?**
- Highest disruption sensitivity: food delivery demand spikes or collapses instantly with weather
- Highest volume: ~5 million active food delivery partners in India
- Shortest earning cycle: workers check earnings daily/hourly — weekly premium aligns naturally
- Highest informal workforce density: most workers have no formal employment contract

### Persona Profile: "Ravi"

| Attribute | Detail |
|---|---|
| **Name** | Ravi Kumar |
| **Age** | 26 |
| **Platform** | Zomato (primary), Swiggy (secondary) |
| **Vehicle** | Electric two-wheeler (leased) |
| **Daily Hours** | 10–12 hours (7 AM–11 AM, 6 PM–12 AM peak blocks) |
| **Avg. Weekly Earnings** | ₹4,000–₹5,500 (varies with surge and season) |
| **Weekly Fixed Costs** | ₹600 (vehicle EMI/lease), ₹300 (fuel/charging), ₹500 (rent daily share) |
| **Digital Literacy** | Uses Zomato/Swiggy app fluently; comfortable with UPI (PhonePe/GPay) |
| **Language** | Kannada (primary), Hindi (functional) |
| **Pain Point** | Earns nothing on rainy days but still pays fixed costs — one bad week wipes his buffer |
| **Insurance Awareness** | Never purchased any; finds it "complicated and expensive" |
| **Ideal Product UX** | WhatsApp-friendly, UPI-based, no paperwork, under 2 minutes to enroll |

### Why Ravi?

Ravi is the median food delivery worker in a Tier-1 Indian city. Digitally comfortable enough to use Zomato daily, financially fragile enough that one bad week forces him to borrow from family. He's never bought insurance in his life — not because he doesn't need it, but because every product he's ever seen required forms, agents, and a monthly commitment that felt like a luxury. He trusts a UPI transfer. He doesn't trust an insurance company. GigShield is built to earn that trust through simplicity: enroll in 2 minutes, pay ₹42 a week, get money back when it rains. That's it.

---

## 3. Real-World Scenarios of Income Loss

### Scenario 1: Mumbai Monsoon Flash Flood (July–September)

**Event:** IMD issues a Red Alert for Mumbai. Rainfall exceeds 65mm in 3 hours. Zomato and Swiggy suspend deliveries in 80% of zones between 2 PM–9 PM.

**Ravi's Loss:**
- Lost 7 hours of peak earnings (dinner rush completely wiped)
- Typical dinner-rush earnings: ₹350–₹450
- Total loss for that disruption window: ~₹400

**Without GigShield:** Ravi earns ₹0, still pays ₹85 (daily EMI share), goes to bed stressed.
**With GigShield:** System detects Red Alert + delivery suspension signal → auto-triggers payout of ₹350 to Ravi's UPI within 12 minutes.

---

### Scenario 2: Delhi Winter Smog — AQI Emergency (November–December)

**Event:** Delhi's AQI crosses 400 (Severe+ category). GRAP Stage 4 restrictions imposed. Outdoor movement advisory issued. Delivery platforms reduce active delivery zones by 60%.

**Ravi's Loss (Delhi variant):**
- Cannot work safely for 2 full days
- Lost income: ₹700–₹900

**Without GigShield:** Ravi either risks health by working or loses ₹800.
**With GigShield:** AQI trigger threshold (>400, sustained 4+ hours) fires → payout of ₹400/qualifying day credited directly.

---

### Scenario 3: Bengaluru Bandh / Section 144 Curfew

**Event:** Sudden political protests or cauvery water disputes lead to a city-wide bandh. Section 144 imposed across 3 districts. Zomato/Swiggy pause all operations in affected pin codes for 6+ hours.

**Ravi's Loss:**
- Lost 6 hours mid-day + evening window
- Estimated loss: ₹300–₹500

**Without GigShield:** No recourse. Loss absorbed.
**With GigShield:** Civic disruption trigger (verified via news API + platform operational pause signal) fires → proportional payout issued.

---

### Scenario 4: Cyclone Warning — Coastal Tamil Nadu / Odisha

**Event:** IMD issues a Cyclone Warning (Category 2) for Chennai. Mandatory evacuation advisories. Delivery completely suspended 12 hours before landfall through 24 hours after.

**Ravi's Loss:**
- 36-hour blackout: lost ~₹1,500–₹2,000

**With GigShield:** Cyclone alert trigger (IMD Cyclone Warning + sustained wind speed data) fires → maximum weekly benefit cap payout issued.

---

### Scenario 5: Platform App Downtime (Extended, >4 hours)

**Event:** Zomato faces a major backend outage. App is non-functional for 5+ hours during peak dinner slot. Workers cannot accept orders.

**Ravi's Loss:**
- Lost prime earning window: ₹250–₹400

**Note:** This trigger is platform-dependent and would require platform API integration (Phase 2 extension). Included here as a future parametric trigger concept.

---

## 4. End-to-End System Workflow

```
┌─────────────────────────────────────────────────────────────────┐
│                     GIGSHIELD SYSTEM FLOW                       │
└─────────────────────────────────────────────────────────────────┘

 ┌──────────────────────────────────────────────────────────────┐
 │  STEP 1: ONBOARDING                                          │
 │                                                              │
 │  Worker opens GigShield app (mobile) or WhatsApp bot         │
 │  → Enters phone number (OTP via SMS)                         │
 │  → Selects platform (Zomato / Swiggy)                        │
 │  → Grants location access (for zone mapping)                 │
 │  → Provides Aadhaar number (KYC via Aadhaar e-KYC API)       │
 │  → Links UPI ID (PhonePe / GPay / Paytm)                     │
 │  → App fetches 8-week historical earnings via                 │
 │     platform API integration (or manual entry fallback)      │
 │                                                              │
 └───────────────────────────┬──────────────────────────────────┘
                             │
                             ▼
 ┌──────────────────────────────────────────────────────────────┐
 │  STEP 2: AI RISK PROFILING                                   │
 │                                                              │
 │  ML Risk Engine runs:                                        │
 │  → City / pin code zone risk score (flood/AQI history)       │
 │  → Individual earnings stability score (variance analysis)   │
 │  → Platform tenure score (< 3 months = higher risk tier)     │
 │  → Historical disruption exposure in their primary zone      │
 │  → Output: Risk Tier (LOW / MEDIUM / HIGH)                   │
 │     → Maps directly to weekly premium tier                   │
 │                                                              │
 └───────────────────────────┬──────────────────────────────────┘
                             │
                             ▼
 ┌──────────────────────────────────────────────────────────────┐
 │  STEP 3: POLICY CREATION                                     │
 │                                                              │
 │  Worker sees their personalised policy card:                 │
 │  → Weekly premium (e.g., ₹49 / week)                        │
 │  → Coverage amount (e.g., ₹500 per qualifying event)         │
 │  → Maximum weekly benefit (e.g., ₹1,000)                    │
 │  → Covered triggers listed in plain language (Hindi/English) │
 │  → Worker taps "Activate" → auto-debit set up via UPI AutoPay│
 │                                                              │
 └───────────────────────────┬──────────────────────────────────┘
                             │
                             ▼
 ┌──────────────────────────────────────────────────────────────┐
 │  STEP 4: CONTINUOUS TRIGGER MONITORING (Background)          │
 │                                                              │
 │  Every 15 minutes, the Trigger Engine checks:               │
 │  → IMD Weather API: rainfall, wind, AQI levels              │
 │  → CPCB AQI API: pollution index per city                   │
 │  → Government / News API: curfew / bandh advisories         │
 │  → Platform operational status (if API available)           │
 │                                                              │
 │  For each active policy, system checks:                     │
 │  → Is the worker's registered zone inside the alert area?   │
 │  → Has the threshold been met for the required duration?    │
 │  → Is this worker's policy currently in force (paid)?       │
 │                                                              │
 └───────────────────────────┬──────────────────────────────────┘
                             │
                             ▼
 ┌──────────────────────────────────────────────────────────────┐
 │  STEP 5: ANTI-FRAUD VALIDATION (Pre-Payout)                  │
 │                                                              │
 │  Fraud Detection Engine runs simultaneously:                 │
 │  → Behavioral signal cross-check (is device stationary?)    │
 │  → GPS consistency check (multi-signal, not just one point)  │
 │  → Network signal validation (Cell tower + WiFi alignment)   │
 │  → Peer cohort check (are other workers in zone claiming?)   │
 │  → Historical pattern analysis (anomaly score)              │
 │                                                              │
 │  Output: Trust Score (0–100)                                │
 │  → >70: Auto-approve                                        │
 │  → 40–70: Soft verification (1-tap confirmation request)    │
 │  → <40: Manual review queue                                 │
 │                                                              │
 └───────────────────────────┬──────────────────────────────────┘
                             │
                             ▼
 ┌──────────────────────────────────────────────────────────────┐
 │  STEP 6: INSTANT PAYOUT                                      │
 │                                                              │
 │  Auto-approved claims:                                       │
 │  → Razorpay / UPI transfer initiated                        │
 │  → Worker receives push notification + SMS                  │
 │  → "₹350 credited to your PhonePe for rain disruption       │
 │     on [date]. Stay safe 🙏"                                │
 │  → Payout typically within 8–15 minutes of trigger fire      │
 │                                                              │
 └───────────────────────────┬──────────────────────────────────┘
                             │
                             ▼
 ┌──────────────────────────────────────────────────────────────┐
 │  STEP 7: ANALYTICS & FEEDBACK                                │
 │                                                              │
 │  Worker Dashboard: earnings protected, policy status         │
 │  Admin Dashboard: claims volume, fraud flags, loss ratios   │
 │  ML Feedback Loop: claims data improves future pricing       │
 │                                                              │
 └──────────────────────────────────────────────────────────────┘
```

---

## 5. Weekly Premium Model

### Why Weekly?

Food delivery workers in India think about money weekly, not monthly. Zomato and Swiggy pay partners every Tuesday. A monthly insurance premium feels like a painful upfront commitment — ₹200/month sounds expensive. The same money spread as ₹49/week feels like skipping a vada pav. That's not a gimmick; it's how people in this income bracket actually budget. Aligning the premium cycle with the income cycle is what makes people actually stay enrolled instead of cancelling after the first payment.

### Premium Calculation Framework

**Base Formula:**

```
Weekly Premium = Base Rate × Zone Risk Multiplier × Earnings Band Multiplier × Tenure Discount
```

**Component Definitions:**

| Component | Description | Example Values |
|---|---|---|
| **Base Rate** | Platform-wide floor premium | ₹35/week |
| **Zone Risk Multiplier** | 0.8–1.5× based on historical disruption frequency in worker's pin code cluster | High-flood zone: 1.4× / Low-risk zone: 0.9× |
| **Earnings Band Multiplier** | Scales coverage proportionally to average weekly earnings | ₹2,000–3,000/week band: 1.0×; ₹4,000–5,500 band: 1.3× |
| **Tenure Discount** | Loyalty reduction for workers active >6 months with no fraudulent claims | -10% after 6 months, -15% after 12 months |

### Premium Tiers (Illustrative)

| Tier | Worker Profile | Weekly Premium | Per-Event Payout | Weekly Benefit Cap |
|---|---|---|---|---|
| **Starter** | New worker, low-risk zone, earnings < ₹3,000/week | ₹29 | ₹200 | ₹600 |
| **Standard** | 3+ months tenure, medium-risk zone, earnings ₹3,000–₹4,500/week | ₹49 | ₹350 | ₹900 |
| **Shield+** | 6+ months tenure, high-risk zone (Mumbai/Chennai coastal), earnings > ₹4,500/week | ₹79 | ₹500 | ₹1,400 |

### Worked Example: Ravi's Policy

```
Ravi's Profile:
  → City: Bengaluru (Koramangala zone — moderate flood risk)
  → Avg. weekly earnings: ₹4,200
  → Tenure: 8 months on Zomato
  → Zone Risk Multiplier: 1.1× (moderate risk)
  → Earnings Band Multiplier: 1.2×
  → Tenure Discount: 10%

Calculation:
  Base Rate:              ₹35.00
  × Zone Multiplier:      × 1.10  = ₹38.50
  × Earnings Multiplier:  × 1.20  = ₹46.20
  × Tenure Discount:      × 0.90  = ₹41.58

  Rounded Weekly Premium: ₹42/week

  Per-event payout:       ₹350
  Weekly benefit cap:     ₹900

  Annual premium cost:    ₹42 × 52 = ₹2,184/year
  Maximum annual benefit: ₹900 × 52 = ₹46,800/year
  Coverage ratio:         21.4× — Exceptional value
```

### UPI AutoPay Integration

- Worker sets up NPCI UPI AutoPay mandate (₹500 weekly max) during onboarding
- Premium debited every Monday morning (start of coverage week)
- If debit fails: 48-hour grace period → reminder sent → policy pauses (not cancelled)
- Worker can pause/resume weekly — no lock-in, no exit penalty

---

## 6. Parametric Trigger Design

A **parametric trigger** is a pre-agreed objective threshold that, once crossed by verified external data sources, automatically initiates a claim. No worker action required.

### Trigger 1: Heavy Rainfall / Flood Alert

| Parameter | Value |
|---|---|
| **Data Source** | IMD (India Meteorological Department) Open API; OpenWeatherMap |
| **Trigger Condition** | Cumulative rainfall > 50mm in 3 hours **OR** IMD issues Orange/Red Alert for the worker's district |
| **Minimum Duration** | Alert must be active for ≥ 2 continuous hours during 7 AM – 11 PM window |
| **Geographic Resolution** | Pin code cluster level (worker's registered operational zone) |
| **Payout** | 100% of per-event amount if ≥ 4 hours disruption; 50% for 2–4 hours |
| **Exclusion** | Worker must have been active on the platform in the 6 hours prior to trigger (verified via app activity) |

**Why this works:** IMD rainfall data is real-time, publicly verifiable, and cannot be spoofed. Cross-referencing with platform order drop-off data provides dual validation.

---

### Trigger 2: Extreme Air Quality (AQI Emergency)

| Parameter | Value |
|---|---|
| **Data Source** | CPCB (Central Pollution Control Board) AQI API; IQAir |
| **Trigger Condition** | AQI index > 400 ("Severe+" category) for the worker's city zone |
| **Minimum Duration** | Sustained ≥ 4 hours during working hours |
| **Geographic Resolution** | City district level (AQI monitoring station nearest to worker's zone) |
| **Payout** | ₹150 per qualifying half-day (up to 2 half-days per week) |
| **Applicability** | Delhi NCR, Mumbai, Kolkata, Lucknow (high-frequency AQI disruption cities) |

**Business Logic:** GigShield does not cover mild pollution days. Only emergency-level AQI that meaningfully reduces outdoor work safety triggers payout. This keeps loss ratios manageable.

---

### Trigger 3: Civic Disruption (Curfew / Bandh / Section 144)

| Parameter | Value |
|---|---|
| **Data Source** | Government notification APIs; NewsAPI (verified sources: PTI, ANI, government portals); Zomato/Swiggy zone-pause signal |
| **Trigger Condition** | Official government order (Section 144 / bandh declaration) for worker's district, verified from ≥ 2 sources |
| **Minimum Duration** | ≥ 3 hours during working window |
| **Geographic Resolution** | District/ward level |
| **Payout** | Full per-event payout |
| **Anti-Fraud Note** | This is the highest-fraud-risk trigger. Requires triple validation: (a) official government source, (b) platform operational status change, (c) peer worker inactivity pattern. |

---

### Trigger 4: Cyclone / Severe Storm Warning

| Parameter | Value |
|---|---|
| **Data Source** | IMD Cyclone Alert API; NDMA alerts |
| **Trigger Condition** | IMD issues Cyclone Watch or Warning for worker's coastal district |
| **Coverage Window** | From warning issuance → 24 hours post all-clear |
| **Geographic Scope** | Workers registered in coastal districts of Tamil Nadu, Odisha, Andhra Pradesh, Maharashtra, West Bengal |
| **Payout** | Maximum weekly benefit cap triggered in one event (severe disruption = multi-day) |

---

### Trigger 5: Heatwave Advisory (New — Innovation Addition)

| Parameter | Value |
|---|---|
| **Data Source** | IMD Heat Action Plan alerts; Accuweather API |
| **Trigger Condition** | Temperature > 45°C AND IMD issues a Heatwave Warning for ≥ 2 consecutive days |
| **Context** | Increasingly relevant: Rajasthan, UP, Bihar, Delhi — May/June |
| **Payout** | ₹100/day per qualifying heatwave day (partial coverage — worker can still do early morning deliveries) |
| **Rationale** | Heatwave doesn't fully stop deliveries but meaningfully reduces earning hours (workers avoid 11 AM–5 PM slot). Partial payout is fair and sustainable. |

---

### Trigger Summary Table

| Trigger | Source | Threshold | Payout Type | Fraud Risk |
|---|---|---|---|---|
| Heavy Rain / Flood | IMD API | >50mm / 3hr or Red Alert | Full / 50% proportional | Low |
| Severe AQI | CPCB API | AQI > 400 for 4hr | Fixed per half-day | Low |
| Civic Disruption | Govt + News API | Official order, ≥2 sources | Full event payout | High |
| Cyclone Warning | IMD Cyclone API | Watch/Warning issued | Weekly cap payout | Very Low |
| Heatwave | IMD Heat Action | >45°C + official warning | Partial daily payout | Low |

---

## 7. AI/ML Integration Plan

### 7.1 Risk Scoring Model

**Objective:** Generate a personalised risk score (0–100) for each worker at onboarding, updated weekly.

The core idea is straightforward: not all delivery workers face the same risk. Someone working in Dharavi during Mumbai's monsoon season is genuinely more exposed than someone working in a low-flood zone of Pune. The risk score captures that difference and feeds it into their premium.

**Input Features:**

```
Geographic Features:
  - Pin code cluster flood history (last 3 years, IMD archives)
  - AQI frequency score (days > 300 AQI per year in city)
  - Cyclone track proximity (for coastal workers)
  - Historical bandh/curfew frequency per city/district

Worker-Level Features:
  - Avg. weekly earnings (₹)
  - Earnings variance (coefficient of variation)
  - Platform tenure (months)
  - Number of platforms active on
  - Average daily active hours
  - Peak hours worked (evening/night = higher rain exposure)

Behavioral Features:
  - Consistency score (works 5–7 days/week vs. sporadic)
  - Zone concentration (works in 1–2 zones vs. spread across city)
```

**Model:** Gradient Boosted Decision Tree (XGBoost)
- Why XGBoost: handles tabular data well, highly interpretable via SHAP values, fast inference
- Training data: synthetic historical data in Phase 1; real platform data via API integration in later phases
- Output: Risk score → maps to premium tier (Low: 0–33, Medium: 34–66, High: 67–100)

**SHAP Explainability:** Every worker's risk score comes with a plain-language explanation:
> "Your premium is slightly higher because your delivery zone (Dharavi, Mumbai) has a history of flooding 8+ times per year."

---

### 7.2 Dynamic Pricing Engine

**Objective:** Nudge next week's premium up or down based on the actual disruption forecast for the coming 7 days.

The logic is simple: if a major storm is likely next week, the insurer's expected claims go up — so the premium goes up a little to stay solvent. If it's going to be a clear, dry week, the premium dips slightly as a loyalty reward. Workers see this as transparency, not manipulation, because the forecast is publicly available (it's IMD data) and the adjustment is small — typically ±10–15%.

**Mechanism:**

```
Dynamic Premium = Base Premium × (1 + Disruption Forecast Multiplier)

Disruption Forecast Multiplier:
  - Input: 7-day weather forecast (OpenWeatherMap API)
  - Input: IMD seasonal outlook
  - Input: Known upcoming civic events (election schedules, festival dates)
  - Model: Logistic regression → P(disruption event in next 7 days)
  - If P(disruption) > 0.6: Multiplier = +15% (insurer manages exposure)
  - If P(disruption) < 0.2: Multiplier = -10% (reward low-risk week → worker loyalty)
```

**Example:**
> It's October 25th. IMD forecasts heavy rain for Bengaluru on Oct 27–28. P(disruption) = 0.72. Ravi's standard premium of ₹42 adjusts to ₹48 for that week. The system notifies him: "Rains expected next week. Your coverage is ready. Premium this week: ₹48."

**Anti-Adverse-Selection Control:** To prevent workers from subscribing only when they know a big storm is coming, the system enforces a 48-hour pre-event enrollment lockout. If a Red Alert is already active at enrollment time, the worker's first eligible claim can only be for a trigger starting 48 hours after enrollment.

---

### 7.3 Fraud Detection

**Objective:** Catch false claims before payout, without creating friction for genuine workers.

The fraud problem for a parametric product is different from traditional insurance. There's no claim form to scrutinise, no assessor to send out. The payout is automatic. That means the fraud detection has to happen before the money moves — ideally in the background, invisible to honest workers.

The full architecture for this is covered in Section 11 (Adversarial Defense). At the model level, we use an Isolation Forest for anomaly detection — unsupervised, so it doesn't need a labelled fraud dataset to get started — with movement trajectory coherence and platform activity as the primary input signals.

---

## 8. Tech Stack

### Frontend (Mobile — Primary Platform)

| Layer | Technology | Rationale |
|---|---|---|
| Mobile App | React Native | Single codebase for Android + iOS; 90% of gig workers use Android |
| UI Framework | NativeBase / Tamagui | Lightweight, accessible components |
| State Management | Zustand | Simple, minimal boilerplate for gig-worker app scale |
| Localization | i18next | Hindi, Kannada, Tamil, Bengali support from Day 1 |
| Push Notifications | Firebase Cloud Messaging (FCM) | Real-time payout alerts |
| Offline Support | React Query + AsyncStorage | Workers in poor connectivity areas can still view policy |

### Backend

| Layer | Technology | Rationale |
|---|---|---|
| API Server | Node.js + Express (TypeScript) | High I/O throughput for trigger monitoring; strong ecosystem |
| Background Jobs | BullMQ + Redis | Reliable queue for trigger evaluation jobs (every 15 min) |
| Authentication | Firebase Auth (Phone OTP) + JWT | Phone number-first auth — no passwords |
| KYC | Aadhaar e-KYC API (Signzy / Karza) | Regulatory compliance; sub-2-minute onboarding |
| Payments | Razorpay (UPI AutoPay + Payouts) | Supports UPI mandate + instant payout to UPI handles |

### ML / AI

| Component | Technology | Rationale |
|---|---|---|
| Risk Scoring | Python (scikit-learn / XGBoost) | Industry-standard, fast training and inference |
| Dynamic Pricing | Python (statsmodels + Prophet for forecasting) | Time-series disruption forecasting |
| Anomaly Detection | Python (Isolation Forest — scikit-learn) | Unsupervised, doesn't need labelled fraud data initially |
| Graph Fraud Detection | Python (PyTorch Geometric / NetworkX) | Detects ring structures in claim submission graphs |
| Model Serving | FastAPI + Docker | REST endpoint for ML inference, containerised for scaling |
| Feature Store | Redis (real-time) + PostgreSQL (historical) | Sub-10ms feature lookup during claim validation |

### External APIs

| API | Purpose | Tier Used |
|---|---|---|
| IMD Open Data API | Rainfall, cyclone, heatwave alerts | Free |
| CPCB AQI API | Real-time Air Quality Index | Free |
| OpenWeatherMap | 7-day forecast for dynamic pricing | Free tier (mock for Phase 1) |
| NewsAPI | Civic disruption detection | Developer tier |
| Google Maps Geocoding | Pin code → lat/lng mapping | Standard tier |

### Infrastructure

| Component | Technology |
|---|---|
| Cloud | AWS (Mumbai region — data residency compliance) |
| Container Orchestration | Docker + AWS ECS (Fargate) |
| Database | PostgreSQL (RDS) + Redis (ElastiCache) |
| Storage | AWS S3 (KYC documents, model artifacts) |
| Monitoring | Datadog + PagerDuty |
| CI/CD | GitHub Actions |

---

## 9. System Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│                        GIGSHIELD ARCHITECTURE                       │
└─────────────────────────────────────────────────────────────────────┘

  [Worker's Phone]
       │  React Native App (Android/iOS)
       │  WhatsApp Bot (fallback)
       │
       ▼
  ┌────────────────────────────────────────────────────────────────┐
  │                      API GATEWAY (AWS API GW)                  │
  │           Auth → Rate Limiting → Request Routing               │
  └───────────────┬────────────────────────────────────────────────┘
                  │
       ┌──────────┴──────────┐
       ▼                     ▼
  ┌──────────┐         ┌───────────────┐
  │  Core    │         │  ML Service   │
  │  API     │         │  (FastAPI)    │
  │ (Node.js)│◄───────►│               │
  └──────────┘         │ - Risk Score  │
       │               │ - Dyn. Price  │
       │               │ - Fraud Score │
       │               └───────────────┘
       │
  ┌────▼────────────────────────────────────────────┐
  │              CORE SERVICES LAYER                │
  │                                                 │
  │  ┌─────────────┐  ┌──────────────┐              │
  │  │  Onboarding │  │  Policy Mgmt │              │
  │  │  Service    │  │  Service     │              │
  │  └─────────────┘  └──────────────┘              │
  │                                                 │
  │  ┌─────────────┐  ┌──────────────┐              │
  │  │  Trigger    │  │  Claims &    │              │
  │  │  Engine     │  │  Payout Svc  │              │
  │  └─────────────┘  └──────────────┘              │
  └──────────────────────────────────────┬──────────┘
                                         │
  ┌──────────────────────────────────────▼──────────┐
  │              DATA LAYER                         │
  │                                                 │
  │  PostgreSQL (RDS)     Redis (ElastiCache)        │
  │  - Workers            - Session cache           │
  │  - Policies           - Feature store           │
  │  - Claims             - Job queues (BullMQ)     │
  │  - Payouts            - Rate limit counters     │
  │  - Audit logs                                   │
  └─────────────────────────────────────────────────┘

  ┌──────────────────────────────────────────────────┐
  │          EXTERNAL INTEGRATIONS                   │
  │                                                  │
  │  IMD API → Trigger Engine                        │
  │  CPCB API → Trigger Engine                       │
  │  NewsAPI → Civic Disruption Detector             │
  │  Razorpay → Claims & Payout Service              │
  │  Aadhaar e-KYC → Onboarding Service              │
  │  Firebase → Auth + Notifications                │
  └──────────────────────────────────────────────────┘

  ┌──────────────────────────────────────────────────┐
  │          BACKGROUND JOBS (BullMQ)                │
  │                                                  │
  │  - Trigger Monitor Job (every 15 min)            │
  │  - Premium Debit Job (every Monday 6 AM)         │
  │  - Weekly Risk Re-Score Job (every Sunday)       │
  │  - Fraud Graph Analysis Job (post-claim batch)   │
  └──────────────────────────────────────────────────┘
```

### Key Architectural Decisions

**Mobile-first (not web):** 94% of gig workers access internet exclusively via smartphone. A mobile app with offline cache and WhatsApp fallback maximises reach.

**Microservices-lite:** Not a full microservices architecture (over-engineered for Phase 1), but a services-oriented monolith with clear domain boundaries, ready to split as volume scales.

**ML Inference as a Sidecar:** The ML service is a separate FastAPI container. This allows independent scaling, model updates without redeploying the core API, and isolation of Python ML dependencies from the Node.js backend.

**BullMQ for Reliability:** Trigger evaluation is a background job, not an inline API request. This ensures that even if the API server is under load, trigger checks run reliably. Jobs are idempotent (safe to retry on failure).

---

## 10. Dashboard Design

### Worker Dashboard (Mobile App)

**Home Screen — "Your Shield"**
```
┌────────────────────────────────────────┐
│  🛡️ GigShield                   [Ravi] │
├────────────────────────────────────────┤
│                                        │
│  ✅ SHIELD ACTIVE                      │
│  Covered until: Sunday, Mar 29         │
│  Premium paid: ₹42 this week           │
│                                        │
│  ┌──────────┬─────────────────────┐   │
│  │ ₹3,850   │ ₹900                │   │
│  │ Protected │ Max this week       │   │
│  │ this year │                     │   │
│  └──────────┴─────────────────────┘   │
│                                        │
│  🌧️ WEATHER ALERT                      │
│  Heavy rain expected Wed–Thu           │
│  Your coverage is ready ✓              │
│                                        │
│  Recent Payouts:                       │
│  Mar 15: ₹350 (Rain) — Credited ✓     │
│  Feb 28: ₹350 (Rain) — Credited ✓     │
│                                        │
│  [Pause Shield]   [Claim History]      │
└────────────────────────────────────────┘
```

**Claim Notification (Push + In-App):**
> 🛡️ **GigShield Payout Sent!**
> ₹350 has been credited to ravi@phonepe for the Mumbai Red Alert rain disruption on Mar 15. Stay safe! 🌧️

---

### Admin / Insurer Dashboard (Web)

**Overview Panel:**
- Total active policies: real-time count
- Weekly premium collected: ₹ total
- Active trigger events: live map view
- Claims processing queue: pending / auto-approved / flagged counts
- Estimated payout liability: ₹ for current active events
- Loss ratio: (total payouts / total premiums collected) × 100
- Fraud prevention savings: ₹ blocked via fraud detection this month

**Real-Time Trigger Map:**
- India map with pin code heat overlay showing active disruption zones
- Color-coded severity (yellow = watch, orange = warning, red = alert)
- Click zone → see affected policy count + estimated payout

**Claims Fraud Queue:**
- Sortable table: fraud_score, claim_amount, worker_id, signals
- One-click approve / reject with reason capture
- Flag for investigation → creates case file

**Predictive Analytics Panel:**
- Next 7-day disruption probability by city (from ML forecast)
- Projected claim volume and payout liability for next week
- Premium adequacy check: is current pricing covering predicted claims?

---

## 11. Adversarial Defense & Anti-Spoofing Strategy

> The threat: a coordinated syndicate fakes GPS location inside a Red Alert zone and drains the liquidity pool via mass auto-payouts. Simple GPS verification is obsolete. Our defense requires faking multiple independent signals simultaneously — which is where the attack falls apart.

### 11.1 Differentiating a Real Claim from a Spoofed One

- GPS tells you where a device *claims* to be. Movement patterns tell you where a person *actually was* — much harder to fake simultaneously
- A real worker has a 2-hour delivery trail leading up to the disruption: pickup stops, drop points, road-consistent movement within their registered zone
- A spoofer's trace shows them stationary at home all morning, then their coordinate teleports inside the disaster zone the moment the trigger fires — no trail, no delivery history in that area
- The system evaluates the **2-hour movement window before the trigger** as the primary differentiator
- No delivery activity in the claimed zone in that window = first flag; not proof alone, but the foundation of the fraud score

### 11.2 Data Signals Beyond GPS

**Movement & Location Trajectory (Primary Signal)**
- GPS path continuity check: genuine workers show road-consistent movement; spoofed coordinates produce physically impossible jumps
- Speed plausibility: a two-wheeler cannot move 8km in 4 minutes — location teleportation is an automatic flag
- Zone consistency: worker's location at trigger time must be coherent with where they were heading based on prior movement
- 2-hour pre-trigger trace must show activity within the registered operational zone

**Platform Activity (Independent Ground Truth)**
- Zomato/Swiggy order logs provide timestamps, pickup and drop GPS — entirely independent of our system
- Zero platform activity in the claimed zone in the past 6 hours = no external corroboration the worker was ever there
- A worker with both a clean movement trail *and* recent platform delivery activity in the affected zone is almost certainly genuine

**Submission Timing Patterns**
- Claims in GigShield are auto-triggered — no worker "files" anything, so there is no natural submission timestamp from the worker
- Worker opening the GigShield app multiple times in the 30 minutes before trigger = behavioural flag (genuine workers in a storm aren't monitoring an insurance app)
- 50+ workers having claims created within a 90-second window = coordinated ring signature; legitimate claims trickle in as the system processes zone by zone

### 11.3 UX for Flagged Claims — Protecting Honest Workers

**Trust Score > 70 — Auto-approve**
- Payout initiated immediately, worker gets a notification, no action required

**Trust Score 40–70 — One soft check**
- Payout held for up to 4 hours
- Worker receives a neutral (not accusatory) message: *"We're processing your payout. Just a quick check — were you unable to work today because of the weather? [Yes, I couldn't work] [Contact Support]"*
- One tap → payout released immediately
- No response within 4 hours → payout goes through anyway (benefit of doubt to the worker)
- Designed specifically for genuine workers with bad signal days, choppy GPS, or phone that died in the rain

**Trust Score < 40 — Human review**
- Claim goes to reviewer queue; worker notified of 24-hour review window
- Reviewer can call the worker directly; full signal data available
- If approved: payout sent + ₹10 goodwill credit for the wait
- If rejected: plain-language explanation given + in-app appeal option (worker can upload a photo of their actual situation)
- Goal: fraud detection stays invisible to honest workers; no genuine worker ever feels accused

---

## 12. Future Scalability Ideas

**Expand to other delivery personas**
- Grocery/Q-Commerce (Zepto, Blinkit): 24x7 operations, different peak hours, night-time cyclone exposure
- E-commerce (Amazon, Flipkart): longer routes, warehouse-zone strikes, highway closures
- Each persona gets its own trigger calibration and risk model on the same core infrastructure

**Hyper-local risk pools**
- Move from pin code cluster level to individual pin code level
- Workers in historically high-flood corridors pay more than workers 3km away who never flood
- Makes pricing fairer and loss ratios more predictable

**Crew-based coverage**
- Allow 5–10 workers who know each other to pool premiums
- Workers who don't claim in a month get a small rebate — peer accountability no ML model can replicate
- Proven model in African and Southeast Asian micro-insurance contexts

**Platform-embedded distribution (B2B2C)**
- White-label GigShield as a native benefit inside Zomato/Swiggy partner apps
- Premium deducted directly from weekly earnings — zero separate payment friction
- Reaches 5M+ workers at near-zero acquisition cost; platforms get a genuine retention tool

**Voice-based onboarding**
- WhatsApp voice bot enrollment in Hindi, Kannada, Tamil, Bengali
- Covers workers in Tier-3 cities and older workers less comfortable with apps

**Predictive pre-warning**
- 72-hour disruption forecasts pushed to workers: *"Heavy rain expected Thursday — your Shield activates automatically"*
- Builds trust, reduces surprise, and is a tangible retention driver

---

## 13. Business Viability

**Market Size**
- 12M+ gig delivery workers in India, growing at 25% CAGR
- 5% penetration = 600,000 active weekly policies
- At ₹42/week average: ₹25M+ weekly premium volume at scale

**Unit Economics (per worker, per year)**
```
Annual premium revenue:          ₹42 × 52 = ₹2,184
Expected payouts (45% loss ratio):          ₹982
Gross profit per worker:                    ₹1,202
Operating cost per worker:                  ₹400
Net contribution:                           ₹800

At 100,000 workers → ~₹80M annual net contribution
```

**Why workers will pay**
- ₹42/week = cost of 3 cups of chai; feels affordable against ₹400–₹800 lost on a single rain day
- Workers already know exactly what disruption days cost them — not an abstract risk
- UPI AutoPay means set-and-forget; most micro-insurance lapses because people forget to pay
- Weekly debit aligns with weekly income — no monthly budget strain

**Why insurers will partner**
- No assessors, no dispute process — trigger either fired or it didn't; claims cost is near-zero
- ML risk scoring gives actuaries visibility they don't get from traditional gig worker products
- Dynamic pricing keeps loss ratios manageable week-to-week
- GigShield handles distribution and tech; insurer provides balance sheet and regulatory cover

**Regulatory path**
- IRDAI sandbox framework explicitly covers parametric products
- Bima Sugam (launched 2024) provides digital micro-insurance distribution infrastructure
- Model: GigShield as insurtech layer + licensed non-life insurer (New India Assurance, HDFC ERGO) as underwriter

---

## 14. Platform Choice Justification

**Primary: Mobile App (React Native) — Secondary: WhatsApp Bot**

**Why mobile over web**
- 94% of gig workers access the internet exclusively via smartphone
- Background location collection (needed for movement trail fraud detection) is only possible in a native app — a web app cannot do this
- Push notifications for payout alerts require native app; PWA notifications are unreliable on Android
- UPI AutoPay mandate setup works natively in-app
- Workers already use Zomato/Swiggy apps daily — no new mental model to learn

**Why WhatsApp as fallback**
- 600M+ Indians use WhatsApp; workers who won't download another app can still enroll
- Full enrollment flow possible via WhatsApp Business API: earnings entry, UPI linking, payment mandate
- Better regional language support for Tier-3 onboarding
- Workers onboarded through WhatsApp get a slightly simpler fraud scoring path (no background location) but remain fully covered

**Why not web-only**
- Cannot access device sensors required for movement trail analysis
- No native UPI mandate UI
- Unreliable push notifications on Android (dominant OS for this user base)
- Poor UX loading a web app on a 4G connection during an active rainstorm

---

*Submission by: [Your Team Name] | DEVTrails 2026 | Guidewire University Hackathon | Phase 1 Deadline: March 20, 2026*

*Built with ❤️ for India's 12 million gig workers*
