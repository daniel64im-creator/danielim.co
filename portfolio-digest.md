# portfolio-digest.md
> Generated from a full read of every HTML file, the shared CSS, and the nav component.
> Accuracy policy: "NOT FOUND" is written where data is absent rather than inferred.

---

## 1. STACK AND BUILD

**Framework:** No framework. Plain HTML, CSS, and vanilla JavaScript.

**Styling approach:**
- Shared global stylesheet: `assets/css/sf-theme.css` (loaded via `<link>` on resume, projects-library, 404, and all project pages)
- `index.html` does NOT link `sf-theme.css`; it instead contains a full inline `<style>` block that duplicates most of the shared rules
- Each project page includes a repeated inline `<style>` block defining `.proj-card-grid`, `.proj-card-col`, `.proj-bubbles`, `.proj-bubble-*`, `.proj-tools`, `.proj-tool-tag`, `.proj-thumbnail` (identical across all 11 project pages)
- Two legacy SASS source trees exist under `assets/sass/` (base, components, layout, libs) but they are NOT compiled or linked anywhere in the site; they appear to be leftover from a prior theme and are unused

**Build and deploy:**
- No build command, no package.json, no bundler, no CI config found
- Deployed via GitHub Pages using a `CNAME` file with value `danielim.co`
- Git remote: `https://github.com/daniel64im-creator/danielim.co.git`, branch `main`
- Output is the repo root itself (no `/dist` or `/build` folder)

**Component library / UI framework:**
- No third-party UI framework (no Bootstrap, Tailwind, etc.)
- Custom Salesforce Lightning-inspired design system built entirely from scratch in `sf-theme.css`
- Font Awesome webfonts are present in `assets/webfonts/` (fa-brands-400, fa-regular-400, fa-solid-900 in eot/svg/ttf/woff/woff2) but there is no `all.css` or `fontawesome.css` linked anywhere; the icons are NOT loaded in any HTML page — these files appear unused
- Nav component at `components/sf-nav.html` is loaded at runtime via `fetch()` in every page except `index.html` (which has nav hardcoded inline)

---

## 2. SITEMAP

| File path | URL path | Purpose |
|---|---|---|
| `index.html` | `/` | **Home / landing page.** Identity card, About section, 4 Featured Projects cards |
| `resume.html` | `/resume.html` | Resume with Skills, Work Experience timeline, Education |
| `projects-library.html` | `/projects-library.html` | Tabbed project library with 3 category tabs; cards rendered by JavaScript |
| `404.html` | (GitHub Pages 404 fallback) | Custom 404 error page |
| `projects/expired-lead-digest.html` | `/projects/expired-lead-digest.html` | Project: Expired Lead Follow-Up Automation |
| `projects/enrichment.html` | `/projects/enrichment.html` | Project: 10,000-Account CRM Enrichment |
| `projects/allocation-TL.html` | `/projects/allocation-TL.html` | Project: Account Ownership & Cross-Sell Rules |
| `projects/fte-lookup.html` | `/projects/fte-lookup.html` | Project: Account Data Lookup Tool |
| `projects/demo-email.html` | `/projects/demo-email.html` | Project: Salesforce Demo Email Capture Workflow |
| `projects/pip-governance.html` | `/projects/pip-governance.html` | Project: Performance Intervention Framework |
| `projects/roe-compliance-reporting.html` | `/projects/roe-compliance-reporting.html` | Project: CRM Outreach Eligibility Reporting |
| `projects/account-dedup.html` | `/projects/account-dedup.html` | Project: Salesforce Account Deduplication & Ownership Cleanup |
| `projects/team-lead-dashboard.html` | `/projects/team-lead-dashboard.html` | Project: Team Lead Performance Dashboard |
| `projects/lead-cleanup.html` | `/projects/lead-cleanup.html` | Project: Event Lead Cleanup & Reassignment |
| `projects/executive-advisory-targeting.html` | `/projects/executive-advisory-targeting.html` | Project: Customer Advisory Target Account List |

Note: `lead-cleanup.html` and `executive-advisory-targeting.html` are NOT listed in `sitemap.xml` and are NOT included in any `projectData` tab in `projects-library.html` (they use an older page layout without the PSO card grid). They exist as standalone pages accessible only by direct URL.

---

## 3. PAGE CONTENT

### index.html — Home

**App bar:** Sales Ops Cloud | Home | Projects | Resume | [LinkedIn icon]

**Context bar breadcrumb:** Contacts > Daniel Im | Record ID: 003Dn00000REVOPS

**Record header fields:**
- Email: daniel64im@gmail.com
- Location: San Jose, CA
- LinkedIn: linkedin.com/in/daeim
- Education: B.A. Economics (Int'l Macro-Finance), UC Davis

**Section label:** About

> I am a problem finder. Most inefficiencies don't announce themselves. They hide in repetitive manual steps, in CRM fields that nobody trusts, in processes that quietly break down over time. I look for them before they become someone else's fire drill. Whether it's a data gap causing silent automation failures, a lead ownership model creating duplicate outreach, or a lookup that costs every rep 30 seconds per account, I dig into the root cause rather than the symptom.

> I am a problem solver. Once I find the problem, I build the fix. My toolkit spans Salesforce Flow Builder, Google Sheets, Apps Script, CRM governance design, and data enrichment workflows. I don't patch around issues. I build systems that eliminate them. The 10,000-account CRM enrichment didn't just clean bad data; it restored the reporting accuracy the team was making decisions from. The expired lead automation didn't just send emails; it turned a silent ownership loss point into a structured re-engagement channel.

> I build for scale. Every solution I build is documented, repeatable, and designed to outlast my involvement. If the system breaks when I'm not in the room, I haven't done my job.

**Section label:** Featured Projects

Button: View All →

**Card 1: Expired Lead Follow-Up Automation** (tag: CRM & Automation)
> Built a native Salesforce system that captures lead expiration events and delivers a personalized weekly digest to each rep, turning silent ownership losses into an active re-engagement channel.
Button: View Project →

**Card 2: 10,000-Account CRM Enrichment** (tag: Data Infrastructure)
> Audited and enriched 10,000 Salesforce accounts to restore segmentation accuracy, establishing clean data foundations that improved targeting and pipeline reporting across the team.
Button: View Project →

**Card 3: Account Ownership & Cross-Sell Rules** (tag: Governance)
> Designed account routing logic and ownership rules that eliminated duplicate outreach across shared institutional accounts and improved cross-sell coordination across product lines.
Button: View Project →

**Card 4: Account Data Lookup Tool** (tag: Data Infrastructure)
> Built a Google Sheets tool that reduced SDR enrollment lookup time from 30 seconds to 3 seconds, eliminating a daily friction point and freeing up prospecting capacity across the team.
Button: View Project →

---

### resume.html — Resume

**Page title (h1):** Resume

**Header fields:** Location: San Jose, CA | Email: daniel64im@gmail.com | LinkedIn: linkedin.com/in/daeim

**Section: Skills**

CRM & Automation:
- Salesforce Flow Builder
- Record-Triggered Flows
- Scheduled Flows
- Custom Objects
- CRM Governance
- Reports & Dashboards

Data & Reporting:
- Google Sheets
- Apps Script
- Data Enrichment
- Segmentation

Sales Operations:
- GTM Process Design
- Rules of Engagement
- Pipeline Management
- ICP Targeting
- Account Routing

**Section: Work Experience**

**Sales Development Team Lead — YuJa, Inc.** (tag: Current) Jun '24 – Present
Focus: Salesforce administration, CRM governance, and GTM process automation
- Rebuilt Salesforce account data foundation across ~10,000 accounts, mapping IPEDS firmographic data by Account ID to restore segmentation accuracy and improve targeting precision across the SDR team.
- Designed and published a Rules of Engagement framework across 4 product lines in Salesforce Flow Builder, enforcing a 14 day lead ownership window and improving account targeting quality, cutting duplicate demo bookings and resolving cross team conflicts.
- Resolved 800 duplicate account records within the 10,000 account CRM base using a tiered confidence grouping and merge framework, then documented governance standards to prevent recurrence.
- Built a 4 component native Salesforce automation (Record Triggered Flow, Scheduled Flow, custom logging object) delivering a personalized weekly expired lead digest to reps, replacing a silent, unlogged ownership loss point.
- Built a custom Lightning component on the Salesforce Lead page giving SDRs instant institution size lookups and AE routing guidance, cutting account research time from 30 seconds to 3 seconds.
- Built a cross team performance dashboard in Salesforce Reports & Dashboards consolidating demos held, no shows, reschedules, and quota attainment, giving team leads a single source of truth each quarter.

**Founding SDR — Miarec** Jul '23 – Jun '24
- Sole SDR responsible for all top-of-funnel activity, executing 150+ manual dials per day while independently sourcing leads through LinkedIn and ZoomInfo.
- Drove a management-approved auto-dialer trial after identifying manual dialing as an operational bottleneck, then refocused on prospect list quality and targeting precision to consistently generate qualified pipeline.

**Senior SDR — Arkose Labs** Nov '22 – Apr '23
- Ramped to full productivity within 30 days in a complex enterprise cybersecurity sales cycle, booking qualified meetings by end of month one.
- Self-initiated a Korean market expansion into untapped territory with no internal Korean-speaking coverage: translated pitch materials, built a prospecting playbook, and booked 2 qualified meetings before the SDR team was cut in a restructure.

**Founding SDR — SpecTrust** Jul '21 – Nov '22
- Built outbound sequences, cadences, and Salesforce CRM standards from scratch as one of two founding SDRs, owning the prospecting infrastructure for the team.
- Designed a C-level email program writing outbound under the CEO and COO names to leverage executive credibility and lift meeting volume; averaged 105% of quota (20 meetings/month) across tenure.

**Account Executive — Xerox** Jan '19 – Jun '21
- Managed the full B2B sales cycle from prospecting through close while maintaining Salesforce pipeline accuracy and account records.

**Section: Education**

B.A. Economics (Int'l Macro-Finance) — University of California, Davis

---

### projects-library.html — Project Library

**Page title (h1):** Project Library

**Tab 1: CRM & Automation** (count: 2)
- Expired Lead Follow-Up Automation
- Salesforce Demo Email Capture Workflow

**Tab 2: Governance Systems** (count: 3)
- Account Ownership & Cross-Sell Rules
- Performance Intervention Framework
- CRM Outreach Eligibility Reporting

**Tab 3: Data Infrastructure** (count: 3)
- 10,000-Account CRM Enrichment
- Account Data Lookup Tool
- Salesforce Account Deduplication & Ownership Cleanup

(Note: "Event Lead Cleanup & Reassignment" and "Customer Advisory Target Account List" exist in the `projectData` JS object but are NOT in any category array — they are never rendered in any tab. The library shows 10 projects across three tabs.)

Each card shows: thumbnail image, category tag, project title, summary text, "View Project →" button.

---

### 404.html — Page Not Found

**Heading:** 404
**Subheading:** Page not found
**Body:** The page you're looking for doesn't exist or may have moved.
**Button:** Go to Homepage

---

## 4. PROJECTS

Projects are presented in two locations: the Featured Projects section on `index.html` (4 cards) and the tabbed Project Library on `projects-library.html` (10 cards across 3 tabs). Each project has a dedicated detail page in `projects/`.

---

### Project 1: Expired Lead Follow-Up Automation
**File:** `projects/expired-lead-digest.html`
**Category:** CRM & Automation
**Impact statement:** When leads expired out of rep ownership after the 14-day window, they disappeared silently — no notification, no log, and no way to re-engage. This project built a native Salesforce system that captures every expiration event and delivers a personalized weekly digest to each rep every Monday.

**Problem bubbles:**
- Silent lead ownership loss
- No expiration feedback loop
- Prior owner value lost on transfer
- No re-engagement channel

**Solution bubbles:**
- Custom logging object
- Record-Triggered Flow (immediate + async)
- Weekly digest email per rep
- Log cleanup Scheduled Flow

**Outcome bubbles:**
- Weekly expired lead digest per rep
- Re-engagement channel activated
- All expiration events logged
- Zero manual effort required

**How It Works (arch-box):**
```
Lead Expiration Flow Trigger
  → Immediate path captures prior owner before record updates
  → Async path writes log record (Lead name, Company, Prior Owner, Record ID)
  → Fault path isolates logging failure from core expiration process

Every Monday (Scheduled Flow)
  → Queries log object for each rep's prior-week expirations
  → Emails personalized digest with lead name, company, direct record link

Trailing Cleanup (Scheduled Flow)
  → Deletes log records older than retention window
```

**Metrics cited:** 14-day ownership window (referenced in impact text)

**Tools:** Salesforce Flow Builder, Record-Triggered Flows, Scheduled Flows, Custom Objects, Governor Limit Handling, Sandbox to Production Deployment

---

### Project 2: 10,000-Account CRM Enrichment
**File:** `projects/enrichment.html`
**Category:** Data Infrastructure
**Impact statement:** Restored firmographic accuracy across ~10,000 Salesforce accounts by sourcing institutional data from IPEDS, normalizing it in Google Sheets, and re-importing by Account ID — improving segmentation, territory reporting, and CRM reliability.

**Problem bubbles:**
- Firmographic fields missing across thousands of accounts
- Inconsistent naming and website formatting
- Time zone inaccuracies affecting outreach timing
- Unreliable segmentation and territory reporting

**Solution bubbles:**
- Salesforce Account export
- IPEDS firmographic data pull
- Google Sheets normalization
- ID-based record mapping
- Pre-import QA validation

**Outcome bubbles:**
- ~10,000 accounts enriched
- Restored segmentation accuracy
- Reliable territory reporting
- CRM as a trusted data layer

**How It Works (arch-box):**
```
Salesforce Account Export
  → IPEDS Data Pull (FTE, domain, geography, time zone)
  → Google Sheets Normalization
  → QA Sampling
  → CSV Export
  → Salesforce Re-Import by Account ID
  → Clean CRM Dataset
```

**Metrics cited:** ~10,000 accounts enriched

**Tools:** IPEDS, Google Sheets, Salesforce CRM, Salesforce Data Import Wizard, Data Normalization, QA Validation

**Screenshots shown:** Salesforce Data Import Wizard — Import Configuration; Salesforce Data Import Wizard — Field Mapping

---

### Project 3: Account Ownership & Cross-Sell Rules
**File:** `projects/allocation-TL.html`
**Category:** Governance Systems
**Impact statement:** Eliminated duplicate outreach on existing customers by building a centralized routing framework that enforced team-level ownership and cross-sell boundaries across a multi-product SDR organization.

**Problem bubbles:**
- No account ownership model
- Duplicate outreach across product teams
- No routing logic for shared accounts
- Reassignment had no process or visibility

**Solution bubbles:**
- Master customer list
- Team routing rules
- Rep assignment layer
- Cross-sell guardrails
- Reassignment controls

**Outcome bubbles:**
- Duplicate outreach eliminated
- Clear rep-level ownership
- Enforced cross-sell governance
- Repeatable routing model

**How It Works (arch-box):**
```
Account Identified
  → Team Routing Rules Applied
  → Rep Ownership Assigned
  → Cross-Sell Check Enforced
  → Outreach Permitted or Blocked
```

**Metrics cited:** none verbatim

**Tools:** Google Sheets, Account Routing Design, Cross-Product Governance, Ownership Framework Design

---

### Project 4: Account Data Lookup Tool
**File:** `projects/fte-lookup.html`
**Category:** Data Infrastructure
**Impact statement:** Reduced institutional enrollment lookup time from ~30 seconds to ~3 seconds by embedding FTE data directly into the SDR workflow — first in the Google Sheets demo rotation tracker, then as a search component on the Salesforce Lead page.

**Problem bubbles:**
- Constant tool switching for FTE data
- Slow institutional size research
- No consistent account size signals
- Repeated manual effort every session

**Solution bubbles:**
- Embedded FTE lookup dataset
- v1 built into Google Sheets demo tracker
- v2 search component on Salesforce Lead page
- Standardized output format

**Outcome bubbles:**
- 30s → 3s lookup time
- Consistent account prioritization
- No more manual research
- No CRM context switching

**How It Works (arch-box):**
```
Institution Search
  → FTE Dataset Queried
  → Result Returned (size range + segment classification)
  → SDR Uses Size Signal for Targeting Decision
```

**Metrics cited:** 30 seconds to 3 seconds lookup time

**Tools:** Google Sheets, Salesforce CRM, Apps Script, Workflow Embedding, Data Lookup Design

---

### Project 5: Salesforce Demo Email Capture Workflow
**File:** `projects/demo-email.html`
**Category:** CRM & Automation
**Impact statement:** Eliminated marketing automation enrollment failures caused by missing demo attendee email on Opportunity records by automating field population through a record-triggered Salesforce Flow.

**Problem bubbles:**
- Email missing on Opportunity records
- Marketing automation enrollment failures
- Manual data copying by SDRs
- No enforcement mechanism

**Solution bubbles:**
- Record-Triggered Flow on demo event creation
- Scoped to demo event types only
- Auto-copies contact email to Opportunity field
- Removes reliance on manual SDR updates

**Outcome bubbles:**
- No enrollment failures
- Eliminated manual copying
- Improved CRM data integrity
- Marketing automation alignment restored

**How It Works (arch-box):**
```
Demo Event Created
  → Flow Triggered
  → Primary Contact Email Retrieved
  → Opportunity Email Field Updated
  → Marketing Automation Enrollment Succeeds
```

**Metrics cited:** none verbatim

**Tools:** Salesforce CRM, Record-Triggered Flow, Marketing Automation Integration, Field Mapping Logic

---

### Project 7: Performance Intervention Framework
**File:** `projects/pip-governance.html`
**Category:** Governance Systems
**Impact statement:** The first formalized PIP framework in the organization — drafted from scratch, refined with management, approved by HR, and integrated into new hire onboarding. Replaced inconsistent manager-by-manager interventions with objective trigger thresholds and a documented review process.

**Problem bubbles:**
- No formal PIP structure existed
- No objective trigger thresholds
- Inconsistent manager interventions
- No timeline, checkpoints, or documentation standards

**Solution bubbles:**
- Measurable quota trigger criteria
- 30/60/90-day timeline structure
- Daily activity expectations
- Exit criteria and escalation paths
- Signed documentation package

**Outcome bubbles:**
- Consistent interventions across managers
- HR-aligned documentation
- Published to Confluence
- Integrated into new hire onboarding

**How It Works (arch-box):**
```
Performance Monitoring
  → Trigger Threshold Reached (quota attainment below defined %)
  → PIP Type Determined (Month-to-Month or Quarterly)
  → Timeline Set + Daily KPI Monitoring Begins
  → Weekly Checkpoint Reviews
  → Exit Criteria Met or Escalation Path Activated
```

**Metrics cited:** 30/60/90-day timeline structure; quota attainment below defined % (specific % NOT FOUND in page text)

**Tools:** Confluence, Canvas (LMS), Process Documentation, HR Governance, Performance Framework Design

---

### Project 9: CRM Outreach Eligibility Reporting
**File:** `projects/roe-compliance-reporting.html`
**Category:** Governance Systems
**Impact statement:** Eliminated duplicate demo bookings and cross-team ownership disputes by building an enforceable outreach eligibility framework across four product lines — combining Salesforce automation, decision workflow documentation, and published training materials.

**Problem bubbles:**
- No outreach eligibility process
- SDRs could self-assign leads indefinitely
- Cross-product teams conflicted on same accounts
- Duplicate demo bookings occurring
- No enforceable accountability framework

**Solution bubbles:**
- 14-day lead ownership enforcement (Salesforce Flow)
- Opportunity guardrail decision tree
- Cross-product outreach logic
- Escalation layer for disputed accounts
- Published to Confluence + Canvas onboarding

**Outcome bubbles:**
- Duplicate demo bookings eliminated
- Reduced ownership disputes
- Standardized eligibility process
- Enforceable lead ownership boundaries

**How It Works (arch-box):**
```
Account Evaluated
  → Customer Status Verified
  → Opportunity Presence Checked
  → Active Contact Protection Applied
  → Lead Ownership Verified (14-day expiration enforced)
  → Outreach Permitted or Escalated
```

**Metrics cited:** 14-day lead ownership window; four product lines

**Decision workflow screenshots:** Account Qualification Workflow, Opportunity Conflict Analysis, Lead Ownership Evaluation

**Tools:** Salesforce CRM, Salesforce Flow Builder, Confluence, Canvas (LMS), Rules of Engagement Design, Cross-Product Governance

---

### Project 10: Salesforce Account Deduplication & Ownership Cleanup
**File:** `projects/account-dedup.html`
**Category:** Data Infrastructure
**Impact statement:** Resolved duplicate Account records across Salesforce by building a structured review process using name normalization, confidence-level grouping, and a merge decision framework — then created CRM governance standards to prevent future duplication.

**Problem bubbles:**
- Duplicate Account records across CRM
- Ownership conflicts on same accounts
- Inconsistent naming made duplicates hard to detect
- No process to prevent future duplication
- Reporting reliability impacted

**Solution bubbles:**
- Account name normalization
- Multi-criteria duplicate detection
- High / Medium / Low confidence grouping
- Merge decision framework
- Ownership conflict resolution
- CRM governance standards

**Outcome bubbles:**
- Cleaner Account database
- Clearer ownership across CRM
- More reliable reporting
- Governance standards documented
- Repeatable cleanup process built

**How It Works (arch-box):**
```
Salesforce Account Export
  → Name Normalization (punctuation, abbreviations, formatting)
  → Duplicate Detection (name, domain, location, owner, activity)
  → Confidence Grouping (High / Medium / Low)
  → Merge Decision Review
  → Ownership Conflict Resolution
  → QA Validation
  → CRM Governance Standards Documented
```

**Metrics cited:** none verbatim

**Tools:** Salesforce CRM, Salesforce Reports, Google Sheets, Apps Script, Data Normalization, CRM Governance

---

### Project 11: Event Lead Cleanup & Reassignment
**File:** `projects/lead-cleanup.html`
**Category:** Data Infrastructure (tag present but page uses older layout — no PSO card grid)
**Impact statement:** Accelerated post-event follow-up and eliminated routing confusion by building a standardized intake and redistribution process for conference lead lists.

**Body text (visible):**
Structured intake and cleanup workflow designed to convert raw conference lead lists into clean, actionable SDR outreach queues while preserving ownership clarity and reducing duplicate follow-up.

Event leads were typically delivered as raw CSV exports with inconsistent formatting and unclear ownership routing. Without structured cleanup and distribution, these leads introduced delays, duplicates, and confusion around follow-up responsibility.

This project implemented a standardized intake process to normalize, deduplicate, categorize, and redistribute event leads into SDR-ready outreach lists.

**Structural Gap:** Raw event lists contained inconsistent formatting. Duplicate records existed across events and CRM. No standardized routing model for lead ownership. Manual list sharing created delays after events.

**Architecture:**
- Lead Intake Layer — Raw conference lists imported into a structured working sheet.
- Data Normalization — Standardized name formatting, company names, and contact fields.
- Deduplication Pass — Removed obvious duplicates prior to distribution.
- Product Categorization — Leads grouped by product interest or contextual relevance.
- Ownership Routing — Leads distributed into SDR-specific outreach queues.

**Operational Impact:** Accelerated post-event outreach speed. Reduced duplicate follow-up incidents. Improved ownership clarity for SDR teams. Created repeatable intake process for future conferences.

**Future Improvements:** Require standardized lead templates from marketing. Add automated duplicate detection rules. Formalize routing logic into documented decision trees.

**Metrics cited:** none verbatim

**Tools (listed as text, not tool-tag badges):** Google Sheets processing workflow, CRM lead datasets, Manual QA validation pass

---

### Project 12: Customer Advisory Target Account List
**File:** `projects/executive-advisory-targeting.html`
**Category:** Data Infrastructure (tag present but page uses older layout — no PSO card grid)
**Impact statement:** Replaced informal invite suggestions with a structured segmentation workflow — applying NPS, product category, ICP level, and contract size criteria — to produce a validated invite list for a client dinner at EDUCAUSE.

**Body text (visible):**
Customer targeting and segmentation workflow built to identify the right Panorama customers for a client dinner hosted during EDUCAUSE conference week in Nashville. The goal was to strengthen relationships with high-fit, satisfied customers and increase their receptiveness to future expansion across other product lines.

Leadership wanted to host a client dinner during EDUCAUSE to deepen relationships with current customers — specifically Panorama customers, our highest-value product, where satisfaction was highest and upsell potential was strongest. Previous invite lists had been assembled informally through individual suggestions, with no consistent criteria and limited visibility into whether invitees were the right fit.

**Architecture:**
- Product Filter — Scoped the candidate pool to current Panorama customers only.
- NPS Screening — Filtered for customers with strong NPS signals.
- ICP Qualification — Targeted Director-level contacts or established primary points of contact.
- Account Size Filter — Excluded small institutions; prioritized larger contract-holding customers.
- Deduplication Pass — Removed duplicate institutions and redundant contacts.
- Stakeholder Review Output — Final validated list delivered to leadership for review and approval.

**Scale:** Event: client dinner, EDUCAUSE conference week, Nashville (October 2024). Source pool: all current Panorama customers. Objective: produce a high-fit, validated invite list for executive approval.

**Metrics cited:** none verbatim (EDUCAUSE Nashville October 2024 cited as context)

**Tools (listed as text, not tool-tag badges):** Salesforce CRM (customer data, NPS, contract records), Google Sheets (segmentation, filtering, list output)

---

## 5. LINKS AND ASSETS

**External links:**
| URL | Where it appears |
|---|---|
| https://www.linkedin.com/in/daeim/ | App bar (all pages via nav component), index.html header fields |
| mailto:daniel64im@gmail.com | index.html header fields, resume.html header fields |
| https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap | index.html `<link>` (inline); also `@import` in sf-theme.css |

**OG image:**
- Path: `og-image.png` (repo root)
- Used as `og:image` meta in index.html, resume.html, projects-library.html

**Favicon files:**
- `images/favicon 16x16.png`
- `images/favicon 32x32.png`
- `images/favicon 48x48.png`
- `images/favicon 96x96.png`

**Project thumbnail / screenshot images:**

| File | Used in |
|---|---|
| `images/expired-lead-digest.jpg` | expired-lead-digest.html header; index.html featured card |
| `images/enrichment-sheet.webp` | enrichment.html header; index.html featured card |
| `images/enrichment-import-wizard.webp` | enrichment.html screenshots section |
| `images/enrichment-field-mapping.webp` | enrichment.html screenshots section |
| `images/account-ownership-thumbnail.png` | allocation-TL.html header; index.html featured card |
| `images/fte-lookup-component.webp` | fte-lookup.html header; index.html featured card |
| `images/demo-email-flow.webp` | demo-email.html header |
| `images/pip-governance.png` | pip-governance.html header |
| `images/dedupe-thumbnail.png` | account-dedup.html header |
| `images/roe-lead-ownership.png` | roe-compliance-reporting.html header + screenshot |
| `images/roe-account-qualification.png` | roe-compliance-reporting.html screenshots section |
| `images/roe-opportunity-analysis.png` | roe-compliance-reporting.html screenshots section |
| `images/team-lead-dashboard.png` | team-lead-dashboard.html header; projects-library.html card |

**Company logo images (used in resume.html timeline):**

| File | Company |
|---|---|
| `images/yuja_logo.jpg` | YuJa, Inc. |
| `images/miarec_logo.jpg` | Miarec |
| `images/arkoselabs_logo.jpg` | Arkose Labs |
| `images/specprotected_logo.jpg` | SpecTrust |
| `images/xerox_logo.jpg` | Xerox |

---

## 6. DESIGN TOKENS

All tokens below are read directly from `assets/css/sf-theme.css` and the inline `<style>` blocks in the HTML files.

### Colors

| Token / Usage | Hex |
|---|---|
| Page background | `#f3f2f2` |
| Primary body text | `#181818` |
| Secondary / muted text | `#706e6b` |
| App bar background (deep navy) | `#032d60` |
| Primary blue (links, active states, buttons) | `#0176d3` |
| Primary blue hover | `#014486` |
| App name accent (light blue) | `#4bb3fd` |
| Heading / title color (dark navy) | `#16325c` |
| White (panel backgrounds) | `#ffffff` |
| Border / divider | `#dddbda` |
| Light border | `#e5e4e2` |
| Very light background (table row, hover) | `#fafaf9` |
| Stat card background | `#f8f9fb` |
| Tag: CRM & Automation (green) — background | `#ecfdf3` |
| Tag: CRM & Automation (green) — text | `#16a34a` |
| Tag: CRM & Automation (green) — border | `#bbf7d0` |
| Tag: Governance Systems (orange) — background | `#fff3e8` |
| Tag: Governance Systems (orange) — text | `#c65200` |
| Tag: Governance Systems (orange) — border | `#fad2a8` |
| Tag: Data Infrastructure (blue) — background | `#e8f4fd` |
| Tag: Data Infrastructure (blue) — text | `#0176d3` |
| Tag: Data Infrastructure (blue) — border | `#c9e5f8` |
| Status badge (green) — background | `#ecfdf3` |
| Status dot | `#22c55e` |
| PSO card: Problem top border | `#e45c3a` |
| PSO card: Solution top border | `#0176d3` |
| PSO card: Outcome top border | `#2e844a` |
| PSO bubble: Problem background | `#fef3ef` |
| PSO bubble: Problem border | `#f5c4b0` |
| PSO bubble: Solution background | `#e8f4fd` |
| PSO bubble: Solution border | `#a8cff0` |
| PSO bubble: Outcome background | `#edf7ee` |
| PSO bubble: Outcome border | `#a2d0aa` |
| Contact record icon background | `#7B5EA7` (purple, index.html inline style) |
| Resume header icon background | `#f59331` (orange, resume.html inline style) |
| Projects header icon background | `#e287b2` (pink, projects-library.html inline style) |
| Context bar icon: contact | `#47ccd6` |
| Context bar icon: projects | `#e287b2` |
| Context bar icon: resume | `#f59331` |
| Breadcrumb separator | `#c9c7c5` |
| Record ID text | `#b0adab` |
| Light bullet / inactive dot | `#c9c7c5` |

### Fonts

| Property | Value |
|---|---|
| Primary font family | `'Inter'`, `-apple-system`, `BlinkMacSystemFont`, `'Segoe UI'`, `Arial`, `sans-serif` |
| Monospace (arch-box, record ID) | `'Courier New'`, monospace |
| Font load | Google Fonts: `https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap` — loaded via `@import` in `sf-theme.css` AND via `<link>` in `index.html` |
| Base font size (html) | `16px` |
| Font rendering | `-webkit-font-smoothing: antialiased` |

### Heading / Type Scale

| Element | Size | Weight | Color |
|---|---|---|---|
| Record / page title (h1 equivalent) | `1.8rem` | 700 | `#16325c` |
| Project title `.sf-proj-title` | `1.5rem` | 700 | `#16325c` |
| Timeline role `.sf-timeline-role` | `1.05rem` | 700 | `#16325c` |
| Tab button `.sf-tab-btn` | `0.78rem`–`0.92rem` | 600 | `#706e6b` / `#0176d3` active |
| Section label `.sf-section-label` | `0.8rem` | 700 | `#706e6b` / `#444` (varies) |
| Project section title `.sf-proj-section-title` | `0.67rem` | 700 | `#706e6b` |
| Body / description text | `0.84rem`–`0.9rem` | 400 | `#181818` |
| Field label | `0.67rem`–`0.68rem` | 600 | `#706e6b` |
| Button | `0.77rem` | 600 | varies |
| Badge / tag | `0.66rem`–`0.7rem` | 600–700 | varies |
| App bar nav links | `0.78rem` | 500 | `rgba(255,255,255,0.72)` |
| App name | `0.82rem` | 700 | white |

### Spacing

| Component | Value |
|---|---|
| Max content width | `1200px` |
| Container padding | `16px 20px` (tablet: `16px 24px`; mobile: `10px 14px`) |
| Page top padding (fixed nav offset) | `92px` (52px app bar + 40px context bar) |
| Page bottom padding | `60px` |
| App bar height | `52px` |
| Context bar height | `40px` |
| Panel/card border-radius | `4px` |
| Button padding | `6px 16px` |
| Timeline item margin-bottom | `28px` |
| Section gap | `16px` (grid), `22px` (detail sections) |

### Reusable Components

**`.sf-app-bar`** — Fixed top nav, `#032d60`, height 52px, flex row, z-index 1000

**`.sf-context-bar`** — Fixed below app bar, white, height 40px, breadcrumb + record ID, z-index 999

**`.sf-card` / `.sf-panel`** — White card, `1px solid #dddbda`, border-radius 4px, `box-shadow: 0 2px 5px rgba(0,0,0,0.06)`

**`.sf-btn`, `.sf-btn-primary`, `.sf-btn-secondary`, `.sf-btn-ghost`** — Button variants; primary is blue fill, secondary is white/border, ghost is transparent

**`.sf-tag`** + modifier classes — Pill labels: `-automation` (green), `-governance` (orange), `-data` (blue), `-current` (blue), `-previous` (gray)

**`.sf-section-label`** — Uppercase label with bottom border: `2px solid #0176d3` (in index.html inline version) or `1px solid #e5e4e2` (in sf-theme.css shared version) — NOTE: these differ between the homepage and shared CSS

**`.sf-proj-header`** / **`.sf-proj-body`** / **`.sf-proj-section`** — Project page layout containers

**`.sf-arch-box`** — Monospace code-style block, left `3px solid #0176d3` accent, `#f8f8f8` background

**`.sf-screenshot`**, **`.sf-screenshot-grid`** — Screenshot display; 2-column grid collapses to 1 column at ≤860px

**`.proj-card-grid`** / **`.proj-card-col`** — 3-column PSO card layout (inline-defined per project page); top border colors: red (`#e45c3a`) / blue (`#0176d3`) / green (`#2e844a`)

**`.sf-table`** — Data table with gray header row, hover states

**`.sf-mobile-nav-panel`** — Hidden by default; displayed as flex column when `.open` class added; `#032d60` background

**Breakpoints:**
- Tablet: `max-width: 860px` — hide desktop nav, show hamburger, collapse to single column
- Mobile: `max-width: 580px` — tighter padding, stack fields, single-column grids

### Salesforce Lightning Design System (SLDS) patterns referenced

The design is custom-built but closely mirrors SLDS patterns:
- App launcher dot-grid icon (SVG, hardcoded)
- App bar with "Sales Ops Cloud" branding
- Context bar with object icon chip and breadcrumb
- Record header with highlight field labels
- Related list table headers (uppercase, gray, tight padding)
- Tab bar with active blue underline indicator
- Count pill badge on tabs
- Status badge with colored dot

No SLDS component library is imported or linked; all CSS is bespoke.

---

## 7. STATE AND GAPS

**Broken / encoding issues:**
- Previously, `projects/lead-cleanup.html` and `projects/executive-advisory-targeting.html` had corrupted arrow characters rendering as `?`. These have been fixed: arch-box `→` arrows and `←` Back to Projects buttons now render correctly.

**Pages not in sitemap.xml:**
- `projects/lead-cleanup.html` — NOT in sitemap.xml
- `projects/executive-advisory-targeting.html` — NOT in sitemap.xml

**Pages not rendered in Project Library tabs:**
- `lead-cleanup.html` (key `conference`) and `executive-advisory-targeting.html` (key `advisory`) exist in the `projectData` object in `projects-library.html` but are NOT assigned to any category array (`crm`, `governance`, or `data`), so they are never rendered in the library UI

**Different page structure:**
- `lead-cleanup.html` and `executive-advisory-targeting.html` use an older page layout without the PSO card grid, bubble elements, or tool-tag badges; they also lack inline per-page styles. This is inconsistent with all other project pages.

**Unused assets:**
- `assets/sass/` — Full SASS source tree (base, components, layout, libs) present but not compiled and not linked anywhere. Appears to be legacy from a prior theme.
- `assets/webfonts/` — Font Awesome font files (fa-brands, fa-regular, fa-solid in 5 formats each) present but no Font Awesome CSS is linked; icons are NOT loaded on any page. These files are unused.
- `images/allocation-sheet.png` — Present in repo but not referenced in any HTML file.
- `og-image.png` — Referenced as og:image meta but not a visible on-page asset.

**Inconsistency between index.html and sf-theme.css:**
- `index.html` does not link `sf-theme.css`; it has a large self-contained `<style>` block. Shared updates to `sf-theme.css` do NOT affect the homepage.
- The `.sf-section-label` in index.html uses `border-bottom: 2px solid #0176d3` and `color: #444`; the version in sf-theme.css uses `border-bottom: 1px solid #e5e4e2` and `color: #706e6b` — they are styled differently.
- `.sf-tab-btn` font-size is `0.92rem` in index.html inline styles vs `0.78rem` in sf-theme.css.

**NOT FOUND items:**
- No JavaScript files in `assets/js/` or any standalone `.js` files; all JS is inline `<script>` blocks
- No build tooling (no package.json, Gruntfile, Webpack config, etc.)
- No GitHub Actions or CI workflow files
- No analytics tag (Google Analytics, Plausible, etc.) in any page
- No contact form
- No print stylesheet (only `@media print` rules inside resume.html inline styles)
- No dark mode styles
- Font Awesome CSS file: NOT FOUND (webfonts present but CSS not linked)
- Specific PIP trigger quota percentage: NOT FOUND in page text (referenced as "quota attainment below defined %" without a specific number)
- Specific number of duplicate accounts resolved in account-dedup project: NOT FOUND
- `allocation-sheet.png` usage: NOT FOUND in any HTML file
