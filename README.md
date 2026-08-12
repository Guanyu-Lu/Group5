# CareLink SG — Multi-end Home Recovery Support Prototype

CareLink SG is a static GitHub Pages prototype created for the **Healthcare Beyond Hospitals** design challenge. It demonstrates how a simple AI-enabled web application can support home recovery, health check-ins, medication adherence, caregiver coordination, emergency contact support, and community healthcare handoff.

**Live Demo:** [https://guanyu-lu.github.io/Group5/](https://guanyu-lu.github.io/Group5/)

**QR Code:**  
![CareLink SG Web QR Code](./Web_QR.png)

---

## Prototype Focus

CareLink SG helps users manage recovery and health concerns from home. The prototype supports a two-end workflow:

- **Patient end:** used by patients to check in, monitor health, review AI-supported guidance, manage medication, view exercises, contact caregivers, and access community care.
- **Caregiver end:** used by caregivers to view bound patients at a high level through colour-coded status cards and receive demo emergency alerts.

The prototype is designed for classroom demonstration only. It does **not** diagnose medical conditions or replace qualified healthcare professionals.

---

## Demo Accounts

Use the following fixed demo accounts to test the role-based prototype.

| Role | Name | Phone Number | Password |
|---|---|---|---|
| Patient | David Tan | `+65 9123 4567` | `carelink123` |
| Patient | Mdm Tan | `+65 12345678` | `carelink456` |
| Caregiver | Rachel Tan | `+65 98765432` | `carelink789` |

David Tan and Mdm Tan are demo patients bound to Rachel Tan as their caregiver. Rachel Tan is the daughter of David Tan and Mdm Tan.

---

## Main Features

### 1. Role-based Login and Registration

- Supports phone-number login.
- Includes a registration form.
- New users can choose to register as either:
  - **Patient**
  - **Caregiver**
- Login role determines which interface is shown.
- Patient accounts enter the patient dashboard.
- Caregiver accounts enter the caregiver dashboard.

### 2. Patient Dashboard

The patient dashboard provides a home recovery overview for the logged-in patient.

It includes:

- Daily health summary
- Health score
- Heart rate, blood pressure, sleep, and steps
- Recovery plan timeline
- Quick actions for health tracking
- Essential emergency contact module
- Caregiver connection status

### 3. Essential Emergency Contact

The Essential module is placed on the patient dashboard for quick access.

It supports:

- A long-press emergency contact demo
- Three-second hold interaction
- Emergency contact activation modal
- Rachel Tan as the bound caregiver contact
- Demo patient location shown in the alert flow

The demo location used in this prototype is:

```text
JCU · 149 Sim Dr, Singapore 387380
```

In a production system, this would require secure location permission handling, backend support, and emergency workflow integration.

### 4. Caregiver Dashboard

Rachel Tan's caregiver account shows a separate caregiver interface rather than placing caregiver features inside the patient side.

The caregiver dashboard includes:

- Bound patient list
- Colour-coded patient status only:
  - **Green / Healthy**
  - **Yellow / Danger**
  - **Red / Urgent**
- Bind / unbind patient controls
- Add patient demo function
- Emergency alert popup when a patient activates Essential support
- Patient location display inside the alert popup

The caregiver view intentionally avoids showing detailed private health data such as exact heart rate, blood pressure, medication details, or symptom notes. This supports a privacy-aware caregiver workflow.

### 5. Patient–Caregiver Binding

The prototype supports demo binding relationships between patients and the caregiver.

Patient side:

- Patients can bind or unbind Rachel Tan in the Care Network page.
- If no caregiver is bound, the Essential emergency contact flow is disabled.
- If Rachel Tan is bound, the patient can activate the Essential contact flow.

Caregiver side:

- Rachel Tan can view currently bound patients.
- Rachel Tan can bind / unbind patients.
- Rachel Tan can add a local demo patient through the caregiver dashboard.

### 6. Something Feels Different Check-in

The Check-in page supports a low-friction health concern workflow.

It includes:

- Voice / text / guided selection entry points
- “Something feels different” starting point
- Adaptive follow-up style questions
- Urgent safety screening
- Next-step guidance
- Confidence level
- “Why this recommendation?” explanation
- Follow-up reminder option
- Shareable health summary
- Consent-based sharing option
- Check-in history

This makes the prototype more than a static health tracker. It demonstrates how users can describe concerns without needing to know a medical category first.

### 7. Health Monitoring

The Health Monitoring page allows patients to add and review home health readings.

Supported readings include:

- Heart rate
- Systolic blood pressure
- Diastolic blood pressure
- Sleep hours
- Steps
- Date and time

It also includes:

- Latest blood pressure summary
- Recent readings table
- Blood pressure trend chart
- Demo sample button for rising blood pressure
- Reset demo readings function

### 8. AI Health Insights

The AI Insights page demonstrates how recent readings and prototype trend signals can be turned into plain-language explanations.

It includes:

- AI-supported trend explanation
- Local trend detection logic
- Gemini API integration option
- “How the AI Insight Works” explanation
- Safety-focused guidance that avoids medical diagnosis

The prototype explains health trends and suggests safer next steps, but it does not diagnose conditions.

### 9. Medication Manager

The Medication page supports medication adherence demonstration.

It includes:

- Medication schedule
- Dose timing
- Taken / upcoming status
- Add medication function
- Weekly adherence display
- Next reminder information

### 10. Exercise Guidance with Images

The Exercises page provides visual recovery activity support.

It includes image-based guidance for:

- Shoulder & Neck Release
- Breathing Reset
- Gentle Walk

Each exercise includes:

- Illustration
- Step-by-step instructions
- Safety note
- “How to do this” detail modal

This improves the recovery experience because users can see how to perform an activity instead of relying on text-only instructions.

### 11. Care Network

The Care Network page manages the patient’s trusted caregiver connection.

It includes:

- Rachel Tan caregiver profile
- Bind / unbind action
- Sharing preference controls
- Demo caregiver notification flow
- Consent-focused information sharing explanation

### 12. Community Care

The Community Care page demonstrates a pathway from home support to community-based care.

It includes prototype cards for:

- Community Health Centre
- Telehealth consultation
- Caregiver support

It also includes an urgent-care reminder explaining that emergency symptoms require professional help.

### 13. AI Assistant

The AI Assistant page provides a chatbot-style support interface.

It includes:

- Prompt input
- Quick demo prompts
- Gemini API integration when connected
- Prototype context summary
- Plain-language response formatting

### 14. Settings and Privacy Information

The Settings page includes:

- Gemini API connection box
- Connect and test function
- Clear / disconnect function
- Large text mode toggle
- About section
- Q&A section
- Privacy Protection Statement
- Reset demo data option

The API key is stored in `sessionStorage` only and is not committed to the repository.

---

## Accessibility and Inclusive Design

CareLink SG includes several accessibility-focused design choices:

- Large text mode
- Simple button labels
- Visual status indicators
- Colour-coded patient status
- Guided selection for check-ins
- Image-based exercise instructions
- Mobile responsive layout
- No wearable device required for core use

---

## Data Storage and Prototype Limitations

This is a static front-end prototype. It uses browser storage only.

### Stored in `localStorage`

- Health readings
- Medication entries
- Caregiver list
- Patient-caregiver binding state
- Check-in history
- Custom demo patients
- Display preferences
- Demo emergency alerts

### Stored in `sessionStorage`

- Current login session
- Gemini API key

### Important limitations

- There is no backend database.
- Data is stored only in the browser used for testing.
- Cross-device real-time alerts are not fully supported in this static prototype.
- Caregiver emergency alert popup is a classroom demo interaction.
- Real deployment would require authentication, secure backend storage, audit logs, consent management, and notification infrastructure.

---

## Gemini API Use

CareLink SG can optionally connect to Gemini for AI-supported explanations.

The prototype sends only selected demo context when the user asks for an AI response, such as:

- Recent health readings
- Medication status
- Check-in summary
- Trend signal

No API key is included in the source code. Users must enter their own key at presentation time.

---

## Project Files

```text
Group5-main/
├── index.html
├── styles.css
├── app.js
├── carelink-logo.png
├── Web_QR.png
├── README.md
└── images/
    ├── shoulder-release.svg
    ├── breathing-reset.svg
    └── gentle-walk.svg
```

---

## Deployment

This project does not require a build step.

To deploy on GitHub Pages:

1. Upload all files to the repository root.
2. Make sure `index.html`, `styles.css`, `app.js`, `carelink-logo.png`, `Web_QR.png`, and the `images/` folder are in the root directory.
3. Go to **Settings → Pages**.
4. Select the main branch and root folder.
5. Open the deployed GitHub Pages URL.

Recommended test URL after uploading a new version:

```text
https://guanyu-lu.github.io/Group5/
```

Adding a query string helps avoid browser cache issues during testing.

---

## Testing Notes

Recommended test sequence:

1. Login as David Tan.
2. Check the patient dashboard.
3. Bind Rachel Tan in Care Network if needed.
4. Long-press the Essential contact button.
5. Logout.
6. Login as Rachel Tan.
7. Check the caregiver dashboard and emergency alert popup.
8. Review the patient status colour cards.
9. Test Add patient, Bind, and Unbind actions.
10. Test the Register page with both Patient and Caregiver roles.

Browser cache may keep old versions of static files. If a change does not appear, open the site in a private window or clear site data for `guanyu-lu.github.io`.

---

## Author

**Guanyu Lu**

Design Sprint TR2 2026

James Cook University Singapore

12 August 2026

## Disclaimer

CareLink SG is a **classroom prototype only**. It supports demonstration of health awareness, recovery support, caregiver coordination, and community care workflows. It does not diagnose medical conditions, provide medical treatment, or replace qualified healthcare professionals.
