# Bravo Pricing Risk Intelligence

## Executive Summary

This project presents an end-to-end **Pricing Risk Intelligence framework** designed to support proactive retail pricing decisions.

While competitor prices are visible, the real risk lies in **how the market reacts to those prices**.
This project focuses on identifying that risk early and translating it into measurable financial exposure.

## Business Problem

Retailers often rely on reactive pricing strategies. Even with full visibility of competitor prices, they struggle to:

* Quantify pricing risk in real time
* Understand financial impact of price gaps
* Detect hidden risks driven by promotions and stock levels

As a result:

* Revenue loss goes unnoticed
* Decisions are delayed
* Opportunities are missed

## Solution

This project transforms raw market data into **actionable pricing intelligence** by:

* Monitoring competitor prices
* Measuring price gaps and positioning
* Estimating demand using stock-based proxy
* Calculating risk scores and financial exposure

## Data Collection

Separate scraping processes were implemented for each retailer due to differences in website structure:

* `scraping_bravo.ipynb`
* `scraping_araz.ipynb`
* `scraping_bazarstore.ipynb`

## Data Processing & Analysis

The core analytical workflow is implemented in:

* `analysis_pricing_risk.ipynb`

This notebook includes:

* Data loading and preparation
* Inventory-based sales proxy calculation
* Price alignment across competitors
* Risk scoring logic
* KPI generation


## Core Metrics

* **Price Gap %** → Difference vs. lowest competitor
* **Price Index** → Relative market position
* **Weighted Risk Score (0–100)** → Risk intensity
* **Commercial Risk (AZN)** → Estimated financial exposure
* **Promo Pressure** → Competitor promotion impact
* **Sales Proxy** → Estimated demand using stock changes

## Key Logic

Sales are approximated using stock movement:
Sales Proxy ≈ Morning Stock − Evening Stock
Commercial Risk is calculated based on:

* price gap
* estimated sales
* risk multipliers


## SQL Layer

* `sql_queries.sql`

Includes:

* Fact table logic
* Metric calculations
* Data modeling structure


## AI Chatbot Integration

An AI-powered chatbot was developed as an extension of this project to make pricing analysis more interactive and accessible.

The chatbot allows users to:

* Ask natural language questions about pricing risk
* Explore SKU-level insights
* Understand pricing opportunities
* Receive action-oriented recommendations

🔗 Chatbot: https://hamidaquliyeva.github.io/market-pricing-ai/


## Dashboard (Power BI)

### Executive Overview

### Competitive Position Position

### Market Pressure & Risk Diagnosis

### Time reaction
---
## Project Structure

```
bravo-pricing-risk-intelligence/
│
├── scraping_bravo.ipynb
├── scraping_araz.ipynb
├── scraping_bazarstore.ipynb
│
├── analysis_pricing_risk.ipynb
├── sql_queries.sql
│
├── overview.jpg
├── competitive-price-position.jpg
├── market-pressure-and-risk-diagnosis.jpg
├── time-reaction.jpg
│
├── AI-chatbot/
```


## Key Insights

* Overpriced products create **direct financial exposure**, not just positioning issues
* Competitive pricing alone is insufficient — **promo pressure amplifies risk**
* Stock levels significantly impact realized risk
* Pricing decisions should be **proactive, not reactive**


## Tech Stack

* **Python** → Data collection and analysis
* **SQL** → Data modeling and metrics
* **Power BI** → Visualization and decision support

## Business Value

This project demonstrates how pricing analytics can evolve from descriptive reporting into a **decision intelligence system**.

It enables:

* Early risk detection
* Quantified financial exposure
* Actionable pricing decisions

---

## Author
Hamida Quliyeva
