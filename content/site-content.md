# Site content

Every piece of text on the website, in page order. This file is the source of
truth for wording; `index.html` holds the design.

## How to use this file

1. Find the section you want to change.
2. Edit the text, or copy that section's **Template** block to add a new card.
3. Run `/sync-content` to apply the changes to the website.

Rules:

- Cards appear on the site in the order they appear here. Move a card to reorder
  it; delete a card to remove it.
- Each card starts with a `###` heading. Keep the field names (`Role:`, `Dates:`
  and so on) exactly as written.
- `Tags:` is a comma-separated list, so a single tag cannot contain a comma.
- `*text*` is italic, `**text**` is bold, and `<br>` is a line break.
- To split a project text block into paragraphs, leave a blank line and indent
  the next paragraph four spaces so it lines up under the first.
- Each template says which fields are optional. Do not leave any other field
  blank; `/sync-content` will stop and ask.
- Icons, colors, layout and analytics code are not in this file.

## Page settings

Text that is not inside a section: what search engines, browser tabs and link
previews show, plus the navigation bar and footer.

- Browser tab title: Daniel Rueda-Ramirez
- Social preview title: Daniel Rueda-Ramirez | Business Analytics & Consulting
- Search and social description: Portfolio of Daniel Rueda-Ramirez — Business Analytics and Impact Consulting student at Notre Dame specializing in data analytics, impact consulting, process automation, and AI implementation. Experienced in Python, SQL, R, PowerBI, Tableau, and machine learning.
- Author: Daniel Rueda-Ramirez
- Search keywords: Daniel Rueda-Ramirez, Business Analytics, Impact Consulting, Notre Dame, management consulting, data analytics, predictive modeling, Python, SQL, R, PowerBI, Tableau, machine learning, operational strategy, business intelligence, data science
- Navigation name (top left): Daniel Rueda-Ramirez
- Navigation links:
  - Home -> #home
  - About -> #about
  - Experience -> #experience
  - Education -> #education
  - Projects -> #projects
  - Skills -> #skills
  - Contact -> #contact
- Footer: © 2026 Daniel Rueda-Ramirez. All rights reserved.

## Hero

- Name: Daniel Rueda-Ramirez
- Tagline: Analyzing Data · Optimizing Systems · Driving Strategic Growth
- Description: Senior at Notre Dame who has cut operations documentation time by 20%, synthesized a decade of customer data to drive retention strategy, and engineered a data-driven market entry strategy into the African continent, all within a single internship. I optimize processes and drive strategy by combining data analysis, machine learning, process automation, and consulting frameworks into analysis that non-technical executives can act on.
- Headshot file: assets/headshot.jpg
- Headshot description (for screen readers): Daniel Rueda-Ramirez — Business Analytics and Impact Consulting student at the University of Notre Dame
- Contact bubbles (in order): Email, LinkedIn, Phone
- Resume button label: Download Resume

The email address, phone number, LinkedIn link and resume file are set once, under
Contact.

## About

- Heading: About

One paragraph per block, separated by a blank line.

I study Business Analytics and Impact Consulting within the Business Honors Program at the University of Notre Dame, a merit-based, interdisciplinary program that combines rigorous quantitative training in machine learning, predictive analytics, and data management with the structured problem-solving and client communication frameworks of management consulting. It is the kind of program that prepares you to walk into any room, find the highest-leverage problem, and build the solution.

At Verso Ministries, I walked into a Google Sheets operation and began to identify systems I could improve with my technical toolkit from day one. Within months, I had transformed manual processes with technically sophisticated data infrastructure and automated workflows, which have allowed the company to effectively manage trip logistics for over 100 trips and launch a market entry strategy into the African continent. The instinct to look at a process that everyone else has accepted and see exactly how it could be better is a defining characteristic of my work ethic and the fuel behind my analytical and technical rigor.

Outside of business work, I lead music ensembles as a conductor, pianist, and baritone. Five years of managing high-stakes performances, running rehearsals under tight time constraints, and getting rooms full of people to move in the same direction have taught me more about leadership than any classroom. It turns out that standing in front of a choir and standing in front of a client are not as different as they seem.

I am eager to bring that growth-oriented drive to organizations where the problems are hard, the stakes are real, and the work actually matters. What that looks like in practice awaits below.

## Experience

- Heading: Experience

Newest first.

**Template** (copy, paste above the first card, fill in):

```markdown
### Company name
- Location: City, ST
- Role: Job title
- Dates: Mon YYYY - Mon YYYY
- Intro: One or two sentences on what the organization does and your place in it.
- Bullets:
  - First accomplishment.
  - Second accomplishment.
- Tags: Skill one, Skill two, Tool one
```


### Verso Ministries

- Location: South Bend, IN
- Role: Pilgrim Support Intern
- Dates: Aug 2026 - Present
- Intro: Verso Ministries organizes Catholic pilgrimages for 1,000+ global travelers, with various standard and custom itineraries across five continents, coordinating trip logistics on behalf of trip leaders with Destination Management Companies. As a pilgrim support intern, I serve as a point of contact for travelers throughout their trip, resolving portal and documentation questions for non-technical users while building the automated tracking that keeps more than 2,100 pilgrims' passports, flights, and payments on schedule.
- Bullets:
  - Architected an automated pipeline for tracking task completion for over 2,100 customers using APIs and Google Apps Script
  - Provide technical support to clients navigating trip portal software, achieving an 86% satisfaction score by simplifying digital processes for non-technical users
  - Maintain detailed customer interaction records to support departmental logistics and process improvement
  - Serve as a point of contact for pilgrim inquiries, delivering personalized support across the client lifecycle
  - Manage passport compliance, flight details, and payment records to ensure proper documentation and keep itineraries on schedule
- Tags: Technical Support, Process Automation, CRM Management (HubSpot CRM), Customer Support, Compliance Documentation

### Dhiyasoft LLC

- Location: Remote
- Role: App Developer Intern
- Dates: Jun - Aug 2026
- Intro: Dhiyasoft LLC is a certified Salesforce consulting partner based in Wayne, New Jersey, specializing in Salesforce CRM implementation, Data Cloud solutions, and enterprise digital transformation for business clients. Reporting directly to founder Sriram Srinivasan, this role sits at the intersection of software development and technology consulting — building, testing, and documenting application features within a client-facing tech consulting environment.
- Bullets:
  - Contributed to the development and verification of Salesforce application features, identifying and resolving software issues through structured debugging, user story execution, and formal code review
  - Collaborated with the consulting team, maintaining client deliverable quality through structured documentation updates and daily progress reporting across all assigned development tasks
  - Operated enterprise CRM ecosystems, Salesforce integrations, and technology consulting workflows in a certified Salesforce partner environment
- Tags: CRM Development, User Story Execution, Code Review, Technical Documentation, Agile Development, Salesforce, Apex, Jira, VS Code, ESLint

### Verso Ministries

- Location: Notre Dame, IN
- Role: Operations Intern
- Dates: Aug 2025 - May 2026
- Intro: Verso Ministries organizes Catholic pilgrimages for 1,000+ global travelers, with various standard and custom itineraries across five continents, coordinating trip logistics on behalf of trip leaders with Destination Management Companies. As an operations intern, I sit at the intersection of data infrastructure, process optimization, and client-facing logistics, building the systems that keep complex international travel operations running reliably.
- Bullets:
  - Engineered a data-driven market entry strategy into the African continent by scraping, cleaning, and benchmarking DMC service offerings across the region, driving informed decision-making for new business partnerships and widening the company's global footprint
  - Synthesized 10 years of disparate customer data from multiple sources using Python for a targeted outreach strategy, driving a personalized approach to customer engagement and retention
  - Identified critical friction points in documentation workflows, automating manual processes using spreadsheet functions, backend JavaScript, and Google Gemini to engineer SOPs that reduced documentation time by 20% across 100+ trip offerings
  - Maintained a 100% ticket resolution rate in HubSpot CRM within a 24-hour SLA across all customer inquiries
  - Managed sensitive datasets integrating traveler flight, health, and passport information for international DMCs, ensuring data integrity across a high-stakes, compliance-sensitive operation
- Tags: Logistics Management, International Logistics, Python, Google Apps Script, Web Scraping, Workflow Optimization, HubSpot CRM, SOP Development

### Confidential Hedge Fund

- Location: Bethesda, MD
- Role: Research & Analytics Intern
- Dates: Jul - Aug 2025
- Intro: Embedded within a boutique Bethesda hedge fund for a two-month engagement, I built data infrastructure and research pipelines to inform investment decisions for senior staff. The role was fast-paced and output-driven, with findings presented directly to investment leadership within days of completion.
- Bullets:
  - Synthesized complex market and industry research into executive-ready intelligence, delivering findings directly to senior investment leadership to inform high-stakes portfolio decision-making
  - Developed Python scripts to scrape and process bulk financial data at scale, storing structured results in MongoDB to automate and accelerate the firm’s decision-making pipeline
  - Architected web-scraping tools to systematically extract critical metadata from financial news sources and industry publications, dramatically reducing the time required to surface accurate market intelligence
- Tags: Python, MongoDB, Web Scraping, Market Research, Executive Communication

### Dietrich Logistics

- Location: Bogotá, Colombia
- Role: Accounting & Sales Research Intern
- Dates: Jul - Aug 2024
- Intro: Dietrich Logistics is an international freight and logistics company based in Bogotá, Colombia, operating with a global footprint across four continents. This internship was conducted entirely in Spanish within a Colombian business environment, combining accounting operations, ERP data management, and market research to support the company’s expansion into southern Asia.
- Bullets:
  - Conducted data-driven market research to identify and qualify hundreds of potential logistics providers across southern Asia, directly supporting an international business expansion initiative
  - Logged and audited 80+ international shipping transactions within the company’s ERP system, ensuring high data accuracy across cross-border financial records
  - Revised the company’s account plan and streamlined international record-keeping workflows, improving organizational efficiency across the accounting function
- Tags: ERP Systems, Excel, Market Research, Spanish

## Education

- Heading: Education

**Template:**

```markdown
### School name
- Dates: Mon YYYY - Mon YYYY
- Degree: Degree or diploma
- GPA: 0.00
- Bullets:
  - Major, minors, honors or achievements.
- Coursework heading: Relevant Coursework
- Coursework tags: Course one, Course two
```

The two `Coursework` lines are optional; delete both to leave coursework off a card.

### University of Notre Dame

- Dates: Aug 2023 - May 2027
- Degree: Bachelor in Business Administration
- GPA: 3.63
- Bullets:
  - Major: Business Analytics
  - Minors: Business Honors Program, Impact Consulting, Liturgical Music Ministry, and Theology
  - Competed in five corporate consulting case competitions, delivering data-driven strategic recommendations to senior representatives from Deloitte, KPMG, West Monroe, DaVita, and 84.51° — each involving independent research, quantitative analysis, and a live presentation under time constraints.
  - Completed weekly real-world pricing analytics cases throughout the semester, producing both managerial memos and technical R reports for each, including the Tropicana/Jewel retail pricing case featured in the Projects section.
- Coursework heading: Relevant Coursework
- Coursework tags: Pricing Analytics, Business Problem Solving, Data Management, Predictive Analytics, Machine Learning, Unstructured Data Analytics, Cloud Computing, Innovation & Design Thinking

### The Heights School

- Dates: Sept 2019 - June 2023
- Degree: High School Diploma
- GPA: 3.98
- Bullets:
  - Completed a merit-based senior thesis program selective to 14 students, writing and presenting a 50-page research paper synthesizing 60+ sources — including NIH studies, peer-reviewed psychology journals, and primary Gallup data — to analyze the behavioral economics of smartphone addiction.
  - AP Scholar with Distinction

## Projects

- Heading: Projects

**Template:**

```markdown
### Project title
- In development: no
- Text blocks:
  - Context: What the project was and who it was for.
  - Problem: The question or pain point.
  - Approach: What you built or analyzed, and how.
  - Key Findings & Recommendation: What came out of it.
- Tags: Skill one, Tool one
- Buttons:
  - Type: download
    Label: Download Report
    File: assets/File-Name.pdf
    Analytics label: Short Name Report
  - Type: contact link
    Label: Interested in Project? Let's talk
    Analytics label: Project Inquiry
```

- `In development: yes` shows the "In Development" badge next to the title.
- Text blocks can have any labels and any number of blocks; they appear in order.
- `Buttons` is optional. A `download` button needs its file placed in `assets/`
  first. A `contact link` button scrolls to the contact form.
- `Analytics label` is the name this button's clicks are reported under in Google
  Analytics. Visitors never see it.

### United Airlines Consulting Project

- In development: no
- Text blocks:
  - Context: Solo consulting project for a business problem solving class analyzing United Airlines' customer satisfaction crisis amid its "United Next" expansion strategy. This presentation was prepared as a strategic recommendation for United CEO Scott Kirby and COO Brett Hart.
  - Problem: United's aggressive scheduling at core hubs like ORD and EWR pushed on-time performance below 70%, with each delay costing 16 NPS points per passenger. With the FAA implementing flight caps at the world's busiest airports, how can United mitigate the customer satisfaction damage that each delay causes, and what is the financial case for doing so?
  - Approach: Built a full consulting engagement from the ground up. Developed a comprehensive fact pack covering United's competitive position, operational performance at core hubs, financial trajectory, and customer satisfaction benchmarks relative to Delta and Southwest. Conducted a PESTEL analysis and structured an issue tree to identify the highest-leverage intervention points. Used Bain & Co. NPS driver research, JD Power customer satisfaction data, Airlines for America delay cost benchmarks, BTS flight data, FAA operational records, and DOT enforcement data to build the evidentiary foundation. Designed a three-phase implementation timeline spanning June 2026 to May 2029, and built a detailed five-line-item P&L model projecting costs and returns across platform build, delay cost savings, cancellation avoidance, call-center deflection, and NPS retention lift.
  - Key Findings & Recommendation: Proposed *ClearPath*, an AI-powered United app feature that proactively flags flights with high delay probability, notifies passengers before they leave home, and enables free rebooking in under one minute. *ClearPath* directly addresses the two primary NPS destroyers: untimely notification and slow rebooking, resulting in projected +10 NPS per customer and $608M in savings by Year 3. A three-phase rollout was designed beginning with ML model training on BTS and ASPM delay data, piloting, and then scaling.
- Tags: Consulting, Executive Communication, Financial Modeling, Industry Research, KPI Identification, Structured Problem Solving, Presentation Design, App Mockup, Canva, UX Pilot
- Buttons:
  - Type: download
    Label: Download Memo
    File: assets/United-Airlines-Memo.pdf
    Analytics label: United Airlines Memo
  - Type: download
    Label: Download Slide Deck
    File: assets/United-Airlines-Slidedeck.pdf
    Analytics label: United Airlines Slidedeck
  - Type: download
    Label: Download Toolkit
    File: assets/United-Airlines-Toolkit.pdf
    Analytics label: United Airlines Toolkit

### FlightSense: Flight Price Tracking & Prediction Platform

- In development: yes
- Text blocks:
  - Context: A solo full-stack personal project built to help travelers book flights at their price floor. FlightSense is a Python-based flight tracking platform with a live data pipeline, persistent database, and an interactive user dashboard. Currently in active development with a machine learning price prediction layer and automated email notifications planned as next phases.
  - Problem: Travelers currently rely on their own methods for predicting flight prices, which are constantly fluctuating. Additionally, those managing multiple upcoming flights across different itineraries have no centralized, automatically-updating tool that aggregates their flight data in one place. This lack of visibility makes it difficult for travelers to book more affordable flights and manage their travel plans effectively.

    Beyond the personal inconvenience, this problem has broader economic implications. Airlines use dynamic pricing algorithms to maximize revenue, which can lead to price volatility and unpredictability for consumers. By providing a tool that helps travelers identify price floors and manage their itineraries, FlightSense aims to empower consumers to make more informed decisions, potentially leading to more competitive pricing in the airline industry overall.

    Finally, while a few existing datasets track flight prices, they only record one price per flight. This is insufficient for predicting price floors, which requires a time series of prices for each flight. This project addresses this gap by scraping and storing three price points per day for each flight, starting 180 days before departure, enabling more accurate predictions of when a flight is likely to be priced at its floor.
  - Approach: Built a full-stack application in Python with embedded HTML for the user interface. Implemented a dual-source flight data scraping pipeline using fast-flights as the primary source and SerpAPI as a fallback, with flights refreshing automatically every few hours. All flight data is stored and managed in a PostgreSQL database. The user interface allows travelers to create trips, add flights to each trip, and view a live dashboard tracking the status of all upcoming flights across all itineraries.

    Currently, an automated pipeline using the same logic as FlightSense is collecting real-world pricing data eight times per day, across 1,241 combinations of 325 unique airports across the globe. Each airport pair simultaneously tracks four fixed departure dates spread across different seasons, producing a continuous time-series where the key feature — days to departure — decreases naturally from ~180 days to 0, capturing the full pricing arc without artificial bucketing. The dataset achieves broad representational coverage across four distance bands (short, medium, long, and ultra-long-haul), seven geographic regions, and includes rich connection-aware features such as hub tier classification, corridor efficiency scores, and layover quality metrics for the 70+ known global connection hubs. At current collection velocity, the pipeline accumulates sufficient labeled training examples within 60-90 days to train an XGBoost price floor prediction model targeting ≥70% precision on "buy now" signals — the core output that drives FlightSense's booking alert engine.

    Once data collection and the XGBoost model are complete, the model and an automated email notification system will be implemented to alert users when their flight is predicted to be at its price floor. Once the first iteration is running, the model will be enhanced to update based on live data.
  - Current Status & Roadmap: **Phase 1 (Complete):** Live flight tracking dashboard with PostgreSQL-backed data pipeline and automatic refresh. <br> **Phase 2 (In Progress):** Automated data collection for machine learning. <br> **Phase 3 (Planned):** Machine learning price prediction model trained on recent flight price data from 325 airports worldwide. <br> **Phase 4 (Planned):** Automated email notification system to alert users when a tracked flight is predicted to reach its floor.
- Tags: Python, PostgreSQL, Web Scraping, SerpAPI, HTML, Data Pipeline Architecture, Full-Stack Development, Streamlit, Machine Learning (Planned)
- Buttons:
  - Type: contact link
    Label: Interested in FlightSense? Let's talk!
    Analytics label: FlightSense Inquiry

### Tropicana Retail Pricing & Merchandising Optimization Analysis

- In development: no
- Text blocks:
  - Context: Pricing analytics case study for Jewel, a high-low grocery retailer, that was evaluating whether to reduce its promotional reliance on Tropicana 12oz frozen orange juice after profits dropped from $233,075 in 2016 to $139,237 in 2017 despite a surge in units sold. The CEO was concerned the store had gone too far with promotions. This analysis was prepared for Debabrata Chakravarti, Jewel's head merchant, to present to CEO Stephen Gray.
  - Problem: Jewel's promotional strategy for Tropicana shifted dramatically across three years, with deep, frequent promotions in 2017 boosting volume but cratering margins, and a pullback in 2018 recovering profits but sacrificing units sold. The central question was what promotion frequency and depth would maximize Jewel's profitability for Tropicana in 2019 and whether a proposed alternative scenario of more frequent, deeper promotions would outperform the 2018 baseline.
  - Approach: Analyzed three years of weekly point-of-sale data across four retail price zones (High, Medium, Low, CubFighter) using R. Built a log-log regression model with interaction terms for merchandising, price zone, and year to isolate the individual and combined effects of price and merchandising on units sold. Identified and removed a statistically anomalous outlier at week 124 using IQR analysis. Ran a scenario analysis comparing 2018 actual profits against a proposed Scenario 1 featuring more frequent and deeper price promotions.
  - Key Findings & Recommendation: The regression model revealed a baseline price elasticity of −2.8, meaning consumers are moderately price sensitive. That sensitivity nearly doubles during merchandising weeks, with a 4.02× sales multiplier and a combined elasticity of −3.976. Scenario 1 generated $17,311 less profit than the 2018 baseline ($104,342 vs. $121,653), confirming that deeper promotions cut too far into margins without proportionally compensating through volume. I recommend that Jewel offer more frequent but shallower price promotions, always paired with merchandising, to capture the 4.02× volume multiplier while protecting profit margins. This middle-ground strategy outperforms both the 2017 deep-discount approach and the proposed Scenario 1.
- Tags: R, ggplot2, Linear Regression, Log-Log Modeling, Scenario Analysis, Outlier Detection, Pricing Strategy, Data Visualization, Managerial Reporting
- Buttons:
  - Type: download
    Label: Download Report
    File: assets/Tropicana-Merchandising-Analysis.pdf
    Analytics label: Tropicana Report

### TaskFlow: Cross-Platform Personal Productivity System

- In development: yes
- Text blocks:
  - Context: A solo-designed, iteratively developed native desktop productivity application built for myself to unify task management, goal tracking, project planning, habit monitoring, and personal analytics into a single cohesive system. Architected from scratch and rebuilt from a Python/CustomTkinter prototype into a production-grade cross-language desktop app — TypeScript/React frontend running inside a Rust/Tauri shell, with all data persisted locally in SQLite.
  - Problem: Most productivity tools treat tasks, habits, projects, and wellbeing as separate, disconnected concerns. The goal was to design a system that models them as interconnected data feeding a unified scoring and analytics engine — giving a genuine, data-driven picture of how day-to-day execution accumulates over time, with enough flexibility to handle the competing demands of coursework, music direction, multiple internships, and personal projects simultaneously.
  - Approach: Designed and architected a cross-language desktop application with TypeScript/React UI communicating with a Rust backend over Tauri IPC — chosen over Electron for smaller binary size, lower memory footprint, and native OS-level filesystem access. Implemented Google Calendar OAuth2 with a Rust-side loopback TCP listener, Google Places API with automatic OpenStreetMap Nominatim fallback for resilience, and rich text editing via Tiptap. Designed a versioned SQLite schema supporting multi-level task subgroups as JSON paths, RFC 5545 RRULE recurrence generation with scope-aware editing, and a carry-forward scoring engine that computes rolling daily averages across tasks, habits, routines, and happiness data. Packaged with an NSIS Windows installer and custom icon generation pipeline.
  - Key Findings & Recommendation: Delivered five interconnected modules — a Tasks workspace with Google Calendar day view, drag-and-drop reordering, multi-level nested subgroups, deferred visibility, and native desktop notifications; a Goals module with RRULE-based habit tracking, reorderable routines, and daily happiness scoring with 7-day and 30-day trend views; a Projects layer with hierarchical Section to Milestone to Checkpoint structure, rich text documentation via Tiptap, and full task behavioral parity; and a gamified Dashboard with a five-tier leveling system, composite scoring engine rewarding execution quality over quantity, a full-year activity heatmap, and a scatter chart correlating happiness scores against productivity. Shared interaction primitives built once and reused across all modules to eliminate cognitive load and code duplication.
- Tags: TypeScript, React, Rust, Tauri, SQLite, OAuth2, Google Calendar API, REST API Integration, Desktop App Development, Local-First Architecture, Windows Packaging, TanStack Query, Framer Motion, Tiptap, Product Design, UX Design, AI-Augmented Development
- Buttons:
  - Type: contact link
    Label: Interested in TaskFlow? Let's talk!
    Analytics label: TaskFlow Inquiry

### Sectional: Self-Hosted Stem Separation & Practice Rig

- In development: yes
- Text blocks:
  - Context: A self-hosted stem separation and practice tool, built for personal use as a pianist and singer, running entirely on a CPU-only laptop with no GPU or cloud dependency.
  - Problem: Commercial stem-separation tools (e.g. Moises) collapse piano, strings, and backing vocals into a single undifferentiated "other" bucket, require uploading audio to third-party servers, and offer a fixed instrument set.
  - Approach: Built a six-stage subprocess pipeline (Demucs, BS-RoFormer specialist checkpoints, CNN14 cost-gating) behind a FastAPI backend with priority job queueing. Every stage is benchmarked in seconds of processing per second of audio, and a cheap CNN14 classifier gates whether a ~9x-real-time specialist extraction is worth running at all. The core technical contribution is reconstructing stems as a residual (mix minus everything else, via ridge-regularized least squares) rather than trusting raw model output directly — this took usable string audio from 28% to 100% coverage of playing time. Time-varying subtraction fits (3-second windows, crossfaded) and per-interferer removal methods (magnitude subtraction, ratio masking, level restoration) handle bleed that a single global gain can't catch. A browser-based mixer (Web Audio API) provides per-family faders and real-time level meters, paired with a teleprompter and chord chart that share a single transport across browser tabs.
  - Key Findings / Status: Base separation validated by ear across 16 songs; piano and high-band strings cleanup approved on listening; mixer, library, and teleprompter flows verified end-to-end. Known limitations (brass, woodwinds, a tempo-detection octave error) are documented with their measured causes rather than hidden. A 29-rule internal conventions document codifies failure modes discovered when measurements disagreed with what the audio actually sounded like.
- Tags: Python, PyTorch, FastAPI, Signal Processing, Web Audio API, JavaScript, Demucs, Machine Learning, Audio Engineering, REST API Design, Performance Optimization, Empirical Verification, Scientific Methodology, CPU-Constrained Inference, AI-Augmented Development
- Buttons:
  - Type: contact link
    Label: Interested in Sectional? Let's talk!
    Analytics label: Sectional Inquiry

### Delta Airlines Flight Delay Performance Dashboard

- In development: no
- Text blocks:
  - Context: Operational analytics dashboard built to benchmark Delta Airlines' flight delay patterns across routes, hubs, and delay categories. The route and delay cause analysis from this dashboard laid the foundation for the subsequent United Airlines consulting project.
  - Problem: Delay data in its raw form is voluminous and difficult to interpret, with thousands of rows of flight records across hundreds of routes, dozens of airports, and multiple delay cause categories. This project sought to understand how delay patterns distribute across Delta's hub network and what the anatomy of a delay looks like in terms of cause and cascade.
  - Approach: Sourced flight delay data from the Bureau of Transportation Statistics and built an interactive dashboard in Microsoft PowerBI using DAX measures to calculate on-time performance rates, average delay minutes, and delay cause breakdowns by hub, route, month, and delay category. Structured the dashboard around three analytical layers: hub-level OTP benchmarking, delay cause decomposition (carrier-caused, NAS, weather, late aircraft, security), and reactionary delay chain analysis, examining how an initial delay propagates through a hub's daily operation as late aircraft trigger cascading downstream delays. Particular attention was paid to the late aircraft category, which accounts for approximately 40% of all delay minutes industry-wide and is the primary driver of the reactionary delay domino effect.
  - Key Findings & Recommendation: The dashboard allows the user to focus on specific hubs and route types, particularly short-haul high-frequency corridors where reactionary delays compound most aggressively. Late aircraft delays are the single largest controllable delay category, reinforcing the subsequent United Airlines project thesis that proactive delay prediction and early passenger notification is the highest-leverage intervention available to an airline. The dashboard provides the competitive benchmarking foundation for understanding what operational excellence in delay management must entail.
- Tags: Power BI, DAX, Operations Analytics, Data Visualization
- Buttons:
  - Type: download
    Label: Download Dashboard
    File: assets/Delta-Flight-Delay-Dashboard.pbix
    Analytics label: Delta Dashboard

## Skills

- Heading: Skills

**Template:**

```markdown
### Category name
- Icon: bi-icon-name
- Tags: Skill one, Skill two
```

`Icon` is a Bootstrap Icons name; browse them at [https://icons.getbootstrap.com/](https://icons.getbootstrap.com/).

### Data & Analytics

- Icon: bi-database
- Tags: Python, Pandas, NumPy, R, SQL, PostgreSQL, MongoDB, Excel, Web Scraping

### Visualization

- Icon: bi-bar-chart-line-fill
- Tags: Tableau Desktop (Salesforce Certified Tableau Desktop Foundation), Microsoft PowerBI, Streamlit, ggplot2

### Development

- Icon: bi-code-slash
- Tags: HTML, TypeScript, React, Rust, Tauri, FastAPI, Web Audio API, Apex, ESLint, VS Code Salesforce Extensions, GitHub

### AI & Automation

- Icon: bi-robot
- Tags: AI Workflow Automation, Generative AI Prompting, Claude Code, Gemini Deep Research, GitHub Copilot, Google AppsScript, NotebookLM, Product Design, Desktop App Development, Windows Packaging

### Machine Learning & Unstructured Data Analytics

- Icon: bi-eye
- Tags: Scikit-learn, HuggingFace, YOLO, PyTorch, Signal Processing, Audio Engineering, CNN14, Demucs

### Enterprise Tools

- Icon: bi-briefcase
- Tags: HubSpot CRM, Salesforce, Jira, Microsoft Office, Google Workspace, Zoom Workspace, Canva, Slack, WordPress, YouLi, Asana

### Languages

- Icon: bi-globe
- Tags: English (Fluent), Spanish (Fluent)

## Contact

- Heading: Let's Connect!
- Blurb: Senior at the University of Notre Dame, graduating May 2027. Actively recruiting for full-time roles in tech consulting and business analytics beginning summer 2027. U.S. citizen eligible for security clearance.
- Links:
  - danielrr0713@gmail.com -> mailto:danielrr0713@gmail.com
  - +1 240-401-0249 -> tel:+12404010249
  - LinkedIn -> https://www.linkedin.com/in/daniel-rueda-ramirez-8a2963265/
  - GitHub -> https://github.com/druedaramirez
- Resume button label: Download Resume
- Resume file: assets/Daniel Rueda-Ramirez_Resume.pdf
- Resume downloads as: Daniel-Rueda-Ramirez-Resume.pdf

The email address, phone number, LinkedIn link and resume file are also used in
the Hero section and in the form's failure message. `/sync-content` updates every
copy from the values here.

### Contact form

- Fields:
  - Name | placeholder: Your name | required
  - Email | placeholder: your@email.com | required
  - Organization | placeholder: Company or university | optional
  - Message | placeholder: What's on your mind? | required
- Send button: Send Message
- Button text while sending: Sending…
- Success message: Message Sent! ✓
- Failure message: Failed to Send. Please email danielrr0713@gmail.com directly.
