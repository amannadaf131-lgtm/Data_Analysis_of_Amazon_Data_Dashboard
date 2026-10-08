# Data_Analysis_of_Amazon_Data_Dashboard
Analysis and visualization
# 📊 Amazon India Sales Dashboard (Excel)

An interactive Microsoft Excel dashboard analysing **10,000 Amazon India marketplace orders** (Jan 2024 – Aug 2026). It uses PivotTables, PivotCharts and a slicer to answer core e-commerce questions: which categories and products drive revenue and profit, how healthy fulfilment is, and where returns and cancellations hurt the business.

![Excel](https://img.shields.io/badge/Tool-Microsoft%20Excel-217346?logo=microsoftexcel&logoColor=white)
![PivotTables](https://img.shields.io/badge/Feature-PivotTables%20%26%20Slicers-blue)
![Domain](https://img.shields.io/badge/Domain-E--commerce%20Analytics-orange)

---

## 📌 Project Overview

Online sellers need to know what sells, what earns, and what leaks revenue. This project turns raw order-level data into a one-page dashboard that a business user can filter and read without writing any formulas.

**Objectives**
- Measure total sales, profit and profit margin across product categories
- Identify top-performing products and revenue concentration
- Track order status (delivered, shipped, cancelled, returned)
- Monitor return and cancellation rates over time
- Let users drill into the data interactively with a slicer

---

## 🗂️ Dataset

| Property | Detail |
|---|---|
| Records | 10,000 orders (one row per order, all unique `Order_ID`s) |
| Period | 1 Jan 2024 – 30 Aug 2026 |
| Categories | 5 |
| Products | 25 |
| Ship-to states | 10 |
| Missing values | None |

**Columns**

| Column | Description |
|---|---|
| `Order_ID` | Unique order identifier (e.g. `IN-AMD-100000`) |
| `Order_Date` | Date the order was placed |
| `Category` | Product category (Electronics & Mobiles, Apparel & Fashion, Home & Kitchen, Beauty & Personal Care, Pantry & Groceries) |
| `Product` | Product name |
| `Quantity` | Units ordered |
| `Unit_Price_INR` | Price per unit in ₹ |
| `Discount_Pct` | Discount applied (0–1) |
| `Total_Sales_INR` | Order revenue after discount, in ₹ |
| `Profit_INR` | Order profit in ₹ |
| `Payment_Method` | UPI, Credit/Debit Card, COD, Net Banking, Amazon Pay Later |
| `Fulfillment` | Amazon (FBA), Seller Flex, Merchant (FBM) |
| `Order_Status` | Delivered, Shipped, Cancelled, Returned |
| `Ship_State` | Destination state |
| `Returned Rate count` | Helper flag (`A` / `B`) used for return-rate calculations |

---

## 🧱 Dashboard Components

| # | Visual | Type | What it shows |
|---|---|---|---|
| 1 | **Category: Sum of Total Sales & Profit** | 3D clustered column | Sales vs profit for each category |
| 2 | **Top 10 Products** | Horizontal bar | Ten highest-revenue products |
| 3 | **Count of Order Status** | Column | Volume of orders in each status |
| 4 | **Returned / cancelled orders by category** | Column | Which categories lose the most orders (Electronics has the highest count) |
| 5 | **Return and Cancellation Rate %** | Line | Return rate (~4.85%) vs cancellation rate (5.0%) |
| 6 | **Order_Status slicer** | Slicer | Filters the linked PivotTables and charts by status |

The workbook has a cleaned data sheet (`Sheet1`), several PivotTable/PivotChart sheets, and a combined dashboard sheet.

---

## 🔍 Key Insights

- **Total sales ≈ ₹15.58 crore** (₹155.8M) with **total profit ≈ ₹3.32 crore** (₹33.2M), a blended **profit margin of about 21%**.
- **Electronics & Mobiles generates ~79% of all revenue** (₹12.36 crore) and ~79% of profit, which signals strong concentration risk. Home & Kitchen is a distant second (~₹1.80 crore), followed by Apparel (~₹0.98 crore).
- **Top 5 products are all electronics or accessories**: Laptop Backpack, Power Bank 20000mAh, 5G Smartphone, Wireless Earbuds and Smartwatch, each at roughly ₹2.3–2.7 crore.
- **~81.5% of orders are delivered**; about **5.0% are cancelled** and **4.8% returned**, so nearly 1 in 10 orders does not complete successfully.
- **Amazon FBA fulfils ~70%** of orders, ahead of Seller Flex (~20%) and Merchant FBM (~10%).
- **UPI is the leading payment method (~50%)**; Cash on Delivery still accounts for ~15% of orders.
- **Maharashtra, Karnataka and Delhi** are the top three states by revenue.
- Quarterly revenue is stable at around ₹1.4–1.6 crore (2026 Q3 is a partial quarter), with no strong seasonality.

> Figures were calculated from the dataset in this workbook.

---

## 🛠️ Excel Skills Demonstrated

- Data cleaning and structuring for analysis
- PivotTables with Sum and Count aggregations
- PivotCharts (3D column, bar, column, line)
- Slicers for interactive filtering
- Top-N filtering (Top 10 products)
- KPI design: profit margin, return rate, cancellation rate
- Dashboard layout and visual storytelling

---

## 🚀 How to Use

1. Download `Amazon_Sales_Data_India.xlsx` from this repository.
2. Open it in **Microsoft Excel 2013 or later** (slicers and PivotCharts are not fully supported in Google Sheets or LibreOffice).
3. Go to the dashboard sheet and click the **Order_Status** slicer buttons to filter the charts.
4. To refresh after editing data: **Data → Refresh All**.

---

## 💡 Business Recommendations

1. **Diversify beyond electronics.** Promote Home & Kitchen and Apparel to reduce dependence on a single category.
2. **Reduce returns and cancellations.** Investigate the products and payment methods (such as COD) most linked to failed orders.
3. **Protect high-margin bestsellers.** Keep top-10 products well stocked and prioritise them for FBA.
4. **Target high-revenue states** with regional campaigns, and test growth in lower-performing states.

---

## 📁 Repository Structure

```
├── Amazon_Sales_Data_India.xlsx   # Dashboard + data
├── README.md                      # Project documentation
└── dashboard-preview.png          # (Optional) screenshot of the dashboard
```

---

## 🔮 Future Improvements

- Add slicers for Category, Year and State
- Add a profit-margin-by-category KPI card
- Build a state-level map of sales
- Add month-over-month growth and forecasting
- Recreate the dashboard in Power BI or Tableau

📧 amannadaf131@gmail.com

⭐ If you found this project useful, consider giving the repository a star!
