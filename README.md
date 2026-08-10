# CareLink SG — AI-enabled Community Health Prototype

CareLink SG is a static HTML/CSS/JavaScript prototype for the **Healthcare Beyond Hospitals** design challenge. It demonstrates home health monitoring, AI-supported trend explanation, medication adherence, caregiver sharing, community-care handoff, a simulated wearable connection, and an AI assistant.

## Features

- Responsive health dashboard and wellness snapshot
- Home health reading entry + 7-day blood-pressure chart (Chart.js)
- Rule-based demo trend signal
- Gemini 2.5 Flash AI health explanation
- Medication schedule, taken/not-taken status, weekly adherence
- Caregiver / family care network and data-sharing controls
- Community care / telehealth handoff simulation
- AI assistant using the current demo health context
- Runtime Gemini API key input with **Clear / Disconnect**
- Browser-local demo data (localStorage)
- API key stored in **sessionStorage only** — never hard-coded in the repository

## Gemini API

The site calls:

`https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash:generateContent`

At presentation time:

1. Open **Settings**.
2. Paste a Gemini API key.
3. Click **Connect & test**.
4. Use AI Insights or AI Assistant.
5. Click **Clear / Disconnect** before leaving the demo machine.

### Important security note

This is a client-side student prototype. Runtime entry avoids committing the key to GitHub, but a browser-held key is still accessible to the person using that browser session. Use a dedicated/restricted demo key and do not use this design as production secret management. A real deployment should put Gemini calls behind a backend/serverless endpoint and apply appropriate authentication, authorization, logging, data governance, and healthcare/privacy review.

## GitHub Pages deployment

No build step is needed.

1. Create a GitHub repository.
2. Upload `index.html`, `styles.css`, `app.js`, and this README to the repository root.
3. Open **Repository Settings → Pages**.
4. Choose **Deploy from a branch**.
5. Select `main` and `/ (root)`.
6. Save and open the generated Pages URL.

## Local preview

You can double-click `index.html`, but running a small local web server is more representative:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Prototype safety / scope

CareLink SG is for classroom demonstration only. It does not diagnose conditions, prescribe treatment, or replace qualified healthcare professionals. Community services shown in the interface are labelled as demo services and are not connected to real providers.
