# Automatic Post Creation System from Web Page to Telegram and Facebook

An automated pipeline that turns **news articles from a website** into **ready-to-publish posts** for **Telegram** and **Facebook**, with human approval and content validation steps built in.

---

## 🔍 Project Overview

This system uses **Make.com**, **OpenAI**, and messaging integrations to:

- Monitor a news website for new articles  
- Generate summaries and draft posts automatically  
- Route posts through a Telegram-based approval flow  
- Validate content, store it in Google Sheets, and publish approved posts to social media  

The result is a controlled, semi-automated content machine where humans approve, and automations do the rest.

---

## 🎯 Problem & Goals

The client needed:

- **Automated monitoring** of specific news sources  
- **Automatic summarization** and post creation based on new articles  
- A way to **approve or reject** posts from a convenient interface (Telegram)  
- **Structured publishing** to Telegram and Facebook once approved  
- Central tracking of all posts and statuses in Google Sheets  

**Goal:** significantly reduce manual work around content sourcing, drafting, and posting, while still keeping humans in the loop for quality and fact-checking.

---

## 🧩 Solution & Workflow

The solution is built around multiple Make.com scenarios (with the option to merge/streamline them, depending on client needs):

1. **Scenario 1 – From website to Telegram (drafts & summaries)**  
   - Monitors a website or RSS feed for new news articles.  
   - Automatically:
     - Fetches article content  
     - Summarizes it using the OpenAI API  
     - Generates a **preliminary post** (text + link, optional hashtags)  
   - Sends the draft post to a **Telegram bot** for user review and approval.

2. **Scenario 2 – Validation & post preparation**  
   - When a user interacts with the Telegram bot (e.g., approving a post):  
     - The system flags that article as “selected” or “approved” in Google Sheets.  
     - Additional validation checks can be performed (e.g., verifying content with other sources or using tools like Prepl).  
     - The final post text is generated and stored in Google Sheets, ready for publishing.

3. **Scenario 3 – Approval tracking & publishing**  
   - Regularly checks Google Sheets for posts with an **approved** status.  
   - Automatically publishes confirmed posts to:
     - **Telegram** (channel/group)  
     - **Facebook** (page)  
   - Logs publishing timestamps and statuses back to Google Sheets for tracking.

4. **Optional streamlining**  
   - Depending on requirements, the logic can be combined into **two scenarios** instead of three:
     - One for monitoring + drafting + approval  
     - One for validation + publishing  

---

## 🛠 Tools & Technologies Used

- **Make.com** – orchestrating all flows and API calls  
- **OpenAI API** – summarization and post text generation  
- **Telegram integration** – approval bot and notifications  
- **Facebook integration** – automatic page posting  
- **Google Sheets** – status tracking, content storage, and simple analytics  

---

## 📈 Results & Impact

- **End-to-end automation** of the social post creation pipeline (from article detection to publishing).  
- **Reduced manual workload** by automating repetitive tasks like summarization, formatting, and posting.  
- **Higher consistency and quality** thanks to structured validation and approval steps.  
- **Clear visibility** into what was posted, where, and when via Google Sheets logs.

---

## 🖼 Screenshots

**RSS to Telegram bot for approval**  
![RSS to telegram bot for approval](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automatic%20Post%20Creation%20System/RSS%20to%20telgram%20bot%20for%20approval.png)

**Check by Prepl and write post – save to Google Sheets**  
![Check by Prepl and write post - save to GS](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automatic%20Post%20Creation%20System/Checks%20by%20Prepl%20and%20generate%20posts%20-%20save%20to%20GS.png)

**Make a post**  
![Make a post](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Automatic%20Post%20Creation%20System/make%20a%20Posts.png)
