# 🤖 AI Job Helper

> An AI-powered workflow built with **n8n** that automates the job application process by analyzing resumes, matching them with job descriptions, generating personalized cover letters, storing results in Google Sheets, and sending a complete report via Gmail.

![n8n](https://img.shields.io/badge/n8n-Workflow%20Automation-EA4B71?style=for-the-badge&logo=n8n)
![Gemini](https://img.shields.io/badge/Google-Gemini%20AI-4285F4?style=for-the-badge&logo=google)
![Google Sheets](https://img.shields.io/badge/Google%20Sheets-Database-34A853?style=for-the-badge&logo=googlesheets)
![Gmail](https://img.shields.io/badge/Gmail-Email-EA4335?style=for-the-badge&logo=gmail)

---

# 📖 Project Overview

Applying for jobs often involves repeating the same steps:

- Reading the job description
- Comparing it with your resume
- Finding missing skills
- Improving your resume
- Writing a custom cover letter
- Keeping track of every application

This workflow automates the complete process using AI.

The user simply submits:

- Resume (PDF)
- Job URL
- Personal Information

The workflow automatically analyzes everything and emails a detailed job match report.

---

# 🚀 Features

- 📄 Resume PDF Extraction
- 🌐 Job Description Extraction from URL
- 🤖 AI Resume Analysis
- 📊 Resume Match Score
- 🧠 Skill Gap Identification
- 💡 Resume Improvement Suggestions
- ✍️ AI Generated Cover Letter
- 📧 Automated Email Report
- 📑 Stores Results in Google Sheets
- ⚡ Fully Automated with n8n

---

# 🏗 Workflow Architecture

```
User Form
     │
     ▼
Resume PDF Extraction
     │
     ▼
Job Description Scraper
     │
     ▼
AI Job Description Parser
     │
     ▼
Merge Resume + Job Data
     │
     ▼
Resume Analyzer (Gemini AI)
     │
     ▼
Cover Letter Generator
     │
     ├─────────────► Google Sheets
     │
     ▼
Send Email Report
```

---

# ⚙ Workflow Components

## 1️⃣ Form Submission

Collects:

- Candidate Name
- Email Address
- Resume PDF
- Job URL

---

## 2️⃣ Resume Extraction

Uses the **Extract from PDF** node to convert the uploaded resume into plain text.

Output:

- Resume Content

---

## 3️⃣ Job Description Fetch

Uses an HTTP Request node to download the HTML content from the provided job posting.

---

## 4️⃣ HTML Cleaning

JavaScript node removes unnecessary HTML tags and extracts readable content.

---

## 5️⃣ Job Description Analyzer

Google Gemini AI extracts structured information:

- Job Title
- Company Name
- Required Skills
- Responsibilities
- Experience
- Location

---

## 6️⃣ Merge Node

Combines:

- Resume Text
- Job Description

into a single AI input.

---

## 7️⃣ Resume Analysis

Gemini AI analyzes:

- Match Score
- Missing Skills
- Resume Improvements

Example Output

```
Match Score : 82%

Skill Gaps

• Docker
• Kubernetes
• AWS

Resume Improvements

• Add project metrics
• Improve professional summary
• Highlight backend skills
```

---

## 8️⃣ Cover Letter Generator

Creates a personalized cover letter using:

- Candidate Information
- Resume
- Job Description

---

## 9️⃣ Google Sheets Database

Stores every job application automatically.

Columns:

| Name | Company | Job Title | Match Score | Skill Gaps | Resume Improvements | Cover Letter |
|------|----------|-----------|-------------|-------------|---------------------|--------------|

---

## 🔟 Gmail

Sends a professional HTML report containing:

- Job Details
- Match Score
- Missing Skills
- Resume Suggestions
- Generated Cover Letter

---

# 🛠 Technologies Used

| Tool | Purpose |
|------|----------|
| n8n | Workflow Automation |
| Google Gemini AI | Resume Analysis & Cover Letter |
| Google Sheets | Database |
| Gmail | Email Reports |
| JavaScript | HTML Cleaning |
| HTTP Request | Fetch Job Description |

---

# 📷 Project Screenshots

## Workflow

> Replace the image below with your workflow screenshot.

![Workflow](https://github.com/Jeswin-Madona/n8n-Workflows/blob/f800e810e4365ebc82c3cbb89259af8ca9b2951d/AI%20Job%20Helper/Node%20setup%201.png)

---

## Google Sheet Before Execution

Empty database before running the workflow.

![Google Sheet Before](https://github.com/Jeswin-Madona/n8n-Workflows/blob/f800e810e4365ebc82c3cbb89259af8ca9b2951d/AI%20Job%20Helper/Blank%20Sheet%202.png)

---

## Workflow Execution

Workflow running successfully inside n8n.

![Execution](https://github.com/Jeswin-Madona/n8n-Workflows/blob/f800e810e4365ebc82c3cbb89259af8ca9b2951d/AI%20Job%20Helper/Successful%20Execution%203.png)

---

## Google Sheet After Execution

Application data stored automatically.

![Google Sheet After](https://github.com/Jeswin-Madona/n8n-Workflows/blob/f800e810e4365ebc82c3cbb89259af8ca9b2951d/AI%20Job%20Helper/Sheet%20Output%204.png)

---

## Email Output

Generated Job Match Report received in Gmail.

![Mail Output](https://github.com/Jeswin-Madona/n8n-Workflows/blob/f800e810e4365ebc82c3cbb89259af8ca9b2951d/AI%20Job%20Helper/Mail%20Output%205.png)

---

# 📊 Sample Workflow Output

```
Company:
JumpCloud

Job Title:
Full Stack Software Engineer

Match Score:
78%

Skill Gaps

• Docker
• Kubernetes
• AWS

Resume Improvements

• Improve Professional Summary

• Add measurable project impact

• Highlight Backend Experience

Cover Letter

Generated automatically using Gemini AI.
```

---

# 🎯 Future Improvements

- ATS Resume Score
- Multi-AI Model Comparison
- Automatic Job Application Tracking
- Notion Database Integration
- LinkedIn Easy Apply Automation
- Company Research Agent
- Interview Question Generator

---

# 📂 Repository Structure

```
AI Job Helper/

│
├── README.md
├── workflow.json
├── images
│   ├── workflow.png
│   ├── execution.png
│   ├── google-sheet-before.png
│   ├── google-sheet-after.png
│   └── email-output.png
│
└── assets
```

---

# 👨‍💻 Author

**Jeswin Madona**

Computer Science Engineering Student

Learning AI Automation • Java Backend • n8n

GitHub:
https://github.com/Jeswin-Madona

LinkedIn:
https://linkedin.com/in/jeswinmadona

---

## ⭐ If you found this project useful, consider giving it a Star!
