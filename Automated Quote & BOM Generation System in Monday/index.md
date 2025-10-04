# Automated Quote & BOM Generation System in monday.com

##  Project Overview
This project delivers a fully automated quoting and bill-of-materials (BOM) solution inside monday.com.  
It connects multiple boards—Deals, Quote Generation, Item Management, BOM, and Customer—to handle everything from quote creation to BOM file generation in one seamless workflow.

##  Problem & Goals
Manually building quotes and BOMs was time-consuming and error-prone.  
The goal was to automate quote creation, ensure accurate tax/total calculations, and generate BOM files on demand, all while keeping data synchronized across boards.

##  Solution & Implementation
- **Inter-linked Boards**: Deals, Quote Generation, Item Management, BOM, and Customer boards are fully connected.
- **Quote Automation**: Moving a deal to the **Create Quote** group auto-creates a linked item in the Quote Generation board.
- **One-Click Quote Creation**: Users add required items as subitems and click **Create Quote** to instantly generate a Quote file from a predefined template.  
  - Automatic total and tax calculations  
  - File saved to OneDrive and attached in monday.com
- **BOM Generation**: Item Management board connects to BOM board; a **Create BOM** button generates a complete BOM file within seconds, mirroring all necessary fields.

##  Tools & Technologies Used
- monday.com (Boards, Automations, File Columns)
- Make.com (Integromat) for automation logic
- OneDrive for secure file storage and access

##  Results & Outcomes
- **Time Savings**: Quotes and BOMs—regardless of line-item count—are created in seconds.  
- **Accuracy**: Built-in tax and total calculations remove manual errors.  
- **Scalability**: Supports any volume of quotes or items with minimal user input.

##  Screenshots

- **Quote Generation Board**  


- **Create Quote Automation**  


- **BOM Management Board**  

