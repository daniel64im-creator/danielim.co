# danielim.co — Portfolio Site

## Project Goal
This is Daniel Im's personal portfolio website, built to support a job search targeting **Sales Operations** and **Revenue Operations / Deal Desk** roles. The site serves as a portfolio of real work built during his time as a Sales Development Team Lead at YuJa, Inc. It is hosted at danielim.co and deployed via GitHub.

## About Daniel
- **Current role:** Sales Development Team Lead, YuJa, Inc. (Jun '24 – Jun '26)
- **Background:** 7 years in B2B SaaS, started as an SDR/AE, transitioned into Sales Ops work
- **Target roles:** Sales Operations, Revenue Operations, Deal Desk
- **Location:** San Jose, CA
- **Email:** daniel64im@gmail.com
- **LinkedIn:** linkedin.com/in/daeim

## Site Structure
Static HTML/CSS site with a Salesforce Lightning-inspired design ("Sales Ops Cloud" theme).

### Pages
- `index.html` — Homepage (About, Featured Projects)
- `resume.html` — Resume with timeline, skills, education
- `projects-library.html` — Project library with 3-tab category filter
- `projects/*.html` — Individual project detail pages (11 projects)
- `assets/css/sf-theme.css` — Shared CSS (max-width: 1200px)
- `components/sf-nav.html` — Shared nav component (loaded via fetch)

### Project Categories
- **CRM & Automation:** Expired Lead Follow-Up Automation, Demo Email Capture Workflow, Real-Time Demo Booking Alerts
- **Governance Systems:** Account Ownership & Cross-Sell Rules, Performance Intervention Framework, SDR Account Allocation System, CRM Outreach Eligibility Reporting
- **Data Infrastructure:** 9,000-Account CRM Enrichment, Account Data Lookup Tool, Salesforce Account Deduplication & Ownership Cleanup, (Event Lead Cleanup, Customer Advisory List — removed from library)

## Design Conventions
- Salesforce Lightning color palette: `#0176d3` (blue), `#16325c` (dark navy), `#706e6b` (gray), `#f3f2f2` (background)
- Category tag colors: green = CRM & Automation, orange = Governance, blue = Data Infrastructure
- Section labels: `font-size: 0.8rem`, uppercase, blue `2px` bottom border
- Buttons use `.sf-btn .sf-btn-primary` (blue) or `.sf-btn-secondary` (white/border)
- **No em dashes anywhere in visible text** — rewrite sentences to avoid them
- Project pages use: tag + title + impact statement + thumbnail + Problem/Solution/Outcome cards + How It Works arch-box + tool badges

## Workflow
- Auto-push all changes without asking for permission
- All bash commands allowed
- Git remote: `https://github.com/daniel64im-creator/danielim.co.git`
- Branch: `main`

## Key Decisions Made
- GitHub icon removed from nav (Sales Ops positioning — don't send people to code repos)
- Connect page removed (content absorbed into homepage)
- Homepage sections: About (3 paragraphs: problem finder / problem solver / builds for scale) → Featured Projects (4 cards)
- Resume consolidated into one unified panel (Skills → Work Experience → Education)
- Project pages redesigned from wall-of-text to visual card layout
- "Workflow Automation" renamed to "CRM & Automation" sitewide
- LinkedIn display URL shortened to `linkedin.com/in/daeim`
