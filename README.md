<div align="center">

# 🤖 B2B Lead Outreach AI Automation

### AI-powered lead research, website analysis & personalized outreach — fully automated with n8n

<p>
  <img src="https://img.shields.io/badge/n8n-Automation-EA4B71?style=for-the-badge&logo=n8n&logoColor=white" alt="n8n"/>
  <img src="https://img.shields.io/badge/OpenAI-GPT--4o--mini-412991?style=for-the-badge&logo=openai&logoColor=white" alt="OpenAI"/>
  <img src="https://img.shields.io/badge/Airtable-Database-18BFFF?style=for-the-badge&logo=airtable&logoColor=white" alt="Airtable"/>
  <img src="https://img.shields.io/badge/JavaScript-Data%20Processing-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript"/>
</p>

<p>
  <a href="#-overview">Overview</a> •
  <a href="#-features">Features</a> •
  <a href="#-architecture">Architecture</a> •
  <a href="#-workflow">Workflow</a> •
  <a href="#-setup">Setup</a>
</p>

</div>

---

## 📸 Project Preview

<p align="center">
  <img src="./assets/workflow.png" alt="B2B Lead Outreach AI Automation Workflow" width="100%">
</p>

> **From raw lead → website intelligence → AI qualification → personalized email → outreach-ready lead.**

---

## 🧠 What Is This?

**B2B Lead Outreach AI Automation** is an AI-powered outbound sales workflow built with **n8n**.

Instead of manually researching every prospect, the system automatically:

```text
Lead
 ↓
Validate
 ↓
Find verified contact
 ↓
Check duplicates
 ↓
Analyze website
 ↓
Identify business opportunities
 ↓
Recommend service
 ↓
Generate personalized email
 ↓
Store outreach draft
```

The goal is to transform a basic lead database into a **researched and outreach-ready pipeline**.

---

# ✨ Why This Project?

Traditional cold outreach often looks like this:

```text
Find company
    ↓
Open website
    ↓
Read website
    ↓
Find problems
    ↓
Decide what to offer
    ↓
Write email
    ↓
Track everything manually
```

This project automates the repetitive parts.

### Instead:

```text
                    AI + AUTOMATION

Airtable Lead
      │
      ▼
┌───────────────┐
│ Lead Validation│
└───────┬───────┘
        ▼
┌───────────────┐
│ Contact Check │
└───────┬───────┘
        ▼
┌───────────────┐
│ Deduplication │
└───────┬───────┘
        ▼
┌───────────────┐
│ Website Audit │
└───────┬───────┘
        ▼
┌───────────────┐
│   GPT-4o-mini │
│ AI Analysis   │
└───────┬───────┘
        ▼
┌───────────────┐
│ Service Match │
└───────┬───────┘
        ▼
┌───────────────┐
│ Email Writer  │
└───────┬───────┘
        ▼
┌───────────────┐
│ Outreach Draft│
└───────────────┘
```

---

# 🚀 Features

<table>
<tr>
<td width="50%">

### 🔎 Lead Processing

- Airtable lead ingestion
- Company validation
- Website validation
- Contact verification
- Lead routing
- Duplicate detection

</td>

<td width="50%">

### 🧠 AI Intelligence

- Website analysis
- Business problem detection
- Lead scoring
- Service recommendation
- Sales angle generation
- AI summaries

</td>
</tr>

<tr>
<td>

### ✍️ Personalized Outreach

- Company-specific observations
- Personalized subject lines
- Personalized email body
- Service-specific messaging
- Low-friction CTA

</td>

<td>

### 🗃️ Data Management

- Airtable integration
- Website analysis storage
- Email draft storage
- Processing status
- Outreach tracking
- Duplicate protection

</td>
</tr>
</table>

---

# 🏗️ Architecture

<p align="center">
  <img src="./assets/architecture.png" alt="System Architecture" width="90%">
</p>

### System Components

| Component | Responsibility |
|---|---|
| **n8n** | Workflow orchestration |
| **Airtable** | Lead & outreach database |
| **HTTP Request** | Website retrieval |
| **JavaScript** | Content extraction & routing |
| **GPT-4o-mini** | Website intelligence |
| **GPT-4o-mini** | Email generation |

---

# 🔄 Workflow

## 01 — Lead Ingestion

The workflow receives company and contact information from Airtable.

```text
New Company
     │
     ├──► Website Available?
     │
     └──► Retrieve Contacts
```

---

## 02 — Contact Verification

The system checks whether the company has a usable verified contact.

```text
Company
   │
   ▼
Verified Contacts?
   │
   ├── YES → Continue
   │
   └── NO  → Separate Route
```

---

## 03 — Duplicate Protection

Before spending resources on AI analysis, existing records are checked.

The system checks:

- Existing email
- Existing website analysis
- Company status
- Company identity

```text
              ┌───────────────┐
              │ Existing Data │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │ Duplicate?    │
              └───────┬───────┘
                  YES │ NO
                      │
               ┌──────┴──────┐
               ▼             ▼
             SKIP          PROCESS
```

This helps prevent repeatedly analyzing the same company or generating duplicate outreach.

---

# 🌐 Website Intelligence

Once a company passes validation, its website is fetched automatically.

The workflow extracts useful information such as:

```text
Page Title
Meta Description
H1
H2
H3
Important Links
Visible Text
```

Unnecessary HTML elements are removed before sending the content to the AI layer.

### Processing Pipeline

```text
Website HTML
     ↓
Remove Scripts
     ↓
Remove Styles
     ↓
Remove SVG
     ↓
Remove Comments
     ↓
Extract Text
     ↓
Normalize Content
     ↓
AI Analysis
```

---

# 🧠 AI Website Analysis

The website information is analyzed using **GPT-4o-mini**.

The AI evaluates multiple dimensions:

| Metric | Description |
|---|---|
| 🎨 Design Score | Visual/design quality |
| 📱 Mobile Score | Mobile experience |
| 🎯 Conversion Score | Conversion potential |
| 🔍 SEO Score | SEO-related signals |
| 🌐 Website Score | Overall website assessment |
| 📈 Lead Score | Overall outreach opportunity |

The AI also identifies:

- Main problems
- Business opportunities
- Primary pain point
- Recommended service
- Secondary service
- Sales angle
- Follow-up recommendation

---

# 🎯 Service Recommendation

Instead of sending the same offer to every company, the AI identifies a relevant service based on the available evidence.

Examples:

```text
Website Redesign
Website Development
Landing Page Development
Local SEO
SEO
E-commerce Development
Website Performance Optimization
Conversion Optimization
CRM Integration
Business Automation
```

### Example

```text
Company
   ↓
Website Analysis
   ↓
Problem Identified
   ↓
Business Opportunity
   ↓
Recommended Service
   ↓
Personalized Sales Angle
```

---

# ✍️ AI Email Generation

After the website analysis is saved, the workflow generates a personalized outreach email.

The email generator receives information such as:

```json
{
  "company": "Example Company",
  "industry": "Real Estate",
  "websiteScore": 72,
  "primaryPainPoint": "Weak lead conversion",
  "recommendedService": "Conversion Optimization",
  "salesAngle": "Improve visitor-to-lead conversion"
}
```

The AI then creates:

```text
Subject
   +
Personalized Opening
   +
Specific Observation
   +
Relevant Opportunity
   +
Recommended Service
   +
Low-friction CTA
```

---

# 📊 Data Flow

<p align="center">
  <img src="./assets/data-flow.png" alt="Data Flow" width="90%">
</p>

```text
┌──────────────────┐
│     Airtable     │
│   Lead Database  │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│   n8n Workflow   │
│   Orchestration  │
└────────┬─────────┘
         │
         ├──────────────┐
         ▼              ▼
┌──────────────┐ ┌──────────────┐
│   Website    │ │   Contacts   │
│    Data      │ │     Data     │
└──────┬───────┘ └──────┬───────┘
       │                │
       └────────┬───────┘
                ▼
        ┌───────────────┐
        │ GPT-4o-mini   │
        │ AI Analysis   │
        └───────┬───────┘
                ▼
        ┌───────────────┐
        │ Website       │
        │ Analysis      │
        └───────┬───────┘
                ▼
        ┌───────────────┐
        │ GPT-4o-mini   │
        │ Email Writer  │
        └───────┬───────┘
                ▼
        ┌───────────────┐
        │ Email Draft   │
        └───────────────┘
```

---

# 🗄️ Airtable Structure

The system uses Airtable as the central data layer.

### Companies

Stores company-level information:

```text
Company
Website
Industry
Location
Rating
Reviews
Analysis Status
Lead Score
Recommended Service
Website Scores
```

### Contacts

Stores:

```text
Company
Contact Name
Email
Role
Verification Status
```

### Website Analysis

Stores:

```text
Company
Website
Website Score
Design Score
Mobile Score
Conversion Score
SEO Score
Main Problems
Opportunities
Primary Pain Point
Recommended Service
Secondary Service
Sales Angle
Lead Score
AI Analysis
```

### Email Messages

Stores:

```text
Company
Lead
Analysis
Recipient Email
Subject
Email Body
Recommended Service
Lead Score
Status
Created At
Sent At
```

---

# 🛡️ Duplicate Protection

The workflow uses multiple checks instead of relying on a single duplicate filter.

```text
          Lead
           │
           ▼
    Existing Email?
       │       │
      YES      NO
       │       │
      SKIP     ▼
        Existing Analysis?
             │       │
            YES      NO
             │       │
            SKIP     ▼
                  Continue
                     │
                     ▼
              Final Duplicate
                   Gate
                     │
                     ▼
              Generate Email
```

This is especially important when workflows are triggered repeatedly.

---

# 🧩 Main n8n Nodes

| Node | Purpose |
|---|---|
| `01 - Manual Trigger` | Manual execution |
| `00a - New Company` | New company trigger |
| `00b - Verified Contact` | Contact trigger |
| `02 - Get Companies` | Retrieve companies |
| `03 - Filter Valid Companies` | Website validation |
| `04 - Get Contacts` | Retrieve contacts |
| `E1 - Existing Emails` | Existing email lookup |
| `E2 - Existing Analyses` | Existing analysis lookup |
| `07 - Route Company` | Processing route |
| `08 - Fetch Website` | Website request |
| `09 - Extract Website Content` | Content extraction |
| `10 - AI Website Analysis` | AI analysis |
| `11 - Save Website Analysis` | Store analysis |
| `F1 - Recheck Existing Email` | Final email check |
| `F2 - Final Duplicate Gate` | Duplicate protection |
| `12 - AI Email Generator` | Email generation |
| `13 - Save Email Draft` | Store email |
| `EmailValidation` | Validate email |
| `Send a message` | Outreach delivery |
| `14 - Update Company Status` | Update status |

---

# 🛠️ Tech Stack

<p align="center">

<img src="https://skillicons.dev/icons?i=js" height="55" alt="JavaScript"/>
&nbsp;
<img src="https://skillicons.dev/icons?i=html" height="55" alt="HTML"/>
&nbsp;
<img src="https://skillicons.dev/icons?i=github" height="55" alt="GitHub"/>

</p>

<div align="center">

| Technology | Role |
|---|---|
| **n8n** | Automation & orchestration |
| **OpenAI** | LLM intelligence |
| **Airtable** | Data management |
| **JavaScript** | Data processing |
| **HTTP APIs** | Website retrieval |

</div>

---

# 📁 Repository Structure

```text
b2b-lead-outreach-ai/
│
├── README.md
│
├── workflow/
│   └── b2b-lead-outreach.json
│
├── assets/
│   ├── workflow.png
│   ├── architecture.png
│   ├── data-flow.png
│   └── demo.png
│
├── prompts/
│   ├── website-analysis.md
│   └── email-generation.md
│
├── docs/
│   ├── architecture.md
│   └── airtable-schema.md
│
└── examples/
    └── sample-output.json
```

---

# ⚡ Quick Start

## 1. Clone

```bash
git clone https://github.com/YOUR_USERNAME/b2b-lead-outreach-ai.git

cd b2b-lead-outreach-ai
```

## 2. Install / Run n8n

```bash
npm install n8n -g
```

```bash
n8n start
```

## 3. Import Workflow

Open n8n:

```text
Workflows
   ↓
Import from File
   ↓
b2b-lead-outreach.json
```

## 4. Configure Credentials

Connect:

```text
Airtable
OpenAI
```

## 5. Configure Airtable

Create the required tables:

```text
Data
Data2
Website Analysis
Email Messages
```

## 6. Test

Start with **one test company**.

Verify:

```text
✓ Website fetched
✓ Website content extracted
✓ AI analysis generated
✓ Analysis stored
✓ Duplicate check passed
✓ Email generated
✓ Email stored
```

---

# 🔐 Security

Never commit:

```text
❌ API keys
❌ OAuth tokens
❌ Airtable credentials
❌ SMTP credentials
❌ Private lead databases
❌ Personal contact information
```

Use n8n's credential system instead.

---

# 📈 Future Roadmap

### Lead Intelligence

- [ ] LinkedIn enrichment
- [ ] Hunter integration
- [ ] Company enrichment
- [ ] Industry classification
- [ ] Better lead scoring

### Website Intelligence

- [ ] Page-speed analysis
- [ ] Core Web Vitals
- [ ] Broken-link detection
- [ ] Technical SEO analysis
- [ ] Mobile UX analysis

### Outreach

- [ ] Automated follow-ups
- [ ] Reply detection
- [ ] Reply classification
- [ ] Meeting detection
- [ ] Campaign analytics

### CRM

- [ ] CRM synchronization
- [ ] Pipeline tracking
- [ ] Lead lifecycle
- [ ] Conversion analytics

---

# 🎯 Use Cases

This system can be adapted for:

- Digital agencies
- Web development agencies
- SEO agencies
- Marketing agencies
- AI automation agencies
- B2B sales teams
- Freelancers
- Lead-generation operations

---

# 💡 What This Project Demonstrates

This project combines multiple practical AI engineering concepts:

```text
┌───────────────────────────────┐
│       AI APPLICATION           │
├───────────────────────────────┤
│                               │
│  LLM Integration              │
│  ↓                            │
│  Structured AI Output         │
│  ↓                            │
│  Web Data Extraction          │
│  ↓                            │
│  Business Intelligence        │
│  ↓                            │
│  Lead Qualification           │
│  ↓                            │
│  Personalized Generation      │
│  ↓                            │
│  Workflow Automation          │
│  ↓                            │
│  Persistent Data Layer        │
│                               │
└───────────────────────────────┘
```

---

# 📸 Screenshots

### n8n Workflow

<p align="center">
  <img src="./assets/workflow.png" alt="n8n workflow" width="100%">
</p>

### AI Analysis

<p align="center">
  <img src="./assets/analysis.png" alt="AI website analysis" width="90%">
</p>

### Generated Email

<p align="center">
  <img src="./assets/email.png" alt="AI generated email" width="80%">
</p>

---

# 🔍 Example

### Input

```text
Company:
Example Roofing

Website:
https://example.com

Industry:
Roofing

Contact:
John Doe

Role:
Owner
```

### AI Analysis

```text
Website Score: 72/100
Conversion Score: 54/100
SEO Score: 61/100

Primary Pain Point:
Weak lead conversion path

Recommended Service:
Conversion Optimization

Lead Score:
78/100
```

### Output

```text
Personalized outreach email
        ↓
Stored in Airtable
        ↓
Validated
        ↓
Ready for outreach
```

---

# ⚠️ Responsible Outreach

This automation is intended for legitimate B2B outreach.

Before sending messages at scale, verify applicable:

- Email regulations
- Anti-spam requirements
- Privacy requirements
- Provider policies
- Opt-out requirements

AI-generated content should also be reviewed before large-scale outreach.

---

# 👨‍💻 Author

<div align="center">

### Sham Kumar

**AI / GenAI Engineer**

Building practical systems around:

`AI Agents` • `Generative AI` • `RAG` • `Automation` • `n8n`

<a href="https://github.com/shyam007-srec">
  <img src="https://img.shields.io/badge/GitHub-shyam007--srec-181717?style=for-the-badge&logo=github" alt="GitHub"/>
</a>

</div>

---

# ⭐ If You Find This Useful

If this project helped you understand how AI can be combined with workflow automation for real-world B2B applications, consider giving the repository a ⭐.

<div align="center">

### Built with ⚡ n8n + 🧠 AI + 📊 Airtable

</div>
