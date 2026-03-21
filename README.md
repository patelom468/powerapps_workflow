# WorkFlow Automator — Power Apps Case Study

> A Microsoft Power Apps low-code solution that replaced a paper-based internal approval process with a fully digital, automated workflow — cutting processing time by 80% and eliminating manual data entry errors.

---

## 📋 Overview

This project is a single-page case study website (`workflow-automator-case-study.html`) documenting the design, development, and outcomes of a Microsoft Power Platform workflow automation solution. Built as part of Om Patel's portfolio, it showcases the full project lifecycle — from problem discovery to measured results.

---

## 🚀 Key Results

| Metric | Result |
|--------|--------|
| Processing Time Saved | **80%** per approval cycle |
| Paper Forms Eliminated | **Zero** — fully digital |
| Workflow Steps Automated | **3 core steps** |
| Audit Trail Coverage | **100%** — every action logged |

---

## 🛠 Tech Stack

### Application (Power Platform)
- **Microsoft Power Apps** — Canvas app for the submission form and approval queue (responsive, desktop + mobile)
- **Power Automate** — Two cloud flows: submission trigger → approver email; status change trigger → requester notification with conditional approve/reject branching
- **SharePoint** — Data layer with two lists (active requests + archive); column-level permissions for role-based access
- **Outlook / Office 365** — HTML-formatted email notifications via Power Automate's built-in connector
- **Azure AD / Microsoft 365** — Authentication and user identity; no separate login system required

### Case Study Website
- **HTML5 / CSS3 / Vanilla JavaScript** — No frameworks, no build tools
- **Google Fonts** — Syne (display), DM Sans (body), DM Mono (mono accents)
- **IntersectionObserver API** — Scroll-triggered reveal animations
- **Custom cursor system** — Dot + ring with LERP-based trailing, hover/text/click states

---

## 📁 Project Structure

```
/
├── workflow-automator-case-study.html   # Main case study page (self-contained)
└── README.md
```

The case study is intentionally a **single self-contained file** — all CSS and JavaScript are inlined, with no external dependencies beyond Google Fonts.

---

## ✨ Features

### Case Study Content
- **Problem & Solution breakdown** — side-by-side comparison of the old paper process vs. the digital workflow
- **5-step workflow walkthrough** — Request Submission → Automated Notification → Approver Review → Decision Notification → Archive & Reporting
- **App screen mockups** — Submission form and Approval Queue, built with pure HTML/CSS
- **Tech stack cards** — Each tool with its specific role in the architecture
- **Outcomes grid** — Six measured improvements with quantified values
- **Reflections / Learnings** — Five key takeaways from building the solution

### UI / UX
- Dark theme with CSS custom properties (`--bg`, `--accent`, `--accent2`, etc.)
- Fluid typography with `clamp()` for responsive scaling
- Custom animated cursor with five states:
  - **Default** — dot + trailing ring
  - **Hover** (`c-hover`) — ring expands and turns teal over interactive elements
  - **Text** (`c-text`) — ring collapses to a vertical bar over readable content
  - **Click** (`c-click`) — dot pulses larger on mousedown
  - **Hidden** — automatically disabled on touch/mobile devices
- Fixed nav with scroll-shrink behaviour
- Gradient metric values and section headings

---

## 🔧 How the Workflow Works

```
Staff Member → [Power Apps Form] → SharePoint List (Pending)
                                         ↓
                              [Power Automate Flow 1]
                                         ↓
                              Approver Email Notification
                                         ↓
                              [Approver reviews in app]
                                         ↓
                         Approve / Reject / Flag for Follow-up
                                         ↓
                              [Power Automate Flow 2]
                                         ↓
                        Requester Notified of Outcome + Notes
                                         ↓
                       [Auto-archive to SharePoint Archive List]
                                         ↓
                         Live Dashboard — Pending / Approved / Rejected
```

---

## 🖥 Running Locally

No build step required — open the HTML file directly in any modern browser:

```bash
# Option 1: Open directly
open workflow-automator-case-study.html

# Option 2: Serve locally (avoids any CORS quirks with fonts)
npx serve .
# or
python -m http.server 8080
```

---

## 🔗 Links

- **Portfolio** — [patelom468.github.io/portfolio](https://patelom468.github.io/portfolio/)
- **GitHub Repo** — [github.com/patelom468/powerapps-workflow](https://github.com/patelom468/powerapps-workflow)
- **Contact** — [patelom468.github.io/portfolio/#contact](https://patelom468.github.io/portfolio/#contact)

---

## 📄 License

© 2026 Om Patel. Built with HTML, CSS & JavaScript.
