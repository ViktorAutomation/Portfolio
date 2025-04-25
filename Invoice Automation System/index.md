# Invoice Management System Integration  
**Monday.com + Xero + Make.com**

---

📌 **Project Overview**  
This project delivered a fully automated invoice and bill management workflow using Monday.com as the central hub, Make.com for automation, and Xero for accounting. It streamlined the handling of invoices, suppliers, items, and bill creation, while ensuring data accuracy and transparency across all systems.

---

🎯 **Problem & Goals**  
The client needed an end-to-end system to manage vendor invoices, line items, and supplier records with minimal manual input. Goals included:
- Automating PDF invoice extraction and structured data entry.
- Ensuring Xero and Monday.com remain in sync for suppliers, items, and bills.
- Reducing duplicate data and manual errors.
- Providing clear status feedback for every automation event.

---

🛠️ **Solution & Implementation**  
Created five structured boards in Monday.com:
- **Invoice Management** – central board for invoice details and Xero bill initiation.  
- **Item Management** – stores invoice line items with links to respective invoices and suppliers.  
- **Suppliers Directory** – tracks and verifies supplier records.  
- **Xero Bills** – logs draft bills created in Xero with live links.  
- **GL Account Management** – maintains updated Xero account codes.

Developed four Make.com scenarios to automate the process:
1. **Email to Invoice Parser**: Extracts key fields from PDF invoices via OpenAI API, searches for matching suppliers/items, and creates a new invoice record.
2. **Supplier Sync**: Upon approval, checks Xero for existing supplier or creates a new one.
3. **Item Sync**: Similar logic applied to invoice items, with duplicate code detection and handling.
4. **Bill Creation**: Generates a draft bill in Xero with linked supplier and item data when a button is clicked in monday.com.

All scenarios include advanced error handling and return clear status messages (e.g., *“Error – Item code already exists”*) to help managers quickly resolve issues.

---

⚙️ **Tools & Technologies Used**  
- Monday.com  
- Make.com  
- Xero  
- OpenAI API (for invoice text extraction)

---

📈 **Results & Outcomes**  
- Reduced manual data entry and duplicate entries through smart automation.  
- Improved processing time and data consistency between systems.  
- Enhanced operational transparency with detailed error reporting and traceable workflows.  
- Allowed team managers to easily manage approvals and resolve exceptions.

---

📸 **Screenshots**   
