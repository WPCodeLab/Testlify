# Testlify — QA Visual Tester

A zero-dependency, browser-based QA testing tool for manually verifying websites before release. Works entirely offline using `localStorage` — no server, no install, no accounts.

---

## Overview

Testlify gives QA testers and developers a structured checklist-driven workflow to test any website. You create a test session, step through every check, mark pass/fail, log bugs, write notes, and generate a shareable PDF report — all from a single HTML file.

---

## Features

- **Two test types** — choose the right checklist for your task:
  - **Visual Testing** (30 steps) — Layout, typography, images, forms, interactivity, responsiveness, performance, SEO
  - **Form Testing** (31 steps) — Field validation, input behavior, submit flow, edge cases, accessibility
- **Session management** — create, switch between, and resume multiple test sessions; all stored in browser `localStorage`
- **Pass / Fail / Pending** tracking — mark each step individually; a progress bar shows overall completion
- **Bug logger** — log multiple bugs per step; mark each as resolved when fixed
- **Tester notes** — attach free-text notes to any step
- **Live stats dashboard** — total, passed, failed, pending, and open bug counts update in real time
- **Final verdict** — automatic accept/reject decision shown when all steps are completed
- **QA Report** (`report.html`) — full HTML report with:
  - Letter grade (A–F) with colored glow
  - Pass rate, metrics grid, category progress bars
  - Full step results table with alternating rows
  - Bug report with open/resolved breakdown
  - Tester notes section
  - Print / Save PDF support

---

## How to Use

### 1. Open the tester

Open `index.html` directly in any modern browser (Chrome, Edge, Firefox, Safari). No web server required.

### 2. Create a session

A "New Test Session" dialog appears automatically. Enter:
- **Target URL** — the site you want to test
- **Session name** (optional) — e.g. `Homepage v2 - May 2026`
- **Test type** — Visual Testing or Form Testing

Click **Create Session**.

### 3. Test the site

- Paste or type the URL into the URL bar and click **Open in New Tab ↗** to load the site alongside the tester.
- Work through each step in the checklist:
  - Click a step to expand it and read the detailed description.
  - Click **Pass** if the check passes.
  - Click **Fail** if the check fails — a bug input field opens automatically.
- **Log bugs** — type a bug description and press Enter or click **Add**. Resolve bugs later with the **Resolve** button.
- **Add notes** — use the notes field inside each step for any observations.

### 4. Track progress

The stats bar at the top shows live counts of passed, failed, pending steps, and open bugs. The progress bar fills as you complete steps.

### 5. View the report

Click **View Report →** in the top nav (or open `report.html` in a browser). The report shows:
- A letter grade and verdict (Accepted / Not Accepted)
- Category-by-category breakdown with progress bars
- Full results table for all steps
- All logged bugs with open/resolved status
- All tester notes

Click **Print / Save PDF** to export the report.

### 6. Switch sessions

Click **Sessions** in the nav to see all saved sessions, resume a previous one, or create a new one.

---

## File Structure

```
index.html   — Main QA tester UI
report.html  — Report viewer (reads from localStorage)
README.md    — This file
```

No build step. No dependencies. No CDN beyond Google Fonts for typography.

---

## Browser Compatibility

Works in all modern browsers. Requires JavaScript and `localStorage` enabled. Data is stored per-browser and per-device — sessions do not sync across devices.
