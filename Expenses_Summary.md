# n8n Expense Tracker Extension – Financial Insights

## Objective
Extend the existing automated expense tracker to provide actionable financial insights. The workflow analyzes logged expenses, identifies spending patterns, highlights weak points, and suggests ways to optimize spending and grow wealth.

## Tools Used
- **n8n** – Automate data retrieval, processing, and AI integration.
- **Google Sheets API** – Fetch expense data and maintain logs.
- **Grok AI (`gpt-oss-120`)** – Analyze expense data and provide financial recommendations.
- **Telegram API** – Deliver insights directly as messages.
- **Cron-Job** – Keep the workflow active for regular processing.

## Workflow Overview
1. **Trigger**
   - Scheduled or event-based trigger in n8n.
   - Ensures the workflow runs at set intervals or on demand.

2. **Fetch Expenses**
   - Pulls all logged expenses from the Google Sheet.
   - Extracts only relevant fields: `Date`, `Amount`, `Category`, `Details`.

3. **Process Data**
   - Converts all rows into a structured text format:
     ```
     August 1, 2025 | ₹215 | food | Food expense
     August 2, 2025 | ₹140 | food | Food expense
     ...
     ```
   - Combines all rows into a single `chatInput` string for AI analysis.

4. **AI Analysis**
   - Sends combined expense data to Grok AI.
   - Generates actionable financial insights:
     - 💰 Summary of total and category-wise spending
     - ⚠️ Weak points or areas of overspending
     - 💡 Practical advice to optimize expenses and grow wealth
   - Output is formatted for **Telegram**: concise, readable, and emoji-enhanced.

5. **Telegram Notification**
   - Sends insights directly to the user via Telegram.
   - Ensures immediate access to actionable advice.

## Key Features
- Automated analysis without manual intervention.
- Focus on reducing unnecessary spending and growing wealth.
- Plain text output optimized for messaging platforms.
- Fully cloud-hosted and free to run (Render + n8n free tier).

## Future Enhancements
- Add trend charts for spending categories over time.
- Monthly/weekly summaries automatically sent via Telegram.
- Integration with bank APIs for real-time transaction logging.
- Budget alerts and notifications for high spending categories.

## Outcome
- Provides an **extension** to the expense tracker with actionable financial insights.
- Helps users **understand spending habits** and make better financial decisions.
- Reduces the need for manual review of Google Sheets.

---

**n8n Workflow Resources**
- Fetch expenses → Process & format → AI analysis → Telegram notification
- Hosted on Render for continuous automation
- <img width="1581" height="630" alt="s12" src="https://github.com/user-attachments/assets/fa57a43b-06e9-4986-a7fe-c2a19c5dc28e" />

