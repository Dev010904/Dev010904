# Dev Panchal

**Web developer. I build interfaces that behave like instruments, not templates.**

Final-year B.Tech CSE (AI & Data Science) at ITM SLS Baroda University. Based in Vadodara, Gujarat — working remote.
Three sites in production. Hand-written GLSL. No model files, no downloaded assets, no page builders.

[Portfolio](https://devpanchal04.netlify.app) · [GitHub](https://github.com/Dev010904) · [LinkedIn](https://linkedin.com/in/dev-panchal-9b8047383) · [Email](mailto:devpanchal.web@gmail.com) · [WhatsApp](https://wa.me/918460289432)

---

## What I actually do

I ship AI-integrated full-stack products end to end, and I build the 3D and motion layer by hand rather than reaching for a library that does it for me.

That distinction is the whole point. Most portfolio 3D is a downloaded `.glb` dropped into a scene. Mine is generated procedurally in code — every coordinate in the identity comes from one source file, and the geometry, the favicon and the SVG are all derived from it. When something is wrong, there is exactly one place to fix it.

The same instinct runs through the rest of my work: one animation loop instead of five, exponential damping so motion is identical at 60Hz and 144Hz, and a measurement before a claim.

---

## Selected work

### KAAM KARO — AI-powered deadline survival app
**Solo build · Vibe2Ship Hackathon (Coding Ninjas × Google for Developers) · Live**

A multilingual (English, Hindi, Gujarati) productivity app that uses the Google Gemini API to generate day-by-day task breakdowns and classify every deadline in real time as **Safe, At Risk, Critical or Overdue**.

- Engineered an autonomous **Rescue Mode** that triggers an emergency recovery plan the moment a deadline turns critical.
- Built a local fallback planning engine so the app stays usable during API latency or rate limiting — the AI is a feature, not a single point of failure.
- Shipped the full stack solo: React 19, TypeScript, Vite, Tailwind, Node/Express, Firebase Firestore + Auth, deployed to Google Cloud Run.

[Live app](https://kaam-karo-438754462552.us-west1.run.app) · [Source](https://github.com/Dev010904/KAAM-KARO-Web-App) · [Project doc](https://docs.google.com/document/d/1vwfp8hTZQeC5pEsjglndPLwIyxIXtnyS4SvliP-DicI/edit)

### Portfolio — a procedural 3D web experience
**Solo build · Live · [devpanchal04.netlify.app](https://devpanchal04.netlify.app)**

A scroll-choreographed WebGL site on a **single persistent Three.js canvas that survives route changes** — no remounts, no white flashes. Camera, materials and geometry morph between scene states instead of tearing down and rebuilding.

- The identity is a **DP monogram that only resolves as `DP` from exactly one viewing angle** — one shared stem carrying two bowls at different Z depths. Rotate it and it becomes abstract sculpture. Generated entirely in code.
- Hand-written GLSL for the sweep lines, lightning discharge, card dissolve and footer fog. Raymarched volumetric light shafts occluded by the mark's own geometry.
- Every animation driven from **one `gsap.ticker` loop** with `1 - exp(-k·dt)` damping, so motion is genuinely frame-rate independent rather than 2.4× fast on a 144Hz display.
- Profiled and fixed real forced-layout thrash: the annotation path went from **0.255 ms/frame to 0.014 ms**, and the worst section's p95 frame time dropped 18.7 ms → 12.4 ms.

[Source](https://github.com/Dev010904/dev-panchal-portfolio)

### Panchal Gases & Panchal Enterprise — two live commercial sites
**Design + build · In production**

Cinematic dark-theme marketing sites for industrial gas businesses, built on a **hand-rolled scroll engine with zero third-party animation libraries**.

- WebGL fragment-shader backgrounds, `IntersectionObserver`-driven scroll scenes, cursor-reactive tilt — while keeping page weight low and honouring `prefers-reduced-motion`.
- Resolved live production issues across CSP headers, cross-device routing and map links; migrated transactional email from SMTP to the Resend HTTP API.

[panchalgases7.netlify.app](https://panchalgases7.netlify.app) · [panchalenterprise9.netlify.app](https://panchalenterprise9.netlify.app)

---

## Recognition

**Ranked #8** among the Top 15 Coding Ninjas learners at **Vibe2Ship** — India's largest vibe-coding hackathon, hosted by Coding Ninjas with Google for Developers, 2026.

**Certificate of Excellence (Top Performer)** in both IIT Mandi TIH Live data analytics modules — Analytics & Excel, and Power BI.

---

## Stack

| | |
|---|---|
| **Languages** | Python · JavaScript · TypeScript · SQL · Java · C |
| **Frontend** | React 19 · Next.js 15 · Vite · Tailwind CSS · HTML5 · CSS3 |
| **3D & motion** | Three.js · React Three Fiber · WebGL / GLSL shaders · GSAP · Lenis |
| **Backend & cloud** | Node.js · Express · Firebase (Firestore, Auth) · Google Cloud Run · Netlify · Vercel |
| **AI & data** | Google Gemini API · Google AI Studio · IBM watsonx Assistant · Power BI · pandas · Excel |
| **Concepts** | LLM integration & prompt engineering · Agentic and multi-agent architectures · RAG · Responsible AI · DSA · Data visualization |

---

## Certifications

Selected from eleven issued credentials, newest first. Every one has a real certificate or badge behind it.

| Date | Credential | Issuer |
|---|---|---|
| Jul 2026 | AI Automation & Intelligent Solutions Internship | AICTE / IBM SkillsBuild |
| Jul 2026 | Intelligent Virtual Agents with IBM watsonx Assistant | IBM Training |
| Jul 2026 | Make Agentic AI Work for You — AI Agents, Multiagent Systems, RAG | IBM SkillsBuild |
| Jun 2026 | Getting Started with Generative AI — Foundations, LLMs, AI Ethics | IBM SkillsBuild |
| Jun 2026 | Text Analytics 101 | CognitiveClass.ai / IBM |
| May 2026 | Data Visualization with Power BI | IIT Mandi TIH Live × Coding Ninjas/NSDC |
| Apr 2026 | Introduction to Analytics & Excel | IIT Mandi TIH Live × Coding Ninjas/NSDC |
| Apr 2026 | Introduction to Agentic AI & LLM Architectures | Simplilearn |
| Jan 2026 | Data Analysis Workshop — "Ignite the Future" | M. S. University of Baroda |

Full archive with certificates: **[devpanchal04.netlify.app/credentials](https://devpanchal04.netlify.app/credentials)**

---

## Education

**ITM SLS Baroda University** — Vadodara, Gujarat
B.Tech, Computer Science & Engineering (AI & Data Science) · 2023–2027

---

## How I work

**Measure before claiming.** On the portfolio build, five separate "successes" turned out to be broken instruments — a counter returning the same value at every scroll position, a harness that never advanced a frame, a probe reading accumulated garbage. Now a number gets checked against a second, independent instrument before it goes anywhere near a README.

**One source of truth.** Every coordinate in the identity lives in one file. Every animation timing lives in one config. Two copies of a fact is how one of them ends up wrong.

**Ship it, then keep it working.** Three sites are live and I still maintain them — CSP headers, routing edge cases, email deliverability. Building it is the easy half.

---

## Contact

**devpanchal.web@gmail.com** · **+91 84602 89432**

Open to internships, freelance builds, and hackathon teams. Vadodara, Gujarat · Remote.
