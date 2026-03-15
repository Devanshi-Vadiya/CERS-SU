<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=220&section=header&text=CERS%2B&fontSize=90&fontColor=fff&fontAlignY=38&desc=Community%20Emergency%20Response%20System&descAlignY=60&descAlign=50&animation=fadeIn" width="100%"/>

<br/>

![React](https://img.shields.io/badge/React-19-61dafb?style=for-the-badge&logo=react&logoColor=white&labelColor=0d1117)
![TypeScript](https://img.shields.io/badge/TypeScript-5.8-3178c6?style=for-the-badge&logo=typescript&logoColor=white&labelColor=0d1117)
![Firebase](https://img.shields.io/badge/Firebase-Firestore-ff9100?style=for-the-badge&logo=firebase&logoColor=white&labelColor=0d1117)
![Vite](https://img.shields.io/badge/Vite-6.x-646cff?style=for-the-badge&logo=vite&logoColor=white&labelColor=0d1117)
![Gemini](https://img.shields.io/badge/Google_Gemini-AI-4285f4?style=for-the-badge&logo=google&logoColor=white&labelColor=0d1117)

<br/>

### 🚨 *When every second counts — CERS+ answers the call.* 🚨

> A **real-time, AI-powered emergency response platform** that connects victims, hospitals, first responders, and now — **insurance providers** — in one unified ecosystem.

<br/>

[![🚨 Live Demo](https://img.shields.io/badge/🚨_LIVE_DEMO-CLICK_HERE-FF4757?style=for-the-badg)](https://cers-4.onrender.com/)
[![⭐ Star this Repo](https://img.shields.io/badge/⭐_Star_this_Repo-If_it_blew_your_mind-ffd700?style=for-the-badge)](.)

</div>

---

## 💥 The Problem We're Solving

> **Every year, thousands of lives are lost — not because help didn't exist, but because it arrived too late, or got buried in paperwork.**

- 🕐 Average emergency response time in urban India: **8–12 minutes**. The golden hour is wasted.
- 📋 Post-emergency insurance claims take **weeks** — victims deal with trauma AND bureaucracy simultaneously.
- 🏥 Hospitals operate blind — no real-time incident feed, no dispatch intelligence.
- 🧍 Bystanders freeze — no guidance, no way to report effectively.

**CERS+ tears down every one of these walls — simultaneously.**

---

## 🌍 Real-World Impact

<div align="center">

| 💀 The Old Way | ✅ The CERS+ Way |
|:-:|:-:|
| Call 108, wait on hold | One-tap SOS — dispatched in **< 3 seconds** |
| Describe location verbally | Auto GPS + reverse geocoding — **pinpoint accuracy** |
| Bystanders can't help | Guest Mode — **anyone** can report an accident |
| Hospital staff use whiteboards | Live command dashboard — **zero lag** |
| Insurance claim filed weeks later | **Instant claim initiation** at point of emergency |
| AI? What AI? | Gemini-powered triage assistant — **24/7, real-time** |

</div>

**CERS+ doesn't just digitize emergency response. It reimagines it from the ground up.**

---

## ⚡ What is CERS+?

CERS+ (**Community Emergency Response System Plus**) is a full-stack web application that digitizes and accelerates every stage of the emergency lifecycle — from the moment of crisis to the final insurance settlement.

```
🧑 Victim / Bystander
        │  One-Tap SOS / Guest Report
        ▼
📡 CERS+ Platform  ──▶  Firestore Real-time Sync
        │
        ├──▶  🏥 Hospital Dashboard    → Accept, Dispatch, Track, Arrive
        ├──▶  🛡️  Admin Panel          → Vet & Approve Hospitals
        └──▶  🧾 Insurance Dashboard  → Instant Claim Feed, Policy Matching, Deals
```

---

## 🗂️ User Roles

| Role | Description |
|------|------------|
| 👤 **General User** | Triggers personal SOS, reports guest emergencies, gets ambulance ETA, views insurance options |
| 🏥 **Hospital** | Views SOS queue, accepts cases, dispatches ambulances, tracks fleet |
| 🧾 **Insurance Provider** | Views emergency claims feed, matches policies, redirects users to relevant deals |
| 🛡️ **Admin** | Vets & approves hospitals and insurance providers, blacklists violators |

---

## 🔥 Core Features

### 🆘 Personal SOS System

<table>
<tr>
<td width="50%">

**One-tap SOS Button**
- Single press triggers an emergency alert immediately
- Auto-captures GPS coordinates via browser Geolocation API
- Reverse-geocodes coordinates to a readable address using OpenStreetMap / Nominatim
- Emergency dispatched to Firestore in real time

</td>
<td width="50%">

**Emergency Type Selection**
- 8 emergency categories: Heart Attack, Accident, Bleeding, Burns, Stroke, Breathing, Seizure, Panic / Other
- Each type includes step-by-step protocol instructions, Dos, and Don'ts
- Color-coded by severity (Critical → Urgent → Moderate)

</td>
</tr>
</table>

---

### 📍 Real-Time Location & Tracking

- **Live GPS capture** — high-accuracy coordinates from device
- **Ambulance ETA countdown timer** — live countdown from hospital-set ETA
- **TrackingMap** — interactive Google Maps component showing incident location
- **Location update stream** — Firestore listeners push location changes to hospitals instantly

---

### 📹 Video Evidence Recording

- **MediaRecorder-powered** in-browser video capture (no app needed)
- Auto-starts recording when emergency type is selected
- **Front / Rear camera toggle** during recording
- **Mute / Unmute** audio control
- Review mode with **Save or Discard** before uploading
- Evidence stored as a Blob URL and attached to the Firestore emergency document
- Hospitals and insurance providers can view evidence in a **full-screen video modal** with metadata overlay

---

### 🤖 AI Chat Assistant (Gemini-Powered)

- Powered by **Google Gemini API** (`@google/genai`)
- In-app AI assistant answers medical and safety questions in real time
- Provides first-aid guidance, calming advice, protocol suggestions
- Available as a dedicated **"Assistant"** tab in the user dashboard

---

### 👥 Guest Emergency Mode *(Bystander Reporting)*

> **Allows a logged-in user to report an emergency for someone else** — e.g., a road accident witnessed on a highway.

<table>
<tr><td>

**Step 1 — Emergency Type Selection**
- Choose the type of emergency witnessed (Road Accident, Medical Emergency, etc.)
- Orange "Guest Mode" UI clearly distinguishes it from personal SOS

</td></tr>
<tr><td>

**Step 2 — Victim Details & Medical Info**
- Toggle victim condition: Conscious / Unconscious, Bleeding / Not, Breathing / Not
- Select number of victims: 1 / 2–5 / Mass Accident
- Optional bystander-provided medical info: Blood Group, Known Conditions, Current Medications, Allergies
- All data synced to Firestore only if provided

</td></tr>
<tr><td>

**Step 3 — Active Tracking + First Aid Guide**
- Live map of the incident GPS location
- Ambulance ETA countdown once a hospital accepts
- Step-by-step First Aid Guide and Do's/Don'ts for the emergency type
- Quick-action buttons: **Notify Community Responders**, **Responder Chat**, **Evidence Camera**

</td></tr>
</table>

---

### 🏥 Hospital Command Dashboard

| View | Features |
|------|----------|
| **Command Center** | Live SOS feed, incident cards, accept/dispatch/arrived workflow |
| **Active SOS Queue** | Full list of open emergencies, search, emergency type + location |
| **Fleet & Beds** | Visual ambulance units and ER bed capacity from hospital profile |
| **Medical Staff Roster** | Personnel table with active status |
| **Data Insights** | Hospital reliability score, average response time, ETA accuracy % |
| **Shift Report** | Auto-generated printable PDF-style shift handover document |

**Live incident cards show:**
- 🟠 `GUEST REPORT` badge for bystander-reported emergencies
- Colour-coded victim condition pills (Conscious / Bleeding / Breathing)
- Access Medical Profile (registered user) or Victim Info (guest-provided data) — hidden if no info available
- Video evidence viewer with duration, timestamp, and patient metadata

---

### 🧾 Insurance Dashboard *(NEW — Exclusive to CERS+)*

> **The missing link between emergency response and financial protection — built directly into the crisis flow.**

CERS+ introduces a dedicated **Insurance Provider Dashboard** that plugs seamlessly into the emergency lifecycle alongside the Hospital and User dashboards. The moment an SOS is triggered, the insurance layer activates — turning a crisis moment into a claim-ready event, automatically.

<table>
<tr>
<td width="50%">

**📋 Live Emergency Claims Feed**
- Insurance providers see a real-time stream of active and resolved emergencies — filtered to their coverage zones and policy types
- Each claim card shows: emergency type, victim profile, GPS location, video evidence link, hospital accepted status, and ETA
- Claims are pre-tagged by severity (Critical / Urgent / Moderate) so adjusters can prioritize instantly — no manual sorting

</td>
<td width="50%">

**🤝 Policy Matching & Deal Redirect Engine**
- The dashboard intelligently matches each emergency case to relevant insurance products — health, accident, hospitalization, or vehicle cover
- Victims and bystanders browsing the User Dashboard are shown **personalized insurance deal cards** curated by providers — contextually relevant, zero cold ads
- One-click redirect takes users to the insurer's deal or claim initiation page, pre-filled with emergency metadata (date, type, location)

</td>
</tr>
<tr>
<td width="50%">

**📊 Provider Analytics & Claim Insights**
- Insurers get an analytics panel showing claim volume by emergency type, geographic hotspots, average claim response time, and policy conversion rates
- Helps providers identify underserved regions and optimize deal targeting in real time

</td>
<td width="50%">

**🔐 Secure Provider Onboarding**
- Insurance companies register via a dedicated portal — separate from Hospital and Admin flows
- Admin approves insurer accounts before any emergency data is accessible
- All claim data is **read-only** for insurers — zero ability to modify emergency records

</td>
</tr>
</table>

> 💡 **Why it matters:** Victims shouldn't be Googling insurance options from a hospital bed. CERS+ puts the right policy in front of the right person at the exact right moment — making financial protection as fast as the ambulance.

---

### 🛡️ Admin Panel

- Secured by username + password (`/admin-panel` route)
- View all registered hospitals **and insurance providers** with full profile details
- **Approve**, **Reject**, or **Blacklist** with reason
- Blacklisted entities cannot log in to the system

---

### 📊 Hospital Reliability Scoring

CERS+ tracks hospital performance automatically using a weighted formula:

```
Reliability Score = (0.4 × ETA Accuracy) + (0.4 × Response Speed) + (0.2 × Completion Rate)
```

- Scored out of 100
- Calculated from real ambulance arrival times vs promised ETAs
- Rolling average — recent cases have slightly higher weight
- Displayed as a large score card in the Hospital Analytics dashboard

---

### 🔐 Authentication & Security

- **General users** — phone number-based registration and login
- **Hospitals** — email + password with admin approval gate
- **Insurance Providers** — dedicated portal with admin approval gate
- **Password reset** — via `/reset-password` route
- **Session persistence** — `sessionStorage` keeps users logged in across page refreshes
- **Blacklist enforcement** — blocked entities shown a specific rejection reason on login attempt

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────┐
│              React 19 + Vite + TypeScript        │
└────────────────┬────────────────────────────────┘
                 │
       ┌─────────▼──────────┐
       │   EmergencyContext  │  ← Global State (React Context)
       │   (Firestore sync)  │  ← Real-time onSnapshot listeners
       └──────┬──────┬───────┘
              │      │
    ┌─────────┼──────┼──────────────┐
    ▼         ▼      ▼              ▼
GeneralApp  Hospital  Insurance   AdminDashboard
    │       Dashboard  Dashboard
    ├── SOSButton              └── Claims Feed
    ├── GuestEmergencyFlow         Policy Matcher
    ├── ActiveEmergency            Deal Redirect Engine
    │     ├── TrackingMap          Provider Analytics
    │     ├── VideoRecorder
    │     └── AmbulanceCountdown
    └── ChatAssistant (Gemini AI)
```

```
Firebase Firestore Collections:
├── emergencies               ← Active & resolved SOS incidents
├── users                     ← General user profiles
├── hospitals                 ← Hospital profiles + status
├── insurance_providers       ← Insurer profiles + approval status
├── insurance_claims          ← Emergency-linked claim records
├── hospital_stats            ← Reliability scores (live)
└── hospital_response_history ← Per-case response records
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- Firebase project with Firestore enabled
- Google Maps API key
- Google Gemini API key

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/cers-plus.git
cd cers-plus

# Install dependencies
npm install

# Start development server
npm run dev
```

### Environment Setup

Create a `firebaseConfig.ts` with your Firebase credentials:

```typescript
import { initializeApp } from 'firebase/app';
import { getFirestore } from 'firebase/firestore';

const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
  // ...
};

const app = initializeApp(firebaseConfig);
export const db = getFirestore(app);
```

### Build for Production

```bash
npm run build
```

---

## 🧰 Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | React 19, TypeScript 5.8, Vite 6 |
| **Styling** | Tailwind CSS (utility classes) |
| **Database** | Firebase Firestore (real-time) |
| **Maps** | @react-google-maps/api |
| **AI** | Google Gemini API (`@google/genai`) |
| **Charts** | Recharts |
| **Icons** | Lucide React |
| **Geocoding** | OpenStreetMap Nominatim (free, no API key) |
| **Video** | Browser MediaRecorder API |

---

## 📁 Project Structure

```
CERS/
├── App.tsx                      # Root router & auth state machine
├── types.ts                     # All TypeScript interfaces & enums
├── constants.ts                 # Emergency type definitions + protocols
├── firebaseConfig.ts            # Firebase initialization
│
├── contexts/
│   └── EmergencyContext.tsx     # Global state, Firestore sync, all actions
│
└── components/
    ├── LandingPage.tsx           # Public landing page
    ├── AuthScreen.tsx            # Login screen
    ├── SignUpFlow.tsx            # General user registration
    ├── HospitalSignUpFlow.tsx    # Hospital registration
    ├── InsuranceSignUpFlow.tsx   # Insurance provider registration  ← NEW
    ├── ResetPassword.tsx         # Password reset
    │
    ├── GeneralApp.tsx            # User dashboard (SOS + Guest + Tabs)
    ├── SOSButton.tsx             # Animated SOS trigger button
    ├── ActiveEmergency.tsx       # Live emergency view (user)
    ├── GuestEmergencyFlow.tsx    # Guest/bystander reporting flow
    │
    ├── TrackingMap.tsx           # Google Maps component
    ├── VideoRecorder.tsx         # MediaRecorder-based video evidence
    ├── AmbulanceCountdown.tsx    # Live ETA countdown timer
    ├── ChatAssistant.tsx         # Gemini AI chat interface
    │
    ├── HospitalDashboard.tsx     # Hospital command center
    ├── InsuranceDashboard.tsx    # Claims feed + deal redirect engine  ← NEW
    └── AdminDashboard.tsx        # Admin vetting panel
```

---

## 👩‍💻 Author

<div align="center">

**Devanshi Vadiya**

Built with ❤️ and zero sleep for hackathon innovation in emergency response systems.

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=120&section=footer" width="100%"/>

*CERS+ — Because every second matters.* 🚑

</div>
