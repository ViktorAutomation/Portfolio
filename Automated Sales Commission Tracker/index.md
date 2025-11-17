# Automated Sales Commission Tracker in Monday.com

A fully automated **sales commission tracking system** built in **Monday.com** and powered by **Make.com**.  
It calculates commissions per salesperson, manages payment dates, and keeps data secure with separate views for leadership and individual reps.

---

## 🔍 Project Overview

This solution replaces manual spreadsheets and ad-hoc calculations with a structured commission engine inside Monday.com.

Key elements:

- A **central management board** for leadership with full visibility  
- **Private boards for each salesperson** so they see only their own deals and commissions  
- Automated creation and calculation of commission records as deals are completed  

---

## 🎯 Problem & Goals

Previously:

- Commissions were calculated **manually**, which was slow and error-prone  
- Sales reps had **no easy way** to check their current or upcoming commissions  
- Leadership lacked a real-time, centralized overview  

**Goals:**

- Automate commission creation and calculation when deals are completed  
- Give leadership a clear, real-time overview of all commissions  
- Provide each salesperson with a private, self-service view of **only their own commissions**  

---

## 🧩 Solution & Workflow

1. **Central Commission Tracker (Leadership View)**  
   - A main **Commission Tracker** board accessible only to sales management.  
   - Contains all deals, commission amounts, payment dates, and key deal details.  

2. **Individual Salesperson Boards (Private Views)**  
   - Each salesperson has a dedicated, permission-controlled board.  
   - They can:
     - Create and track their deals  
     - See calculated commissions for only their own records  

3. **Automated record creation**  
   - When a deal in a salesperson’s board is moved to the **Completed** stage:
     - An automation (via Monday.com + Make.com) creates a linked item in the **Commission Tracker** board.  
     - Core deal data (value, margin, salesperson, dates) is synced or mirrored.

4. **Automatic commission calculations**  
   - Make.com handles custom logic for:
     - Commission percentages  
     - Amounts based on deal value / margin  
     - Payment dates (e.g., end of month / after client payment)  
   - Results are written back to the Commission Tracker and to the salesperson’s board.

5. **Privacy & permissions**  
   - Leadership can see the **full portfolio of commissions**.  
   - Each salesperson sees only:
     - Their own deals  
     - Their corresponding commission lines and statuses  

---

## 🛠 Tools & Technologies Used

- **Monday.com** – boards, automations, mirrored/linked columns, permissions  
- **Make.com (Integromat)** – advanced commission logic, data syncing, and automation flows  

---

## 📈 Results & Impact

- **Efficiency:** Commission records and calculations are now fully automated once deals are marked as completed.  
- **Accuracy:** Manual errors are removed thanks to standardized formulas and automation.  
- **Transparency & privacy:**  
  - Sales reps can check their commissions at any time in their private boards.  
  - Leadership keeps a complete overview in one central management board.  
- **Scalability:** New reps, new commission rules, or additional data points can be added without breaking the system.

---

## 🖼 Screenshots

**Create new deal in personal board**  
![Create new deal in Personal board](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automated%20Sales%20Commission%20Tracker/create%20deal%20in%20personal%20board.png)

**Update commission in personal board**  
![Update commission in personal board](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automated%20Sales%20Commission%20Tracker/Update%20commission%20in%20personal%20board.png)
