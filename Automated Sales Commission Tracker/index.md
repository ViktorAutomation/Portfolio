# Automated Sales Commission Tracker in monday.com

## Project Overview
This project delivers a fully automated commission tracking system in monday.com, powered by Make.com.  
It calculates commissions for each salesperson automatically, manages all payment dates, and ensures privacy by providing individual boards for each salesperson alongside a central management board for leadership.

## Problem & Goals
Manual commission calculation was time-consuming, error-prone, and unabled for sales team members to check their commissions on daily basis.  
The goal was to automate commission calculations, provide leadership with a clear overview, and give each salesperson private access to only their own commissions.

## Solution & Implementation
- **Main Board (Leadership View):** Centralized tracker visible only to sales management, showing all deals, commissions, and payment dates.  
- **Salesperson Boards (Private Views):** Each salesperson has a private board showing only their deals and commission records.  
- **Automations:**  
  - When a deal is moved to the **Completed** stage, a new record is created in the Commission Tracker board.  
  - Key deal data (value, margin, dates, etc.) is mirrored automatically.  
  - Commission amounts and payment dates are calculated automatically.  

## Tools & Technologies Used
- monday.com (Boards, Automations, Permissions)  
- Make.com (Integromat) for advanced automation logic  

## Results & Outcomes
- **Efficiency:** Commission records and calculations are fully automated.  
- **Accuracy:** Eliminated manual errors by automatically calculating values and dates.  
- **Privacy:** Each salesperson can view only their own commissions, ensuring confidentiality.  
- **Visibility:** Sales leadership has full oversight in one central board.  

## Screenshots

- **Create new deal in Personal board**  
![Create new deal in Personal board](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automated%20Sales%20Commission%20Tracker/create%20deal%20in%20personal%20board.png)

- **Update commission in personal board**  
![Update commission in personal board](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automated%20Sales%20Commission%20Tracker/Update%20commission%20in%20personal%20board.png)

