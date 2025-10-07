# 📧 Serverless Email Marketing Service using AWS

A **fully serverless email marketing automation system** built using **AWS EventBridge, Lambda, SES, S3, and CloudWatch**.  
This project automatically sends personalized email campaigns using AWS services, stores templates and contact lists in S3, and tracks executions through CloudWatch.

---

## 🌐 Project Overview

This project demonstrates how to build a **cost-effective, scalable, and automated email marketing service** without managing servers or infrastructure.

### 🧱 AWS Services Used
- **💌 AWS SES (Simple Email Service)** – For sending customized HTML emails.  
- **⚙️ AWS Lambda** – For processing and sending emails programmatically.  
- **🕒 AWS EventBridge** – For scheduling and triggering email campaigns automatically.  
- **🗂️ AWS S3** – For storing email templates and recipient contact lists.  
- **📊 AWS CloudWatch** – For logging, monitoring, and error tracking.
<img width="322" height="177" alt="Screenshot 2025-10-08 020003" src="https://github.com/user-attachments/assets/3ce8a3a2-3ad1-4683-8ff0-c46e2838316a" />

---

## ⚙️ How It Works

1. **Upload Email Template and Contacts**
   - Upload `email_template.html` and `contacts.csv` to your S3 bucket.  

2. **Configure SES**
   - Verify your domain and sender email address in AWS SES.  

3. **Deploy Lambda**
   - Create a Lambda function (Python or Node.js runtime).  
   - Attach the IAM policy from `Permissions and policies.pdf`.  
   - Fetch:
     - Contacts from S3.  
     - Email template from S3.  
   - Personalize and send emails using `SES.sendEmail()` or `SES.sendRawEmail()`.  

4. **Set Up EventBridge Rule**
   - Schedule Lambda executions (e.g., weekly or daily campaigns).  

5. **Monitor Logs**
   - View execution logs and metrics in **CloudWatch** for success or failure details.  

---

## ✨ Features

✅ **Serverless & Auto-Scaling**  
✅ **Fully Automated Campaigns**  
✅ **Customizable HTML Templates**  
✅ **Dynamic Recipient Personalization**  
✅ **Event-Driven Email Delivery**  
✅ **Real-Time CloudWatch Monitoring**

---

## 🧰 Technologies Used

| Service | Purpose |
|----------|----------|
| 🧠 **AWS Lambda** | Serverless compute logic |
| 💌 **AWS SES** | Email delivery service |
| 🕒 **AWS EventBridge** | Event scheduling and automation |
| 🗂️ **AWS S3** | Storage for templates and contact lists |
| 📊 **AWS CloudWatch** | Logs and monitoring |
<img width="427" height="164" alt="Screenshot 2025-10-08 015929" src="https://github.com/user-attachments/assets/510ebffa-e1c6-4449-bfc3-ec7b4dca7f8b" />
<img width="317" height="178" alt="Screenshot 2025-10-08 015947" src="https://github.com/user-attachments/assets/b32242ae-770a-4038-aafa-52c5f1b07093" />
---

## 🔒 Security

- ✅ Only verified sender domains/emails can send via SES.  
- 🔐 Contacts and templates are stored securely in S3.  
- 🔑 IAM permissions are limited strictly to **SES** and **S3** access.  

---

## 📈 Future Enhancements

🚀 **DynamoDB Integration**  
Use **Amazon DynamoDB** to replace static CSV storage, enabling real-time management of contact lists, campaign logs, and delivery statuses.

🖥️ **UI-Based API Dashboard**  
Build a **React-based web dashboard** with **API Gateway** and **Lambda APIs** to:
- Add, edit, and delete contact records stored in DynamoDB.  
- Upload new email templates directly from the UI.  
- Trigger campaigns and monitor execution in real-time.  
- View delivery analytics and campaign statistics.

📡 **Extended Monitoring & Notifications**  
Integrate **CloudWatch Metrics** and **SNS** notifications to:
- Alert admins on delivery failures.  
- Send weekly summaries of campaign performance.

---

## 📂 Folder Structure

```bash
serverless-email-marketing-service/
├── email_template.html       # HTML email content
├── contacts.csv              # Recipient list
├── Permissions and policies.pdf  # IAM policies for SES & S3
└── README.md                 # Documentation


