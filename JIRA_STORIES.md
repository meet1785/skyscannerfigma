# JIRA Stories — Skyscanner Ad Platform Redesign

All stories below follow the standard JIRA template format and are ready to be entered into your project board. Each story references the corresponding design mockup in the `designs/` folder.

---

## Story 1: Implement Advertisement Creation Page

| Field            | Value                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Project**      | Skyscanner Ad Platform Redesign                                       |
| **Issue Type**   | Story                                                                 |
| **Summary**      | Build the redesigned advertisement creation wizard                    |
| **Priority**     | High                                                                  |
| **Sprint**       | Sprint 1                                                              |
| **Story Points** | 8                                                                     |
| **Assignee**     | Frontend Development Team                                             |
| **Labels**       | redesign, ui-ux, ad-creation, partner-portal                         |
| **Epic Link**    | Ad Platform Redesign                                                  |

### Description

**As a** partner (external advertiser),
**I want** to create advertisements through an intuitive step-by-step wizard,
**so that** I can launch campaigns on Skyscanner without needing training or internal support.

### Background
The current ad creation flow was built for internal power users and requires deep product knowledge. The redesigned wizard simplifies this into 4 clear steps with real-time preview, contextual help, and form validation.

### Design Reference
- **Mockup file:** `designs/1-ad-creation.html` (open in any browser to view the interactive prototype)
- Screenshot / Figma link: _(paste your Figma link here after importing)_

### Acceptance Criteria

- [ ] **Step-by-step wizard** with 4 stages: Campaign Setup → Ad Content → Targeting → Review & Publish
- [ ] **Progress stepper** at the top showing completed, active, and upcoming steps
- [ ] **Ad format selection** with visual cards (Banner, Native, Video, Sponsored)
- [ ] **Form fields** for headline (max 60 chars), description (max 150 chars), destination URL, and CTA dropdown
- [ ] **Image upload** via drag-and-drop or file browser (PNG/JPG, max 5 MB, recommended 1200×628 px)
- [ ] **Live ad preview** panel on the right that updates in real-time as the user fills out fields
- [ ] **Save as Draft** button in the header that persists work-in-progress
- [ ] **Contextual help tooltips** (?) on every form field explaining what the field is for
- [ ] **Form validation** with inline error messages for required fields
- [ ] **Responsive layout** — preview panel stacks below the form on screens < 900px
- [ ] **Navigation** — Back and Continue buttons with proper state management between steps
- [ ] **Breadcrumb navigation** showing Dashboard > Campaigns > Create New Ad

### Technical Notes
- Use existing campaign API for draft saving
- Image upload should use the media service endpoint
- Preview component should be reusable for the review step

### Definition of Done
- All acceptance criteria met
- Cross-browser tested (Chrome, Firefox, Safari, Edge)
- Responsive down to 768px
- Accessibility audit passes (WCAG 2.1 AA)
- Code reviewed and merged to develop branch

---

## Story 2: Implement Ad Performance Tracking Dashboard

| Field            | Value                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Project**      | Skyscanner Ad Platform Redesign                                       |
| **Issue Type**   | Story                                                                 |
| **Summary**      | Build the ad performance monitoring dashboard                         |
| **Priority**     | High                                                                  |
| **Sprint**       | Sprint 1                                                              |
| **Story Points** | 8                                                                     |
| **Assignee**     | Frontend Development Team                                             |
| **Labels**       | redesign, ui-ux, analytics, performance, partner-portal               |
| **Epic Link**    | Ad Platform Redesign                                                  |

### Description

**As a** partner (external advertiser),
**I want** to view my campaign performance through a clear, visual dashboard,
**so that** I can understand how my ads are performing and make data-driven optimization decisions.

### Background
Partners need to quickly assess campaign health without deep analytics expertise. The dashboard presents key metrics prominently, trend charts for patterns, traffic source breakdowns, and a sortable campaign table — all filterable by date range, campaign, and status.

### Design Reference
- **Mockup file:** `designs/2-ad-performance.html` (open in any browser to view the interactive prototype)
- Screenshot / Figma link: _(paste your Figma link here after importing)_

### Acceptance Criteria

- [ ] **6 metric cards** at the top: Impressions, Clicks, CTR, Conversions, Total Spend, ROAS
- [ ] Each metric card shows the **current value** and **% change vs. previous period** (green ▲ for positive, red ▼ for negative)
- [ ] **Filter bar** with: Date range picker (start/end), Campaign dropdown, Status dropdown (All/Active/Paused/Ended)
- [ ] **Performance Over Time** line chart showing Impressions and Clicks trends with legends and data points
- [ ] **Traffic Sources** donut/pie chart with breakdown (Search, Mobile App, Social, Direct) and center total
- [ ] **Campaign Details table** with columns: Campaign name, Status badge, Impressions, Clicks, CTR, Conversions, Spend, Trend
- [ ] Status badges: Active (green), Paused (amber), Ended (grey)
- [ ] **Search input** above the table to filter campaigns by name
- [ ] **Export buttons**: "Export CSV" and "Download Report" in the header
- [ ] **"+ New Campaign"** button linking to the ad creation page
- [ ] **Responsive layout** — charts stack vertically on screens < 900px, metric cards go to 2-column grid on mobile
- [ ] All data fetched from the analytics API with loading states

### Technical Notes
- Use a charting library (e.g., Chart.js, Recharts, or D3) for the line and donut charts
- Metric card data should refresh on filter change
- Table should support client-side sorting by column

### Definition of Done
- All acceptance criteria met
- Charts render correctly with real or mock data
- Cross-browser tested
- Responsive down to 768px
- Accessibility audit passes (WCAG 2.1 AA)
- Code reviewed and merged to develop branch

---

## Story 3: Implement User Feedback Collection Page

| Field            | Value                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Project**      | Skyscanner Ad Platform Redesign                                       |
| **Issue Type**   | Story                                                                 |
| **Summary**      | Build the user feedback survey page                                   |
| **Priority**     | Medium                                                                |
| **Sprint**       | Sprint 2                                                              |
| **Story Points** | 5                                                                     |
| **Assignee**     | Frontend Development Team                                             |
| **Labels**       | redesign, ui-ux, feedback, partner-portal, research                   |
| **Epic Link**    | Ad Platform Redesign                                                  |

### Description

**As a** partner (external advertiser),
**I want** to easily provide feedback about my experience on the platform,
**so that** Skyscanner can improve the product based on real user input.

### Background
Continuous feedback collection is essential to validating the redesign and identifying further improvement opportunities. The survey is short (6 questions, ~2 minutes), supports anonymous submission, and includes a mix of rating scales, multiple choice, and open text to gather both quantitative and qualitative data.

### Design Reference
- **Mockup file:** `designs/3-user-feedback.html` (open in any browser to view the interactive prototype)
- Screenshot / Figma link: _(paste your Figma link here after importing)_

### Acceptance Criteria

- [ ] **Welcome banner** with title, description, and estimated completion time ("~2 minutes")
- [ ] **Progress bar** that updates as questions are answered (e.g., "3 of 6 answered")
- [ ] **Q1 — Star rating** (1-5 stars) for overall satisfaction, with labels "Very Unsatisfied" to "Very Satisfied"
- [ ] **Q2 — Radio select** for ease of ad creation (5 options from "Very easy" to "Very difficult")
- [ ] **Q3 — Multi-select chips** for most useful features (Ad Creation Wizard, Performance Dashboard, Campaign Search, Report Export, Audience Targeting, Live Preview, Draft Saving)
- [ ] **Q4 — NPS scale** (0-10) for likelihood to recommend, with labels "Not likely" to "Extremely likely"
- [ ] **Q5 — Radio select** for biggest improvement area (Navigation, Ad creation flow, Performance reporting, Billing, Documentation)
- [ ] **Q6 — Open text area** (optional, max 500 chars) with live character counter
- [ ] Optional questions are visually distinguished (grey left border, "Optional" tag)
- [ ] **Anonymous toggle** — switch to submit feedback without attaching user identity
- [ ] **Submit button** — on click, hides form and shows a **Thank You confirmation** with a button to return to the dashboard
- [ ] **Responsive layout** for mobile screens
- [ ] Feedback data submitted to the feedback API endpoint

### Technical Notes
- NPS responses should be categorized server-side (0-6 Detractors, 7-8 Passives, 9-10 Promoters)
- Anonymous submissions should strip user identifiers before storing
- Consider triggering the feedback survey after a user completes their first campaign

### Definition of Done
- All acceptance criteria met
- Form submits correctly and shows confirmation state
- Cross-browser tested
- Responsive down to 768px
- Accessibility audit passes (WCAG 2.1 AA)
- Code reviewed and merged to develop branch

---

## Risk Mitigation Summary

| Risk | How These Designs Address It |
|------|------|
| **Value Risk** | Preview features, clear ROI metrics, and visual charts make the platform attractive and demonstrate tangible value to partners |
| **Usability Risk** | Step-by-step wizard, contextual tooltips, visual charts over raw data, and short feedback forms ensure new users can navigate with minimal training |
| **Feasibility Risk** | Designs build upon existing ad creation and analytics infrastructure; no entirely new backend capabilities are required |
| **Investment Justification** | Built-in feedback loop (Story 3) provides continuous data to validate the investment; self-service reduces support costs |
