# **Amazon Sales Analytics: End-to-End Data Preparation and Power BI Visualizations**

This project demonstrates a full data analytics pipeline: from raw e-commerce sales data preprocessing with Python to in-depth business intelligence visualizations developed in Power BI. It shows expertise in data cleaning, preprocessing, feature engineering, and interactive dashboarding for actionable business insights

## **Dataset Description**

**Content:** Product ID, name, category, prices (discounted/actual), discount %, ratings, rating counts, reviews, user information, images, and product links.

**Rows:** ~1,465

**Columns:** 16

**Key fields:** productid, category, actualprice, discountedprice, discountpercentage, rating, ratingcount, etc

## **Data Preparation (Python)**

### **Steps**

**Loading Data:** Read CSV using pandas and validate data presence.​​

**Initial Audit:** Checked data types, null values, and duplicates; removed or corrected as needed.

**Type Correction:** Converted price, discount, rating, and count columns to numeric types after stripping currency/commas.

**Outlier & Error Handling:** Identified and removed problematic rows (e.g., ratings with special characters or impossible values).

**Null Handling:** Dropped records with missing essential numeric metrics.

### **Feature Engineering:**

**Profit Margin:** Calculated as (actualprice - discountedprice) / actualprice * 100.

**Discount Level:** Categorized as High (≥60%), Medium (>30%, <=60%), or Low (<=30%).

Price Category: Products split into Low, Mid, and High price groups by quartile.

**Export: Saved the fully cleaned dataset as Excel for BI integration.

### **Tools Used**

pandas, numpy, matplotlib/seaborn (for basic analysis and quality checking)

Scikit-learn (for simple regression/EDA)

Jupyter Notebook.

## **Power BI Visualizations**

### **Dashboard Features**​

**Top 10 Categories:** Stacked bar chart showing total ratings (“popularity proxy”) split by discount level.

**Impact of Discounts:** Breakdown by categories and the effect of Low, Medium, and High discounts on rating counts.

**Product Price vs. Rating:** Scatter chart with size as a proxy for sales, colored by discount level.

**Net Profit by Discount Level:** Treemap showing how Medium, High, and Low discounts contribute to total net profit.

**Interactive Insights:** Filters, tooltips, and dynamic highlighting to support category drilldown.

## **Key Findings**

**Medium Discounts Generate Most Profit:** Despite high sales volume for heavily discounted items, medium-level discounts result in the highest net profit for the seller.​

**Popularity Tied to Discounting:** High discounts boost sales volume/ratings for certain electronics categories, but profitability does not necessarily scale.

**Price-Rating Relationship:** Products at different price points and discounts show varying customer satisfaction (proxy by average ratings).
