# Orbit — Personal Student Calendar

Orbit is an AI-native, social-first personal calendar designed exclusively for middle and high school students. It unifies academic timetables and personal commitments into one elegant, real-time schedule interface, and facilitates seamless hangout planning with friends.

This repository contains the interactive prototype, the full product requirements documentation, and executive briefing notes.

---

## 🚀 Interactive App Demo
*   **App File:** [`index.html`](index.html)
*   **How to run:** 
    *   Simply double-click [`index.html`](index.html) to open it locally in your web browser.
    *   No installation, servers, or external build steps required.

---

## 📦 Key Highlights & Snapchat Integrations
1.  **Snapchat Connect SSO:** A simulated onboarding option that bypasses traditional signup screens, verifies age limits, and imports your friends list instantly.
2.  **Dynamic Bitmoji Profiles:** Custom SVG rendering engine that generates and modifies vector Bitmoji avatars in real-time based on hair, skin, outfit, and accessory options.
3.  **My AI Chat Companion:** A customizable chatbot (🤖 tab) that is integrated directly with the calendar storage. Ask My AI about your schedule today, upcoming periods, free friends, or study tips!
4.  **Individual Day Themes:** Select from Sunset, Ocean, Forest, Midnight, Rose, and Gold color themes to tint individual days of the week view.
5.  **Saturn Countdown Mechanics:** Includes a real-time period progress tracker and percentage counts showing how much of the school day remains.

---

## 📄 Documentation
*   **Product Requirements Document (PRD):** [`Orbit-Student-Calendar-PRD.md`](Orbit-Student-Calendar-PRD.md)
*   **PRD Word Export:** [`Orbit-Student-Calendar-PRD.docx`](Orbit-Student-Calendar-PRD.docx)
*   **CEO Strategy Briefing:** [`Orbit-CEO-Presentation-Brief.docx`](Orbit-CEO-Presentation-Brief.docx)

---

## 🛠️ Technology Stack
*   **Core:** HTML5, CSS Variables, ES6 JavaScript.
*   **Rendering:** XML inline SVGs (no external asset dependencies).
*   **State Machine:** React-free client state machine backed by `localStorage` persistence.
