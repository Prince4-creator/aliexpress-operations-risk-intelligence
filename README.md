# AliExpress Global | Operations & Risk Intelligence Dashboard

An interactive, 3-page Power BI dashboard designed to monitor high-level B2B sales trends, map regional logistics bottlenecks, and analyze supplier risk profiles.

## 📊 Live Dashboard Screenshots
*Include screenshots of your beautiful pages here!*
![Overview Page](path/to/overview-screenshot.png)
![Logistics Page](path/to/logistics-screenshot.png)
![Supplier Risk Page](path/to/supplier-risk-screenshot.png)

## 🎯 Key Business Problems Addressed
1. **Catalog vs. Logistics Returns:** Investigated why 27% of total orders were returned. Discovered that the root cause was "Description Mismatch" rather than shipping delays.
2. **Supply Chain Exposure:** Identified high-defect suppliers and analyzed contract risk profiles to flag underperforming vendors.
3. **Fulfillment Bottlenecks:** Mapped average port clearance times to target delivery delays at specific international customs hubs.

## ⚙️ Data Architecture & Modeling
This project utilizes a optimized **Star Schema** to ensure fast, scalable DAX calculations:
* **Fact Table:** `FactTransactions` (orders, quantities, pricing details, dates)
* **Dimension Tables:** `DimProducts`, `DimSuppliers`, and `DimLocations`

## 💻 Key DAX Measures Created
Here are a few of the custom measures built for this project:

* **Gross Merchandise Value (GMV):**
  ```dax
  GMV = SUM(FactTransactions[SalesAmount])
  Return Rate = DIVIDE(
    CALCULATE(COUNT(FactTransactions[OrderID]), FactTransactions[OrderStatus] = "Returned"),
    COUNT(FactTransactions[OrderID]),
    0)

## 🛠️ Tools & Technologies Used
1. Power BI Desktop (Data Modeling, DAX, Interactive Slicers, UI/UX Navigation Layouts)
2. Power Query (Data Extraction, Cleaning, and Schema Alignment)
3. GIMP (Custom graphic design for sidebar elements and brand-matching visual icons)    
