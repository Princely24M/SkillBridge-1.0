# SkillBridge — Youth Opportunity & Skills Platform

> **Primary Tagline:** Connecting Youth to Opportunities That Move Them Forward.  
> **Supporting Tagline:** Find opportunities. Build skills. Bridge your future.

SkillBridge is a modern, mobile-first web platform designed to help young South Africans discover jobs, internships, learnerships, bursaries, courses, and skills programmes in one accessible, trustworthy location.

Built strictly using **HTML5, CSS3, Vanilla JavaScript (ES6+), and JSON**, this project demonstrates strong core frontend engineering fundamentals without reliance on external CSS or JavaScript frameworks.

---

## Table of Contents

1. [Introduction](#1-introduction)
2. [Problem Statement](#2-problem-statement)
3. [Project Goal](#3-project-goal)
4. [Target Users](#4-target-users)
5. [Proposed Solution](#5-proposed-solution)
6. [Key Features](#6-key-features)
7. [Technology Stack](#7-technology-stack)
8. [Project Structure](#8-project-structure)
9. [JSON Dataset Explanation](#9-json-dataset-explanation)
10. [Accessibility Features (WCAG 2.1)](#10-accessibility-features-wcag-21)
11. [Responsive Design Implementation](#11-responsive-design-implementation)
12. [How to Run Locally](#12-how-to-run-locally)
13. [Git & GitHub Version Control Instructions](#13-git--github-version-control-instructions)
14. [Deployment Instructions](#14-deployment-instructions)
15. [Testing & Quality Assurance](#15-testing--quality-assurance)
16. [Known Limitations](#16-known-limitations)
17. [Future Improvements](#17-future-improvements)

---

## 1. Introduction

Youth unemployment and fragmented access to entry-level career pathways represent one of South Africa's most urgent developmental challenges. Many talented matriculants, TVET graduates, and university leavers struggle to identify legitimate development pathways, understand application criteria, or protect themselves from predatory recruitment syndicates.

**SkillBridge** addresses this barrier by providing a clean, accessible, and transparent bridge between youth talent and verified opportunities.

---

## 2. Problem Statement

Young job seekers and learners face four recurring obstacles:
1. **Information Fragmentation:** Opportunities (bursaries, internships, learnerships, and jobs) are scattered across dozens of individual company websites, SETA notices, social media groups, and PDFs.
2. **Deceptive & Predatory Recruitment:** Unemployed youth are frequently targeted by syndicates demanding upfront "application fees," medical exam charges, or banking credentials.
3. **Unclear Requirements:** Job seekers often apply for roles without knowing what specific documents are required or how to certify their credentials.
4. **Poor Mobile Usability:** Many corporate application portals are built exclusively for desktop computers, alienating youth who access the internet primarily via mobile smartphones.

---

## 3. Project Goal

To build a high-performance, mobile-first, standards-compliant web application that allows a first-time user to:
* Instantly understand the platform’s purpose.
* Search and multi-filter opportunities based on keywords, category, location, experience level, and closing date.
* Inspect complete opportunity requirements, eligibility lists, and document checklists.
* Learn practical job application skills (CV building, STAR interview technique, certification).
* Report suspicious or outdated listings.
* Enjoy a seamless, accessible experience across mobile devices, tablets, and desktops.

---

## 4. Target Users

* **School Leavers & Matriculants:** Seeking bursaries, entry-level learnerships, and funded skills programmes.
* **TVET College & University Students:** Looking for vacation work, experiential learning, and graduate internships.
* **Unemployed Youth (Ages 18–35):** Searching for entry-level employment, vocational skills, and career transition pathways.
* **Community Career Mentors & Educators:** Assisting young people in identifying verified, safe opportunities.

---

## 5. Proposed Solution

SkillBridge provides a centralized, human-centered web application built around four pillars:
* **Discover:** Six distinct categories (Jobs, Internships, Learnerships, Bursaries, Courses, Skills Programmes) accessible through dynamic multi-criteria search.
* **Compare:** Side-by-side comparison of locations, experience tiers, closing dates, and stipends.
* **Prepare:** An integrated Career Resources hub covering CV writing, cover letters, STAR interview prep, certified document preparation, and scam defense.
* **Stay Safe:** Prominent recruitment scam awareness warnings, official domain verification guidelines, and a direct reporting workflow.

---

## 6. Key Features

### 6.1 Dynamic Opportunities Directory
* **Multi-Criteria Filtering:** Simultaneous filtering by Keyword, Category, Location, Experience Level, and Closing Date.
* **Closing Soon Calculation:** Automatically calculates remaining days until the deadline; flags opportunities closing within 7 days with a highlighted badge.
* **Automatic Expiration Handling:** Identifies closed opportunities based on deadline; removes expired listings from active views while offering a transparent review toggle.
* **Reactive Search:** Real-time, debounced keyword matching across title, organisation, description, and location.

### 6.2 Rich Opportunity Details View (`opportunity-details.html?id=...`)
* **Interactive Document Checklist:** Users can check off required documents (ID, CV, Matric Certificate) directly on page.
* **Demonstration Safety Modal:** Safe application button clearly labeled `Demo Application` that reinforces verification on official corporate portals without misleading links.
* **Deep Metadata:** Includes remuneration/stipend information, work mode (Hybrid, On-site, Remote), last updated date, and eligibility bullets.

### 6.3 Bookmarking & Local Storage Persistence
* Users can bookmark/save opportunities for later review across browser sessions.
* Tracks recently viewed opportunities in `localStorage`.

### 6.4 Career Resources & STAR Method Toolkit (`resources.html`)
* Comprehensive guides for CV structure, professional profiles (LinkedIn/GitHub), cover letters, document certification standards (3-month validity rule).
* Interactive STAR behavioral question framework (Situation, Task, Action, Result).
* Detailed recruitment scam warning signs.

### 6.5 Interactive Multi-Tab Contact & Report Center (`contact.html`)
* **General Enquiry Form:** For community queries.
* **Report an Opportunity Form:** Pre-fills opportunity titles from details page; categorizes report reasons (Expired, Suspicious, Incorrect info, Bad link).
* **Suggest an Opportunity Form:** Community submission for legitimate opportunities.
* **Accessible Validation:** Visual indicators (`is-invalid`), ARIA attributes (`aria-invalid`), descriptive error messages, and success notifications.

### 6.6 Theme Switching (Light & Dark Mode)
* Clean dark mode palette with automated contrast adjustment and persistence in `localStorage`.

---

## 7. Technology Stack

This application is strictly built with vanilla web technologies to highlight core competencies:

* **HTML5:** Semantic architecture (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`), ARIA attributes.
* **CSS3:** Custom properties (CSS variables), Flexbox, CSS Grid, media queries, subtle micro-interactions, responsive typography.
* **Vanilla JavaScript (ES6+):** Async/await `fetch`, DOM manipulation, query string parsing (`URLSearchParams`), `localStorage`, array filters, event delegation.
* **JSON:** Structured data source representing demonstration opportunities.
* **Vector Graphics (SVG):** Custom-designed vector logo, favicon, and hero pathway illustration.

> **Zero External Frameworks:** No React, Vue, Angular, Bootstrap, or Tailwind CSS were utilized.

---

## 8. Project Structure

```text
SkillBridge/
│
├── index.html                   # Home page with hero, categories, featured & deadlines
├── opportunities.html           # Directory with live keyword search and multi-filters
├── opportunity-details.html     # Dynamic detail view with interactive checklist
├── resources.html               # Career preparation guides & scam awareness toolkit
├── contact.html                 # Contact, Report Opportunity, and Suggest forms
│
├── css/
│   └── style.css                # Master mobile-first design system and theme styles
│
├── js/
│   └── script.js                # Shared vanilla JavaScript application logic
│
├── data/
│   └── opportunities.json       # JSON dataset containing 18 demonstration opportunities
│
├── images/
│   ├── logo.svg                 # SkillBridge brand logo (Bridge & Pathway motif)
│   ├── favicon.svg              # Brand browser favicon
│   └── hero-pathway.svg         # Bespoke career milestone pathway illustration
│
└── README.md                    # Comprehensive project documentation
```

---

## 9. JSON Dataset Explanation

The dataset located at `data/opportunities.json` includes **18 diverse demonstration opportunities** covering South African economic hubs: Cape Town, Johannesburg, Pretoria, Durban, Gqeberha, Polokwane, and Bloemfontein.

### Data Schema

```json
{
  "id": 1,
  "title": "Junior Frontend Web Developer",
  "organisation": "Apex Digital Innovations (Demo)",
  "category": "Job",
  "location": "Cape Town",
  "closingDate": "2026-10-10",
  "experienceLevel": "Junior",
  "description": "Short summary displayed on opportunity cards...",
  "fullDescription": "Full comprehensive opportunity description...",
  "eligibility": [
    "South African citizen or permanent resident",
    "Completed relevant diploma, degree, or accredited coding bootcamp"
  ],
  "qualifications": [
    "National Senior Certificate (Matric)",
    "Diploma or Degree in Information Technology"
  ],
  "documents": [
    "Updated Curriculum Vitae (CV)",
    "Certified copy of South African ID",
    "Certified copy of Matric certificate"
  ],
  "applicationInstructions": "Review the full requirements and submit via our demonstration portal...",
  "applicationLink": "#demo-application",
  "organisationDescription": "Apex Digital Innovations is a simulated technology services firm...",
  "lastUpdated": "2026-09-28",
  "isSample": true,
  "stipendOrSalary": "R18,000 - R22,000 / month",
  "workType": "Hybrid (2 days on-site)",
  "featured": true
}
```

* All records explicitly contain `"isSample": true`.
* Closing dates cover closing-soon milestones (October 2026), future deadlines (November/December 2026), and historical expired listings (September 2026) for validation of expiration logic.

---

## 10. Accessibility Features (WCAG 2.1)

* **Skip Navigation Link:** `<a href="#main-content" class="skip-link">Skip to main content</a>` allows keyboard users to bypass top navigation.
* **Keyboard Navigable:** All interactive controls (buttons, links, search inputs, modal close) are accessible via `Tab` and `Enter`/`Space`.
* **Visible Focus Indicators:** Customized `:focus-visible` outline rings with strong color contrast.
* **Screen Reader Optimization:** Semantic headings (`<h1>` through `<h4>`), ARIA attributes (`aria-expanded`, `aria-controls`, `aria-label`, `aria-live="polite"`).
* **High Contrast Ratios:** Deep navy text on off-white backgrounds (exceeding WCAG AAA contrast ratio > 7:1).
* **Non-Color Reliance:** Badges use icons and descriptive text (e.g. `⏰ Closing Soon (4 days left)`) rather than relying purely on color.

---

## 11. Responsive Design Implementation

The site uses a strict **mobile-first** CSS architecture tested across multiple viewports:

| Breakpoint | Target Devices | Design Adjustments |
|---|---|---|
| **320px – 375px** | Small Smartphones (e.g., iPhone SE) | Single column layout, touch targets >= 44px, full-width buttons. |
| **768px** | Tablets & Foldables (e.g., iPad) | Two-column grid layouts for opportunity cards and features. |
| **1024px** | Small Laptops & Desktops | Full horizontal navigation bar, multi-column search filter bar. |
| **1440px+** | Large Desktop Monitors | Max container constrained to 1200px with centered breathing room. |

* No horizontal scrollbars.
* Flexible SVG graphics that scale crisply at any pixel density.

---

## 12. How to Run Locally

Because SkillBridge fetches its opportunity dataset via the standard browser `fetch()` API (`data/opportunities.json`), it should be served through a local HTTP server rather than opening `file:///` directly (to prevent browser CORS file restrictions).

### Option 1: Python Built-In HTTP Server (Recommended)
Open your terminal in the project root directory and run:

```bash
# Python 3
python -m http.server 8000
```
Then navigate to: `http://localhost:8000`

### Option 2: Node.js `npx serve`
```bash
npx serve .
```

### Option 3: VS Code Live Server
1. Install the "Live Server" extension in VS Code.
2. Right-click `index.html` and select **"Open with Live Server"**.

---

## 13. Git & GitHub Version Control Instructions

To initialize and push this project to your GitHub repository:

```bash
# 1. Initialize git repository
git init

# 2. Add all project files
git add .

# 3. Create initial commit
git commit -m "feat: complete modern SkillBridge youth opportunity platform"

# 4. Rename main branch
git branch -M main

# 5. Connect your remote GitHub repository
git remote add origin https://github.com/<your-username>/SkillBridge.git

# 6. Push code to GitHub
git push -u origin main
```

---

## 14. Deployment Instructions

SkillBridge contains zero server dependencies or build steps, making it instantly deployable on static hosting providers:

### 14.1 Deploying to GitHub Pages
1. Push your repository to GitHub.
2. Go to repository **Settings** > **Pages**.
3. Under **Branch**, select `main` and `/ (root)`.
4. Click **Save**. Your site will be published at `https://<username>.github.io/SkillBridge/`.

### 14.2 Deploying to Netlify
1. Log in to [Netlify](https://www.netlify.com).
2. Click **Add new site** > **Import an existing project**.
3. Select your GitHub repository.
4. Leave build command blank and publish directory as `.`.
5. Click **Deploy Site**.

### 14.3 Deploying to Vercel
1. Log in to [Vercel](https://vercel.com).
2. Click **Add New Project** and select your repository.
3. Keep Framework Preset as **Other**.
4. Click **Deploy**.

---

## 15. Testing & Quality Assurance

The application underwent rigorous manual and automated test suites:

* **Navigation Verification:**
  - All navigation links route correctly across all 5 pages.
  - Mobile hamburger drawer opens, closes, traps focus, and closes on `Esc`.
  - Skip to main content link works with keyboard `Tab` navigation.
* **Search Functionality:**
  - Case-insensitive multi-field search across title, organisation, location, and description.
  - Debounced input prevents excessive re-renders.
* **Filter Functionality:**
  - Category, Location, Experience Level, and Closing Date filters operate simultaneously.
  - "Clear Filters" button resets all inputs and updates the URL and DOM dynamically.
* **Opportunity Details:**
  - URL parameter `?id=X` correctly renders the matching opportunity.
  - Fallback error state displayed if an invalid ID is provided.
  - Interactive document checklist allows users to toggle required items.
  - Demo application modal opens with clear educational notice.
* **Form Validation:**
  - Email format validation using regex.
  - Required fields highlight with `.is-invalid` and announce errors via ARIA.
  - Success banner rendered on completion with form reset.
* **Expired & Closing-Soon Logic:**
  - Opportunities closing within 7 days display warm amber badge and countdown label.
  - Expired opportunities are excluded from active listings and upcoming deadlines.

---

## 16. Known Limitations

* **Client-Side Simulation:** Data is loaded from a static `opportunities.json` rather than a live relational database with real-time employer APIs.
* **Local Storage Scope:** Bookmarked opportunities are stored within the specific browser's `localStorage` and do not sync across different physical devices.
* **Demonstration Submissions:** The contact and report forms simulate server processing and display client-side validation confirmations rather than sending backend emails.

---

## 17. Future Improvements

* **Email Notification Alerts:** Allow youth to subscribe to email alerts for specific categories or cities.
* **Offline PWA Support:** Add a service worker and web manifest to enable full offline access in low-bandwidth areas.
* **CV Builder Tool:** An interactive browser tool allowing youth to fill in their details and generate a downloadable PDF CV.
* **Multi-language Support:** Add interface translations in isiZulu, Sesotho, and Afrikaans to expand accessibility across South Africa.

---

## License & Credits

* **Project:** SkillBridge (Academic Frontend Demonstration)
* **Author:** Princely Makhwara
* **Year:** 2026
* **Disclaimer:** This website is an educational demonstration project. Opportunities displayed are sample demonstration records. Always verify vacancies through the official company or institution domains.
