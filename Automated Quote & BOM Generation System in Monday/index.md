# Automated Quote & BOM Generation System in Monday.com

A fully automated **quoting** and **bill-of-materials (BOM)** system built inside **Monday.com**, powered by **Make.com** and connected boards.  
It takes a deal from “ready to quote” to a generated Quote file and BOM file in just a few clicks.

---

## 🔍 Project Overview

This solution connects several Monday.com boards—**Deals**, **Quote Generation**, **Item Management**, **BOM**, and **Customer**—into one cohesive workflow.

From a single deal, users can:

- Create a structured quote based on selected items  
- Automatically calculate totals and taxes  
- Generate a BOM file on demand  
- Store files in OneDrive and attach them back to Monday.com  

Everything stays linked and in sync across boards.

---

## 🎯 Problem & Goals

Before this system:

- Quotes and BOMs were being built manually in documents or spreadsheets  
- Copy-paste across tools caused **errors** and took a lot of time  
- Data often drifted between deals, items, and customer records  

**Goals:**

- Automate quote creation directly from the **Deals** pipeline  
- Ensure **accurate tax and total calculations** every time  
- Generate **BOM files** in seconds whenever needed  
- Keep all data synchronized across multiple Monday.com boards

---

## 🧩 Solution & Workflow

1. **Interlinked Monday.com boards**  
   - Boards involved:
     - **Deals / Opportunities**
     - **Quote Generation**
     - **Item Management**
     - **BOM**
     - **Customer**  
   - Relations and mirror columns connect these boards so each quote and BOM stays tied to the right deal and customer.

2. **Quote automation from the Deals board**  
   - When a deal is moved to a specific group (e.g. **Create Quote**), an automation:
     - Creates a **linked item** in the **Quote Generation** board  
     - Pulls in relevant deal and customer data  

3. **One-click quote creation**  
   - In the **Quote Generation** board:
     - Users add required line items as **subitems** (pulled from the Item Management board).  
     - Clicking a **Create Quote** button triggers a Make.com scenario that:
       - Fills a **predefined quote template**  
       - Calculates line totals, subtotals, tax, and grand total  
       - Generates a Quote file (PDF/Doc)  
       - Saves the file to **OneDrive** and attaches it back to Monday.com  

4. **Automated BOM generation**  
   - The **Item Management** board is connected to a **BOM** board.  
   - A **Create BOM** button triggers another Make.com scenario that:
     - Collects all required item data  
     - Builds a structured BOM file with all necessary fields  
     - Stores it on **OneDrive** and links it back to the relevant deal/quote in Monday.com  

5. **Supplier quote parsing (optional component)**  
   - A separate Make.com scenario parses supplier quotes and maps them into the system.  
   - This supports comparing internal quotes vs. supplier data and updating BOMs accordingly.

---

## 🛠 Tools & Technologies Used

- **Monday.com** – boards, relations, automations, file columns  
- **Make.com (Integromat)** – core automation and document generation logic  
- **OneDrive** – secure file storage and access for generated quotes & BOMs  

---

## 📈 Results & Impact

- **Time savings:** Quotes and BOMs—regardless of the number of line items—are created in seconds instead of manually building documents.  
- **Higher accuracy:** Built-in calculations for totals and taxes eliminate manual mistakes.  
- **Scalability:** The system supports high volumes of deals and items with minimal additional effort.  
- **Better structure:** All quotes and BOMs remain linked to deals, items, and customers inside Monday.com, improving visibility for sales and operations teams.

---

## 🖼 Screenshots

**Quote Generation Scenario**  
![Quote Generation Scenario](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automated%20Quote%20&%20BOM%20Generation%20System%20in%20Monday/Quote%20Generation.png)

**Quote File**  
![Quote](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automated%20Quote%20&%20BOM%20Generation%20System%20in%20Monday/Quote.png)

**BOM Scenario**  
![BOM Scenario](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automated%20Quote%20&%20BOM%20Generation%20System%20in%20Monday/BOM%20Scenario.png)

**Quote Generation Board**  
![Quote Generation Board](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automated%20Quote%20&%20BOM%20Generation%20System%20in%20Monday/Quote%20Board.png)

**BOM Generation Board**  
![BOM Generation Board](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automated%20Quote%20&%20BOM%20Generation%20System%20in%20Monday/BOM%20Board.png)

**Supplier Quote Parsing Scenario**  
![Quote Parsing Scenario](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automated%20Quote%20&%20BOM%20Generation%20System%20in%20Monday/Quote%20Scenario.png)
