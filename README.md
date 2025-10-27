Inventory Management System - Excel Dashboard br
📊 System Overview
A comprehensive Excel-based inventory management solution designed for electronic goods retailers. This dashboard provides real-time inventory tracking, automated reordering alerts, and business performance analytics through an integrated set of worksheets.

🏗️ System Architecture
Core Modules:
Master Data Management (Products, Vendors, Customers)

Transaction Processing (Purchases, Sales)

Inventory Control & Alerts

Business Intelligence Dashboard

📑 Worksheets Breakdown
1. Dashboard (Daboard)
Purpose: Real-time operational alerts and notifications

Displays low stock alerts with vendor contact information

Shows products requiring immediate reordering

Format: 📞 ProductName Need to Reorder +91 XXXXXXXXXX

2. Master Data Tables
Customers (Costomers)
Field	Description	Sample Data
Customer ID	Unique identifier	101, 102, 103...
Name	Customer full name	Rajesh Kumar, Priya Sharma...
Email	Contact email	rajesh.kumar@email.com
Address	Customer location	Delhi, Mumbai, Kolkata...
Products (Products)
Field	Description	Sample Data
HSN Code	Product identifier (N1001-N1010)	N1001, N1002...
Product Name	Item description	Laptop, Mobile, Tablet...
Cost Price	Purchase cost	40000, 15000, 12000...
Selling Price	Retail price	45000, 18000, 14000...
Vendors (Vendors)
Field	Description	Sample Data
HSN Code	Links to Products	N1001, N1002...
Product Name	Corresponding product	Laptop, Mobile...
Vendor Name	Supplier business name	Sharma Electronics, Gupta Traders...
Phone Number	Contact details	+91 9876543210
Address	Vendor location	Delhi, Mumbai...
3. Transaction Modules
Purchase Management (Purchase)
Data Flow: HSN Code → Auto-populates Product Name, Vendor, Cost

Key Fields: HSN Code, Date, Units, Auto-calculated Amount

Automation: VLOOKUP to Products and Vendors tables

Calculation: Amount = Units × Cost Price

Sales Management (Sales)
Data Flow: Customer ID + HSN Code → Auto-populates all details

Key Fields: Customer ID, HSN Code, Date, Units, Auto-calculated Amount

Automation: VLOOKUP to Customers and Products tables

Stock Validation: Real-time stock level checking

4. Inventory Control (Inventory)
Core Function: Real-time stock monitoring and alert generation

Metric	Calculation	Purpose
P Unit	SUMIF(Purchase[Product])	Total purchased units
S Unit	SUMIF(Sales[Product])	Total sold units
Stock	P Unit - S Unit	Current inventory level
Stock Amount	Stock × Cost	Inventory valuation
Notification	IF(Stock<5, "Reorder")	Low stock alerts
Alert Trigger: Stock < 5 units → Generates vendor contact notification

5. Business Intelligence (Pivot)
Dashboard Metrics:

Customer Count: 10

Product Count: 10

Total Purchase Amount: ₹173,500

Total Sales Amount: ₹78,000

Total Stock Value: ₹78,000

Profit & Loss: ₹-17,500 (Current deficit)

Sales Analysis:

Top Selling: Tablet (3 units), Mobile (2 units)

Total Units Sold: 5

⚙️ Automation Features
1. Smart Data Lookups
excel
=IFERROR(VLOOKUP(D6,Products_Data[#All],2,0),"")
=IFERROR(VLOOKUP(Table5[[#This Row],[HSN Code]],Vendors_Data[#All],3,0),"")
2. Auto Calculations
Purchase Amount: Units × Cost Price

Sales Amount: Units × Selling Price

Stock Levels: Purchased - Sold

Inventory Value: Stock × Cost Price

3. Proactive Alerts
excel
=IF(Table7[[#This Row],[Stock]]<5,
   "📞"&E6&"Need to Reorder"&
   VLOOKUP(Table7[[#This Row],[HSN Code]],Vendors_Data[#All],4,0),
   "")
🚀 Usage Workflow
Adding New Products:
Update Products sheet with HSN Code, Name, Cost, Selling Price

Update Vendors sheet with corresponding supplier information

Processing Purchase:
Navigate to Purchase sheet

Enter: HSN Code, Date, Units

System auto-populates: Product Name, Vendor, Cost, Amount

Processing Sale:
Navigate to Sales sheet

Enter: Customer ID, HSN Code, Units, Date

System auto-populates: Customer Name, Product Name, Price, Amount

Monitoring Operations:
Check Dashboard for urgent reorder alerts

Review Inventory for stock levels and values

Analyze Pivot for business performance

📈 Business Insights
Current Status:
Low Stock Items: Multiple products below threshold

Sales Performance: Limited transaction volume (5 units total)

Inventory Health: ₹78,000 tied in current stock

Financial Position: Operating at deficit (-₹17,500)

Recommended Actions:
Immediate: Reorder low-stock items using vendor contacts from alerts

Sales Focus: Increase sales volume to improve cash flow

Inventory Optimization: Balance stock levels based on sales patterns

🔧 Technical Notes
Structured References: Uses Excel Tables for dynamic ranges

Error Handling: IFERROR functions prevent formula breakdowns

Data Validation: Ensures referential integrity across sheets

Scalability: Designed to accommodate growing product and customer base

📞 Support & Maintenance
Regularly backup the Excel file

Update master data tables when adding new products/vendors/customers

Verify formula ranges if modifying sheet structure

Monitor Pivot sheet for accurate business intelligence

This inventory management system provides a robust, automated solution for tracking electronic goods inventory with real-time alerts and comprehensive business analytics—ideal for small to medium-sized electronics retailers.
