# Lead Acquisition & CRM Automation

A real-world lead automation pipeline designed to automatically process leads generated through Google Ads campaigns.

The system connects a landing page form with **n8n, SMS notifications, and HubSpot CRM**, allowing new leads to be processed immediately without depending on manual intervention.

> **Portfolio Version:** This repository contains a sanitized demonstration version of a workflow developed for a real business. Credentials, phone numbers, webhook URLs, customer information, and other sensitive data have been removed or replaced with placeholders.

---

## 🎯 Business Problem

The business generates leads through Google Ads campaigns that direct potential customers to dedicated landing pages.

When a visitor submits the form, the business needs to:

* Receive the lead information immediately.
* Confirm the request with the potential customer.
* Store the lead automatically in the CRM.
* Reduce the risk of leads being lost due to delayed manual processing.

The original process required more manual intervention after a form submission.

This automation creates an immediate connection between **lead generation, communication, and CRM management**.

---

## ⚙️ Solution

The automation processes every new form submission in real time.

```text
Google Ads
    ↓
Landing Page
    ↓
Lead Form
(Name + Phone)
    ↓
n8n Webhook
    ↓
Data Processing
    ↓
    ├──→ SMS Confirmation → Lead
    │
    ├──→ SMS Notification → Business
    │
    └──→ Create / Update Contact → HubSpot CRM
```

---

## 🔄 Workflow

### 1. Google Ads

A potential customer clicks an advertisement from a Google Ads campaign.

### 2. Landing Page

The visitor is directed to a dedicated landing page designed for lead generation.

### 3. Lead Form

The visitor submits:

* Name
* Phone number

### 4. Webhook

The form submission triggers an n8n webhook and sends the lead information to the automation workflow.

### 5. Lead Processing

n8n receives and processes the form data before executing the required actions.

### 6. Customer SMS

The potential customer automatically receives an SMS confirming that the request was received.

### 7. Business Notification

The business receives an SMS notification informing the team that a new lead has been generated.

### 8. HubSpot CRM

The lead is automatically created or updated inside HubSpot CRM for centralized lead management and future follow-up.

---

## 🛠️ Tech Stack

* **n8n** — Workflow automation and orchestration
* **HubSpot CRM** — Lead and contact management
* **SMS API** — Automated customer and business notifications
* **Google Ads** — Lead acquisition
* **Webhooks** — Real-time communication between the landing page and automation
* **REST APIs** — Integration between services
* **JSON** — Data exchange between systems

---

## 🏗️ Architecture

```text
                    GOOGLE ADS
                         │
                         ▼
                   LANDING PAGE
                         │
                         ▼
                    LEAD FORM
                  Name + Phone
                         │
                         ▼
                      WEBHOOK
                         │
                         ▼
                       n8n
                         │
            ┌────────────┼────────────┐
            │            │            │
            ▼            ▼            ▼
        SMS LEAD    SMS BUSINESS   HUBSPOT CRM
            │            │            │
            ▼            ▼            ▼
      Confirmation   New Lead      Contact
                      Alert       Created/Updated
```

---

## 🔐 Security & Privacy

The production workflow is **not included in this repository**.

The workflow available here is a sanitized portfolio version.

The following information has been removed or replaced:

* API keys
* Access tokens
* Authentication credentials
* Production webhook URLs
* Real phone numbers
* Customer information
* CRM identifiers
* Internal business information

Example placeholders are used where necessary:

```text
YOUR_HUBSPOT_CREDENTIAL
YOUR_SMS_API_CREDENTIAL
YOUR_BUSINESS_PHONE
YOUR_N8N_WEBHOOK
```

No real lead or customer data is included in this repository.

---

## 📂 Repository Structure

```text
lead-acquisition-crm-automation/
│
├── README.md
│
├── n8n/
│   └── lead-automation-workflow.json
│
├── architecture/
│   └── workflow-diagram.png
│
├── screenshots/
│   └── n8n-workflow.png
│
└── examples/
    └── sample-lead.json
```

---

## 🧪 Example Lead

The repository uses fictitious information for demonstration purposes.

```json
{
  "name": "Marie Example",
  "phone": "+15555550123"
}
```

---

## 💡 What This Project Demonstrates

This project demonstrates practical experience with:

* Workflow automation
* Webhook-based integrations
* CRM automation
* API integrations
* Lead management
* SMS automation
* Event-driven workflows
* Data transformation
* Marketing automation
* Google Ads lead processing
* Production workflow design

Most importantly, this is based on a **real-world business automation use case**, rather than a theoretical automation exercise.

---

## 🚀 Future Improvements

Possible future versions of the system could include:

* Automated follow-up sequences
* Lead status tracking
* Appointment scheduling integration
* AI-assisted lead qualification after initial contact
* Lead scoring
* Conversion tracking between the CRM and advertising platforms
* Automated reporting and analytics

---

## ⚠️ Disclaimer

This repository is intended for **portfolio and demonstration purposes**.

The published workflow does not contain production credentials, customer data, or confidential business information.

The production environment and its credentials remain private.
