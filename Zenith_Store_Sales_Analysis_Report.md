# Zenith Store Sales Analysis — Excel Dashboard Project

**Tool used:** Microsoft Excel (no external tools, no AI assistance)  
**Dataset:** Zenith Store order data — January to December 2022  
**Total Records:** 31,047 rows across 17 columns  

---

## About This Project

This is my first data analysis project, and I built the entire thing from scratch in Microsoft Excel. No Python, no Power BI, no AI help — just raw Excel skills. The dataset is a sales record from Zenith Store covering the full year of 2022, with order details like customer demographics, sales channels, product categories, delivery statuses, and shipping information spread across India.

The goal was simple: take messy transactional data and turn it into something that actually tells a story. I wanted to understand which channels are driving the most sales, who the customers really are, what they're buying, and how the business performed month over month.

---

## Dataset Overview

The raw data lives in the **Zenith Store** sheet and has the following columns:

| Column | Description |
|---|---|
| Order ID | Unique identifier for each order |
| Cust ID | Customer identifier |
| Gender | Customer gender (Men / Women) |
| Age | Customer's age |
| Age Group | Bucketed age category (Teenager, Adult, Middle Aged, Senior) |
| Date | Order date |
| Status | Delivery status (Delivered, Returned, Cancelled, Refunded) |
| Channel | Sales platform (Amazon, Myntra, Flipkart, Ajio, Nalli, Meesho, Others) |
| Category | Product type (Set, Kurta, Western Dress, Top, Saree, etc.) |
| Size | Clothing size |
| Qty | Quantity ordered |
| Amount | Order value in INR |
| ship-city, ship-state, ship-postal-code | Shipping location details |
| B2B | Whether the order is business-to-business |

**Time period covered:** January 4, 2022 – December 6, 2022  
**Total unique orders:** 28,471  
**Total revenue:** ₹2,11,76,377  

---

## What I Did in Excel

### 1. Data Cleaning

The raw data had some inconsistencies — city names with mixed casing (e.g., "Bengaluru", "BENGALURU", "bangalore" all referring to the same city), missing entries, and date formatting issues. I cleaned these manually and standardized key columns to make the pivot tables accurate.

### 2. Pivot Tables

I created multiple pivot tables on the **Pivot Tables** sheet to slice the data in different ways:

- **Monthly Sales Trend** — Order count and revenue by month
- **Sales Channel Performance** — Order volume by platform
- **Order Status Breakdown** — Delivered vs Returned vs Cancelled vs Refunded quantities
- **Size Distribution** — How orders break down across size categories
- **Category Revenue** — Revenue generated per product type
- **Gender & Age Group Matrix** — Cross-tab of customer demographics
- **Gender Revenue Split** — Men vs Women contribution to total revenue

### 3. Dashboard

All the key visuals were assembled on the **Zenith Store Analysis Dashboard** sheet. The dashboard pulls from the pivot tables and presents everything in a clean, readable format with charts.

---

## Key Findings

### Sales Channels

Amazon is the dominant platform by a significant margin, accounting for 11,016 orders — roughly 35.5% of all sales. Myntra comes in second at 7,254 orders, followed by Flipkart at 6,703. The smaller platforms — Ajio (1,931), Nalli (1,484), and Meesho (1,398) — have meaningful but noticeably smaller share.

| Channel | Orders |
|---|---|
| Amazon | 11,016 |
| Myntra | 7,254 |
| Flipkart | 6,703 |
| Ajio | 1,931 |
| Nalli | 1,484 |
| Meesho | 1,398 |
| Others | 1,261 |

**Takeaway:** If the store wants to grow, Amazon and Myntra are where most of the eyeballs already are. Meesho and Ajio have room to grow with the right strategy.

---

### Monthly Sales Trend

Sales peaked in **March 2022** (₹19,28,066 / 2,819 orders) and showed a gradual decline through the second half of the year, hitting a low in **November** (₹16,15,356 / 2,383 orders) before a slight December recovery.

| Month | Revenue (₹) | Orders |
|---|---|---|
| January | 18,20,601 | 2,702 |
| February | 18,75,932 | 2,750 |
| March | 19,28,066 | 2,819 |
| April | 18,29,263 | 2,685 |
| May | 17,97,822 | 2,617 |
| June | 17,50,966 | 2,597 |
| July | 17,72,300 | 2,579 |
| August | 18,08,505 | 2,617 |
| September | 16,88,871 | 2,490 |
| October | 16,66,662 | 2,424 |
| November | 16,15,356 | 2,383 |
| December | 16,22,033 | 2,384 |

The Q1 spike likely reflects post-winter restocking and seasonal buying. The H2 dip is worth investigating — it could be competition, seasonality, or assortment gaps.

---

### Order Status

The fulfillment rate is strong overall:

| Status | Quantity |
|---|---|
| Delivered | 28,822 |
| Returned | 1,050 |
| Cancelled | 844 |
| Refunded | 521 |

**92.3% delivery rate.** Returns and cancellations together account for about 6.1% of volume, which is reasonable for apparel e-commerce. Refunds at 1.7% are relatively low.

---

### Product Categories

Sets are the top-selling category by both volume and revenue, followed by Kurtas. Together these two account for the majority of the business — which makes sense for an Indian ethnic wear store.

| Category | Revenue (₹) |
|---|---|
| Set | 1,05,07,546 |
| Kurta | 49,59,377 |
| Western Dress | 31,48,836 |
| Top | 11,86,199 |
| Saree | 10,10,471 |
| Ethnic Dress | 1,95,256 |
| Blouse | 1,40,888 |
| Bottom | 27,804 |

Sets alone bring in nearly **50% of total revenue**. Western Dress at ₹31L is the third biggest earner, suggesting the customer base has a mix of ethnic and contemporary tastes.

---

### Customer Demographics

**Gender Split:**
Women make up the majority of customers — 21,553 orders vs 9,494 from men. Women also account for **64% of total revenue** (₹1,35,62,773 vs ₹76,13,604 for men). The store is clearly more women-focused, which aligns with the product catalog.

**Age Groups:**

| Gender | Adult | Middle Aged | Senior | Teenager |
|---|---|---|---|---|
| Men | 3,579 | 3,357 | 908 | 1,650 |
| Women | 8,151 | 7,585 | 2,044 | 3,773 |

Adults (roughly 25–40) and Middle Aged (roughly 40–60) together form the core customer base for both genders. The Teenager segment is significant, especially for women — this probably skews toward the sets and tops categories.

---

### Size Distribution

| Size | Orders |
|---|---|
| M | 5,485 |
| L | 5,144 |
| XL | 4,437 |
| S | 4,176 |
| XXL | 4,065 |
| 3XL | 3,347 |
| XS | 2,503 |
| Free | 1,408 |

M and L are the most ordered sizes, which is pretty standard. However, the significant volume in XXL and 3XL (combined nearly 7,400 orders) is worth noting — the store is clearly serving plus-size customers meaningfully, not just as an afterthought.

---

### Geographic Distribution

Maharashtra leads in orders with 4,519, followed closely by Karnataka at 3,988. These two states alone account for nearly 27% of all sales. Uttar Pradesh (2,882), Tamil Nadu (2,679), and Telangana (2,527) round out the top five.

**Top 10 States by Orders:**

| State | Orders |
|---|---|
| Maharashtra | 4,519 |
| Karnataka | 3,988 |
| Uttar Pradesh | 2,882 |
| Tamil Nadu | 2,679 |
| Telangana | 2,527 |
| Delhi | 1,804 |
| Kerala | 1,549 |
| West Bengal | 1,425 |
| Andhra Pradesh | 1,369 |
| Haryana | 1,118 |

The customer base is spread across the country, but metros and tier-1 cities clearly dominate. There's interesting penetration in states like UP and Kerala too, which suggests decent reach beyond just the metro markets.

---

### B2B vs B2C

Almost all orders are B2C (30,861 orders / ₹2,10,50,056 revenue). B2B is a tiny sliver with just 186 orders (₹1,26,321 revenue). Not a significant channel right now, but worth tracking.

---

## What I Learned Building This

This project taught me a lot more than I expected. A few honest reflections:

**Pivot tables are more powerful than I thought.** Once I understood how to structure the source data properly, creating slices of the data became fast. The cross-tab of gender vs age group was the one I struggled with most before it clicked.

**Data cleaning is the most time-consuming part.** Raw data is messy. City names inconsistencies alone took a while to deal with. In hindsight, I should've standardized this first before building any pivots.

**Dashboard design takes iteration.** My first version of the dashboard was cluttered. I had to remove charts, rearrange things, and ask myself "what's the one thing someone should notice first?" more than once.

**Column naming matters.** The "Channel " column has a trailing space in the original data, which caused some confusion. Small things like this matter when you're working with large datasets.

---

## Files in This Repository

```
├── Zenith_Store_Sales_Analysis.xlsx   # Main Excel file
│   ├── Zenith Store                   # Raw data sheet (31,047 rows)
│   ├── Pivot Tables                   # All pivot tables used for analysis
│   └── Zenith Store Analysis Dashboard # Final dashboard
└── README.md                          # This file
```

---

## Tools Used

- **Microsoft Excel** — 100% of the work: data cleaning, pivot tables, charts, and dashboard layout
- No Python, no Power BI, no Tableau, no AI tools

---

## What's Next

This is my first project and I'm proud of how it turned out, but there's clearly more to explore:

- Break down return rates by category to identify which products have quality or sizing issues
- Look at average order value trends month-over-month, not just total revenue
- Analyze channel performance on a per-state basis (does Meesho perform differently in Tier-2 cities?)
- Build a second version of this using Python (pandas + matplotlib) to compare workflows

---

*Built with Excel. No shortcuts taken. Feedback welcome.*
