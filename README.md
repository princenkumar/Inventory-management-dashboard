# Inventory Management Dashboard

A comprehensive Excel-based inventory management system with dashboard functionality for tracking products, vendors, customers, purchases, and sales.

## 📊 Project Overview

This Excel dashboard provides a complete inventory management solution with automated calculations, notifications, and reporting features.

## 📁 File Structure

The Excel workbook contains the following sheets:

### 1. **Dashboard** (`Daboard`)
- Main dashboard interface
- Real-time notifications for low stock items
- Quick overview of inventory status

### 2. **Customers** (`Costomers`)
- Customer database with contact information
- Customer ID, Name, Email, and Address details
- 10 sample customer records

### 3. **Products** (`Products`)
- Product catalog with HSN codes
- Cost price and selling price information
- 10 product categories including Laptop, Mobile, Tablet, etc.

### 4. **Vendors** (`Vendors`)
- Vendor information for each product
- Contact details and addresses
- Links products to their respective suppliers

### 5. **New Entry** (`New Entery`)
- Entry points for new purchase and sales transactions
- Simple interface for data input

### 6. **Purchase** (`Purchase`)
- Records all purchase transactions
- Automated calculations using VLOOKUP formulas
- Tracks HSN codes, vendors, dates, units, costs, and amounts

### 7. **Sales** (`Sales`)
- Sales transaction records
- Links to customer database
- Automated stock level tracking and price calculations

### 8. **Inventory** (`Inventory`)
- Real-time inventory tracking
- Stock level calculations (Purchase Units - Sales Units)
- Automated low stock notifications with vendor contact details
- Stock amount calculations

### 9. **Pivot** (`Pivot`)
- Summary reports and analytics
- Customer count, product count, purchase/sales amounts
- Profit and loss calculations
- Stock analysis by product categories

  ## Dasboard
    "D:\=DOCUMENTS=\=EXCEL=\Project File\Inventory Mangemant.png"

## 🔧 Key Features

- **Automated Notifications**: Low stock alerts with vendor contact information
- **Real-time Inventory Tracking**: Automatic stock level updates
- **Financial Reporting**: Purchase vs sales analysis and profit calculations
- **Vendor Management**: Complete vendor database with contact details
- **Customer Management**: Comprehensive customer information storage
- **Data Validation**: Error handling with IFERROR functions
- **Automated Calculations**: VLOOKUP and SUMIF formulas for accurate data processing

## 📋 Data Structure

### Products Included:
- Laptop, Mobile, Tablet, Printer, Monitor
- Keyboard, Mouse, Headphones, Smartwatch, Speaker

### Sample Data:
- 10 Customers across major Indian cities
- 10 Products with HSN codes
- 10 Vendors with contact information
- Sample purchase and sales transactions

## 🚀 How to Use

1. **Add New Products**: Use the Products sheet to add new items
2. **Record Purchases**: Use Purchase sheet for new stock acquisitions
3. **Record Sales**: Use Sales sheet for customer transactions
4. **Monitor Inventory**: Check Inventory sheet for stock levels
5. **View Reports**: Use Pivot sheet for analytical insights

## 📞 Notification System

The system automatically generates reorder notifications when stock levels fall below 5 units, displaying:
- Product name
- "Need to Reorder" message
- Vendor phone number for quick contact

## 💰 Financial Tracking

- **Cost Price**: Product acquisition cost
- **Selling Price**: Customer sale price
- **Stock Amount**: Total value of current inventory
- **Profit/Loss**: Automated calculation of business performance

## 🔄 Formulas Used

- `VLOOKUP` for data validation and cross-referencing
- `SUMIF` for conditional summation
- `IFERROR` for error handling
- Array formulas for complex calculations
- Conditional formatting for notifications

## 📍 Locations Covered

The system includes data from major Indian cities:
Delhi, Mumbai, Kolkata, Bangalore, Hyderabad, Pune, Jaipur, Chandigarh, Lucknow, Chennai, Ahmedabad

## 💡 Tips for Use

1. Always use the provided HSN codes for consistency
2. Update vendor information regularly
3. Check notifications daily for stock alerts
4. Backup the file regularly
5. Use the pivot tables for monthly reporting

---

*This inventory management system is designed for small to medium businesses to efficiently track and manage their product inventory.*
