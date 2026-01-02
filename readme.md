# Daily Applicant Digest by Role with Gemini AI Extraction

### 🤖 AI-Powered Recruitment Digest (n8n | Google Drive | Gemini AI | Gmail)

This workflow automates the screening process for hiring managers. It monitors folders for new resumes, uses Google Gemini AI to extract key information (skills, experience, contact details), categorizes applicants by role, and sends a structured daily digest email. This eliminates the need for manual resume opening and ensures managers see the best talent first.

---

## ⚡ Quick Implementation Steps

- Import the workflow JSON into your n8n instance.
- Connect your **Google Drive**, **Google Gemini AI**, and **Gmail** credentials.
- Set up a specific Google Drive folder for resume uploads.
- Activate the workflow to receive your organized hiring summary every day.

---

## 🎯 Who's It For

- **Hiring Managers:** Quickly scan candidate profiles without opening dozens of PDFs.
- **HR Teams:** Automate the initial screening and data extraction process.
- **Startup Founders:** Stay on top of recruitment while managing other business areas.
- **Technical Leads:** Get a direct list of candidate technical skills delivered to your inbox.

---

## 🛠 Requirements

| Tool                  | Purpose                                               |
| :-------------------- | :---------------------------------------------------- |
| **n8n Instance**      | To orchestrate the document processing and AI logic   |
| **Google Drive**      | Source folder where resumes (PDF/Docx) are uploaded   |
| **Gemini AI API Key** | To read resumes and extract structured candidate data |
| **Gmail Account**     | To send the daily summary digest to hiring managers   |

---

## 🧠 What It Does

- **Folder Monitoring:** Scans a designated Google Drive folder for new resumes added in the last 24 hours.
- **AI Extraction:** Gemini AI parses the resume text to find Name, Years of Experience, Key Skills, and Role Suitability.
- **Data Organization:** Groups candidates based on the role they applied for (e.g., Frontend, Backend, Sales).
- **HTML Digest:** Compiles an easy-to-read daily email containing a table of all new candidates.
- **Automated Delivery:** Sends the report at a scheduled time every morning.

---

## 🧩 Workflow Components

- **Schedule Trigger:** Triggers the digest once per day (or at your preferred interval).
- **Google Drive Node:** Downloads files from the specified recruitment folder.
- **Gemini AI Node:** Uses a custom prompt to extract structured JSON data from the resume content.
- **Code Node:** Aggregates and formats the AI-extracted data into an HTML table.
- **Gmail Node:** Sends the final formatted digest.

---

## 🔧 How To Set Up – Step-by-Step

1. **Import Workflow:** Upload the `.json` file into your n8n workspace.
2. **Connect Credentials:**
   - **Google Drive:** Connect via OAuth2.
   - **Gemini AI:** Enter your API key from Google AI Studio.
   - **Gmail:** Connect your Gmail account via OAuth2.
3. **Configure Nodes:**
   - **Drive Node:** Select the folder ID where you store incoming resumes.
   - **Gemini Node:** Ensure the prompt is set to look for the specific skills your team values.
4. **Define Timing:** Adjust the **Schedule Trigger** (e.g., 9:00 AM daily).
5. **Activate:** Toggle to **Active**.

---

## ✨ How To Customize

| Customization          | Method                                                                                    |
| :--------------------- | :---------------------------------------------------------------------------------------- |
| **Extract More Data**  | Update the Gemini prompt to look for "Current Salary" or "Notice Period".                 |
| **Role-Based Routing** | Use a "Switch" node to send Backend resumes to the CTO and Sales resumes to the CSO.      |
| **Slack Integration**  | Send individual candidate alerts to a Slack channel as soon as they apply.                |
| **Resume Ranking**     | Ask Gemini to give each candidate a "Match Score" from 1-10 based on the job description. |

---

## ➕ Add-ons (Advanced)

- **Auto-Reply:** Send a personalized "Thank You" email to the candidate after AI extraction.
- **CRM Sync:** Push the extracted data directly into Greenhouse, Lever, or a custom Airtable DB.
- **Sentiment Analysis:** Have the AI detect the "Tone" of the candidate's cover letter or summary.

---

## 📈 Use Case Examples

- **Technical Hiring:** A daily list of applicants sorted by programming languages and years of experience.
- **High-Volume Retail:** Quickly screening hundreds of seasonal applicants for specific shift availability.
- **Executive Search:** Summarizing high-level profiles for board review.

---

## 🧯 Troubleshooting Guide

| Issue                   | Possible Cause            | Solution                                                                |
| :---------------------- | :------------------------ | :---------------------------------------------------------------------- |
| **No files found**      | Folder ID is incorrect    | Copy the ID from the Google Drive URL and paste it into the node.       |
| **AI extraction fails** | Resume format unsupported | Ensure files are PDF or text-based; scan quality must be high.          |
| **No email sent**       | Empty list logic          | The workflow only sends an email if new resumes were found.             |
| **Missing Skills**      | AI Prompt too broad       | Be more specific in the Gemini node about which keywords to prioritize. |

---

## 📞 Need Assistance?

Need help customizing the AI prompt to extract specific technical certifications or integrating this with your ATS?

👉 **Contact WeblineIndia** — Expert automation partners for AI recruitment and HR tech.
