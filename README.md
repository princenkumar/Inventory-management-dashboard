# Inventory Management System - Excel Dashboard

A comprehensive Excel-based inventory management solution designed for electronic goods retailers. This dashboard provides real-time inventory tracking, automated reordering alerts, and business performance analytics.

## 📋 Features

- **Real-time Inventory Tracking** - Monitor stock levels automatically
- **Automated Reordering Alerts** - Get notified when stock runs low
- **Purchase & Sales Management** - Streamlined transaction processing
- **Business Intelligence Dashboard** - Comprehensive performance analytics
- **Vendor & Customer Management** - Centralized contact database

## 🏗️ System Architecture

### Core Modules:
- **Master Data Management** (Products, Vendors, Customers)
- **Transaction Processing** (Purchases, Sales)
- **Inventory Control & Alerts**
- **Business Intelligence Dashboard**

## 📊 Worksheets

### 1. Dashboard (`Daboard`)
- Real-time operational alerts and notifications
- Low stock alerts with vendor contact information
- Products requiring immediate reordering

### 2. Master Data Tables
- **Customers** - Customer database with contact details
- **Products** - Product catalog with cost and selling prices
- **Vendors** - Supplier information with contact details

### 3. Transaction Modules
- **Purchase Management** - Track inventory purchases
- **Sales Management** - Record customer sales

### 4. Inventory Control
- Real-time stock monitoring
- Automated alert generation
- Inventory valuation

### 5. Business Intelligence (`Pivot`)
- Key performance metrics
- Sales analysis
- Profit & loss tracking

## 🚀 Quick Start

### Prerequisites
- Microsoft Excel (2016 or later recommended)
- Enable macros for full functionality

### Installation
1. Download the `Inventory Management Dashboard.xlsx` file
2. Open the file in Microsoft Excel
3. Enable editing if prompted
4. Enable macros for automated features

### Basic Usage

#### Adding Products:
1. Update `Products` sheet with HSN Code, Name, Cost, Selling Price
2. Update `Vendors` sheet with corresponding supplier information

#### Processing Purchase:
1. Navigate to `Purchase` sheet
2. Enter: HSN Code, Date, Units
3. System auto-populates remaining details

#### Processing Sale:
1. Navigate to `Sales` sheet
2. Enter: Customer ID, HSN Code, Units, Date
3. System auto-populates customer and product details

## ⚙️ Automation Features

### Smart Data Lookups
```excel
=IFERROR(VLOOKUP(D6,Products_Data[#All],2,0),"")
=IFERROR(VLOOKUP(Table5[[#This Row],[HSN Code]],Vendors_Data[#All],3,0),"")
Auto Calculations
Purchase Amount: Units × Cost Price

Sales Amount: Units × Selling Price

Stock Levels: Purchased - Sold

Inventory Value: Stock × Cost Price

Proactive Alerts
excel
=IF(Table7[[#This Row],[Stock]]<5,
   "📞"&E6&"Need to Reorder"&
   VLOOKUP(Table7[[#This Row],[HSN Code]],Vendors_Data[#All],4,0),"")
📈 Current Metrics
Customer Count: 10

Product Count: 10

Total Purchase Amount: ₹173,500

Total Sales Amount: ₹78,000

Total Stock Value: ₹78,000

Profit & Loss: ₹-17,500 (Current deficit)

🔧 Technical Specifications
Structured References: Uses Excel Tables for dynamic ranges

Error Handling: IFERROR functions prevent formula breakdowns

Data Validation: Ensures referential integrity across sheets

Scalability: Designed to accommodate growing business needs

📞 Support & Maintenance
Regularly backup the Excel file

Update master data tables when adding new records

Verify formula ranges if modifying sheet structure

Monitor Pivot sheet for accurate business intelligence
