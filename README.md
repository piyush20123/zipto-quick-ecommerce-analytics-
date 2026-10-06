# 📊 Quick Commerce Analytics — Dark Store Performance Challenge


> **Quick Commerce Analytics Challenge | Zipto Quick Commerce | Noida Cluster**  
> **Analysis Period: 18 May – 28 June 2026**

---
## 🏆 Achievement

🥈 **Silver Medal – Data Analytics Hackathon**

Organized by **AccioJob, Pune**  
Date: **6 October 2026**


## 📌 Project Overview

This project was developed as part of a **Quick Commerce Analytics Challenge** focused on understanding dark-store profitability, delivery performance, and promotion economics.

The central business question was:

> **Which two stores should be fixed first, what exactly is broken, and what is fixing it worth in rupees?**

The project transforms operational data into business insights using **Microsoft Fabric, Power BI, Power Query, DAX, and SQL**.

---

# 🎯 Business Objectives

The analysis is divided into three analytical lanes.

### 🏪 Lane 1 — Store Performance

**Business Question:**  
Which stores make money and which stores lose money?

Analysis includes:

- Store contribution
- Store P&L
- Monthly rent
- Order volume
- Return rate
- Return losses
- Identification of loss-making stores

### 🚚 Lane 2 — Delivery & Fulfilment

**Business Question:**  
Are we delivering what we say we deliver?

Analysis includes:

- Delivery success rate
- On-time delivery rate
- Late deliveries
- Average delivery time
- Average trip distance
- Delivery performance by store

### 🛍️ Lane 3 — Product & Promotions

**Business Question:**  
What are we selling, and what are the discounts costing us?

Analysis includes:

- Product sales value
- Discount spend
- Contribution by promotion
- Loss-making promotions
- Products associated with loss-making promotions
- Store exposure to loss-making promotions

---

# 🛠️ Tools & Technologies

- **Microsoft Fabric**
- **Power BI**
- **Power Query**
- **DAX**
- **SQL / MySQL**
- **GitHub**
- Data Cleaning & Transformation
- Data Modeling
- Business Intelligence
- Data Visualization

---

# 📊 Dashboard 1 — Dark Store Performance & Profitability

![Store Performance Dashboard](dashboard/store-performance.png)

### Key KPIs

| KPI | Value |
|---|---:|
| Store Loss | ₹450.24K |
| Store Contribution | ₹3.03M |
| Total Orders | 52K |
| Return Rate | 4.90% |

### Key Findings

The current analytical model identifies:

**S07** as the largest P&L loss-making store.

- Store P&L: **−₹658.67K**
- Store Contribution: **−₹202.67K**
- Return Rate: **~14%**
- Return Loss: **₹374.43K**
- Sales associated with loss-making promotions: **₹579.68K**

**S03** is the second-largest P&L loss-making store.

- Store P&L: **−₹312.26K**
- Store Contribution: **₹79.74K**
- Return Rate: **~7.94%**
- Return Loss: **₹199.24K**
- Sales associated with loss-making promotions: **₹564.88K**

### Business Interpretation

S07 should be investigated first because it combines:

**Negative contribution + high return rate + high return loss + high promotion exposure**

S03 generates positive contribution, but its contribution is insufficient to cover its fixed monthly rent.

---

# 🛍️ Dashboard 2 — Promotion & Product Performance

![Promotion & Product Dashboard](dashboard/promotion-product-performance.png)

### Key KPIs

| KPI | Value |
|---|---:|
| Product Sales Value | ₹28.64M |
| Total Discount Spend | ₹1.56M |
| Loss-Making Promotions | 2 |
| Negative Contribution from Loss-Making Promotions | ₹422.44K |
| Delivered Contribution | ₹3.03M |

### Promotion Findings

Two promotions show negative contribution:

| Promotion | Contribution |
|---|---:|
| FRESH50 | −₹366.91K |
| SAVE20 | −₹55.53K |

Combined negative contribution:

### **₹422.44K**

Product sales associated with these loss-making promotions:

### **₹3.33M**

---

## 🏪 Store Exposure to Loss-Making Promotions

The highest product sales associated with loss-making promotions are:

| Rank | Store | Associated Sales |
|---:|---|---:|
| 1 | S07 | ₹579.68K |
| 2 | S03 | ₹564.88K |
| 3 | S01 | ₹351.93K |
| 4 | S02 | ₹317.70K |
| 5 | S04 | ₹309.45K |

> **Important:** Sales associated with a loss-making promotion are not themselves financial loss. This analysis identifies association/exposure and does not claim that the promotion alone caused the loss.

---

# 🧮 Contribution Logic

The challenge economics were implemented using the prescribed contribution logic.

### Delivered Orders

```text
Contribution =
Net Amount − COGS − Delivery Cost
