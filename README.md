# 📧 Simple AI Email Generator – n8n Workflow

This repository contains an n8n workflow that creates a **friendly AI assistant** capable of generating and sending emails based on user queries. It uses OpenAI to draft the email content, a Google Sheet (as a contact database) to look up recipient email addresses, and a Gmail node to send the final message.  

## 🚀 Features

✅ Automatically generates professional, polite emails from chat messages  
✅ Uses a contact database to resolve recipient names to email addresses  
✅ Sends emails via Gmail integration  
✅ Designed with memory support for maintaining context in longer conversations  
✅ Easy to import and customize in your own n8n instance  

## 🛠️ Workflow Components

- **Trigger Node**: Starts when a new chat message is received  
- **OpenAI Chat Model**: Drafts email content in response to the user query  
- **Simple Memory Node**: Maintains conversation context  
- **contactDatabase Tool**: Looks up recipient emails in a Google Sheet  
- **sendEmail Node**: Sends the final email to the recipient  

## 📂 Files

- `Simple_email_generator.json` — The exported n8n workflow file you can import into your own instance.

## 🔧 Setup & Usage

1. **Import the workflow**  
   - Open your n8n instance.
   - Go to the canvas, click the three dots (•••) menu, and choose **Import workflow**.
   - Upload `Simple_email_generator.json`.

2. **Configure credentials**
   - Set up your OpenAI credentials using n8n’s Credentials Manager.
   - Set up your Gmail credentials in n8n for sending emails.
   - Make sure your contact database (Google Sheet) is accessible if you want the contact lookup to work.

3. **Run the workflow**
   - Trigger it by sending a chat message or manually execute the workflow in n8n.
   - Check your email inbox to see the generated email!

## 🔒 Security & Best Practices

- **Credentials**: This workflow uses references to credential IDs only; your actual API keys and secrets are stored securely in your n8n instance and are not included in the JSON export.
- **Instance ID**: The JSON file contains an `instanceId` reference, which is harmless but can be replaced with a placeholder if you prefer.
- **Webhook ID**: If you use public webhooks, consider regenerating or replacing the webhook ID to prevent potential misuse.

## ✅ Example Usage

- **User input**: “Send an email to John asking about the meeting schedule for next week.”
- **Workflow behavior**:
  - Look up John's email in the contact database.
  - Generate a polite, professional email with OpenAI.
  - Send the email via Gmail.
  - Confirm to the user that the email was sent successfully.

## 🔎 Workflow Overview

Here’s what the n8n workflow looks like in the editor:

![Workflow Screenshot](images/workflow.png)

## ✅ Example Sent Email

Here’s an example email sent successfully by the workflow:

![Email Confirmation](images/email_sent.png)

---

**Happy automating with n8n!**
