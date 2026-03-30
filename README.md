# Wanderly — Project Checklist

> **AAI 595 Applied Machine Learning · Group 13 · Stevens Institute of Technology**  
> Midterm Progress Tracker · Due April 22, 2026

---

## Overview

This is an interactive HTML progress checklist for **Wanderly.ai**, an AI-powered travel planning web application built as the midterm project for AAI 595 at Stevens Institute of Technology.

The checklist documents:
- ✅ **28 completed features** confirmed in code
- ⚠️ **12 remaining tasks** needed before final submission
- 💪 **10 technical strengths** of the current implementation
- 🔻 **8 honest weaknesses and limitations** to address or disclose

---

## What is Wanderly?

Wanderly is a full-stack AI travel planning app that takes user preferences (budget, travel style, dates, dietary restrictions) and returns personalized destination recommendations with fully AI-generated trip itineraries. It uses a two-layer AI architecture:

- **scikit-learn** for ML-based destination scoring and ranking
- **GPT-4o-mini via Base44** for structured content generation (itineraries, hotels, food, packing lists, etc.)

**Tech stack:** React · Vite · TanStack Query · Tailwind CSS · shadcn/ui · Base44 (auth, DB, LLM) · Python/Flask · scikit-learn

---

## How to Use the Checklist

The checklist is a standalone HTML file — no build step, no dependencies, no server required.

```bash
# Clone or download the repo, then just open the file:
open wanderly_checklist.html
```

Or drag the file directly into any browser.

---

## File Structure

```
wanderly_checklist.html   # The complete checklist — single self-contained file
README.md                 # This file
```

---

## Checklist Sections

### ✅ Completed (28 items)
Features fully built and confirmed in source code, including:
- Base44 entity schema (Trip, UserPreferences, SavedItem)
- 50+ destination knowledge base (`destinations.js`) with per-hub flight estimates, 6 hotel tiers, dietary/family/visa flags, and crowd data
- Rule-based scoring engine (`scoring.js`) with 4-dimension scoring
- Full React frontend — 8 pages with React Router v6
- 5-step onboarding wizard with Framer Motion animations
- Real `.ics` calendar file parser (Google Calendar, Outlook, Apple Calendar)
- LLM integration with JSON schema-constrained output (zero parsing failures)
- 10-tab TripDetail page with lazy loading
- 3 AI chat assistants (trip-level, results-level, profile-level)
- BrowseAndBudget — AI fallback for any destination in the world
- 15 booking deep-link APIs (flights, hotels, activities, insurance, transport)
- Budget mode intelligence (auto-switches to hostel/street food prompts under $500/person)
- Python/Flask ML backend with trained scikit-learn RandomForestRegressor
- In-browser PDF export using jsPDF + html2canvas

### ⚠️ Still Needed (12 items)
Remaining work before final submission, including:
- Connecting the Flask ML backend to the React frontend
- Running MAE/RMSE accuracy evaluation on the trained model
- Documenting feature importance from the RandomForest
- Running an ML vs rule-based A/B comparison
- LLM content accuracy spot-check (3–5 destinations manually verified)
- Reconciling scoring weight discrepancy between proposal and code
- Challenges & Solutions documentation (required by rubric)

### 💪 Strengths
Key technical differentiators highlighted for the final presentation:
- Two-layer AI architecture (ML ranking + LLM content generation)
- JSON schema-constrained LLM output
- Hand-curated 50+ destination knowledge base
- Real `.ics` calendar integration
- Transparent scoring (not a black box)
- Dietary awareness threaded through onboarding → AI prompts

### ⚠️ Weaknesses & Limitations
Honest self-assessment for academic integrity and rubric compliance:
- ML backend not yet connected to frontend (frontend runs rule-based JS scoring)
- No ML accuracy metrics run yet (MAE/RMSE missing)
- LLM content unverified (AI-estimated prices, not live data)
- ±10pt random jitter in rankings (non-deterministic results)
- Base44 vendor lock-in and credit limits
- Unknown destination scores default to flat 75 baseline

---

## Project Context

| Field | Value |
|---|---|
| Course | AAI 595 — Applied Machine Learning |
| Institution | Stevens Institute of Technology |
| Student | Saanie Naqvi |
| Group | 13 |
| Due Date | April 22, 2026 |
| Status | Midterm Progress |

---

## Embedding in Presentations

To embed the checklist in a PowerPoint or Google Slides presentation, take a full-page screenshot of the rendered HTML (browser → Print → Save as PDF works well) or use the included PDF version.

For live embedding in a web-based presentation (e.g., reveal.js, Gamma), the file can be hosted via GitHub Pages and embedded in an `<iframe>`:

```html
<iframe 
  src="https://your-username.github.io/wanderly-checklist/wanderly_checklist.html"
  width="100%" 
  height="800px"
  frameborder="0">
</iframe>
```

---

## Publishing on GitHub Pages

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)` folder
4. Your checklist will be live at:  
   `https://your-username.github.io/wanderly-checklist/wanderly_checklist.html`

---

*Built with ✦ for AAI 595 · Stevens Institute of Technology*
