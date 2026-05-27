# Automated Accounts Receivable & Dunning System

This project is an end-to-end automation I built to handle the full invoice-to-cash process; from receiving new invoices to tracking overdue payments and sending smart reminders.

### The Problem
In many finance teams, chasing overdue invoices is still very manual. You end up with scattered reminders, no clear visibility into aging risk, and a lot of time wasted following up on the wrong accounts.

### What I Built
I created two connected workflows that work together:

**Workflow 1 – Invoice Ingestion**  
- Triggers when a new PDF lands in Google Drive  
- Extracts key details using AI  
- Validates the data  
- Logs clean invoices into the master sheet  
- Sends a quick internal notification when a new invoice is added

**Workflow 2 – Daily Collections Engine**  
- Runs every morning  
- Calculates days overdue, aging buckets, and risk levels (Low/Medium/High)  
- AI drafts appropriate reminder emails based on how overdue the invoice is  
- Sends the emails and automatically updates the tracking fields (Last Contacted and Follow-up Stage)

### Tech Stack
- n8n (main automation + AI email drafting)
- Google Sheets (main data layer)
- Power BI (dashboards for visibility)

### Key Features
- Progressive reminders (starts gentle, gets firmer as needed)
- Risk-based escalation
- Full history tracking on every invoice
- Bad data isolation with alerts

The system is now live and running on my test data. It has significantly reduced the manual work while giving clear visibility into what needs attention.

Feel free to check the workflows and dashboards in the repo. Any feedback is welcome!

---
