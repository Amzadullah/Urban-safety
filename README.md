# 🏙️ Urban Safety Alert

### AI-Powered Urban Problem Reporting & Management System

<p align="center">
  <strong>Report Problems. Track Progress. Build Safer Cities.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Android%20%7C%20Web-brightgreen" />
  <img src="https://img.shields.io/badge/AI-Google%20Gemini-blueviolet" />
  <img src="https://img.shields.io/badge/Language-Bangla%20%7C%20English%20%7C%20Banglish-orange" />
  <img src="https://img.shields.io/badge/Backend-Firebase-yellow" />
  <img src="https://img.shields.io/badge/Tests-15%20Passed-success" />
</p>

---

## 📌 Overview

**Urban Safety Alert** is an AI-powered urban safety and civic issue reporting platform that connects citizens with responsible authorities through a transparent, real-time reporting and management system.

Citizens can report urban problems using descriptions, photographs, and GPS-based locations. Artificial intelligence analyzes each report, identifies the issue category and severity, generates a Bengali summary, and recommends the responsible organization.

Authorities receive reports through a centralized dashboard, where they can review, verify, reject, prioritize, and update the progress of each issue.

Citizens can track their reports in real time until the problems are resolved.

The platform is available as an Android application and a web application, sharing the same backend and database.

## 🎯 Problem Statement

Urban communities frequently experience problems such as:

- Broken roads and damaged footpaths.
- Non-functional streetlights.
- Waterlogging and drainage problems.
- Garbage accumulation.
- Accidents and public hazards.
- Criminal activities and safety concerns.

However, citizens often do not know where to report these problems. Even after submitting complaints, they have limited opportunities to track progress or receive updates.

Authorities also face challenges managing scattered, unstructured complaints without accurate locations or priority classifications.

**Urban Safety Alert addresses these challenges through one centralized, AI-powered platform.**

## 💡 Key Features

### 👤 Citizen Application

- Secure account registration and authentication.
- Report submission in Bengali, English, and Banglish.
- Eight predefined issue categories.
- Upload photographs using the camera or gallery.
- Automatic image compression and optimization.
- GPS-based location detection.
- Interactive map-based location selection.
- Automatic address detection.
- Four severity levels: Low, Medium, High, and Critical.
- AI-powered report analysis before submission.
- AI-generated Bengali summaries.
- Responsible authority recommendations.
- Live report status tracking.
- Real-time notifications.
- Offline report storage with automatic submission when connectivity returns.
- Account deletion and privacy controls.

### 🏛️ Authority Dashboard

- Real-time administrative dashboard.
- Total, Pending, In Progress, Resolved, Critical, and Verified statistics.
- Seven-day reporting activity chart.
- Category-based report analytics.
- Advanced search and filtering.
- Interactive map with color-coded report markers.
- Critical report highlighting.
- High-priority issue management.
- Report verification and rejection.
- Administrative review notes visible to citizens.
- One-tap status updates.
- AI re-analysis using Google Gemini.
- CSV export of filtered or complete reports.

## 🤖 AI Integration

Urban Safety Alert uses a two-layer AI architecture to support intelligent report processing both online and offline.

### 1. Google Gemini AI

Google Gemini provides advanced AI analysis using both text and images.

Capabilities:

- Image and text understanding.
- Automatic issue classification.
- Severity assessment.
- Responsible organization recommendations.
- Bengali summary generation.
- AI confidence score.
- Spam detection with explanations.

Gemini analysis can be triggered manually, during submission, or by authorities through the re-analysis feature.

### 2. On-Device AI

The application also includes an offline AI system for preliminary text analysis.

Capabilities:

- Works without an internet connection.
- Supports Bengali, English, and Banglish vocabulary.
- Instant category prediction.
- Severity estimation.
- Preliminary report classification.
- Fallback analysis when Gemini is unavailable.

**Important:** AI provides recommendations only. Citizens control their submissions, and authorized human officials make the final verification, rejection, and resolution decisions.

## 📂 Supported Report Categories

| Icon | Category | Example |
|---|---|---|
| 💡 | Streetlight | Broken or non-functional streetlights |
| 🚨 | Crime | Theft, robbery, suspicious activities |
| 🚗 | Accident | Road accidents and collisions |
| ⚠️ | Hazard | Fire, exposed wires, gas leaks |
| 🌊 | Waterlogging | Flooded roads and drainage issues |
| 🛣️ | Road Damage | Broken roads and potholes |
| 🚶 | Footpath | Damaged or obstructed footpaths |
| 🗑️ | Garbage | Waste accumulation and improper disposal |

## 🔄 Report Management Workflow

The platform follows a transparent four-stage workflow:

```text
       CITIZEN
          |
          v
    Submit Report
          |
          v
     AI Analysis
          |
          v
   AUTHORITY REVIEW
          |
      +---+---+
      |       |
      v       v
   Verify   Reject
      |
      v
  In Progress
      |
      v
   Resolved
      |
      v
 CITIZEN NOTIFIED
```

**Report statuses:**

- **Pending:** Newly submitted report awaiting review.
- **In Progress:** Verified report currently being addressed.
- **Resolved:** Reported issue has been resolved.
- **Rejected:** Report rejected by the authority with an explanatory note.

Citizens receive live updates whenever authorities change report statuses or verification decisions.

## 🗺️ Interactive Map

The authority dashboard includes an interactive map displaying all reported issues.

**Map marker colors:**

- 🟠 Orange — Pending
- 🔵 Blue — In Progress
- 🟢 Green — Resolved

Critical reports are highlighted with larger markers and red outlines for easier identification.

Authorities can filter reports and view their corresponding locations directly on the map.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Android | Mobile application |
| Web Application | Browser-based platform |
| Google Gemini | AI-powered text and image analysis |
| On-Device AI | Offline report classification |
| Firebase Authentication | User authentication |
| Cloud Firestore | Real-time database |
| Firebase Storage | Report image storage |
| Netlify | Web deployment |
| GPS & Maps | Location detection and visualization |
| CSV | Report data export |

**Platform Compatibility:** Android 8 through Android 16.

Both Android and Web applications use the same backend for synchronized data and real-time updates.

## 🔐 Security & Privacy

Security and privacy are fundamental parts of Urban Safety Alert.

- Citizens can access only their own reports.
- New reports always start as Pending and Unverified.
- Citizens cannot verify their own reports.
- Authorities can update administrative fields but cannot modify original citizen descriptions, images, or locations.
- Users cannot change their assigned roles themselves.
- Image uploads require authentication.
- Image uploads are restricted to image files up to 5 MB.
- Firebase Authentication securely manages passwords.
- Users can permanently delete their accounts and associated reports.
- All network communications use HTTPS.
- Firestore Security Rules enforce access restrictions at the database level.

**Production Note:** Authority registration is enabled for the competition demonstration. In production, authority accounts will be created and managed by administrators.

## 🧪 Testing

The project includes 15 automated tests.

| Test Area | Number of Tests | Result |
|---|---:|---|
| On-Device AI | 12 | ✅ Passed |
| Gemini Integration | 3 | ✅ Passed |
| **Total** | **15** | **15 Passed** |

Tests include Bengali, English, and Banglish examples to validate multilingual AI functionality.

## 📱 Application Demonstration

The recommended demonstration uses two devices:

**Device 1 — Citizen**
1. Log in as a citizen.
2. Create a new report.
3. Capture or upload an issue photograph.
4. Select the GPS location.
5. Enter a description in Banglish.
6. View AI analysis and submit the report.
7. Track the report status.

**Device 2 — Authority**
1. Log in as an authority.
2. View the incoming report on the dashboard.
3. Review AI recommendations and report details.
4. Verify the report and add a review note.
5. Change the status to In Progress.
6. Mark the report as Resolved.

Return to the citizen device to demonstrate real-time updates and notifications.

## 🚀 Future Roadmap

Planned improvements include:

- [ ] Administrator-controlled authority registration.
- [ ] Department-based authority management (DNCC, DSCC, Police, Fire Service).
- [ ] Firebase Cloud Messaging for background push notifications.
- [ ] Duplicate report detection.
- [ ] Community confirmation through an "I Have Also Seen This" feature.
- [ ] Geographic issue heatmaps.
- [ ] Average resolution time analytics.
- [ ] Advanced urban safety statistics.
- [ ] Google Play Store publication.

## 🌍 Social Impact

Urban Safety Alert aims to contribute to safer, smarter, and more accountable cities.

**For Citizens:** Makes reporting easier and provides transparency throughout the resolution process.

**For Authorities:** Centralizes complaints, identifies urgent issues, and improves response management.

**For Decision-Makers:** Provides structured data for identifying recurring problems, understanding affected areas, and improving resource allocation.

By combining AI, GPS, real-time communication, and human decision-making, Urban Safety Alert transforms everyday civic complaints into actionable information.

## 👨‍💻 Developer

**Amzadullah Ratul**

Project: Urban Safety Alert

## 📄 License

No license has been specified yet. All rights are reserved by the project author unless a license is added to this repository.

---

<p align="center">
  <strong>🏙️ Urban Safety Alert</strong><br/>
  Making Urban Communities Safer Through Technology and Innovation.
  <br/><br/>
  <i>Report Problems. Track Progress. Build Safer Cities.</i>
</p>
