# 🤖 Customer Feedback Sentiment Analysis Automation

An **n8n workflow automation** that uses **Google Gemini Chat Model** to perform sentiment analysis on customer feedback and automate responses accordingly. The system classifies feedback, updates Google Sheets, and sends alerts to the Customer Success team when negative feedback is detected.

---

## 🚀 Project Overview

This project automates the process of analyzing and organizing customer feedback in real time.  
Whenever a customer submits feedback through a form, the workflow automatically:

1. Receives the submission.  
2. Sends the feedback text to the **Google Gemini Chat Model** for **sentiment analysis**.  
3. Executes **custom JavaScript** logic to interpret the model output.  
4. Routes the data accordingly:
   - **Positive/Neutral** → Appended to a Google Sheet (`Customer Feedback`).
   - **Negative** → Appended to another sheet and triggers an **alert email** to the Customer Success Team via Gmail.

---

## 🧠 Tech Stack

- **n8n** – Workflow automation platform  
- **Google Gemini Chat Model** – AI-powered sentiment analysis  
- **JavaScript** – Logic for conditional data handling  
- **Google Sheets API** – Data storage and tracking  
- **Gmail API** – Automated email alerts  

---

## 🧩 Workflow Structure

- Form Submission Trigger
- Sentiment Analysis (Google Gemini)
- JavaScript Logic
- Conditional Routing (If Node)
- Google Sheets Integration
- Gmail Integration

---

## 🛠️ Setup Instructions

Follow these steps to set up and run the **Customer Feedback Sentiment Analysis Automation** project in your n8n environment:

### 1. Clone the Repository
Clone this repository to your local machine:
```bash
git clone https://github.com/yourusername/customer-feedback-sentiment-automation.git
cd customer-feedback-sentiment-automation

### 2. Import the Workflow into n8n
1. Open your n8n dashboard.
2. Click **Import Workflow → Upload File**.
3. Select the file:  
   `workflow/n8n_workflow.json`
4. Once imported, you’ll see the full workflow with nodes for:
   - Form Submission Trigger
   - Sentiment Analysis (Google Gemini)
   - JavaScript Logic
   - Conditional Routing (If Node)
   - Google Sheets & Gmail Integrations

### 3. Configure Required Credentials
Set up the following integrations in n8n:
- **Google Gemini Chat Model** – Add your Gemini API credentials or connect via the Google AI connector.
- **Google Sheets** – Authorize your Google account and select the sheets for storing feedback.
- **Gmail** – Connect your account for sending automated alert emails.

> You can manage these under **Credentials → Create New** in n8n.

### 4. Adjust Workflow Logic (Optional)
- Open the **Code in JavaScript** node to modify how sentiment results are parsed (e.g., thresholds for positive/negative).
- Update sheet names or alert recipients in the Google Sheets and Gmail nodes as needed.

### 5. Activate the Workflow
1. Turn on the toggle at the top right corner to **Activate** the workflow.
2. Submit a test form to confirm everything works.
3. Check your Google Sheet and Inbox for test entries.

### 6. Monitor Executions
- Use the **Executions** tab in n8n to view logs, track errors, and verify successful automation runs.

