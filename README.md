# Banking Data Analysis 
**Empowering Financial Institutions with Real-Time Performance Insights**

---

## Project Overview  
This Power BI **Banking Dashboard** provides **comprehensive, real-time analytics** for a modern financial institution, enabling leadership and operations teams to monitor **loan performance, deposit trends, customer profitability, risk exposure, and branch efficiency** across regions and time periods.

Built on a robust semantic model with **DAX-driven KPIs**, **dynamic filtering**, and **drill-through capabilities**, the dashboard supports data-driven decisions in **risk management, customer segmentation, product performance, and operational excellence**.

---

## Live Report Link  
https://app.powerbi.com/reportEmbed?reportId=935218bf-3942-4e01-8f18-cf434ee18ce8&autoAuth=true&ctid=6627360e-a7aa-4e24-bd88-a75fbc42bc55

---

## Tools Used  
- **Excel** – Primary data source and initial exploration  
- **Power BI Desktop** – Data modeling, DAX, visualization, and report design  
- **DAX (Data Analysis Expressions)** – Advanced financial calculations and time intelligence  
- **Power Query (M Language)** – Data cleaning, transformation, and date table creation  

---

## Power BI Techniques Implemented  

| Technique | Usage |
|--------|-------|
| **Dynamic DAX Measures** | MTD/QTD/YTD Deposits, Loan Growth, NPA Ratio, CASA Ratio |
| **Time Intelligence** | `DATESMTD`, `DATESQTD`, `SAMEPERIODLASTYEAR`, `PARALLELPERIODS` |
| **Disconnected Slicer Table** | Unified Time Period slicer with `SWITCH` logic |
| **Conditional Formatting** | Risk levels (Green/Yellow/Red), growth indicators |
| **Bookmarks** | Reset filters, navigation toggles, scenario views |
| **KPI Cards & Sparklines** | High-level trends with mini-charts |
| **Responsive Design** |  desktop optimized (Fit to Width) |

## Dashboard Structure  

### 1. **Executive Summary**  
- **KPI Cards**: Total Deposits, Total Loans, CASA Ratio, NPA Ratio, Customer Profitability  
- **Sparkline Trends**: Deposit & Loan Growth (12-month)  
- **Gauge**: Risk Exposure vs. Target  

### 2. **Deposits & Liabilities**  
- **Clustered Column**: Deposits by Product (Savings, FD, RD) & Region  
- **Area Chart**: Deposit Growth YoY  
- **Top 5 Branches** by Deposit Mobilization  
- **CASA vs. Term Deposit Matrix**  

### 3. **Loans & Assets**  
- **Stacked Bar**: Loan Portfolio by Type (Home, Auto, Personal, Business)  
- **NPA Trend Line Chart** (with threshold line)  
- **Risk Heatmap**: NPA % by Region & Loan Type  
- **Top 10 Delinquent Accounts** (drill-through ready)  

### 4. **Customer Analytics**  
- **Donut Chart**: Customer Segment Distribution (Retail, SME, Corporate)  
- **Scatter Plot**: Profitability vs. Relationship Age  
- **New vs. Existing Customers** (Acquisition & Cross-Sell)  
- **Customer Lifetime Value (CLV) Matrix**  

### *(Optional)* **Branch Performance**  
- **Map Visual**: Deposits & Loans by Branch Location  
- **Branch Efficiency Scorecard**  
- **Footfall vs. Conversion Funnel**  

---

## Domain Knowledge (Banking Context)  

| Area | Key Concepts Covered |
|------|------------------------|
| **Deposits** | CASA ratio, term deposits, cost of funds |
| **Loans** | Loan book growth, NPA management, provisioning |
| **Risk** | Credit risk, delinquency tracking, early warning signals |
| **Customer** | Segmentation, profitability, cross-sell potential |
| **Branch** | Performance benchmarking, resource optimization |

---

## Business Terms Used  

- **CASA** – Current Account, Savings Account  
- **NPA** – Non-Performing Asset  
- **YoY Growth** – Year-over-Year change  
- **Customer Profitability** – Net income per customer  
- **MTD / QTD / YTD** – Month/Quarter/Year to Date  
- **Cross-Sell Ratio** – Products per customer  


---

## Importing Data into Power BI  
Data is sourced from **Excel workbooks** containing structured tables:  
`Deposits`, `Loans`, `Customers`, `Accounts`, `Branches`, `Date`, `Geography`  

All files are imported via **Power Query**, cleaned, and loaded into the model.  

**Relationships established via**:  
- `Deposits[CustomerID]` → `Customers[CustomerID]`  
- `Loans[CustomerID]` → `Customers[CustomerID]`  
- `Deposits[BranchID]` → `Branches[BranchID]`  
- `Deposits[Date]` → `Date[Date]`  
- `Branches[RegionID]` → `Geography[RegionID]`  

---

## Dashboard Navigation  

- **Slicers**:  
  - Region  
  - Product Type (Deposit/Loan)  
  - Customer Segment  
  - Risk Status  
  - Unified Time Period  

- **Bookmarks**:  
  - Drill to customer/loan details  
  - Reset all filters  
  - Toggle risk view  

- **Page Navigation**:  
  - Clear icons 


**Ready to deploy?**  
**Publish to Power BI Service** → **Create App** → **Share with stakeholders.**

