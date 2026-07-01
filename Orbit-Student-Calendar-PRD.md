# Product Requirements Document (PRD)
## Project: **Orbit** — The Most Powerful Personal Calendar for School Students

**Author:** Product Team  
**Status:** Draft v1.0  
**Date:** July 1, 2026  
**Inspired by:** Snap Inc. Saturn team mission — *build the most powerful personal calendar, and the most fun way to share calendars with friends*

---

## 1. Executive Summary

School students live in a fragmented scheduling world: class periods, extracurriculars, homework deadlines, social plans, family obligations, and college/application deadlines are spread across paper planners, school portals, group chats, and screenshots. Existing calendars were built for working adults, not for the social, fast-moving, identity-driven lives of students.

**Orbit** is an AI-native, social-first personal calendar designed exclusively for middle and high school students. It unifies academic and personal life into one intelligent schedule, makes sharing availability with friends effortless and fun, and uses AI to eliminate the manual work that makes calendars feel like chores.

**North Star:** Students open Orbit daily—not because they have to, but because it helps them show up on time, protect their time, and make plans with friends in seconds.

---

## 2. Problem Statement

### 2.1 The Student Scheduling Crisis

| Pain Point | Current Behavior | Impact |
|---|---|---|
| **Fragmented schedules** | Bell schedules in PDFs, assignments in LMS, plans in iMessage/Discord | Missed classes, late homework, double-booked social plans |
| **Adult-first calendar UX** | Google/Apple Calendar feels corporate and lonely | Low adoption; students don't treat it as their "source of truth" |
| **Coordination friction** | "When are you free?" loops in group chats | Plans die before they're made |
| **Manual data entry** | Re-typing schedules every semester | Setup drop-off; stale calendars |
| **No context** | Calendar shows *what*, not *why it matters* | Poor prioritization; anxiety |

### 2.2 Why Now

- **AI can finally parse unstructured school data** (syllabi, screenshots, schedule PDFs) into structured events.
- **Gen Z expects social layers on every tool** — calendars should be as shareable as Stories.
- **Snap-scale distribution** proves social calendar demand at millions of users; the opportunity is to expand from niche (high school) to universal student life globally.

---

## 3. Vision & Product Principles

### Vision
> *The calendar students actually want to use—powerful enough to run their academic life, fun enough to plan with friends, and smart enough to feel like magic.*

### Product Principles

1. **Student-first, always.** Every feature must pass: *"Would a 16-year-old choose this over a group chat?"*
2. **Social by default, private by choice.** Sharing should feel like inviting a friend, not configuring ACLs.
3. **AI removes work, not control.** Automate ingestion and suggestions; never surprise-delete or auto-share.
4. **Fast to set up, faster to use.** Zero-to-useful in under 3 minutes.
5. **Delight in the details.** Micro-interactions, stickers, reactions—calendar as self-expression.

---

## 4. Target Users & Personas

### Primary Segment
**US middle & high school students (ages 13–18)**, starting with grades 9–12.

### Personas

| Persona | Name | Needs | Orbit Value |
|---|---|---|---|
| **The Organizer** | Maya, 16, junior | Keeps friend group together; manages club + AP load | Shared availability, group planning, smart reminders |
| **The Overwhelmed** | Jordan, 14, freshman | Bad at deadlines; anxious about missing things | Auto-import schedule, homework view, gentle nudges |
| **The Social Planner** | Alex, 17, senior | Life = friends + sports + college apps | Friend calendar layers, "who's free tonight?" |
| **The Minimalist** | Sam, 15 | Wants simple view, no clutter | Clean day view, one-tap focus blocks |

### Secondary Users (Future)
- College students (semester complexity)
- Parents (read-only visibility into kid's schedule)
- Teachers/clubs (optional broadcast calendars)

---

## 5. Goals & Success Metrics

### Business Goals (12 months)
- **Adoption:** 10M MAU in core demographic (US high school)
- **Retention:** D30 retention ≥ 45%
- **Social density:** ≥ 60% of active users connected to ≥ 5 friends on Orbit
- **Engagement:** ≥ 4 sessions/week per active user

### Product Metrics

| Metric | Definition | Target |
|---|---|---|
| **Time-to-first-value** | Signup → calendar populated with classes | < 3 min (p50) |
| **Schedule completeness** | % users with ≥ 80% of school week mapped | ≥ 70% by D7 |
| **Plan conversion** | "Find time with friends" → event created | ≥ 35% |
| **AI acceptance rate** | Suggested events user keeps | ≥ 75% |
| **Share rate** | Users who share availability weekly | ≥ 50% |

### Guardrail Metrics
- Privacy complaints / unauthorized share reports: < 0.01% of users
- Missed critical reminders (user-reported): declining MoM
- Under-13 signup attempts blocked: 100%

---

## 6. Core User Jobs to Be Done

1. **"Help me know where I need to be today."**
2. **"Don't let me forget homework or tests."**
3. **"Make it easy to hang out with friends without 50 messages."**
4. **"Set up my whole semester without typing everything in."**
5. **"Show my friends I'm busy without oversharing."**

---

## 7. Feature Requirements

### 7.1 MVP (Phase 1) — *Launch & Learn*

#### A. Smart Personal Calendar
| Feature | Description | Priority |
|---|---|---|
| **Day / Week / Agenda views** | Student-optimized layouts; "period" view aligned to block schedules | P0 |
| **Event types** | Class, assignment, exam, practice, social, personal, focus time | P0 |
| **Reminders & nudges** | Configurable; smart defaults ("leave for bus in 8 min") | P0 |
| **Light & Dark Mode** | Dynamic toggle, custom variables, localStorage sync | P0 |
| **Day Themes** | Custom background themes/tints for individual dates in Week view | P1 |
| **Symmetrical Layout & FAB** | Symmetrical 5-tab bottom nav bar (Today, Week, Friends, My AI, Board) with the add action separated to a Floating Action Button in the lower-right | P0 |
| **Focus mode** | Hide social noise during class/study blocks | Muted |

#### B. AI Schedule Ingestion & Assistance
| Feature | Description | Priority |
|---|---|---|
| **School lookup** | Search by name → pre-built bell schedules + holidays | P0 |
| **Photo/PDF import** | Snap syllabus or schedule → parsed events for review | P0 |
| **Natural language add** | "Bio lab every Tuesday 3rd period" → structured event | P0 |
| **My AI Chatbot** | Interactive custom chatbot (renameable) that can query today's schedule, tell user their next class, list free friends, and offer study tips | P0 |
| **Semester rollover** | Clone + adjust schedule for new term | P1 |

**AI UX requirement:** All AI-created events land in a **Review Queue**—never auto-published without confirmation (v1).

#### C. Social Calendar (The Fun Layer)
| Feature | Description | Priority |
|---|---|---|
| **Customizable Bitmoji** | Build SVG avatar with skin tone, hair style, color, expressions, outfits, accessories | P0 |
| **Friend connections** | Add via username, QR, or contact sync (with consent) | P0 |
| **Availability sharing** | Share free/busy blocks; hide event titles by default | P0 |
| **Friend overlay** | See when 2+ friends are free (heatmap / overlap view) | P0 |
| **Plan together** | Propose hangout → friends vote on times → event created | P0 |
| **Reactions & stickers** | React to friends' *shared* public events (game night, concert) | P1 |

**Privacy defaults:**
- Event details **private** unless explicitly marked "friends can see"
- Parents/guardians: no access in MVP unless student invites

#### D. Onboarding
- Age gate (13+) OR **Continue with Snapchat Connect SSO** (skips manual gate, auto-imports friends list)
- Pick school → confirm schedule
- Add 3 friends (optional skip, re-prompt later)
- Connect notifications

---

### 7.2 Phase 2 — *Power Features*

| Feature | Description |
|---|---|
| **Homework hub** | Assignment deadlines synced from photo import + manual entry; "due soon" smart list |
| **Group calendars** | Clubs, teams, study groups with shared events |
| **Study session matcher** | "Find 45 min when me + 3 friends are free before Friday" |
| **Calendar Stories** | Ephemeral "this is my week" share to close friends |
| **Widgets** | Lock screen / home screen "next up" + friend availability |
| **LMS integrations** | Google Classroom, Canvas (where permitted) |

---

### 7.3 Phase 3 — *Scale & Ecosystem*

| Feature | Description |
|---|---|
| **College mode** | Irregular schedules, office hours, registration deadlines |
| **Family view** | Parent read-only; pickup coordination |
| **AI weekly planner** | "Balance SAT prep, soccer, and sleep this week" |
| **School partnerships** | Official schedule feeds, closed-campus modes |
| **Global expansion** | Localization, non-US school systems |

---

## 8. AI Strategy

### AI Use Cases (Prioritized)

1. **My AI Chatbot** — Interactive personal assistant directly in navigation tab (conversational schedule/friend query, custom name, dynamic typing status)
2. **Document understanding** — syllabi, screenshots, emailed schedules
3. **Schedule inference** — bell schedules, rotating days (A/B), early dismissal
4. **Smart reminders** — contextual ("Pack gym clothes—volleyball away today")
5. **Natural language CRUD** — create, move, delete via chat
6. **Conflict resolution** — "You have 3 things at 4pm Thursday—pick one?"
7. **Social coordination** — optimal meeting time across friend graphs


### AI Safety & Trust Requirements
- Transparent labeling of AI-suggested vs. user-created events
- One-tap undo for bulk imports
- No training on private event content without explicit opt-in
- Age-appropriate content filtering on shared/public layers
- Human-readable explanation for every AI suggestion ("Because your syllabus says…")

---

## 9. Social & Privacy Model

### Sharing Tiers

```
┌─────────────────────────────────────────────────────┐
│  PRIVATE (default)     Only you see details         │
├─────────────────────────────────────────────────────┤
│  BUSY ONLY             Friends see blocked time     │
├─────────────────────────────────────────────────────┤
│  FRIENDS SEE DETAILS   Title + time visible         │
├─────────────────────────────────────────────────────┤
│  GROUP / PUBLIC        Club team, optional broadcast│
└─────────────────────────────────────────────────────┘
```

### Requirements
- Granular per-event sharing toggle
- Block list / mute friend overlays
- Report flow for harassment via calendar invites
- COPPA/FERPA-aware data handling; minimal PII collection
- Export & delete account (GDPR-style portability)

---

## 10. Key User Flows

### Flow 1: First Week Setup (< 3 min)
```
Download → Age verify → Pick school → Confirm periods → 
Import syllabus photo → Review 12 events → Add friends → Done
```

### Flow 2: Plan After School
```
Tap "Hang out" → Select friends → Orbit shows overlap slots → 
Vote → Winner becomes calendar event → Push to group
```

### Flow 3: Morning Glance
```
Open app / widget → "Next: Chemistry (Room 204) in 12 min" → 
Tap for homework due today → Share "free after 3" to close friends
```

---

## 11. Non-Functional Requirements

| Category | Requirement |
|---|---|
| **Performance** | Cold start < 2s; calendar render < 500ms |
| **Offline** | Read schedule offline; queue writes |
| **Reliability** | 99.9% uptime for core calendar API |
| **Notifications** | Deliver within 60s of trigger; quiet hours respected |
| **Accessibility** | WCAG 2.1 AA; Dynamic Type; screen reader labels |
| **Platforms** | iOS + Android native (MVP); web read-only (Phase 2) |

---

## 12. Competitive Landscape

| Product | Strength | Gap for Students |
|---|---|---|
| Google Calendar | Ubiquitous, reliable | Not social; bad school setup |
| Apple Calendar | Native, simple | No friend layer; no AI import |
| Notion / planners | Flexible | Too much work; not real-time social |
| Saturn (Snap) | School-native, social | Proven model; opportunity to expand feature depth & AI |
| Group chats | Zero friction | No structured time; plans get lost |

**Differentiation:** Orbit wins on *setup speed* (AI), *daily utility* (student-specific views), and *social coordination* (fun, not spreadsheet).

---

## 13. Monetization (Future — Not MVP)

- **Free core** for all students (network effects depend on this)
- Optional **Orbit+**: advanced AI planner, custom themes, college prep modules
- **No ads in calendar views** (trust killer for minors)
- B2B2S: school/district partnerships for official integrations

---

## 14. Risks & Mitigations

| Risk | Mitigation |
|---|---|
| Low friend adoption (empty social graph) | School-based discovery; invite incentives; useful solo calendar first |
| AI import errors → lost trust | Review queue; confidence scores; easy bulk edit |
| Privacy incident | Private-by-default; security audits; teen safety team |
| Seasonal churn (summer) | Summer mode: jobs, camps, trips, college prep |
| School schedule changes | Push notifications + one-tap "accept schedule update" |
| Regulatory (minors) | Age gates, parental controls roadmap, legal review |

---

## 15. Release Roadmap

### Q3 2026 — Alpha
- School lookup (top 500 US high schools)
- Personal calendar + AI photo import
- Friend connections + availability overlay
- iOS only, 3 pilot cities

### Q4 2026 — Beta Launch
- Android parity
- Plan together flow
- Widgets + push reminders
- Expand to 5,000 schools

### Q1 2027 — GA
- Homework hub
- Group calendars
- Study session matcher
- National US launch + metrics review

### Q2 2027+
- College mode, LMS integrations, international

---

## 16. Open Questions

1. **Authentication:** Snap SSO vs. standalone vs. both?
2. **Moderation:** How to handle inappropriate event titles in shared layers?
3. **School data licensing:** Build crowdsourced DB vs. partner with schedulers?
4. **Teacher/club publishing:** Do we need approval workflows at launch?
5. **Name:** Orbit placeholder — brand fit with Snap portfolio TBD.

---

## 17. Appendix: Sample User Stories

| ID | Story | Acceptance Criteria |
|---|---|---|
| US-01 | As a new student, I want to import my schedule from a photo so I don't type 40 classes manually | ≥ 90% of period blocks correctly parsed; user confirms before save |
| US-02 | As a student, I want to see when my 3 closest friends are free after school | Overlap view shows mutual free windows today + tomorrow |
| US-03 | As a student, I want homework deadlines separate from class times | Agenda view has "Due Today" section |
| US-04 | As a privacy-conscious user, I want friends to see I'm busy without seeing "therapy" | Busy-only mode hides title |
| US-05 | As a club president, I want to publish practice times to members | Group calendar push; members opt-in |

---

## 18. Summary

Orbit reimagines the calendar for the 50M+ US secondary students who deserve a tool built for *their* life—not their parents' workday. By combining **AI-powered setup**, a **student-native daily experience**, and **Snap-inspired social sharing**, we can solve a decades-old problem with a product students choose, friends amplify, and families trust.

**The bet:** Make the calendar powerful enough to be indispensable alone, and fun enough with friends that it spreads through schools the way the best social products always have—one hallway at a time.
