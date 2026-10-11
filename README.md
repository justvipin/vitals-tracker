# Vitals Tracker 🩺

[![Version](https://img.shields.io/badge/version-v6.2-purple.svg)](./vitals_tracker_light_pwa.html)
[![Platform](https://img.shields.io/badge/platform-PWA%20%7C%20Web-blue.svg)](./index.html)
[![Privacy](https://img.shields.io/badge/privacy-100%25%20Offline%20First-success.svg)](./GEMINI.md)

**Vitals Tracker** is a private, offline-first personal health vitals monitoring application designed to record, analyze, and visualize daily cardiovascular, metabolic, and physical metrics.

🌐 **Live GitHub Pages Web App:** [https://justvipin.github.io/vitals-tracker/](https://justvipin.github.io/vitals-tracker/)

---

## 🌟 Key Features

* **Zero Cloud Leakage (100% Offline-First):** All patient data remains strictly in your local browser storage (`IndexedDB` & `localStorage`). No mandatory logins, no tracking, and no external backends.
* **Profile-First Gated Entry:** Initial launch always greets users with profile selection. Seamless "Log Out / Switch Profile" enables private tracking for entire families and caregivers.
* **Context-Sensitive Tracking (7 Vitals):**
  * **Cardiovascular:** Blood Pressure (Systolic & Diastolic) and Pulse.
  * **Metabolic:** Blood Glucose (Fasting, Post-Prandial, Random, Bedtime).
  * **Anthropometric:** Weight, Waist Circumference (with BMI & Waist-to-Height calculations).
  * **Respiratory & Thermal:** Blood Oxygen (SpO2) and Body Temperature.
  * *Note: Medication timing context (`medTiming`) is strictly presented only for Blood Pressure and Glucose readings to eliminate clutter.*
* **Intelligent Medication & Intake Tracking:**
  * **1-Hour Pre-Dose Appearance Window:** Doses only appear 1 hour before scheduled intake (or when overdue), keeping the dashboard calm and distraction-free.
  * **One-Tap Dismissal:** Marking a dose as `Taken` or `Skipped` immediately clears it from the active pending list with real-time adherence scoring and full undo support.
* **Clinical Hypertension & AM/PM Analysis:**
  * Standardized AHA/ACC 2017 Blood Pressure staging.
  * Segregated AM (Trough) vs. PM (Peak) analysis and automatic **Morning Surge Differential (≥ 20 mmHg)** alerts.
* **Modern Physician Consultation Report:**
  * Clinical summary sheet formatted for high-contrast A4 / US Letter printing and PDF export.
* **Data Portability & Backup:**
  * Universal JSON backup & restore utilities and CSV export for spreadsheets.

---

## 🚀 Running the App

### Option A: Online via GitHub Pages
Open [https://justvipin.github.io/vitals-tracker/](https://justvipin.github.io/vitals-tracker/) in any modern desktop or mobile browser. To install as a PWA, tap **Add to Home Screen** or click the install icon in your browser's address bar.

### Option B: Local Offline File
Download or clone the repository and open `index.html` (or `vitals_tracker_light_pwa.html`) directly in Google Chrome, Microsoft Edge, Safari, or Mozilla Firefox. No Node.js or local web server required.

---

## 🛡️ Multi-Tier Rollback Guarantee

Every release follows a strict rollback and versioning protocol:
1. **Pre-Release Snapshots:** Archived under `archive/v<version>/` before every update.
2. **Git Version Tags:** Every release is tagged (e.g. `v5.1`, `v6.0`, `v6.1`, `v6.2`). To roll back locally:
   ```bash
   git checkout tags/v6.1 -- index.html vitals_tracker_light_pwa.html
   ```
3. **Additive IndexedDB Migrations:** Database schemas are strictly non-destructive and backward-compatible.
4. **Data Backups:** Full JSON exports can be restored seamlessly at any time.

---

## 📄 License & Disclaimer

*This application is for personal tracking and informational purposes only. It is not a substitute for professional medical advice, diagnosis, or treatment.*
