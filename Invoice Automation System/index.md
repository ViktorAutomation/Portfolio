# Invoice Management System Integration  
**Monday.com + Xero + Make.com**

An end-to-end **invoice and bill management system** with **Monday.com** as the central hub, **Xero** for accounting, and **Make.com** handling all the automation and syncing between them.

---

## 🔍 Project Overview

This solution replaces fragmented invoice handling with a structured, automated workflow.

From a single Monday.com workspace, the system can:

- Capture invoice data from incoming emails / PDFs  
- Manage suppliers, items, and GL accounts  
- Create draft bills directly in Xero  
- Keep everything linked and traceable across multiple boards  

Five Monday.com boards and four Make.com scenarios work together to deliver a complete invoice processing pipeline.

---

## 🎯 Problem & Goals

The client needed a robust way to:

- Manage **vendor invoices**, line items, suppliers, and GL accounts with **minimal manual input**  
- Extract **structured data** from PDF invoices and map it correctly into their system  
- Keep **Xero and Monday.com in sync** for:
  - Suppliers  
  - Items  
  - Bills  
- Reduce duplicated data, manual errors, and back-and-forth between tools  
- Provide **clear status feedback** for each automation event (success, errors, duplicates, etc.)

**Goal:** build a reliable, transparent invoicing engine where data flows smoothly from email → Monday.com → Xero, with clear oversight and control.

---

## 🧩 Solution & Workflow

### 1. Structured Monday.com boards

Five boards were created and linked:

- **Invoice Management**  
  Central board for all invoice details. Used to initiate Xero bill creation and track statuses.

- **Item Management**  
  Stores invoice line items and links them to invoices and suppliers. Handles item codes and descriptions.

- **Suppliers Directory**  
  Tracks all vendor records and their sync status with Xero.

- **Xero Bills**  
  Logs draft bills created in Xero, including links back to Xero and related Monday items.

- **GL Account Management**  
  Maintains Xero GL account codes to ensure correct coding for each item and bill.

### 2. Make.com scenarios (automation backbone)

Four core scenarios orchestrate the flow:

1. **Email → Invoice Parser**  
   - Listens to a dedicated email inbox for incoming PDF invoices.  
   - Uses **OpenAI API** to extract structured fields (supplier, invoice number, date, totals, etc.).  
   - Searches for matching suppliers/items in Monday.com.  
   - Creates a new record in the **Invoice Management** board and related line items in **Item Management**.

2. **Supplier Sync**  
   - When a supplier is marked as approved in Monday.com:  
     - Checks Xero to see if the supplier already exists.  
     - Creates a new contact in Xero if not found.  
     - Writes back Xero IDs and statuses to the **Suppliers Directory** board.

3. **Item Sync**  
   - Similar logic, but for **items**:  
     - Validates if an item code already exists in Xero.  
     - Creates or updates items as needed.  
     - Handles duplicate code detection with clear error messages like  
       _"Error – Item code already exists"_ so managers can fix issues quickly.

4. **Bill Creation**  
   - Triggered by a button in the **Invoice Management** board (e.g. “Create Bill in Xero”).  
   - Gathers validated supplier, item, and GL data from related boards.  
   - Creates a **draft bill** in Xero with proper lines, amounts, tax, and coding.  
   - Logs the result in the **Xero Bills** board with a direct link to the bill in Xero.

### 3. Error handling & transparency

- Each scenario returns **human-readable status messages** to Monday.com.  
- Errors, duplicates, and missing data are surfaced clearly so managers can resolve them without digging into raw logs.

---

## 🛠 Tools & Technologies Used

- **Monday.com** – boards, automations, relations, permissions  
- **Make.com** – main orchestration and integration layer  
- **Xero** – accounting system (suppliers, items, bills)  
- **OpenAI API** – invoice text extraction and parsing from PDFs  

---

## 📈 Results & Impact

- **Reduced manual data entry** by automating invoice parsing, item creation, and supplier checks.  
- **Fewer errors & duplicates** thanks to smart validation and Xero sync logic.  
- **Faster processing times** – invoices move from inbox to draft bill with minimal human effort.  
- **High transparency** – every automation step is logged with clear status messages and traceable workflows.  
- **Better control for managers** – approvals and exceptions can be handled quickly from within Monday.com.

---

## 🖼 Screenshots

**Monday – Invoice Management System**  
![Invoice Management System](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Invoice%20Automation%20System/6.png)

**Monday – Item Management**  
![Item Management](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Invoice%20Automation%20System/7.png)

**Monday – Supplier Management**  
![Supplier Management](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Invoice%20Automation%20System/8.png)

**Monday – Xero Bills**  
![Xero Bills](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Invoice%20Automation%20System/9.png)

**Make.com scenarios**  
![Make.com scenarios](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Invoice%20Automation%20System/1.png)

**Email parse → Monday invoices board**  
![Email parse - Monday invoices board](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Invoice%20Automation%20System/2.png)

**Monday items approved → Create item in Xero**  
![Monday items approved - Create item in Xero](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Invoice%20Automation%20System/3.png)

**Monday Approved Suppliers → Xero Check/Create**  
![Monday Approved Suppliers - to Xero Check/Create](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Invoice%20Automation%20System/4.png)

**Monday – Create bill in Xero**  
![Monday - Create bill in Xero](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Invoice%20Automation%20System/5.png)
