# Automated LinkedIn Job Tracker with AI 🚀

## 📌 Project Overview

The **Automated LinkedIn Job Tracker** is an AI-powered workflow automation project built using n8n that simplifies job searching and application preparation.

The workflow automatically fetches job postings from a LinkedIn RSS feed, analyzes job descriptions using Google Gemini AI, extracts relevant technical skills and requirements, and generates personalized cover letters for each opportunity.

All the processed job information, including job titles, posting links, publication dates, extracted skills, and generated cover letters, is automatically stored in Google Sheets for easy tracking and management.

## 🎯 Objectives

- Automate the collection of LinkedIn job postings.
- Fetch new opportunities through RSS feeds.
- Analyze job descriptions using Google Gemini AI.
- Extract relevant technical skills and job requirements.
- Generate personalized cover letters for each job opportunity.
- Store structured job information in Google Sheets.
- Simplify job tracking and application preparation.

## ⚙️ Workflow Architecture

The workflow consists of the following stages:

1. **Schedule Trigger:** Automatically executes the workflow every day at 10 AM.
2. **RSS Feed Reader:** Fetches job postings from the configured LinkedIn RSS feed.
3. **Google Gemini Chat Model:** Provides AI capabilities for job description analysis and cover letter generation.
4. **Basic LLM Chain:** Processes job information using a predefined prompt to extract technical skills and generate personalized cover letters.
5. **Structured Output Parser:** Converts the AI-generated response into structured JSON containing job details, extracted skills, and cover letter content.
6. **Google Sheets Node:** Stores all the processed job information in the configured Google Sheet.

## 🛠️ Technologies Used

- **n8n:** Workflow automation and orchestration.
- **Google Gemini AI:** AI-powered job analysis and cover letter generation.
- **LinkedIn RSS Feed:** Fetching job postings and updates.
- **FetchRSS:** RSS feed generation for LinkedIn job listings.
- **Basic LLM Chain:** Managing AI prompts and processing.
- **Structured Output Parser:** Formatting AI responses into structured JSON.
- **Google Sheets:** Storing and tracking job opportunities.
- **JSON:** Structured data exchange between workflow nodes.

## 📊 Google Sheets Configuration

Create a Google Sheet with the following columns:

| Column | Description |
|---|---|
| Title | Job position title |
| Link | Job posting URL |
| Published Date | Date the job was published |
| About Company | Company information and job description |
| job description | Detailed job responsibilities and requirements |
| skills | Extracted technical skills |
| Cover letter | AI-generated personalized cover letter |

Each row represents a processed job opportunity.

## 🤖 AI-Powered Job Analysis

Google Gemini AI performs two major tasks:

### 1. Technical Skills Extraction

The AI analyzes each job description and identifies relevant technical skills, including:

- Programming languages.
- Frameworks and libraries.
- Development tools and technologies.
- Databases.
- Other technical requirements.

It identifies both explicitly mentioned and relevant implicitly required skills.

### 2. Personalized Cover Letter Generation

The AI generates a professional 250–300 word cover letter tailored to each job opportunity.

The cover letter follows three sections:

- **Opening:** Expresses interest in the specific job role and company.
- **Middle:** Highlights relevant technical skills, experience, and qualifications.
- **Closing:** Demonstrates enthusiasm for the opportunity and expresses interest in further communication.

## 🔑 Prerequisites

Before executing the workflow, ensure you have:

- An active n8n instance.
- Google Gemini API key.
- Google Sheets OAuth2 credentials.
- A valid LinkedIn RSS feed URL generated using FetchRSS.
- A Google Sheet configured with the required columns.

**RSS Feed URL:**

https://fetchrss.com/feed/aMgiakD8zFniaMgiUfNukboi.rss

## 🚀 Setup Instructions

1. Clone or download this repository.
2. Open your n8n instance.
3. Import the exported workflow JSON file.
4. Configure the Schedule Trigger to execute daily at 10 AM.
5. Add the LinkedIn RSS feed URL to the RSS Feed Reader node.
6. Configure the Google Gemini API credentials.
7. Connect Google Sheets using OAuth2 credentials.
8. Create a Google Sheet with the required column headers.
9. Configure the Structured Output Parser to return the required JSON fields.
10. Map the generated output fields to their corresponding Google Sheets columns.
11. Test the workflow to verify that job postings are fetched, analyzed, and stored correctly.
12. Activate the workflow.

## 📈 Expected Output

Whenever the scheduled workflow executes:

1. Latest job postings are fetched from the LinkedIn RSS feed.
2. Job titles, links, publication dates, and descriptions are extracted.
3. Google Gemini analyzes the job descriptions.
4. Relevant technical skills are identified.
5. Personalized cover letters are generated for individual job opportunities.
6. Structured results are stored in Google Sheets.

## 💡 Key Features

- Automated daily job collection.
- LinkedIn job posting integration through RSS.
- AI-powered job description analysis.
- Automatic technical skill extraction.
- Personalized cover letter generation.
- Structured JSON output.
- Centralized Google Sheets job tracking.
- Reduced manual effort in job searching and application preparation.

## ⚠️ Important Considerations

- Ensure the LinkedIn RSS feed is active and accessible.
- Verify that the Google Gemini API key is configured correctly.
- Maintain proper Google Sheets column mapping.
- Review generated cover letters before using them in actual applications.
- Avoid duplicate job entries when the workflow runs repeatedly.
- Ensure the schedule timezone is configured correctly.

## 📁 Project Structure

```text
Automated-LinkedIn-Job-Tracker/
│
├── Automated-LinkedIn-Job-Tracker.json
└── README.md
```

## 🔮 Future Enhancements

- Add duplicate job detection using job URLs.
- Filter opportunities based on required technical skills.
- Introduce job matching scores based on applicant profiles.
- Automatically track application status.
- Add email or Telegram notifications for relevant opportunities.
- Integrate resume customization based on job descriptions.
- Generate weekly job market insights and reports.

## 👨‍💻 Author

**Vaishnav Kasarapu**

GitHub: [Vaishnav-Kasarapu](https://github.com/Vaishnav-Kasarapu)

---

*An AI-powered job tracking and application preparation system that combines n8n, Google Gemini, LinkedIn RSS feeds, and Google Sheets to make job searching smarter and more efficient.*
