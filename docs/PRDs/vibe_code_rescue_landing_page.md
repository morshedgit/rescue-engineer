# Product Requirement Document (PRD): Vibe Code Rescue Landing Page

## 1. Overview & Objective

* **Product**: Single-page landing website for an independent Vibe Coding Rescue & Fractional Engineering consultancy.
* **Objective**: Convert non-technical founders, operators, and creators whose AI-generated apps (built via Cursor, Lovable, Bolt, Replit, v0, etc.) are breaking or unlaunchable into paid Code Audits or Discovery Calls.
* **Core Philosophy**: Focus on architectural clarity, security, and senior engineering competence rather than generic bug-fixing.

---

## 2. Target Audience (ICP)

* **Primary**: Non-technical founders and small business operators with working prototypes who have paying users, upcoming launches, or investor demos, but are blocked by security, auth, database, or deployment issues.
* **Secondary**: Solo creators who reached the limit of AI context windows and need a senior engineer to structure their codebase for sustainable development.

---

## 3. Core Value Proposition & Positioning

* **Headline Angle**: *"You built the prototype with AI. I make it secure, scalable, and production-ready."*
* **Key Differentiator**: Senior software engineering expertise bridging the gap between rapid AI prototyping and production-grade reliability.

---

## 4. Homepage Section Architecture

### Section 1: Hero
* **Headline**: Fix, Secure, and Ship Your AI-Built App.
* **Sub-headline**: Hit a wall with Lovable, Bolt, Cursor, or Replit? I take your vibe-coded prototype, resolve security and database vulnerabilities, and turn it into stable production software.
* **Primary CTA**: Book a Free 15-Min Code Triage (links to scheduling calendar).
* **Secondary CTA**: View Audit Scope (smooth-scrolls to pricing section).

### Section 2: The "Vibe Coding Wall" (Problem Breakdown)
Brief empathy section highlighting the 4 most common failure modes:
1. **Broken Auth & Security**: Open database policies, client-side permission checks, or leaked API keys.
2. **Database & State Chaos**: Inconsistent schemas, unhandled race conditions, and sluggish queries.
3. **Failed Integrations**: Broken Stripe webhooks, third-party API rate limits, and unhandled edge cases.
4. **Deployment Hell**: Infinite build errors, environment variable mismatches, and routing failures.

### Section 3: How It Works (Simple 3-Step Process)
* **Step 1: 48-Hour Code Diagnostic**: I review the codebase and provide a prioritized risk report (what to fix, what to leave alone).
* **Step 2: Scoped Stabilization Sprint**: A focused 1–2 week sprint to secure auth, fix critical bugs, add tests, and configure clean deployments.
* **Step 3: Keep Building with Confidence**: Get a clean, documented codebase ready for real users or continued AI feature development.

### Section 4: Services & Transparent Pricing
* **Package 1 — Production Readiness Audit ($750 – $1,250 | Fixed Price, 48-hr turnaround)**:
  * Full review of security, database schemas, auth/RLS, and API integrations.
  * Deliverable: Actionable remediation report and 30-min walkthrough call.
* **Package 2 — Rescue Sprint ($3,500 – $6,500 | 1–2 Weeks)**:
  * Hands-on remediation: fix critical vulnerabilities, secure database policies, integrate reliable payment/webhooks, and set up deployment pipelines.
* **Package 3 — Fractional Advisory ($1,500 – $3,000/mo | Retainer)**:
  * Ongoing architectural oversight, code reviews, and prompt guidance to keep the founder building safely.

### Section 5: Trust Signals (Alternative to Early Case Studies)
Because direct client case studies are not yet available, trust is established via:
* **Senior Engineering Background**: Highlight years of senior software engineering experience, system architecture discipline, and production-grade standards.
* **Sample Architecture Teardown**: A short visual or expandable breakdown of a typical AI code flaw (e.g., *“How an unconfigured Supabase RLS policy allows unauthorized data extraction, and how we fix it in 3 lines”*).
* **Clear Guarantee**: If the initial diagnostic does not identify actionable, high-severity issues, the audit fee is refunded.

### Section 6: Supported Tech Stack & Ecosystem
* **AI Prototyping Platforms**: Lovable, Bolt.new, Cursor, Replit, v0, Claude Code.
* **Core Technologies**: Next.js, React, Node.js, Python, TypeScript, PostgreSQL / Supabase, Firebase, Tailwind CSS, Stripe, Vercel, AWS.

### Section 7: Intake & Final CTA
* **Embedded Scheduler**: Cal.com or Calendly embed for direct booking.
* **Quick Intake Form (Fallback)**:
  * Name & Email
  * App URL / Repository Link (optional)
  * AI Tool Used (Lovable, Bolt, Cursor, etc.)
  * Primary Blocker (Auth, Database, Deployment, Payments, Other)

---

## 5. Technical Requirements & Architecture

### Framework
* **Astro** (with Tailwind CSS for styling and TypeScript).
* Generates zero-JS static HTML by default for near-instant load times (<1s).
* Selective client islands (e.g., React or vanilla JS) used only for interactive elements (calendar widget, intake form).

### Source Control & Repository
* **GitHub**: Single repository containing the Astro codebase and asset files.

### Hosting & Deployment
* **Cloudflare Pages**:
  * Direct GitHub repository connection (Cloudflare automatically detects commits on the main branch and runs the Astro build process).
  * No custom GitHub Actions required—relies entirely on native Cloudflare Pages Git integration.
  * Global edge CDN distribution with custom domain and automatic HTTPS/TLS.

### Backend & Integrations
* **Form Submissions**: Handled via a Cloudflare Pages Function endpoint (or lightweight service like Formspree/Resend) for serverless email dispatch.
* **Calendar Scheduling**: Cal.com or Calendly embedded iframe/popup.
* **Analytics**: Privacy-friendly, lightweight analytics (e.g., Cloudflare Web Analytics or Plausible).

### Performance & Accessibility
* Target **95+ Google Lighthouse scores** across Performance, Accessibility, and Best Practices.
* Fully responsive mobile-first layout.

---

## 6. Success Metrics

* **Primary Conversion Rate**: $\ge$ 3%–5% of unique visitors booking a triage call or submitting an intake request.
* **Performance**: Sub-second global page loads on Cloudflare edge.
* **Lead Quality**: High percentage of inquiries from founders with working MVPs and specific production blockers.
