# n8n-Expense-Tracker  Automation Project – Summary

## Objective
To build an automated expense tracking system that logs daily expenses, categorizes them, calculates totals, and provides visual insights, all in Google Sheets, with minimal manual work.

---

## Tools Used
- **Google Sheets** – for storing expense data.  (API)
- **n8n** – to automate data entry and processing.  
- **Pivot Tables & Charts** – for category-wise summaries and visual insights.
- **Telegram Api** - Servers as Input
- **Grok AI** - gpt-oss-120 model
- **Cron-Job** - to make sure the n8n remains active
- This project is completely built on free of cost and n8n is cloud hosted i.e --> render

---

## Steps Completed

1. **Sheet Setup**
   - Created a Google Sheet with columns:  
     ```
     Date | Category | Tags/Details | Amount | Payment Method (optional)
     ```
   - Added a **Total Spends** calculation using `=SUM(D2:D)` for automatic updates.  
   - Ensured proper formatting so pivot tables and charts work correctly.

2. **Categorization & Consistency**
   - Defined key categories (e.g., Groceries, Loan, Tax, Protein, Ghee).  
   - Used consistent naming and optional dropdown lists to avoid errors.

3. **Pivot Tables**
   - Created a pivot table to summarize **category-wise spending** automatically.  
   - Pivot table updates instantly when new expenses are added.  

4. **Visual Representation**
   - Added **Pie Charts** for category-wise spending distribution.  
   - Added **Bar Charts** to see trends over time.  
   - Charts dynamically update with new data.

5. **Automation with n8n**
   - Configured n8n to **append new expense entries** automatically into Google Sheets.  
   - Set up triggers (e.g., via form submission or API call).  
   - Optionally, automated categorization based on keywords or tags.  
   - Optionally, automated summary emails or notifications.

6. **Outcome**
   - Fully automated, up-to-date expense tracker.  
   - Easy to see total spending, category-wise breakdown, and trends.  
   - Reduces manual work and human error in recording expenses.
  
---

 # n8n Workflow
 
 <img width="1319" height="587" alt="n8n" src="https://github.com/user-attachments/assets/f1545cf0-73f3-4763-98f9-4b96302a7104" />

## Future Enhancements
- Auto-budget alerts (notify when spending exceeds limits).  
- Monthly or weekly summaries sent automatically via email.  
- Integration with bank APIs for automatic transaction logging.  
- Dashboard sheet for an at-a-glance overview.
