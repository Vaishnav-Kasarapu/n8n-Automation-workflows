# Auto AI Internship Applier using n8n 🤖

## 📌 Project Overview

The **Auto AI Internship Applier** is an AI-powered workflow automation project built using n8n that automates the internship application process.

The workflow monitors a Google Sheet for newly added internship opportunities. Whenever a new internship entry is detected, Google Gemini AI generates a personalized, professional application email based on the applicant's profile, skills, experience, and job details.

The generated email is automatically sent to the hiring manager using the applicant's personal Gmail account.

This workflow reduces manual effort, saves time, and makes the internship application process faster and more efficient.

## 🎯 Objectives

- Automate the internship application process.
- Track internship opportunities using Google Sheets.
- Automatically detect newly added job opportunities.
- Generate personalized application emails using Google Gemini AI.
- Structure AI-generated responses into JSON format.
- Automatically send application emails through Gmail.
- Reduce repetitive manual work and improve application efficiency.

## ⚙️ Workflow Architecture

The workflow consists of the following stages:

1. **Google Sheets Trigger:** Monitors the "My Job Applications" Google Sheet and triggers the workflow whenever a new row is added.
2. **Google Gemini Chat Model:** Provides the generative AI capabilities required to create personalized application emails.
3. **Basic LLM Chain:** Passes applicant details and internship information to Gemini using a predefined prompt.
4. **Structured Output Parser:** Converts the AI-generated response into structured JSON containing three fields:
   - `to` – Hiring manager's email address.
   - `subject` – Email subject.
   - `body` – Personalized application email content.
5. **Gmail Node:** Sends the generated application email directly to the hiring manager using the applicant's Gmail account.

## 🛠️ Technologies Used

- **n8n:** Workflow automation and orchestration.
- **Google Gemini AI:** AI-powered personalized email generation.
- **Google Sheets:** Internship tracking and applicant information management.
- **Structured Output Parser:** Formatting AI responses into structured JSON.
- **Basic LLM Chain:** Managing AI prompts and model execution.
- **Gmail API:** Automated email sending.
- **JSON:** Structured data exchange between workflow nodes.

## 📊 Google Sheets Configuration

Create a Google Sheet named **My Job Applications** with the following columns:

| Column | Description |
|---|---|
| Full Name | Applicant's full name |
| Email | Applicant's email address |
| Position Applied | Internship role |
| Details | Educational and professional background |
| Experience (Years) | Relevant experience |
| Skills | Technical skills |
| CompanyName | Company offering the internship |
| HiringManagerEmail | Recipient's email address |
| JobPostURL | Internship posting link |

Each new row represents a new internship application opportunity.

## 🤖 AI Email Generation

Google Gemini generates a personalized application email using the information available in the Google Sheet.

The generated email includes:

- Professional greeting.
- Introduction of the applicant.
- Internship position of interest.
- Relevant technical skills and experience.
- Enthusiasm to learn and contribute.
- Professional closing and thank-you message.

The Structured Output Parser ensures that the generated response follows a predefined JSON structure with `to`, `subject`, and `body` fields.

## 🔑 Prerequisites

Before executing the workflow, ensure you have:

- An active n8n instance.
- Google Gemini API key.
- Google Sheets OAuth2 credentials.
- Personal Gmail OAuth2 credentials.
- A Google Sheet named "My Job Applications" with the required columns.

## 🚀 Setup Instructions

1. Clone or download this repository.
2. Open your n8n instance.
3. Import the exported workflow JSON file.
4. Create the Google Sheet named "My Job Applications".
5. Add all the required column headers and configure your personal profile information.
6. Connect your Google Sheets OAuth2 credentials.
7. Configure the Google Gemini API key.
8. Connect your personal Gmail account using OAuth2 credentials.
9. Configure the Google Sheets Trigger to monitor the correct spreadsheet and sheet.
10. Map the Structured Output Parser fields to the Gmail node:
    - **To:** `to`
    - **Subject:** `subject`
    - **Message:** `body`
11. Test the workflow by adding a new internship opportunity to the Google Sheet.
12. Activate the workflow.

## 📧 Expected Output

Whenever a new internship opportunity is added to Google Sheets:

1. n8n detects the new row.
2. Applicant and internship details are retrieved.
3. Google Gemini generates a personalized application email.
4. The Structured Output Parser formats the response into JSON.
5. Gmail automatically sends the application email to the hiring manager.

## 💡 Key Features

- Automated internship application workflow.
- Google Sheets-based opportunity tracking.
- AI-generated personalized application emails.
- Dynamic email subject and body generation.
- Structured JSON output.
- Automated Gmail integration.
- Reduced manual effort and repetitive tasks.
- Reusable and exportable n8n workflow.

## ⚠️ Important Considerations

- Verify your personal details and technical skills in Google Sheets.
- Ensure the hiring manager's email address is correct.
- Check the AI-generated email before enabling automatic sending.
- Configure Gmail permissions correctly.
- Avoid duplicate applications by maintaining proper records.
- The workflow sends emails automatically, so test it carefully before activating it for real applications.

## 📁 Project Structure

```text
Auto-AI-Internship-Applier/
│
├── Auto-AI-Internship-Applier.json
└── README.md
```

## 🔮 Future Enhancements

- Add an application status tracking system.
- Automatically update Google Sheets after sending an email.
- Generate customized resumes based on internship requirements.
- Add duplicate application detection.
- Include follow-up email automation.
- Integrate job portals and internship search APIs.

## 👨‍💻 Author

**Vaishnav Kasarapu**

GitHub: [Vaishnav-Kasarapu](https://github.com/Vaishnav-Kasarapu)

---

*An AI-powered automation workflow that simplifies internship applications by combining Google Sheets, Gemini AI, and Gmail.*
