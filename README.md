# Dev Panchal

**Full-stack developer working across web apps, data analysis and AI, and the 3D layer by hand.**

Final-year B.Tech CSE (AI & Data Science) at ITM SLS Baroda University. Based in Vadodara, Gujarat, working remote.
Web Development Intern at ANK Design & Automation Solutions (Aug–Oct 2026). Freelance clients across Gujarat. Ranked #8 at Vibe2Ship.

[Portfolio](https://dev-panchal.vercel.app) · [Resume](https://dev-panchal.vercel.app/Dev_Panchal_Resume.pdf) · [GitHub](https://github.com/Dev010904) · [LinkedIn](https://linkedin.com/in/dev-panchal-9b8047383) · [Email](mailto:devpanchal.web@gmail.com) · [WhatsApp](https://wa.me/917284923872)

---

## What I actually do

Three things, and every project below is evidence for at least one of them.

- **Web apps and business software.** Next.js, TypeScript and PostgreSQL, with the rules enforced in the database rather than only on the screen. I built the system a company now runs its inquiries, orders, invoices and attendance on.
- **Data analysis.** Python, pandas, SQL and Power BI: clean it, test it, question it, then a dashboard someone can act on. Before answering a question I check whether the data can answer it at all.
- **AI in the product.** The Gemini API, LLMs, RAG and agents, wired into things people use, with a plan for when the model is slow or wrong.

And I build the 3D and motion layer by hand. My portfolio is one persistent Three.js canvas with hand-written GLSL, no model files and no downloaded assets.

---

## Experience

### Web Development Intern — ANK Design & Automation Solutions LLP
**Vadodara · Aug 2026 – Oct 2026 · 3 months**

- Built **ANK Track** end to end: the company's internal inquiry-to-order management system, live in production and installed by staff as an app on phone and desktop. Inquiries with follow-up alarms, orders and payments, R&D budgets, IP renewals, clients, meetings and quality checks.
- Designed a **35+ table PostgreSQL database** across 45 migrations, with row-level security on every table and trigger-maintained ledgers. GST, totals and balances are calculated by the database, never typed by hand.
- Built quotations, tax invoices and delivery challans: GST per line, gapless numbering that restarts every financial year, and print-ready PDFs generated on the server with headless Chromium.
- Added **fingerprint attendance**: biometric devices send punches over HTTPS, a rules engine works out present, half-day, late, overtime and missed punches, and admins download a monthly Excel register.
- Built the **analytics reports** (cohort-based inquiry conversion, order value by month, payment aging, loss reasons) and led a **security review** of the live system: patched a critical Next.js vulnerability, moved role permissions into the database and blocked forged API writes.
- Client websites: audited a prospect's site (21 findings ranked by severity) and built the pitch concept with a real-time three.js 3D configurator; built the agency's 5-tier website rate card with a cost calculator and printable proformas, and a sample online store.

`Next.js 15` `React 19` `TypeScript` `Supabase` `PostgreSQL` `Recharts` `Vercel`

### Freelance Web Developer — Independent
**Vadodara · 2026 – present**

- **Maruti Gases Pvt. Ltd.**, Halol GIDC: a website for an industrial and medical gas manufacturer, won from a live sample built on their own details. An interactive gas explorer, products, cylinder care, and a quote form that goes straight to WhatsApp. [View site](https://mgpl-sample.vercel.app)
- **Panchal Enterprise**: PE Daily Report, the stock and ledger software the business runs on every day (below).
- **Panchal Gases & Panchal Enterprise**: two live websites, built and kept running.

---

## Selected work

### PE Daily Report — stock & ledger software for an industrial-gas distributor
**Client software · In daily use · Private**

Replaced the business's paper cylinder register with an Android app and a PC web app from one Flutter code base.

- Supply, empty, cash and bill entries, daily stock, cylinder balances for each company, filling-plant and damaged-cylinder tracking, and day and register PDFs.
- **Offline-first:** entries made at the godown are stored in SQLite and sync to the cloud when the internet returns. 15 releases shipped with in-app updates, and the first version's phone data moved to the cloud automatically.
- Tally-style keyboard-only entry on PC. Row-level security, a change history nobody can edit, encrypted sessions and a Cloudflare Worker with strict security headers. Automated tests cover the stock rules, ledgers, sync and the full app flow.

`Flutter` `Dart` `Supabase` `SQLite` `Cloudflare Workers`

### APL Logistics — supply-chain profitability analysis
**Data analysis · Solo**

- Analysed **180,519 order lines** (20,261 customers, 164 countries, $31.64M revenue) to find which customers, products and regions actually make money.
- **18.69% of order lines lose $3.71M**, and one customer in five is loss-making (−17.01% margin). Discounting is not the cause: the correlation between discount and margin is −0.0015.
- Tested data-cleaning pipeline (11 checks), a 17-page research paper, an executive summary and an interactive dashboard.

[Live dashboard](https://apl-logistics-profitability.streamlit.app) · [Source](https://github.com/Dev010904/apl-logistics-profitability-analysis) · [Research paper](https://github.com/Dev010904/apl-logistics-profitability-analysis/blob/main/reports/research_paper.pdf)

`Python` `pandas` `Plotly` `Streamlit` `pytest`

### Smart-factory process health diagnostics — Thales Group dataset
**Data analysis · Solo**

- Analysed **100,000 sensor records** from 50 machines over 69 days to check machine health before building a predictive-maintenance model.
- Showed the target label is a **3-line threshold rule** that reproduces 99.998% of labels, and that no sensor pair correlates above r = 0.0075 after multiple-testing correction. The data was synthetic; a model trained on it would have scored near-perfectly and meant nothing.

[Source](https://github.com/Dev010904/thales-smart-factory-diagnostics)

`Python` `pandas` `Seaborn` `Streamlit`

### KAAM KARO — AI-powered deadline survival app
**Solo build · Vibe2Ship Hackathon (Coding Ninjas × Google for Developers) · Live**

A multilingual (English, Hindi, Gujarati) productivity app that uses the Google Gemini API to generate day-by-day task breakdowns and classify every deadline in real time as **Safe, At Risk, Critical or Overdue**.

- Engineered an autonomous **Rescue Mode** that triggers an emergency recovery plan the moment a deadline turns critical.
- Built a local fallback planning engine so the app stays usable during API latency or rate limiting. The AI is a feature, not a single point of failure.
- Shipped the full stack solo: React 19, TypeScript, Vite, Tailwind, Node/Express, Firebase Firestore + Auth, deployed to Google Cloud Run.

[Live app](https://kaam-karo-438754462552.us-west1.run.app) · [Source](https://github.com/Dev010904/KAAM-KARO-Web-App) · [Project doc](https://docs.google.com/document/d/1vwfp8hTZQeC5pEsjglndPLwIyxIXtnyS4SvliP-DicI/edit)

### Portfolio — a procedural 3D web experience
**Solo build · Live · [dev-panchal.vercel.app](https://dev-panchal.vercel.app)**

A scroll-choreographed WebGL site on a **single persistent Three.js canvas that survives route changes**: no remounts, no white flashes. Camera, materials and geometry morph between scene states instead of tearing down and rebuilding.

- The identity is a **DP monogram that only resolves as `DP` from exactly one viewing angle**: one shared stem carrying two bowls at different Z depths. Rotate it and it becomes abstract sculpture. Generated entirely in code.
- Hand-written GLSL for the sweep lines, lightning discharge, blast, card dissolve and footer fog. A light "drawing sheet" chapter whose figures plot themselves as you scroll, including a margin histogram drawn from the real APL Logistics data.
- Every animation is driven from **one `gsap.ticker` loop** with `1 - exp(-k·dt)` damping, so motion is genuinely frame-rate independent rather than 2.4× fast on a 144Hz display.
- Profiled and fixed real forced-layout thrash: the annotation path went from **0.255 ms/frame to 0.014 ms**, and the worst section's p95 frame time dropped 18.7 ms → 12.4 ms.

[Source](https://github.com/Dev010904/dev-panchal-portfolio)

### Panchal Gases & Panchal Enterprise — two live commercial sites
**Design + build · In production**

Cinematic dark-theme marketing sites for industrial gas businesses, built on a **hand-rolled scroll engine with zero third-party animation libraries**.

- WebGL fragment-shader backgrounds, `IntersectionObserver`-driven scroll scenes and cursor-reactive tilt, while keeping page weight low and honouring `prefers-reduced-motion`.
- Resolved live production issues across CSP headers, cross-device routing and map links; migrated transactional email from SMTP to the Resend HTTP API.

[panchalgases7.netlify.app](https://panchalgases7.netlify.app) · [panchalenterprise9.netlify.app](https://panchalenterprise9.netlify.app)

---

## Recognition

**Ranked #8** among the Top 15 Coding Ninjas learners at **Vibe2Ship**, India's largest vibe-coding hackathon, hosted by Coding Ninjas with Google for Developers, 2026.

**Certificate of Excellence (Top Performer)** in both IIT Mandi TIH Live data analytics modules: Analytics & Excel, and Power BI.

---

## Stack

| | |
|---|---|
| **Languages** | Python · TypeScript · JavaScript · SQL · Dart · Java · C |
| **Web** | Next.js 15 · React 19 · Node.js / Express · Tailwind CSS · REST APIs · PWAs · HTML5 · CSS3 |
| **Data** | pandas · NumPy · Matplotlib · Seaborn · Plotly · Power BI · Excel · Streamlit |
| **AI** | Google Gemini API · LLM integration & prompt engineering · RAG · AI agents & multi-agent systems · IBM watsonx Assistant |
| **Databases & cloud** | PostgreSQL · Supabase (Auth, Row-Level Security) · Firebase · SQLite · Vercel · Cloudflare Workers · Google Cloud Run · Netlify |
| **3D & motion** | Three.js · React Three Fiber · WebGL / GLSL shaders · GSAP · Lenis |
| **Mobile** | Flutter |

---

## Certifications

Selected from twelve issued credentials, newest first. Every one has a real certificate or badge behind it.

| Date | Credential | Issuer |
|---|---|---|
| Sep 2026 | Introduction to Big Data Tools | Simplilearn |
| Jul 2026 | AI Automation & Intelligent Solutions Internship | AICTE / IBM SkillsBuild |
| Jul 2026 | Intelligent Virtual Agents with IBM watsonx Assistant | IBM Training |
| Jul 2026 | Make Agentic AI Work for You: AI Agents, Multiagent Systems, RAG | IBM SkillsBuild |
| Jun 2026 | Getting Started with Generative AI: Foundations, LLMs, AI Ethics | IBM SkillsBuild |
| Jun 2026 | Text Analytics 101 | CognitiveClass.ai / IBM |
| May 2026 | Data Visualization with Power BI | IIT Mandi TIH Live × Coding Ninjas/NSDC |
| Apr 2026 | Introduction to Analytics & Excel | IIT Mandi TIH Live × Coding Ninjas/NSDC |
| Apr 2026 | Introduction to Agentic AI & LLM Architectures | Simplilearn |
| Jan 2026 | Data Analysis Workshop: "Ignite the Future" | M. S. University of Baroda |

Full archive with certificates: **[dev-panchal.vercel.app/credentials](https://dev-panchal.vercel.app/credentials)**

---

## Education

**ITM SLS Baroda University**, Vadodara, Gujarat
B.Tech, Computer Science & Engineering (AI & Data Science) · 2023–2027

**Data Analytics Program**, IIT Mandi TIH Live × Coding Ninjas (NSDC)
Feb 2026 – Oct 2026 · Analytics & Excel · Data Visualization with Power BI · SQL · Python for Data Analysis

---

## How I work

**Measure before claiming.** On the portfolio build, five separate "successes" turned out to be broken instruments: a counter returning the same value at every scroll position, a harness that never advanced a frame, a probe reading accumulated garbage. Now a number gets checked against a second, independent instrument before it goes anywhere near a README. The same goes for data: the smart-factory label looked like a prediction target and was really a rule of its own inputs.

**Put the rules where they cannot be skipped.** In business software the money and the permissions live in the database, so a stale tab or a forged request cannot get around them.

**Ship it, then keep it working.** Software a business uses every morning has no "after launch". The sites and apps I have shipped are live, and I still maintain them.

---

## Contact

**devpanchal.web@gmail.com** · **[WhatsApp](https://wa.me/917284923872)** · **[Resume](https://dev-panchal.vercel.app/Dev_Panchal_Resume.pdf)**

Open to full-time roles, freelance builds and hackathon teams. Vadodara, Gujarat · Remote.
