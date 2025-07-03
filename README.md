# Expense-Tracker-AI-Agent 

📊 Expense Tracker AI Agent (n8n + AI)

An AI-powered expense tracker agent built with n8n that automates daily logging, weekly and monthly summaries, and sends personalized saving advice — all without manual effort.

🚀 Overview

This project automates personal expense tracking and reporting by combining no-code automation (n8n) and AI summarization.  

✅ Daily: Logs your expenses into Google Sheets by parsing bank transaction messages or via manual entry.  
✅ Weekly: Every Sunday at 9 pm, sends a summary email of total expenditure and top 2 biggest expenses.  
✅ Monthly: On the last day of the month, sends a detailed monthly summary with personalized saving tips.

🧩 Workflows

✅ Daily Workflow
- Trigger:  
  - Manually append transaction  
  - Or parse SMS received from banks (ignoring OTP/verification codes)
- Action: Extract transaction details (amount, date, merchant/category)
- Log: Append to Google Sheets

📅 Weekly Summary Workflow
- Trigger: Every Sunday at 9 pm (cron)
- Action: Fetch last week's transactions from Google Sheets
- AI: Use Mixtral model to:
  - Summarize total weekly spend
  - Identify top 2 biggest expenses
- Email: Send summary email to user

📆 Monthly Summary & Advice Workflow
- Trigger: Last day of the month
- Action: Fetch month's transactions
- AI: Use Mixtral model to:
  - Summarize total monthly spend
  - Suggest personalized saving advice
- Email: Send detailed monthly report


🧠 AI Integration
- Mixtral model used to:
  - Summarize transaction data into human-readable insights
  - Identify spending patterns
  - Generate contextual saving tips

🛠 Tech Stack
- n8n: Workflow automation
- Google Sheets API: Store transactions
- Email (Gmail): Send reports
- Mixtral model: Summaries and advice

Privacy : No parsing of OTP or verification codes.
