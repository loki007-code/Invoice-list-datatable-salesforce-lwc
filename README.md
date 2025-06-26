# 📦 Invoice-list-datatable-salesforce-lwc Component

This Lightning Web Component (LWC) is used to display a paginated and sortable list of Invoices and their related Invoice Line Items in Salesforce. Users can also add new products to invoices using a modal form.

## 🚀 Features

- Display list of Invoices with pagination
- View Invoice Line Items for each Invoice
- Sort Invoices and Invoice Lines by columns
- Add Product to Invoice with modal input
- Toast notifications for user feedback
- Navigation to record pages

## 📁 Files

### LWC Component

- `displayInvoiceListTable.html` - UI template for displaying invoices, lines, and modal
- `displayInvoiceListTable.js` - JavaScript logic (data loading, sorting, modal, pagination)
- `displayInvoiceListTable.js-meta.xml` - Metadata file

### Apex Class

- `DisplayInvoiceListTable.cls` - Contains methods to fetch/save invoices and products

## ⚙️ Apex Methods

- `getInvoiceList()` - Returns list of Invoice__c records
- `getInvoiceLineById(invoiceId)` - Returns list of related Invoice_Line__c records
- `getAllProducts()` - Returns list of Product__c records
- `saveInvoiceLine(invoiceLineList)` - Saves a list of new invoice lines

## 📦 Custom Objects & Fields

### Invoice__c

- Invoice_Date__c (Date)
- Buyer_Name__c (Lookup)
- Seller_Name__c (Lookup)
- Invoice_Status__c (Picklist)
- Pending_Amount__c (Roll-up Summary)

### Invoice_Line__c

- Product_Name__c (Lookup)
- Quantity__c (Number)
- Price__c (Currency)
- Taxes__c (Currency)
- Product_Total__c (Formula)
- Grand_Total__c (Formula)

## 📄 Usage

1. Deploy Apex class to Salesforce.
2. Deploy LWC using VS Code or Salesforce CLI.
3. Add the component to a Lightning App Page via Lightning App Builder.
4. Interact with the component on UI.

## ✅ To-Do / Enhancements

- Add loading spinners during data fetch
- Search/filter functionality
- Validation enhancements on modal input

---

## 🙌 Credits

Developed by Logesh Aravindh, Salesforce Developer.

---
