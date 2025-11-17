# Web Scraping & Data Integration to Google Sheets Using Make.com

An automated pipeline that continuously monitors a website with **discounted airline tickets**, extracts key data from new listings, and sends it directly into **Google Sheets** for tracking and analysis.

---

## 🔍 Project Overview

This project uses **Make.com** to watch a specific airline ticket deals website, scrape fresh offers as they appear, and keep a structured log of all relevant data in Google Sheets.

The system runs automatically, so the client always has an up-to-date view of the latest deals without manual copy-paste or checking the site every few minutes.

---

## 🎯 Problem & Goals

The client needed:

- **Real-time monitoring** of new discounted airline ticket postings  
- Automatic extraction of key information such as:  
  - Ticket price  
  - Airline company  
  - Origin city  
  - Destination city  
  - Trip type (round-trip, one-way, etc.)  
- A centralized and **structured data source** in Google Sheets for quick review and analysis  

**Goal:** eliminate manual website checking and data entry, and replace it with a **reliable, automated data feed**.

---

## 🧩 Solution & Workflow

1. **Website monitoring with Make.com**  
   - Make.com scenario periodically checks the target page for new or updated airline ticket offers.  
   - Logic ensures only new entries are processed, avoiding duplicates.

2. **Web scraping & data extraction**  
   - Relevant HTML elements are parsed to pull out key data fields:
     - Airline company name  
     - Ticket price  
     - Origin city  
     - Destination city  
     - Trip type (e.g., round-trip, one-way)  

3. **Data cleaning & formatting**  
   - Parsed values are cleaned (e.g., price normalization, trimming spaces, consistent location formats).  
   - Data is mapped into a structured schema ready for Google Sheets.

4. **Google Sheets integration**  
   - Using Make.com’s Google Sheets modules and/or API calls, new records are appended to a dedicated sheet.  
   - Each row represents a single ticket offer with timestamp and key attributes.

---

## 🛠 Tools & Technologies Used

- **Make.com** – main automation and orchestration platform  
- **Web scraping techniques** – parsing HTML and extracting structured data  
- **API / Google Sheets integration** – pushing clean data into a live spreadsheet  

---

## 📈 Results & Impact

- **Real-time, automated capture** of discount airline ticket data – no more manual copying from the website.  
- **Improved data accuracy** thanks to consistent parsing and formatting rules.  
- **Time savings** – the client no longer needs to constantly monitor the website.  
- **Instant analysis** – all data lands directly in Google Sheets, ready for filtering, sorting, and reporting.  

---

## 🖼 Screenshots

**Make.com scenario**  
![Make.com scenario](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Airplane%20tickets%20data%20extraction/Airplane%20tickets.png)
