# AI-Powered Sales Data Analysis and Email Automation

An AI-powered data analysis project built with n8n, OpenRouter, Google Sheets, and Gmail. It allows users to ask questions about business sales data in natural language, retrieve relevant data, and receive analysis reports through email.

## Project Overview

This project demonstrates how AI and workflow automation can simplify business data analysis and reporting.

Instead of manually filtering spreadsheets and writing reports, users can interact with an AI agent through a chat interface to request sales insights and email reports.

## Workflow Architecture

![n8n Workflow](screenshots/workflow.png)

### Workflow Components

1. **When Chat Message Received** — Accepts questions from the user.
2. **OpenRouter Chat Model** — Powers the AI agent's language understanding and responses.
3. **Simple Memory** — Provides conversational context across supported interactions.
4. **Google Sheets** — Retrieves sales data from the connected spreadsheet.
5. **Gmail** — Sends requested analysis reports through email.
6. **AI Agent** — Coordinates the available tools to answer questions and perform the requested actions.

## Features

- Natural-language questions about sales data.
- Sales analysis by region, city, product, and category, depending on available columns.
- Revenue and percentage calculations when supported by the dataset.
- Product performance and sales comparisons.
- Conversational context through memory.
- Automated email reporting through Gmail.
- Extensible workflow for additional analytics and reporting features.

## Technology Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| OpenRouter | Access to AI language models |
| Google Sheets | Sales data source |
| Gmail | Email report delivery |
| AI Agent | Coordinates analysis and tool usage |

## Example Questions

- What percentage of sales came from the East region?
- Which products generated the highest revenue?
- Compare sales across all regions.
- Summarize the key sales insights.
- Prepare a sales report and email it to my specified address.

Actual results depend on the connected dataset, configured tools, and the AI model being used.

## Prerequisites

- An n8n installation or account.
- An OpenRouter API key and a compatible model.
- A Google account with access to the sales spreadsheet.
- Gmail credentials configured for sending messages.
- An exported n8n workflow JSON file.

## Setup Instructions

### 1. Download the Project

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/ai-sales-analysis-email-automation.git
cd ai-sales-analysis-email-automation
```

Alternatively, download the repository as a ZIP file from GitHub.

### 2. Import the Workflow

1. Open your n8n instance.
2. Create or open a workflow.
3. Open the workflow menu and select the import option.
4. Import `workflow.json`.

The exact menu wording may vary between n8n versions.

### 3. Configure the AI Model

1. Open the OpenRouter Chat Model node.
2. Configure your OpenRouter API credentials in n8n.
3. Select a compatible model.
4. Test the connection.

### 4. Configure Google Sheets

1. Open the Google Sheets tool node.
2. Connect your Google account using n8n credentials.
3. Select your sales spreadsheet and worksheet.
4. Verify that the agent can read the required columns.

### 5. Configure Gmail

1. Open the Gmail node.
2. Configure your Gmail credentials.
3. Grant the required permissions.
4. Confirm the recipient and email body settings.

Use the HTML body field if your workflow generates formatted HTML email reports.

### 6. Test the Workflow

Run the workflow and try:

- Ask for total sales by region.
- Request a percentage calculation.
- Ask for the top-performing products.
- Request an email report and verify delivery.

Do not send test reports to clients until the calculations, recipient, and email formatting have been verified.

## Security

- Never commit API keys, passwords, access tokens, OAuth secrets, or private email information.
- Configure credentials securely inside n8n.
- Review exported workflow JSON before publishing it.
- Replace private spreadsheet IDs and personal information with placeholders when necessary.
- Use sample or anonymized data for public demonstrations.

## Current Scope and Limitations

This project currently uses Google Sheets as its data source and Gmail for sending reports.

Power BI dashboard generation, automatic chart creation, and publishing are not included unless separately implemented and configured in the workflow.

Analysis accuracy depends on data quality, available columns, model capabilities, and the calculations performed by the workflow.

## Future Improvements

- Add automated data cleaning and validation.
- Generate charts and visual summaries.
- Add scheduled sales reports.
- Support Excel and CSV uploads.
- Integrate Power BI for dashboard generation.
- Add error handling and execution logging.

## Author

**Sumit Jadhav**

Aspiring Data Analyst | Business Analysis | AI Automation

This project was created as a practical demonstration of data analysis and workflow automation using AI tools.
