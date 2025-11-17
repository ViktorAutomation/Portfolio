# FB & LinkedIn Auto-posting System Using Custom GPT Action

An AI-powered content pipeline that turns news articles into ready-to-publish posts for **Facebook** and **LinkedIn** – all controlled from a single **Custom GPT** conversation and automated with **Make.com**.

---

## 🔍 Project Overview

This project combines **Custom GPT Actions** with **Make.com** to automate the full social posting pipeline:

- discovering relevant news,
- curating and editing content,
- generating or reusing images,
- publishing to Facebook & LinkedIn,
- and logging results into Airtable.

Everything happens inside **one GPT conversation**, while Make.com scenarios handle the heavy lifting in the background.

---

## 🎯 Problem & Goals

The client wanted to:

- Stop manually searching for articles, copy-pasting links, and rewriting content
- Avoid jumping between multiple tools just to publish a single post
- Ensure a consistent posting flow across **Facebook** and **LinkedIn**
- Track which posts were published, when, and where

**Goal:** build a **single-conversation workflow** that can search, curate, create, publish, and track social posts with minimal manual effort.

---

## 🧩 Solution & Workflow

1. **Custom GPT Actions as the control center**  
   - GPT becomes the “front-end” where the user chats naturally.  
   - Actions call Make.com scenarios with the user’s choices (topics, platforms, edits).

2. **News discovery & content curation**  
   - Make.com scenarios parse predefined news sources / websites.  
   - Curated article options (title, link, summary) are sent back into the GPT conversation.  

3. **Content selection & editing inside GPT**  
   - The user selects an article and can refine the post copy directly in the conversation.  
   - GPT generates platform-ready text tailored to LinkedIn and/or Facebook.

4. **Image handling (original or AI-generated)**  
   - If available, the original article image can be reused.  
   - Alternatively, GPT triggers **OpenAI DALL·E 3** via Make.com to generate a new, engaging image.  

5. **Automated posting to social platforms**  
   - Final content (text + image) is pushed through Make.com to:
     - Facebook pages via API
     - LinkedIn pages/profiles via API  

6. **Tracking & logging in Airtable**  
   - Each successful post is recorded in Airtable (article URL, platforms, timestamps, copy used, etc.).  
   - This creates a simple analytics-ready dataset for future review.

---

## 🛠 Tools & Technologies Used

- **GPT (Custom GPT Actions)** – conversation layer & content generation  
- **Make.com (Integromat)** – orchestration of all steps and API calls  
- **APIs & Integrations:**  
  - Facebook API (page posting)  
  - LinkedIn API (post publishing)  
- **Airtable** – logging, tracking, and lightweight analytics  
- **OpenAI (DALL·E 3)** – image generation for visually rich posts  

---

## 📈 Results & Impact

- **End-to-end workflow** – content sourcing, creation, posting, and tracking managed from a single GPT chat.  
- **Time saved** – manual workflow reduced to a few clicks and short prompts instead of multiple tools and copy-paste steps.  
- **Better consistency** – regular posting schedule, consistent structure, and branding across both platforms.  
- **Improved content quality** – AI-assisted text and images increase post quality and engagement potential.  
- **Clean analytics** – Airtable log of all posts allows quick review of what was posted, where, and when.

---

## 🖼 Screenshots

**Make.com scenario**  
![Make.com scenario](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Action%20GPT%20auto%20posting%20system/1%20-%20Make%20scenario.png)

**Custom GPT main screen**  
![Custom GPT main screen](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Action%20GPT%20auto%20posting%20system/2%20-%20Custom%20GPT%20main%20screen.png)

**Fetch articles**  
![Fetch articles](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Action%20GPT%20auto%20posting%20system/3%20-%20Fetch%20articles.png)

**Post prep**  
![Post prep](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Action%20GPT%20auto%20posting%20system/4%20-%20Post%20prep.png)

**Post creation**  
![Post creation](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Action%20GPT%20auto%20posting%20system/5%20-%20Post%20creation.png)

**Image and make a post**  
![Image and make a post](https://raw.githubusercontent.com/ViktorAutomation/Portfolio-Automation/main/Action%20GPT%20auto%20posting%20system/6%20-%20Image%20and%20make%20a%20post.png)
