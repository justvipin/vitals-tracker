# Vitals Tracker 🩺

[![Version](https://img.shields.io/badge/version-v6.3-purple.svg)](./vitals_tracker_light_pwa.html)
[![Platform](https://img.shields.io/badge/platform-PWA%20%7C%20Web-blue.svg)](./index.html)
[![Privacy](https://img.shields.io/badge/privacy-100%25%20Offline%20First-success.svg)](./GEMINI.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

**Vitals Tracker** is a private, offline-first personal health vitals monitoring application designed to record, analyze, and visualize daily cardiovascular, metabolic, and physical metrics.

🌐 **Live GitHub Pages Web App:** [https://justvipin.github.io/vitals-tracker/](https://justvipin.github.io/vitals-tracker/)

---

## 🌟 Key Features

* **Zero Cloud Leakage (100% Offline-First):** All health records remain strictly on your local device (`IndexedDB` & `localStorage`). No mandatory cloud accounts, no remote backends, and zero telemetry.
* **Profile-First Gated Entry:** Initial launch always presents profile selection. A prominent "Log Out / Switch Profile" button enables seamless multi-profile tracking for families and caregivers.
* **Dynamic Vital Metric Tiles (Recency-Sorted):**
  * Health-styled 2-column cards for all 8 enterable metrics: **Weight**, **BP (Systolic)**, **BP (Diastolic)**, **Resting Heart Rate**, **Blood Glucose**, **Oxygen Saturation (SpO2)**, **Body Temperature**, and **Waist Circumference**.
  * Each card displays the latest value, unit, clinical trend arrow (`↑`/`↓`/`→`), 7-day trend average + delta, and 30-day baseline.
  * **Dynamic Recency Sorting:** Whichever metric was recorded most recently automatically surfaces at the top of the grid.
* **Dedicated Medications Tab (`💊`):**
  * Full prescription cards displaying dosage badges, schedule frequency, and instruction notes.
  * **1-Hour Pre-Dose Window:** Status displays `✔ Take now — HH:MM` within 1 hour of dose time or overdue, and `Upcoming — HH:MM` otherwise.
  * **Adherence & Streaks:** Dual progress bars tracking **7-day** and **30-day Adherence %**, plus a consecutive day streak counter (`🔥 X day streak`).
  * **Rapid Intake Actions:** One-tap `✓ Taken` and `⏭ Skipped` actions with instant `↺ Undo` support.
* **Dashboard Reading Trends & Graphs:**
  * Interactive timeline charts for Weight, Blood Pressure, Resting Pulse, and Blood Glucose placed directly below the vital metric cards.
  * Time-range filters across **7d**, **30d**, **90d**, and **All**.
* **Clinical Hypertension Telemetry:**
  * Standardized AHA/ACC 2017 Blood Pressure categorization.
  * Segregated AM (Trough) vs. PM (Peak) analysis and automated **Morning Surge Differential (≥ 20 mmHg)** alerts.
* **Context-Sensitive Logging Drawer:**
  * Clean quick-entry picker for **Measurements**, **Medications**, and **Mood & Wellbeing** (5-point score, energy states, and context tags).
  * Medication timing context (`medTiming`) is strictly filtered only to Blood Pressure and Blood Glucose to keep forms minimal.
* **Physician Consultation Report:**
  * Formatted clinical report ready for high-contrast A4 / US Letter paper printing and PDF export with patient telemetry and AHA distribution summaries.
* **Data Portability:**
  * Universal JSON backup & restore utility and one-click CSV export for Excel and health records.

---

## 🚀 Running the App

### Option A: Online via GitHub Pages
Open [https://justvipin.github.io/vitals-tracker/](https://justvipin.github.io/vitals-tracker/) in any desktop or mobile browser. To install as a Progressive Web App (PWA), tap **Add to Home Screen** or click the install icon in your browser's address bar.

### Option B: Local Offline File
Clone or download this repository and double-click `index.html` (or `vitals_tracker_light_pwa.html`) in Google Chrome, Microsoft Edge, Safari, or Firefox. No Node.js, build step, or web server required.

---

## 🙏 Acknowledgements

UI layout patterns and tracking workflows were inspired by the thoughtful UX design of the **HealthLog** personal health tracking application. All code, database schemas, and calculation engines in this repository were independently authored and built from the ground up for a 100% offline-first web experience.

---

## 📄 License & Disclaimer

This project is licensed under the **MIT License** — see the [LICENSE](./LICENSE) file for details.

> **Medical Disclaimer:** This application is for personal tracking and informational review only. It is not a substitute for professional medical advice, diagnosis, or treatment. Always consult with a qualified healthcare provider for clinical interpretation and management of vital signs and medication regimens.
