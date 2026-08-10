# CareLink SG — AI-powered Community Health Companion

Static GitHub Pages prototype for the **Healthcare Beyond Hospitals** design challenge.

CareLink SG demonstrates how an AI-enabled digital solution can support home-based health monitoring, preventive care, medication adherence, caregiver connection, and community healthcare handoff.

 **Live Demo:** [Click here to experience our Platform](https://guanyu-lu.github.io/Group5/)

## Supported Features

### 1. Dashboard

- Shows a daily home health snapshot.
- Displays health score, heart rate, blood pressure, sleep, and steps.
- Includes a care plan timeline for daily check-ins and medication reminders.
- Provides quick actions for adding health readings and connecting a simulated smartwatch.
- Supports AI-generated daily summary when Gemini API is connected.

### 2. Health Monitoring

- Allows the user to manually add health readings:
  - Date and time
  - Heart rate
  - Systolic blood pressure
  - Diastolic blood pressure
  - Sleep hours
  - Steps
- Displays the latest blood pressure reading and demo risk label.
- Shows recent entries in a reading history table.
- Includes a blood pressure trend chart using Chart.js.
- Provides reset functionality for demo readings.
- Includes **Load rising blood pressure sample** to quickly generate a presentation-ready rising blood pressure trend.

### 3. AI Health Insights

- Uses Gemini 2.5 Flash to generate plain-language health trend explanations.
- Sends recent demo readings, medication status, and prototype trend signals to Gemini when the user requests an analysis.
- Renders AI output as formatted Markdown preview, including lists and bold text.
- Includes **How the AI Insight Works** to explain the prototype logic:
  - Collect latest stored readings.
  - Detect sustained changes using simple local rules.
  - Use Gemini to explain the result clearly.
  - Escalate safely by encouraging professional support when appropriate.

### 4. Medication Manager

- Shows current medication schedule.
- Supports adding new medication entries.
- Allows medication status to be marked as taken or upcoming.
- Shows weekly medication adherence.
- Displays next reminder information.

### 5. Care Network

- Shows connected caregivers and community care contacts.
- Supports caregiver sharing preferences for:
  - Blood pressure
  - Heart rate
  - Medication adherence
  - Sleep data
- Includes a demo caregiver alert workflow for unusual blood pressure trends.

### 6. Community Care

- Provides prototype cards for community-based support options:
  - Community Health Centre
  - Telehealth consultation
  - Caregiver support
- Demonstrates a safe handoff pathway from home monitoring to community care.
- Includes an urgent-care note to remind users to seek professional help when needed.

### 7. AI Assistant

- Provides a chatbot-style interface powered by Gemini 2.5 Flash.
- Supports quick demo prompts such as explaining blood pressure trends or summarising recent health data.
- Uses the current prototype data as context.
- Displays AI responses with Markdown preview formatting.

### 8. Gemini API Connection

- Includes an API key input field on the Settings page.
- Supports **Connect & test** to check the Gemini connection.
- Supports **Clear / Disconnect** to remove the API key immediately.
- The API key is stored only in `sessionStorage`, not in the repository source code.
- No API key is committed to GitHub.

### 9. Display Mode

- Includes a **Large text version** toggle in Settings.
- Large text mode improves readability during classroom presentation or accessibility-focused demonstration.
- The selected display mode is saved locally in the browser.

### 10. Settings Information Pages

The Settings page includes:

- **About** — explains what CareLink SG is and how it supports healthcare beyond hospitals.
- **Q&A** — provides presentation-ready answers about the prototype, AI role, data storage, and safety limits.
- **Privacy Protection Statement** — explains local storage, API key handling, Gemini data sharing, and prototype limitations.

### 11. Prototype Data Storage

- Health readings, medications, caregiver data, sharing settings, wearable status, and display mode are stored in browser `localStorage`.
- Gemini API key is stored in browser `sessionStorage` only.
- Reset demo data restores the default prototype state.
- Data is intended for classroom demonstration only.

### 12. Responsive Web Design

- Works as a static HTML/CSS/JavaScript website.
- Designed for GitHub Pages deployment.
- Responsive layout for desktop and smaller screens.
- Uses an icon-only CareLink SG product mark with consistent brand styling.

## Files

- `index.html`
- `styles.css`
- `app.js`
- `carelink-logo.png`
- `README.md`
- `.gitignore`

## Important Note

This is a **classroom prototype only**. It supports health awareness, preventive care demonstration, and care coordination scenarios. It does **not** diagnose medical conditions, provide clinical treatment, or replace qualified healthcare professionals.
