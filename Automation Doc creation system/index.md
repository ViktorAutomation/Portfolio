# Automation Google Doc Creation and Parsing System

An end-to-end system that **creates, manages, and parses Google Docs** based on data in **Airtable**, with **Make.com** and **Google Apps Script** handling automation, and **Slack** keeping the team in the loop.

---

## 🔍 Project Overview

This solution turns Airtable into the **single source of truth** for document generation and approval.

From one Airtable base, the system can:

- Generate new Google Docs from a template  
- Notify the right people via Slack with direct links  
- Let users build documents using predefined content blocks  
- Parse approved sections of a Google Doc and push them back to Airtable via Make.com  

Everything is tightly connected so content stays consistent across tools.

---

## 🎯 Problem & Goals

The client needed a way to:

- Create Google Docs from **structured data** stored in Airtable  
- Keep the team updated via **Slack notifications** when new docs were generated  
- Manage a **content approval** process inside Google Docs  
- Automatically **parse approved content** and sync it back into Airtable for tracking and reuse  

**Goal:** replace fragmented manual work (copying text between Sheets, Docs, messages) with a clean, automated workflow from data → document → approval → structured records.

---

## 🧩 Solution & Workflow

1. **Airtable as the central database**  
   - An existing Google Sheet was migrated into a structured **Airtable base** with two linked tables:
     - **Main table** – source records and document generation triggers  
     - **Approved table** – final, approved content blocks  

2. **Template-based Google Doc creation**  
   - A **Google Doc template** was created and a specific folder defined as the storage location.  
   - In Airtable, users tick a **checkbox** to request a new document.  
   - This triggers a Make.com scenario that:
     - Creates a new Google Doc from the template  
     - Inserts relevant data from Airtable  
     - Updates the Airtable record with the document link  

3. **Slack notifications for team visibility**  
   - The same automation sends a **Slack message** with the newly created Doc link to a designated channel.  
   - This keeps the team informed and encourages timely review without manual sharing.

4. **Custom Google Apps Script – document actions**  
   Two custom scripts were added to the Google Doc template:

   - **Custom action menu + “Add block template”**  
     - Adds a menu to the Google Docs UI.  
     - Allows users to quickly insert **predefined text blocks** into the document, ensuring consistent structure and wording.

   - **Parsing & sending approved blocks**  
     - The script scans the document for content blocks that are marked with something like **"Approved: Yes"**.  
     - Only these approved sections are packaged and sent via **webhook** to Make.com.

5. **Make.com webhook & Airtable sync**  
   - Make.com receives the parsed content via webhook.  
   - It then:
     - Creates a new record in the **Approved** Airtable table  
     - Links that approved content back to the relevant record in the **Main** table  

This closes the loop: Airtable → Google Doc → Approval in Google Doc → Airtable (Approved).

---

## 🛠 Tools & Technologies Used

- **Make.com** – orchestration of document creation and data sync  
- **Google Docs** – document template and content workspace  
- **Google Apps Script** – custom menu actions and parsing logic  
- **Airtable** – main database and approval records  
- **Slack integration** – notifications for new documents and workflow visibility  

---

## 📈 Results & Impact

- **Automated document creation** directly from Airtable, significantly reducing manual effort and copy-paste errors.  
- **Better communication** – Slack notifications ensure the right people are notified with direct access to the documents.  
- **Structured approval workflow** – only content marked as approved gets pushed back into Airtable.  
- **Improved data integrity** – Airtable always reflects the current, approved content without manual updates.  

---

## 🖼 Screenshots

**Airtable main table**  
![Airtable Main table](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automation%20Doc%20creation%20system/AT%20base%20Main.png)

**Google Doc template**  
![Google doc template](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automation%20Doc%20creation%20system/Doc%20template%202.jpg)

**Make.com – create Google Doc**  
![Make.com - create Google doc](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automation%20Doc%20creation%20system/Create%20doc.png)

**Catch webhook – send to Airtable**  
![Catch webhook - send to Airtable](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automation%20Doc%20creation%20system/Webhook-to%20AT.png)

**Google Apps Script – Add new block**  
![Google Apps Script - Add new block](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automation%20Doc%20creation%20system/Script-add%20new%20block)

**Google Apps Script – Send approved block to Make.com**  
![Google Apps Script - Send approved block to Make.com](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automation%20Doc%20creation%20system/Script-Send%20Approved.png)

**Airtable Approved table**  
![Airtable Approved table](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automation%20Doc%20creation%20system/AT%20base%20Approved.png)
