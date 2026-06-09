# Credit Card Complaint Analytics Dashboard

> A comprehensive Tableau dashboard that transforms raw complaint data into actionable business intelligence for a major financial institution. Provides real-time visibility into complaint patterns, geographic distribution, and operational metrics across 50+ US states.

## Table of Contents
- [Problem Statement](#problem-statement)
- [Solution Overview](#solution-overview)
- [Key Features](#key-features)
- [Technical Stack](#technical-stack)
- [Dashboard Components](#dashboard-components)
- [How to Use](#how-to-use)
- [Key Insights & Metrics](#key-insights--metrics)
- [Data Preparation](#data-preparation)
- [Improvements & Roadmap](#improvements--roadmap)
- [Data Dictionary](#data-dictionary)
- [Getting Started](#getting-started)
- [Contact & Attribution](#contact--attribution)

## Problem Statement

### Business Challenge
A major financial services organization processes **86,893 credit card complaints** across all 50 US states and multiple submission channels (web, phone, email, postal, fax, referral). However, stakeholders lacked unified visibility into:

- **Geographic concentration** – Which states/regions drive the highest complaint volume?
- **Root cause analysis** – What are the top complaint categories, and how do they trend over time?
- **Operational efficiency** – How effectively and quickly are complaints being resolved? Are SLAs being met?
- **Submission patterns** – Which channels are most effective? Do complaint resolution times vary by submission method?
- **Temporal anomalies** – Why do certain days of the week see complaint spikes? Are there seasonal trends?

This fragmented view made it difficult to allocate resources effectively or identify process improvements.

### Target Stakeholders
- **Operations Management** – Resource allocation and process optimization
- **Regional Leaders** – State-level complaint performance and hotspot identification
- **Compliance & Quality Assurance** – SLA tracking and response effectiveness
- **Executive Leadership** – High-level KPIs and trend analysis

---

## Solution Overview

A **Tableau-based analytical dashboard** that consolidates complaint data into a single source of truth, enabling stakeholders to:

✓ **Monitor SLA Compliance** – Track timely response rates and closure percentages in real-time  
✓ **Identify Hotspots** – Geographic density mapping for complaint concentration by state  
✓ **Prioritize Root Causes** – Ranked view of top 10 complaint categories by volume  
✓ **Optimize Operations** – Analyze complaint patterns by submission channel and day-of-week  
✓ **Track Trends** – 12-month rolling trend analysis with peak identification  
✓ **Enable Drill-Down Analysis** – Interactive filters for deeper investigation (future enhancement)  

---

## Key Features

### 1. **Executive KPI Cards** (Top Row)
- **Total Complaints**: 86,893 (all-time)
- **Rolling 12-Month Complaints**: 20,202 (trend metric)
- **Timely Response Rate**: 85,934 complaints with 98.90% closure rate
- **In-Progress Complaints**: 329 (0.38% of total—indicates strong closure rate)
- **Submitted Via**: Breakdown by channel (Web dominates at 68.92%)

### 2. **Monthly Trend Analysis**
- **Chart Type**: Area chart with trend line overlay
- **Time Range**: 2015–2021 (6+ years of historical data)
- **Key Insight**: Peak complaint volume in 2020 (~2,175 monthly average), with gradual decline through 2021
- **Trend**: Can be changed to see yearly, monthly, weekly and daily trend.
- **Business Use**: Identify seasonal patterns and validate process improvements

### 3. **Geographic Density/filled map Map**
- **Coverage**: All 50 US states with complaint count overlay
- **Color Gradient**: Light (low complaint volume) → Dark brown/red (high concentration)
- **Top Complaint States**:
  - California: 12,102 complaints
  - Texas: 5,625 complaints
  - Florida: 2,914 complaints
  - New York: 2,573 complaints
- **Business Use**: Allocate customer service resources to high-impact regions

### 4. **Top 10 Issue Category Breakdown**
- **Ranked by Volume**: Horizontal bar chart for easy scanning
- **Top Categories**:
  1. Billing disputes: 14,688
  2. Other: 9,049
  3. Identity theft / Fraud / Email compromise: 8,244
  4. Closing/Cancelling account: 5,230
  5. APR or interest rate: 5,426
- **Business Use**: Focus improvement initiatives on highest-impact issue types

### 5. **Company Response Type Analysis**
- **Resolution Distribution**:
  - Closed with explanation: 51,873 (59.70%)
  - Closed with monetary relief: 17,942 (20.65%)
  - Closed without monetary relief: 9,215 (10.60%)
  - Closed without relief: 4,246 (4.89%)
  - Closed with relief: 2,500 (2.88%)
  - Closed: 649 (0.75%)
- **Business Use**: Understand resolution patterns and customer satisfaction drivers

### 6. **Day-of-Week Complaint Distribution**
- **Pattern Insight**: Complaints peak on **Monday (16,203)** and **Sunday (16,559)**
  - Likely driven by weekend backlog and Monday surge processing
- **Secondary Peak**: **Tuesday (15,405)**
- **Lowest Volume**: **Saturday (6,040)**, **Thursday (6,649)**
- **Business Use**: Optimize staffing schedules and weekend processing protocols

---

## Technical Stack

| Component | Tool | Purpose |
|-----------|------|---------|
| **Visualization** | Tableau Desktop | Interactive dashboarding & analytics |
| **Data Source** | Excel |
| **Calculations** | Tableau Calculated Fields | KPI metrics, rolling averages, percentages |
| **Interactivity** | Tableau Filters & Parameters | User-driven exploration |

### Tableau Features Utilized
- **Calculated Fields**: Rolling 12-month complaint averages, percentage calculations
- **Map Layer**: Geographic density mapping with state-level aggregation
- **Parameters**: Dynamic trend selection (Monthly/Quarterly/Yearly)
- **Filters**: Multi-select options for drill-down (channel, category, date range)
- **Dual-Axis Charts**: Trend line with area fill for visual clarity
- **Color Encoding**: Intuitive gradients and categorical palettes

---

## Dashboard Components

### Layout & Information Hierarchy
```
┌─────────────────────────────────────────────────────────────────────┐
│  CREDIT CARD COMPLAINT DASHBOARD                                    │
├─────────────────────────────────────────────────────────────────────┤
│ [Total Complaints] [Timely Response] [In Progress] [Submitted Via]   │
│     86,893             98.90%            329          (Pie Chart)    │
├────────────────────────────┬────────────────────────────────────────┤
│     Monthly Trend          │       Density Map (US States)          │
│   (2015–2021 Area Chart)   │    (Complaint Volume by State)         │
├────────────────────────────┬────────────────────────────────────────┤
│   Top 10 Issues (Horizontal Bar) │  Company Response (Breakdown)    │
├────────────────────────────┼────────────────────────────────────────┤
│       Complaints by Day (Heatmap Grid)                              │
│     Sun    Mon    Tue    Wed    Thu    Fri    Sat                    │
│   16,559  16,203  15,405  13,961  13,406  14,066  6,040            │
└─────────────────────────────────────────────────────────────────────┘
```

### Color Scheme
- **Primary (KPI Cards)**: Light blue/purple background with white text
- **Trend Chart**: Blue line with pink fill area
- **Density Map**: Tan (light) → Brown/Red (dark)
- **Bar Charts**: Red gradient (emphasis on high-impact categories)
- **Day-of-Week**: Blue/teal heatmap with intensity gradient

---

## How to Use

### For Operational Teams
1. **Check Daily Metrics**: Review KPI cards for total complaints and SLA compliance
2. **Identify Regional Issues**: Use Density Map to spot high-complaint states
3. **Allocate Resources**: Cross-reference Top Issues with state data for targeted support
4. **Monitor Trends**: Watch Monthly Trend for spikes indicating process problems

### For Leadership
1. **Review Executive Summary**: Focus on KPI cards and Monthly Trend
2. **Understand Root Causes**: Drill into Top 10 Issues for strategic focus areas
3. **Track SLA Performance**: Monitor Timely Response % for compliance reporting
4. **Assess Channel Effectiveness**: Use Submitted Via breakdown for channel optimization

### For Data Analysts
1. **Validate Data Quality**: Cross-check rolling 12-month total against source data
2. **Investigate Anomalies**: Click into any spike in Monthly Trend for root cause
3. **Create Drill-Down Reports**: Export filtered views for deeper analysis
4. **Prepare Insights**: Use dashboard as foundation for detailed investigations

### Interactive Features (Current)
- **Filters**: Date range, issue category, submission channel, state
- **Hover Details**: Tooltips showing exact counts and percentages
- **Parameter Toggle**: Switch between Monthly/Quarterly/Yearly trend views

---

## Key Insights & Metrics

### Performance Highlights ✓
| Metric | Value | Interpretation |
|--------|-------|-----------------|
| **Timely Response Rate** | 98.90% | Exceeds industry standard (~95%); strong SLA compliance |
| **Closure Rate** | 99.62% | Only 0.38% of complaints remain in-progress |
| **Web Channel Dominance** | 68.92% | Digital-first complaint submission trend |
| **Top Issue Concentration** | 14,688 complaints | Billing disputes alone = 16.9% of all complaints |
| **Geographic Concentration** | CA = 13.9% | Top 4 states = ~37% of all complaints |

### Operational Opportunities 🎯
1. **Billing Process Improvement** – Billing disputes = #1 category; potential for SOP redesign
2. **State-Specific Interventions** – CA, TX, FL, NY warrant localized support
3. **Channel Rebalancing** – Email channel (0.05%) suggests underutilization or low awareness
4. **Staffing Optimization** – Monday/Sunday peaks indicate weekend backlog; adjust schedules
5. **Category Root Cause Analysis** – "Other" (9,049 complaints) needs categorization refinement

---

## Data Preparation

### Data Source
- **Source**: Consumer complaint database (financial institution)
- **Records**: 86,893 complaints
- **Date Range**: 2015–2021
- **Granularity**: Individual complaint records with metadata

### ETL Pipeline (Summarized)
```
Raw Data (Excel)
    ↓
[Data Cleaning]
  - Remove duplicates
  - Standardize date formats
  - Normalize state abbreviations
  - Validate complaint categories
    ↓
[Feature Engineering]
  - Extract year, month, day-of-week
  - Calculate resolution time (days)
  - Assign complaint severity levels
  - Create regional groupings
    ↓
[Aggregation]
  - State-level complaint counts
  - Category-level volume & resolution rates
  - Channel distribution analysis
    ↓
[Tableau Data Source]
  - Connect to extract data
  - Build calculated fields for KPIs
  - Configure dashboard
```

### Key Calculated Fields (Tableau)
```
Rolling 12-Month Complaints: 
1. Calculated Field - Max Date Received (to capture last date month)
2. Parameter - Max date Received - This is linked with Max Date Received calculated field.
3. Calculated Field - Rolling 12 month filter - 
datediff('month',DATETRUNC('month',[Date received]),
DATETRUNC('month',[Parameters].[Max Date Received])) <12
4. Calculated Field - Rolling 12 months Complaints -
Sum(if [Rolling 12 months Filter]= TRUE then [Number of Records] end)

Timely Response %: 
Calculated Field - Timely Response - 
To check if [Timely response?]='Yes' then ([Number of Records]) END

In Progress %: 
Calculated Field - In Progress Count- 
sum(if ([Company response to consumer]='In progress') then [Number of Records] end)

Find the trend
Parameter - Trend to put day duration like yearly, monthly, daily, quarterly
Calculated Field - Trend Dynamic Calc

Density Map and filled Map
Parameter to switch between sheets
```

## Improvements & Roadmap

### **Phase 1: Immediate Enhancements** (High Priority)
- [ ] **Add Drill-Down Interactivity**
  - Click on "Billing disputes" → View top sub-issues (e.g., unauthorized charges, billing errors)
  - Click on state → See complaints by category for that region
  - **Impact**: Reduce investigation time from hours to minutes

- [ ] **Normalize Color Palette**
  - Establish 3–4 core colors (primary, secondary, accent, alert)
  - Apply consistently across all charts
  - **Impact**: Improve visual cohesion and reduce cognitive load

- [ ] **Add SLA Benchmark Context**
  - Display industry standard (95%) as reference line on Timely Response metric
  - Add YoY comparison (2020 vs. 2021 SLA performance)
  - **Impact**: Enable stakeholders to contextualize performance

- [ ] **Annotate Anomalies**
  - Add note to 2020 peak: "Peak driven by [external factor—COVID, regulatory change, etc.]"
  - Explain Monday/Sunday spike in day-of-week chart
  - **Impact**: Reduce confusion and provide narrative context

### **Phase 2: Operational Depth** (Medium Priority)
- [ ] **Split Submission Via Visualization**
  - Chart 1: Volume by channel (current)
  - Chart 2: Avg resolution time by channel
  - **Use Case**: Identify which channels drive faster resolution

- [ ] **Add Resolution Time Distribution**
  - Histogram showing complaint resolution time in days (0–30, 30–60, 60–90, 90+)
  - Filter by category and state
  - **Impact**: Identify bottleneck resolution categories

- [ ] **Category Root Cause Deep Dive**
  - For "Other" category (9,049 complaints): Create detailed view of sub-issues
  - Add customer sentiment tags (if available): Frustration level, escalation risk
  - **Impact**: Uncover hidden patterns in unclassified complaints

- [ ] **Seasonal & Cyclical Analysis**
  - Overlay fiscal quarter performance
  - Month-over-month growth rate calculation
  - **Impact**: Better forecasting and planning

### **Phase 3: Advanced Analytics** (Future)
- [ ] **Predictive SLA Modeling**
  - Build ML model to predict complaints at risk of SLA miss
  - Integrate into dashboard with early-warning indicators
  - **Impact**: Proactive intervention capabilities

- [ ] **Customer Journey Map**
  - Track complaint lifecycle: submission → investigation → resolution → feedback
  - Identify drop-off points in resolution process
  - **Impact**: Process optimization and customer experience improvements

- [ ] **Automated Alerting**
  - Dashboard email alerts when metrics exceed thresholds (e.g., SLA drop below 97%)
  - **Impact**: Real-time notification for operations teams

---

## Data Dictionary

| Field | Type | Description | Example |
|-------|------|-------------|---------|
| `complaint_id` | String | Unique complaint identifier | CMP-2021-001234 |
| `submission_date` | Date | Date complaint was submitted | 2021-03-15 |
| `complaint_category` | String | Issue classification | Billing disputes |
| `sub_category` | String | Detailed issue type | Unauthorized charges |
| `state` | String | US state abbreviation | CA |
| `submission_channel` | String | How complaint was submitted | Web, Phone, Email, etc. |
| `resolution_date` | Date | Date complaint was closed | 2021-04-12 |
| `resolution_type` | String | How complaint was resolved | Closed with explanation |
| `days_to_resolution` | Integer | Time to close (days) | 28 |
| `timely_response` | Boolean | Met SLA (Y/N) | True |
| `customer_satisfaction` | String | Post-resolution feedback | Satisfied / Dissatisfied |

---

## Getting Started

### Prerequisites
- **Tableau Desktop** (v2020.1 or later) or **Tableau Public** (free, cloud-based)
- **CSV/SQL Data Source** (complaints dataset with fields above)
- **Modern Browser** (if using Tableau Public)

### Installation Steps
1. **Download the Dashboard**
   ```
   git clone https://github.com/AnubhaRanjan/credit-card-complaint-dashboard.git
   cd credit-card-complaint-dashboard
   ```

2. **Open in Tableau**
   - Launch Tableau Desktop
   - File → Open → Select `Dashboard.twbx`

3. **Connect Data Source** (if prompted)
   - Navigate to `data/Credit_Card_Complaints.csv`
   - Click "Connect" and refresh data source

4. **Explore the Dashboard**
   - Use filters to slice by date, state, category, channel
   - Hover over charts for detailed tooltips
   - Click on states in density map for state-specific views

### Using Tableau Public (No License Required)
1. Sign up for free account at https://public.tableau.com
2. Drag & drop the `.twbx` file or create new workbook
3. Publish dashboard publicly or keep private
4. Share URL with stakeholders for real-time access

---

## Dashboard Link

**Live Dashboard**: [Credit Card Complaint Dashboard](https://public.tableau.com/app/profile/anubha.ranjan/viz/CreditCardComplainDashboard_17808451062660/Dashboard1?publish=yes)

---

## Contact & Attribution

**Professional Links**:
- 📧 Email: ranjan.anubha@gmail.com
- 💼 LinkedIn: [linkedin.com/in/anubharanjan](https://linkedin.com/in/anubharanjan)

---

## License

This project is provided for **educational and portfolio purposes**. 

---

**Last Updated**: June 2026  
**Status**: Active (Phase 1 enhancements in progress)
