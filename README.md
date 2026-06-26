# JEEArchive - Mock Test Platform

**A full-featured JEE mock test platform with a pixel-accurate NTA exam replica, a custom chapterwise test interface, topic-wise PYQ practice, full-length mocks, and detailed performance analytics with question-level solution breakdowns.**

[jeearchive.com](https://jeearchive.com) · [LinkedIn](https://linkedin.com/in/ayushsinghiiit) · [Contact](mailto:ayushsinghcodes@gmail.com)

---

## Repository Notice

This repository is private to protect proprietary question-bank infrastructure, exam-engine logic, and analytics pipelines. The codebase powers a live mock-test platform with an active beta user base.

**Recruiters and collaborators:** I am happy to grant private repo access or walk you through the codebase on a call. Reach me at [ayushsinghcodes@gmail.com](mailto:ayushsinghcodes@gmail.com).

---

## Demo

<!-- Add Loom video link/embed here -->
**Watch the full walkthrough:** [Loom Video, Mock Test Platform Demo](#)

*A complete walkthrough of the exam interface, chapterwise test flow, PYQ practice modes, and the analytics dashboard.*

---

## Screenshots

### NTA Exam Interface Replica
<!-- Add screenshot -->

### Custom Chapterwise Test Interface
<!-- Add screenshot -->

### Topic-wise and Chapterwise PYQ Practice
<!-- Add screenshot -->

### Question Navigation Panel
<!-- Add screenshot -->

### Test Submission and Answer Review
<!-- Add screenshot -->

### Performance Analytics Dashboard
<!-- Add screenshot -->

### Solution Breakdown View
<!-- Add screenshot -->

### Mobile View
<!-- Add screenshot -->

---

## Overview

JEEArchive Mock Test Platform is a complete practice ecosystem for JEE Main and Advanced aspirants. It includes two distinct testing experiences: a pixel-accurate replica of the NTA exam interface for full exam-day simulation, and a separate, purpose-built chapterwise test interface designed for focused, topic-level practice.

On top of that, the platform supports chapterwise PYQs, topic-wise PYQs, and full-length mock tests, all backed by a question bank of 16,000+ JEE questions. Every test a student takes feeds into a detailed analytics section, and every single question they attempt comes with a full solution breakdown.

**Problem:** JEE aspirants need more than just a mock exam simulator. They need to drill specific chapters, revisit previous year questions by topic, take full-length tests under real exam conditions, and actually understand where and why they're going wrong, all in one place.

**Solution:** A unified platform combining an NTA-accurate exam mode, a dedicated chapterwise practice interface, full PYQ coverage by chapter and topic, full-length mocks, and an analytics layer with per-question solution breakdowns so students know exactly what to fix.

---

## Platform Stats

| Metric | Value |
|---|---|
| Beta Users Onboarded | 1,000+ |
| Question Bank Size | 16,484+ questions |
| REST API Endpoints Consumed | 50+ |
| Subjects Covered | Physics, Chemistry, Mathematics |
| Test Modes | NTA Replica, Chapterwise, Topic-wise PYQ, Chapterwise PYQ, Full-length Mock |
| State Management | Zustand (global test and session state) |
| Launch Status | <!-- Add beta launch date --> |

---

## Features

**NTA Exam Interface Replica**
- Pixel-accurate replication of the NTA exam portal UI, matched in layout, color scheme, and interaction patterns
- Timed paper flow with section-wise and full-paper timers behaving exactly like the live exam
- Question palette with NTA-standard color coding (answered, not answered, marked for review, not visited)
- Built for full exam-day simulation, including time pressure and navigation behavior

**Custom Chapterwise Test Interface**
- A separate, purpose-built interface for chapterwise practice, distinct from the NTA replica
- Designed for focused, distraction-free practice on a single chapter at a time
- Instant access to relevant questions without the overhead of a full exam setup

**PYQ Practice (Chapterwise and Topic-wise)**
- Chapterwise PYQs covering every chapter across Physics, Chemistry, and Mathematics
- Topic-wise PYQs for students who want to drill a specific concept within a chapter
- Full-length mock tests replicating the actual JEE Main and Advanced paper pattern
- Randomized question sets to prevent repetition across attempts

**Review and Submission**
- Dedicated answer review panel before final submission, mirroring the real exam's review screen
- Auto-save of responses to prevent data loss mid-test
- Detailed post-submission breakdown of correct, incorrect, and unattempted answers

**Detailed Analytics Section**
- Chapterwise score visualization across every attempt
- Accuracy trend charts tracked over time per subject
- Weak-area breakdowns to highlight chapters needing more attention
- Per-session performance history so students can track improvement attempt over attempt

**Solution Breakdown**
- Full solution available for every question a user has attempted, across every test mode
- Step-by-step explanation, not just the final answer, so students understand the reasoning
- Helps students immediately review mistakes right after a test instead of searching elsewhere

---

## Tech Stack

| Layer | Technology | Purpose |
|---|---|---|
| Frontend Framework | Next.js | Server-rendered React app, fast page loads, routing |
| Language | TypeScript | Type-safe components and API contracts |
| State Management | Zustand | Lightweight global state for test sessions, submissions, and results sync |
| Styling | Plain CSS | Utility-first styling for pixel-accurate UI replication |
| Data Layer | REST APIs (50+ endpoints) | Question delivery, test session handling, results computation |
| Analytics | Custom charting layer | Chapterwise scores, accuracy trends, weak-area breakdowns |
| Hosting | Cloudflare Worker | <!-- e.g. Vercel --> |

---

## Architecture

```
User Request
     |
     v
Next.js Frontend          <- NTA replica UI, chapterwise UI, PYQ and mock test UI
     |
     v
Zustand State Layer       <- Manages test session, timer, answers, navigation state
     |
     v
REST API Layer (50+)      <- Question delivery, submission handling, results computation
     |
     v
Question Bank              <- 16,484+ questions across Physics, Chemistry, Maths
     |
     v
Analytics and Solutions    <- Chapterwise scores, accuracy trends, weak-area detection, per-question solutions
     |
     v
Performance Dashboard      <- Visual breakdown and solution review returned to the student
```

---

## Key Engineering Highlights

**Two Distinct Testing Interfaces**
The platform maintains two separate test interfaces sharing the same underlying engine: a pixel-accurate NTA replica for full exam simulation, and a custom-built chapterwise interface optimized for focused practice. Both run on the same state management and API layer underneath.

**Complex State Management at Scale**
A single test session involves tracking per-question answer state, marked-for-review flags, visited and not-visited status, section timers, and overall exam timer, all kept in sync across components using Zustand without prop-drilling or unnecessary re-renders.

**API-Driven Test Flow**
Over 50 REST API endpoints handle everything from fetching question sets and saving in-progress answers to computing final scores, generating analytics, and serving solution breakdowns, built to keep the UI responsive even under exam time pressure.

**Question Bank and Solution Architecture**
With 16,484+ questions organized by subject, chapter, topic, and difficulty, the platform supports chapterwise PYQs, topic-wise PYQs, and full-length simulations, with every single question mapped to a full, step-by-step solution.

---

## Team

This project is built by a team of three. I started JEEArchive and lead the project.

**Ayush Singh, Team Lead**
Leads the project and handles the complete frontend of the platform, including the NTA replica interface, the chapterwise test interface, and the analytics dashboard, alongside the two teammates below.

**Tanishq Jain, Backend**
Handles all backend infrastructure, including the API layer, question bank architecture, test session handling, and results computation.

**Utkarsh Singh, User Operations and Growth**
Handles everything user-facing outside the product itself, including conducting sessions, direct user communication, and marketing strategy.

---

## Related Projects

| Project | Description | Link |
|---|---|---|
| JEEArchive Resource Platform | India's largest free JEE resource platform with 800,000+ users | [jeearchive.in](https://jeearchive.in) |
| NEETArchive | Same concept extended for NEET aspirants | [neetarchive.in](https://neetarchive.in) |

---

## About

Built by **Ayush Singh** (Founder and Head, Full-Stack Developer), with **Tanishq Jain** (Backend) and **Utkarsh Singh** (User Operations and Growth).

IIIT Bhagalpur, B.Tech CSE, 2023-2027

[Portfolio](https://ayush.jeearchive.in) · [LinkedIn](https://linkedin.com/in/ayushsinghiiit) · [GitHub](https://github.com/ayushcodes0) · [Email](mailto:ayushsinghcodes@gmail.com)

---

## License

This project is proprietary and not open source. All rights reserved. The source code is not available for public use, reproduction, or distribution.
