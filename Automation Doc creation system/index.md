# Automation Google Doc Creation and Parsing System

## Project Overview

This project automated the creation, management, and parsing of Google Docs using Airtable as a central database, Make.com for automation, and Google Apps Script for enhanced document interactivity and data integration.

## Problem & Goals

The client needed an efficient workflow to create and manage Google Documents from structured data stored in Airtable, streamline team communication through Slack notifications, and automate document content parsing and record updates.

## Solution & Implementation

- Converted an existing Google Sheet into a structured Airtable base consisting of two interconnected tables.
- Created a Google Doc template and designated a storage location for newly generated documents.
- Implemented an automation triggered via Airtable: Upon selecting a checkbox, a new Google Doc is created from a template, a Slack notification containing the document link is sent to a designated channel, and the Airtable record is updated accordingly.
- Developed two custom Google Apps Script functionalities:
  - A custom action menu in Google Docs, including an "Add block template" button to append predefined text blocks.
  - An automated parsing script that reads the Google Doc content, identifies text blocks marked as "Approved: Yes," and sends these blocks via a webhook to Make.com.
- Configured Make.com webhook to receive parsed document data, create a new entry in the "Approved" Airtable table, and link these records back to the main table.

## Tools & Technologies Used

- Make.com
- Google Docs
- Google Apps Script
- Airtable
- Slack integration

## Results & Outcomes

- Automated document creation, saving significant manual efforts and reducing potential errors.
- Improved internal team communication through timely Slack notifications.
- Efficiently managed content approval and data synchronization between Google Docs and Airtable, enhancing workflow productivity.

## Screenshots

- **Airtable Main table**
![Airtable Main table](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automation%20Doc%20creation%20system/AT%20base%20Main.png)

- **Google doc template**
![Google doc template](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automation%20Doc%20creation%20system/Doc%20template%202.jpg)

- **Make.com - create Google doc**
![Make.com - create Google doc](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automation%20Doc%20creation%20system/Create%20doc.png)

- **Catch webhook - send to Airtable**
![Catch webhook - send to Airtable](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automation%20Doc%20creation%20system/Webhook-to%20AT.png)

- **Google Apps Script - Add new block**
![Google Apps Script - Add new block](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automation%20Doc%20creation%20system/Script-add%20new%20block)

- **Google Apps Script - Send approved block to Make.com**
![Google Apps Script - Send approved block to Make.com](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automation%20Doc%20creation%20system/Script-Send%20Approved.png)

- **Airtable Approved table**
![Airtable Approved table](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automation%20Doc%20creation%20system/AT%20base%20Approved.png)
