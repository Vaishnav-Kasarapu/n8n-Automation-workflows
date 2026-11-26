# AI News Summarizer  🚀

## 📌 Project Overview

The **AI News Summarizer** is an automated n8n workflow that collects the latest Artificial Intelligence and technology news from multiple sources, gathers real-time news and live event updates using SerpAPI, and generates a structured daily newsletter using Google Gemini AI.

The workflow runs automatically every day and delivers the summarized report directly to the user's Gmail inbox, helping users stay updated with the latest developments in the AI and technology industry without manually searching multiple websites.

## 🎯 Objectives

- Automate daily collection of AI and technology news.
- Fetch the latest articles from multiple RSS feeds.
- Retrieve real-time news and live event updates using SerpAPI.
- Combine information from different sources into a single dataset.
- Use Google Gemini AI to analyze and summarize the collected information.
- Generate a structured and easy-to-read daily newsletter.
- Automatically deliver the newsletter through Gmail.

## ⚙️ Workflow Architecture

The workflow consists of the following stages:

1. **Schedule Trigger:** Automatically initiates the workflow once every day.
2. **RSS Feed Read (NormalTech):** Fetches the latest AI-related articles from `https://www.normaltech.ai/feed`.
3. **RSS Feed Read (AI Business):** Collects technology and AI news from `https://aibusiness.com/rss.xml`.
4. **SerpAPI (HTTP Request):** Fetches the latest AI news and live event information from Google Search results.
5. **Merge Node:** Combines the data collected from all three sources.
6. **Aggregate Node:** Groups the collected information into a single JSON structure.
7. **Google Gemini Chat Model:** Processes the aggregated news data using generative AI.
8. **LLM Chain:** Uses a custom summarization prompt to generate a structured daily intelligence report.
9. **Gmail Node:** Sends the generated newsletter directly to the configured email address.

## 🛠️ Technologies Used

- **n8n:** Workflow automation and orchestration.
- **Google Gemini AI:** AI-powered news analysis and summarization.
- **SerpAPI:** Fetching Google Search results, latest news, and live event updates.
- **RSS Feeds:** Collecting articles from NormalTech and AI Business.
- **HTTP Request:** Connecting to the SerpAPI service.
- **Gmail:** Automated email delivery.
- **JSON:** Data exchange and workflow export format.

## 📰 Newsletter Structure

The Google Gemini model generates a daily report with the following sections:

### 1. AI NEWS HIGHLIGHTS
- Five of the most important AI developments.
- Key announcements, innovations, and industry updates.

### 2. TECHNOLOGY UPDATES
- Latest developments in the technology industry.
- Important updates gathered from RSS feeds and Google Search.

### 3. LIVE EVENTS
- Relevant upcoming or ongoing AI events.
- Conferences, product launches, and industry announcements identified through search results.

## 🔑 Prerequisites

Before executing the workflow, ensure you have:

- An active n8n instance.
- Google Gemini API key.
- SerpAPI API key.
- Gmail account configured with appropriate credentials in n8n.

## 🚀 Setup Instructions

1. Clone or download this repository.
2. Open your n8n instance.
3. Import the exported workflow JSON file.
4. Configure the Google Gemini credentials.
5. Add your SerpAPI key to the HTTP Request node.
6. Configure Gmail OAuth2 credentials.
7. Replace the placeholder recipient email with your Gmail address.
8. Set the Schedule Trigger to your preferred daily execution time.
9. Save and activate the workflow.

## 📊 Expected Output

Once activated, the workflow automatically:

- Collects the latest AI news from two RSS feeds.
- Retrieves additional news and live event updates through SerpAPI.
- Merges and aggregates the collected information.
- Generates an AI-powered daily newsletter using Google Gemini.
- Sends the final report to the configured Gmail inbox.

## 💡 Key Features

- Fully automated daily execution.
- Multiple-source news aggregation.
- Real-time Google Search integration.
- AI-powered content analysis and summarization.
- Structured daily intelligence reports.
- Automated email notifications.
- Exportable and reusable n8n workflow.

## 📁 Project Structure

```text
AI-News-Summarizer-Part-2/
│
├── AI-News-Summarizer-Part-2.json
└── README.md
```

## 🔮 Future Enhancements

- Add more AI and technology news sources.
- Introduce category-wise news classification.
- Generate weekly and monthly AI news reports.
- Include source links for every summarized development.
- Add duplicate-news detection.
- Improve event filtering based on date and relevance.

## 👨‍💻 Author

**Vaishnav Kasarapu**

GitHub: [Vaishnav-Kasarapu](https://github.com/Vaishnav-Kasarapu)

---

*An AI-powered automation workflow that keeps you informed about the latest developments in Artificial Intelligence and Technology, every day.*
