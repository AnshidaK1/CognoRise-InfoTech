# CognoRise InfoTech
# 📊 CognoRise InfoTech | Data Analytics Internship Projects

This repository contains three end-to-end data analytics projects completed during my internship at **CognoRise InfoTech**. Each project follows the same workflow: understand the business problem, prepare and model the data, build an interactive **Power BI** dashboard, and turn the findings into clear insights, recommendations, and limitations.

---

## 📚 Projects at a Glance

| Project | Domain | Dataset Size | Dashboard Pages | Headline Result |
|---|---|---|---|---|
| [🛒 Retail Sales Analysis](#-1-retail-sales-analysis) | Retail | ~1K transactions | 2 | 456K revenue, most customers buy only once |
| [📦 E-Commerce Customer & Sales Analytics](#-2-e-commerce-customer--sales-analytics) | E-Commerce | ~1M records | 5 | 854.32M net revenue, returns are the biggest profit drain |
| [📣 Marketing Campaign Performance](#-3-marketing-campaign-performance) | Marketing | 200K campaigns | 6 | 2.50bn spend, CPA of 284 despite ~10% CTR |

---

## 🛠️ Tools & Skills

| Area | What I used |
|---|---|
| **Visualization** | Power BI (multi-page dashboards, slicers, page navigation, KPI cards, maps, combo charts, scatter plots) |
| **Data modeling** | DAX measures and calculated columns (Net Revenue, Estimated Profit, Profit Margin %, Loss %, AOV, CTR, CPC, CPA, and more) |
| **Data preparation** | SQL, Excel, data cleaning and age grouping |
| **Analysis** | KPI analysis, segmentation, trend and seasonality analysis, spend vs conversion analysis |
| **Communication** | Key insights, prioritized recommendations, business conclusions, and limitations |

---

## 🛒 1. Retail Sales Analysis

### Objective
Analyze one year of retail transactions (**01-01-2023 to 01-01-2024**) to understand revenue, product category performance, customer demographics, and seasonality, and to recommend ways to grow sales.

### Dataset
**Columns:** Transaction ID, Date, Customer ID, Gender, Age, Product Category, Quantity, Price per Unit, Total Amount

### Key Metrics
| Product Categories | Customers | Transactions | Units Sold | Total Revenue | Avg Order Value |
|---|---|---|---|---|---|
| 3 | ~1K | ~1K | ~3K | ~456K | 456 |

### Dashboard
- **Page 1: Dashboard:** KPI cards, revenue and quantity by month, transactions and quantity by category, revenue and AOV by category, customers by gender, revenue by age group. Includes date range and product category slicers.
- **Page 2: Insights & Recommendations:** key insights, recommendations, business conclusion, and limitations.

### Key Insights
- Revenue is spread evenly across categories. **Clothing and Electronics lead (~155K each)**, while **Beauty trails (~144K)** with the fewest orders and units sold.
- Average order value is similar across categories, so revenue differences come from **order volume, not pricing**.
- Customers ≈ transactions, which shows **very low repeat purchasing**. Most customers bought only once.
- The gender split is nearly **50/50**, so gender alone is not a strong targeting factor.
- Revenue is evenly distributed across ages **20–59** (~20% each). The **50–59** group earns the most (98,340, ~22%), while **30–39** spends the most per customer. Under-20 (~5%) and over-60 (~11%) contribute the least.
- **Sales peaked in May (~53K)**, followed by October (~46K), with smaller peaks in February and December (~44K each). **September was the lowest (~25K)**, with another dip in March (~29K).

### Recommendations
1. **Launch a loyalty program** with reward points, repeat-purchase coupons, and post-purchase follow-up emails to turn one-time buyers into repeat customers.
2. **Boost Beauty sales through cross-selling** by bundling Beauty with Clothing and Electronics.
3. **Increase average order value** with "buy 2, save more" offers and a free-shipping threshold slightly above 456.
4. **Run broad campaigns for ages 20–59**: loyalty rewards for 50–59, premium and bundle offers for 30–39, and engagement offers for under 20 and over 60.
5. **Align inventory and promotions with seasonality**: stock up before May, October, and December, and run campaigns in March and September.

### ✅ Business Conclusion
Sales are healthy and evenly spread across categories and adult age groups, but almost all customers purchase only once. **Growth now depends more on retaining existing customers than on acquiring new ones.**

### ⚠️ Limitations
- Only one year of data, so long-term seasonality cannot be confirmed.
- No repeat-customer history, profit, or cost data, so profitability could not be analyzed.
- Findings are based on transaction-level data only.


---

## 📦 2. E-Commerce Customer & Sales Analytics

### Objective
Analyze large-scale e-commerce data to measure revenue, profit, returns, discounts, and shipping costs, and to find which products, categories, locations, and seasons drive the business and where profit is being lost.

### Dataset
**Columns:** Product ID, Product Name, Category, Price, Discounted Price, Final Price, Tax Rate, Tax Amount, Shipping Cost, Shipping Method, Stock Level, Supplier ID, Popularity Index, Return Rate, Seasonality, Customer Age Group, Customer Gender, Customer Location

**Scope:** ~1M records, 5 categories (Books, Electronics, Footwear, Home Appliances, Apparel), 15 customer locations, 5 age groups, 900 suppliers.

### Key Metrics
| Net Revenue | Estimated Profit | AOV | Avg Profit per Order | Profit Margin | Avg Discount | Avg Return Rate | Loss % |
|---|---|---|---|---|---|---|---|
| 854.32M | 764.69M | 967.24 | 764.69 | 89.51% | 12.52 | 10.49 | 1.0% |

### DAX Measures & Data Work
- Created **Net Revenue, Estimated Profit, Average Profit per Order, Profit Margin %, Loss Records, Loss %, and Average Order Value**.
- Added a **Row ID** column so each row is treated as one order, which makes order count and AOV possible.
- Used SQL for data extraction and transformation.

### Dashboard (5 pages)
| Page | What it shows |
|---|---|
| **Executive Summary** | 14 KPI cards, revenue map by location, revenue and profit by category, revenue by seasonality, revenue by age group |
| **Product Analysis** | Net revenue and quantity by product, profit margin vs popularity scatter, filters by category and location |
| **Location Analysis** | Revenue and profit by city, shipping cost by city, revenue by age group, filters by shipping method and category |
| **Time Analysis** | Seasonal vs non-seasonal revenue, return rate, discount, quantity, and loss records |
| **Insights & Recommendations** | Findings, prioritized actions, conclusion, and limitations |

### Key Insights
- **Returns are the biggest profit drain.** The 10.49% return rate removes about **89.6M** from net revenue, far more than shipping (about 25M).
- **Performance is evenly balanced.** The 5 categories, 15 locations, 5 age groups, and seasonal vs non-seasonal items all deliver similar revenue and profit.
- **Losses are small.** Only about 1% of orders (10K) are loss-making.
- **Discounts are a steady cost.** The average discount of 12.52% applies across all segments with no clear sales lift in any one segment.
- **Seasonality has no effect.** Revenue splits almost 50/50 between seasonal and non-seasonal items, with nearly equal discount and return rates.

### Recommendations
| Priority | Action |
|---|---|
| 🔴 High | **Reduce the return rate.** Improve product descriptions, size guides, and quality checks to lower the 10.49% average return rate. |
| 🔴 High | **Cut discounts on high-return products.** Reduce discounts where return rates are high to protect profit margin. |
| 🟡 Medium | **Review loss-making orders.** Check the ~10K loss orders for high shipping cost, high return rate, or low price, then fix pricing or shipping rules. |
| 🟡 Medium | **Lower shipping costs.** Negotiate carrier rates and set free-shipping thresholds to raise order value. |
| 🟢 Low | **Use one strategy across all segments.** Categories, locations, age groups, and seasons perform almost equally, so focus on returns, discounts, and shipping instead. |
| 🟢 Low | **Match stock to demand.** Use Stock Level against Popularity Index to restock popular items and avoid overstock on slow ones. |

### ✅ Conclusion
Sales are evenly spread, so growth should come from **cutting returns, discounts, and shipping costs**, not from pushing one segment.

### ⚠️ Limitations
- No customer ID or date column, so new vs repeat customers and monthly trends were not analyzed. Seasonality was used as the time view.
- No product cost column, so profit is estimated (net revenue adjusted for returns). The ~90% margin is likely overstated.
- Each row is treated as one order.



---

## 📣 3. Marketing Campaign Performance

### Objective
Evaluate marketing campaigns across channels, campaign types, audiences, and time to find the strongest and weakest performers, understand how spend relates to conversions, and recommend where to **increase, reduce, or optimize** the budget.

### Dataset
**Columns:** Campaign ID, Company, Campaign Type, Target Audience, Duration, Channel Used, Conversion Rate, Acquisition Cost, ROI, Location, Language, Clicks, Impressions, Engagement Score, Customer Segment, Date, CTR, Conversions, CPC, CPA

**Scope:** 200K campaigns, 5 companies, 5 campaign types (Influencer, Search, Display, Email, Social Media), 6 channels (Email, Website, Google Ads, YouTube, Instagram, Facebook), 5 languages.

### Key Metrics
| Total Spend | Conversion Rate | Avg ROI | Clicks | Impressions | CTR | CPC | CPA | Engagement Score |
|---|---|---|---|---|---|---|---|---|
| 2.50bn | 8.01 | 5.00 | 110M | 1bn | 9.98% | 22.74 | 284.04 | 5.49 |

### Dashboard (6 pages)
| Page | What it shows |
|---|---|
| **Executive Summary** | 14 KPI cards, performance over time, campaign performance, channel performance |
| **Campaign Analysis** | Campaigns, cost, conversions, ROI, CTR, CPC, engagement, and CPA by campaign type |
| **Channel Analysis** | The same metrics by channel |
| **Audience Analysis** | The same metrics by target audience, with customer segment and company filters |
| **Time Analysis** | Campaigns by month, and cost, ROI, CTR, engagement, and CPA by quarter |
| **Insights & Recommendations** | Spend vs conversions, CPA by channel and campaign type, findings and actions |

### Key Insights
- **Overall:** 2.50bn spend, about 8.8M conversions, CTR 9.98%, CPC 22.74, CPA 284.04, and ROI about 5.0.
- **Strongest campaigns:** Influencer and Search lead on conversions and ROI.
- **Weakest campaigns:** Email and Social Media trail slightly on conversions, and Display has the highest CPA. The gaps are only about 1–2%.
- **Channels:** Email and Website are the most cost-efficient, with the lowest CPC and CPA. Google Ads has the highest CPC and CPA.
- **Audience:** Men 25–34 give the best ROI. Men 18–24 get the most spend but the lowest ROI.
- **Spend vs conversions:** The relationship is weak and widely scattered. Higher spend does not reliably bring more conversions.
- **Click-to-customer gap:** CTR is strong at nearly 10%, yet each conversion costs about 284. The loss happens after the click.
- **Time:** Spend and CPA peak in Q3, CTR and ROI dip in Q2, and engagement falls sharply in Q4.

### Recommendations
| Action | Details |
|---|---|
| ⬆️ **Increase** | Budget for Influencer and Search campaigns, the Email and Website channels, and the Men 25–34 audience |
| ⬇️ **Reduce** | Spend on high-CPA campaigns, Google Ads bids, and Men 18–24 spend that is not returning ROI |
| 🔧 **Optimize** | Creative, landing pages, and calls to action for Social Media, Facebook, and Women 35–44 to turn clicks into conversions |
| 📅 **Timing** | Tighten Q3 budgets and refresh creative before Q4 |
| 🧪 **Approach** | Shift budget in small steps and A/B test, because differences between segments are small. Track CPA and ROI monthly |



---

## 📁 Repository Structure

```
CognoRise InfoTech/
│
├── Retail-Sales-Analysis/
│   ├── images/
│   ├── Retail_Sales_Analysis.pbix
│   └── dashboard.pdf
│
├── E-Commerce-Analytics/
│   ├── images/
│   ├── E-Commerce_Analytics.pbix
│   └── dashboard.pdf
│
├── Marketing-Campaign-Performance/
│   ├── images/
│   ├── Marketing_Campaign_Performance.pbix
│   └── dashboard.pdf
│
└── README.md
```

---

## 🚀 How to Explore

1. Clone or download this repository.
2. Open any `.pbix` file in **Power BI Desktop**.
3. Use the slicers and the page navigation buttons to explore each dashboard.


---

## 💡 What I Learned

- Building clean, multi-page Power BI dashboards with navigation and slicers
- Writing DAX measures for profit, returns, loss, and marketing efficiency metrics
- Turning dashboard numbers into **prioritized, business-ready recommendations**
- Being honest about **data limitations** and how they affect conclusions

---

## 👤 Author

**Anshida K**
Aspiring Data Analyst | Power BI • SQL • Excel • Python •Tableau
[LinkedIn](www.linkedin.com/in/anshida-k-b50499416) | [GitHub](https://github.com/AnshidaK1)


