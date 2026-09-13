# 💊 DAWAI-SETU

## Drug Availability Watch & Inter-facility Transfer Utility

> **From one empty shelf to a regional shortage — detect it early, understand how it could spread, and act before it becomes a crisis.**

---

# 📌 Problem Statement

A healthcare facility running out of an essential medicine may initially look like an isolated inventory problem, but declining stock at several facilities can be an early signal of a wider supply disruption.

Consumption patterns, replenishment delays, uneven inventories, and geographic constraints can cause shortages to spread before health authorities have enough time to respond.

Without a shared view of demand and supply:

- A facility approaching stockout may not be visible to nearby facilities.
- Surplus medicine at one facility may remain unused while another facility faces a shortage.
- Increasing consumption may go unnoticed until inventory becomes critical.
- Delayed replenishment can turn a manageable shortage into a serious disruption.
- Decision-makers may lack visibility into whether a shortage is isolated or spreading across the region.

The challenge is therefore not only to identify **where medicine is unavailable today**, but to understand:

> **How a local shortage could develop into a wider regional disruption — and what can be done before it happens.**

---

# 💡 Solution Overview

## Why DAWAI-SETU?

Medicine shortages should be addressed **before the shelf becomes empty**.

DAWAI-SETU focuses on reducing the time between an early shortage signal and an informed intervention.

Instead of looking at inventory in isolation, the system brings together:

**Stock + Consumption + Demand Trends + Replenishment + Geography**

to provide a regional picture of medicine availability and identify opportunities for early action.

---

## What is DAWAI-SETU?

DAWAI-SETU is a healthcare supply intelligence and coordination platform that:

- Monitors medicine availability across healthcare facilities.
- Forecasts future demand and potential stockouts.
- Tracks replenishment and lead times.
- Detects emerging regional shortage patterns.
- Communicates risk and forecast confidence.
- Identifies nearby facilities with available surplus.
- Recommends potential medicine redistribution.
- Supports inter-facility transfer workflows.
- Maintains an alert history for tracking and follow-up.

The goal is to move healthcare supply management from:

> **Reactive stockout response**

to:

> **Proactive shortage prevention.**

---

## How Does It Work?

text       
          INVENTORY DATA
                │
                ▼
      HISTORICAL CONSUMPTION
                │
                ▼
       DEMAND FORECASTING
                │
                ▼
      PROJECTED STOCK LEVELS
                │
        ┌───────┴────────┐
        ▼                ▼
 REPLENISHMENT       REGIONAL
 & LEAD TIME         RISK ANALYSIS
        │                │
        └───────┬────────┘
                ▼
       SHORTAGE RISK +
       CONFIDENCE LEVEL
                │
                ▼
      GEOGRAPHIC ANALYSIS
                │
                ▼
      SURPLUS IDENTIFICATION
                │
                ▼
    REDISTRIBUTION RECOMMENDATION
                │
                ▼
       TRANSFER WORKFLOW
                │
                ▼
       RISK RE-EVALUATION

---


Impact

DAWAI-SETU aims to create impact at both the facility level and the regional healthcare-network level.

1. Earlier Shortage Detection

Identify potential stockouts before inventory reaches zero, giving decision-makers more time to intervene.

2. Better Use of Existing Stock

A shortage at one facility may be solvable using surplus that already exists elsewhere in the network.

DAWAI-SETU helps make that surplus visible.

3. Reduced Risk of Regional Disruption

By analyzing multiple facilities holding the same medicine, the system can identify early signals of a wider shortage.

4. Smarter Redistribution

Recommendations consider both urgency and geography, helping identify practical sources of supply.

5. Replenishment-Aware Decisions

A facility may not need emergency redistribution if replenishment is arriving in time. Conversely, a delayed shipment may require immediate intervention.

6. Explainable Decision Support

Instead of simply showing a red warning, the system provides context around:

Why is this facility at risk?

When could it run out?

Is the problem spreading?

What intervention could help?

7. Better Regional Coordination

DAWAI-SETU creates a shared intelligence layer across healthcare facilities, enabling stakeholders to move from isolated inventory management toward coordinated regional supply management.

---

 ⚙️Key Functionalities

 
📊 Regional Command Dashboard
Provides an overall view of medicine availability and facility-level risk across the region.

💊 Medicine & Inventory Monitoring
Tracks medicine stock across facilities using information such as:

Quantity available
Reserved quantity
Daily consumption
Stock cover
Batch number
Expiry date
Last inventory update

🔮 Demand Forecasting
Analyzes historical demand and trends to estimate future consumption and potential shortages.

The forecasting engine combines:

Exponentially weighted demand estimation
Linear trend analysis
Current inventory
Projected consumption
Replenishment information
🚨 Stockout Risk Detection

Identifies facilities that may experience future stockouts and provides projected stockout timelines and risk levels.

📦 Replenishment & Lead-Time Tracking

Tracks incoming medicine supplies and evaluates whether replenishment is expected to arrive before the projected stockout.

🌐 Regional Shortage Analysis

Analyzes the same medicine across multiple facilities to determine whether a shortage is:

Isolated → Emerging → Regional

This helps visualize how a local inventory problem can potentially propagate across a network.

🧠 Confidence-Aware Forecasting

Provides confidence levels alongside predictions based on data quality, historical availability, demand variability, replenishment certainty and forecast horizon.

🗺️ Geographic Supply Mapping

Interactive regional map showing healthcare facilities and their supply/risk context.

Users can:

Zoom
Pan
Select facilities
View facility information
Identify geographically relevant supply sources
🔄 Surplus-to-Shortage Matching

Identifies facilities that may have surplus stock while another facility is approaching a shortage.

💡 Redistribution Recommendations

Generates actionable recommendations by considering:

Shortage urgency
Surplus availability
Distance
Expiry considerations
Replenishment timing
🚚 Inter-Facility Transfer Workflow

Supports:

Request → Approve → Transit → Receive

allowing the recommended intervention to be tracked through the system.

🔔 Persistent Alert History

Maintains a record of shortage and forecast-related alerts, including:

Severity
Facility
Medicine
Alert type
Projected stockout
Forecast information
Recommended action
Status
Resolution information

---

# 🏗️ System Architecture

DAWAI-SETU follows a three-layer architecture connecting the user interface, intelligence layer and database.

```text
┌─────────────────────────────────────┐
│              FRONTEND               │
│                                     │
│  Dashboard • Inventory • Map        │
│  Forecast • Risk • Recommendations  │
│  Transfers • Alerts                 │
│                                     │
│       React + TypeScript + Vite     │
└──────────────────┬──────────────────┘
                   │
                   │ REST APIs
                   ▼
┌─────────────────────────────────────┐
│               BACKEND               │
│                                     │
│  Inventory Management               │
│  Demand Forecasting                 │
│  Risk Analysis                      │
│  Regional Shortage Analysis         │
│  Replenishment & Lead Time          │
│  Recommendation Engine              │
│  Transfer & Alert Management        │
│                                     │
│      Node.js + Express + TypeScript │
└──────────────────┬──────────────────┘
                   │
                   │ Drizzle ORM
                   ▼
┌─────────────────────────────────────┐
│              DATABASE               │
│                                     │
│  Medicines • Facilities             │
│  Inventory • Demand History         │
│  Replenishments • Alerts            │
│  Transfer Records                   │
│                                     │
│            PostgreSQL               │
└─────────────────────────────────────┘

---
 
🛠️ Tech Stack

Frontend
React
TypeScript
Vite
Tailwind CSS
React Query
Recharts
Radix UI
Lucide Icons

Backend
Node.js
TypeScript
Express 5
Zod
Pino

Database
PostgreSQL
Drizzle ORM
Drizzle Kit

API & Data Layer
REST APIs
OpenAPI
Zod validation
Orval API client generation

AI / Forecasting
Historical demand analysis
Exponentially weighted demand estimation
Linear trend analysis
Stockout projection
Replenishment-aware forecasting
Regional risk analysis
Confidence scoring

---
