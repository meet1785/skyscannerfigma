# Skyscanner Ad Platform — UI/UX Redesign

## Project Overview
Skyscanner's advertising platform is being redesigned from an internal-only power-user tool into an intuitive, self-service portal for external advertising partners. This repository contains the **design mockups** (interactive HTML prototypes) and **JIRA story templates** needed to hand off the redesign to the frontend development team.

## Risk Mitigation

| Risk | Approach |
|------|----------|
| **Value** — Would partners want to use it? | Live preview, visual ROI metrics, clear value proposition on every screen |
| **Usability** — Can a new user navigate it alone? | Step-by-step wizard, contextual tooltips, progress indicators, minimal jargon |
| **Feasibility** — Can we build it with current tech? | Designs leverage existing APIs and infrastructure; incremental enhancement |
| **Investment** — Is the redesign worth it? | Built-in feedback loop continuously validates the investment with real user data |

## Designs (3 screens)

Open any file in a browser to view the interactive prototype:

| # | Screen | File | Purpose |
|---|--------|------|---------|
| 1 | **Ad Creation** | [`designs/1-ad-creation.html`](designs/1-ad-creation.html) | Step-by-step wizard for creating ads with live preview |
| 2 | **Ad Performance** | [`designs/2-ad-performance.html`](designs/2-ad-performance.html) | Dashboard for monitoring campaign metrics and trends |
| 3 | **User Feedback** | [`designs/3-user-feedback.html`](designs/3-user-feedback.html) | Survey to collect partner feedback for improvements |

## JIRA Stories

See [`JIRA_STORIES.md`](JIRA_STORIES.md) for three complete stories ready to enter into your JIRA board:

1. **Implement Ad Creation Wizard** — High priority, 8 story points, Sprint 1
2. **Implement Performance Dashboard** — High priority, 8 story points, Sprint 1
3. **Implement Feedback Survey** — Medium priority, 5 story points, Sprint 2

Each story includes: description, acceptance criteria, design links, technical notes, and definition of done.

## How to View the Designs

```bash
# Option 1: Open directly in your browser
open designs/1-ad-creation.html

# Option 2: Serve locally
npx serve designs/

# Option 3: Use VS Code Live Server extension
```

## How to Import into Figma
1. Open each HTML file in a browser
2. Take screenshots or use a browser-to-Figma plugin
3. Alternatively, recreate the layouts in Figma using the HTML as a reference — all colors, spacing, and component specs are documented in the CSS