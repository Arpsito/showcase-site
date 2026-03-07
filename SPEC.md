# Homer Showcase Website — Spec

## Purpose
A single-page showcase website demonstrating what a non-technical PE fundraiser built in 5 weeks using AI agents. This is for a CEO meeting — it needs to look premium, feel impressive, and tell a compelling story.

## Tech Stack
- **Static HTML + CSS + JS** — no build step, no framework dependencies
- **Tailwind CSS via CDN** (v3) — for rapid styling
- **Vanilla JS** — for animations, scroll effects, counters
- **No backend** — everything is client-side
- Must work by opening index.html locally OR serving from any static host

## Design System
- **Theme:** Dark mode, tech-premium feel (think Linear, Vercel, Stripe landing pages)
- **Colors:** 
  - Background: near-black (#0a0a0f) with subtle gradient
  - Primary accent: electric blue (#3b82f6) to cyan (#06b6d4) gradient
  - Secondary accent: violet (#8b5cf6) to pink (#ec4899) gradient  
  - Text: white (#ffffff) and gray (#94a3b8)
  - Cards: dark glass (rgba(255,255,255,0.05)) with subtle border
- **Typography:** Inter font (Google Fonts), clean and modern
- **Effects:** 
  - Glassmorphism cards with backdrop-blur
  - Smooth scroll-triggered fade-in animations (IntersectionObserver)
  - Animated number counters for stats
  - Subtle gradient glow effects behind key elements
  - CSS gradient text for headings
- **Responsive:** Mobile-first, looks great on phone (will demo on phone)

## Sections (in scroll order)

### 1. HERO
- Large bold headline: **"5 Weeks. Zero Code. One AI Agent."**
- Subtitle: "How a PE fundraiser built a 24/7 AI ecosystem from scratch"
- Subtle animated background (CSS gradient mesh or particle effect — keep it lightweight)
- Scroll indicator arrow at bottom

### 2. BY THE NUMBERS (Stats Grid)
- Animated count-up numbers on scroll:
  - **31** Custom AI Skills Built
  - **293** Knowledge Base Documents  
  - **18** Platform Integrations
  - **40+** Days Running 24/7
  - **1,500+** Searchable Knowledge Chunks
  - **6** Daily Automated Workflows
- Each stat in a glassmorphism card with an icon
- Use emoji or simple SVG icons

### 3. THE JOURNEY (Timeline)
- Vertical timeline with week markers
- **Week 1 (Jan 27 - Feb 2):** "Foundation" — Set up Mac mini, installed OpenClaw, configured WhatsApp/Gmail/Calendar, built first 4 custom skills, set up Obsidian vault with Sync, security hardening
- **Week 2 (Feb 3 - Feb 9):** "Acceleration" — Voice enhancement (ElevenLabs TTS), Codex CLI integration, 1Password secret management, automated morning briefings, solo RPG catalog (15 games cataloged)
- **Week 3 (Feb 10 - Feb 16):** "Intelligence" — Self-improvement system, batch 2 skills (family logistics, HN deep dive, solo RPG session, weekly review), People CRM, semantic memory search, Family Hub PWA built in 2 hours
- **Week 4 (Feb 17 - Feb 23):** "Scale" — Telegram multi-channel architecture, autonomous coding loops (Ralph Loop), parallel module building (Dark Factory), QA harness, trend research, content analysis
- **Week 5 (Feb 24 - Mar 7):** "Mastery" — MCP knowledge base (Open Brain) with vector search, automated Economist EPUB pipeline, custom security engine (HomerSec), Homer Simpson voice cloning, 24/7 autonomous operation
- Each week card should have a small icon/badge and 2-3 bullet highlights

### 4. WHAT HOMER DOES (Capability Cards)
- Grid of capability cards (3-4 per row desktop, 1 per row mobile)
- Each card has: icon, title, short description, subtle glow on hover

Cards:
1. 🌅 **Morning Intelligence Brief** — "AI-generated daily briefing covering weather, calendar, tasks, world news, AI developments, and health metrics. Delivered as audio via WhatsApp at 6:30 AM."
2. 🔍 **Research on Demand** — "Deep-dive research briefs on any topic, saved to a searchable knowledge base. Rotating daily topics: AI, industry trends, entertainment."
3. 🎙️ **Voice Interaction** — "Natural voice conversations via WhatsApp. Custom cloned voice. Responds to voice notes with voice. 2-way audio dialogue."
4. 🧠 **Knowledge Base (Open Brain)** — "MCP-compatible vector database. 293 documents, 1,500+ searchable chunks. Any AI tool can query it via universal protocol."
5. 🔒 **Security Engine** — "Custom-built security guardrails. Pattern matching, audit logging, supply chain protection. 1,000 checks in 6ms."
6. 👨‍👩‍👧‍👦 **Family Operations** — "Calendar management, logistics tracking, school coordination, travel planning. Full family command center."
7. 💻 **Autonomous Coding** — "Delegates to coding agents for overnight development. Built entire applications while sleeping. Fresh context per iteration."
8. 📰 **Content Pipeline** — "Automated HackerNews digest, Economist EPUB generation, trend monitoring across Reddit and X. Content delivered daily."

### 5. THE STACK (Architecture Diagram)
- Visual representation using CSS/HTML (not an image)
- Shows layers:
  ```
  [You] ←→ [WhatsApp / Voice] ←→ [Homer (AI Agent)]
                                        ↓
                               [OpenClaw Platform]
                                        ↓
                    [31 Custom Skills + 18 Integrations]
                                        ↓
            [Obsidian Vault | Open Brain | Family Hub | Automation]
  ```
- Clean boxes with connecting lines/arrows
- Subtle animation on scroll (layers appear one by one)

### 6. ALWAYS ON (24/7 Section)
- Visual showing the "always working" nature:
  - 5:30 AM — HackerNews digest generated
  - 6:30 AM — Morning brief researched, compiled, and delivered
  - Every 30 min — Knowledge base auto-syncs
  - On demand — Research, voice conversations, task management
  - 2:00 PM — Afternoon research brief on rotating topics
  - 10:00 PM — Evening accountability check-in
  - Overnight — Autonomous coding runs
- Style as a vertical "activity log" with timestamps and subtle pulse animations

### 7. BUSINESS APPLICATIONS (Placeholder)
- Section header: "Enterprise Potential"
- 3-4 placeholder cards with lock icons:
  - 🔒 **Deal Intelligence** — "Placeholder for deal-specific applications"
  - 🔒 **LP Relations** — "Placeholder for LP management applications"  
  - 🔒 **Market Analysis** — "Placeholder for market research applications"
  - 🔒 **Team Productivity** — "Placeholder for team workflow applications"
- Small note: "Detailed business applications available on request"
- These cards should have a slightly different style (muted, with a lock overlay) to clearly indicate they're placeholders

### 8. WHAT'S NEXT (Vision)
- Bold statement: "This is week 5. Imagine week 50."
- 3 forward-looking cards:
  - **Scale** — "From personal productivity to team-wide AI infrastructure"
  - **Integrate** — "Connect to deal management, CRM, data rooms, and LP portals"
  - **Compound** — "Every skill built makes the next one faster. Every document indexed makes the AI smarter."
- Final tagline: "The question isn't whether AI changes everything. It's whether you're building while others are waiting."

### 9. FOOTER
- Minimal footer
- "Built with AI. By a human who'd never coded before."
- Small text: "Powered by OpenClaw + Claude"

## File Structure
```
showcase-site/
├── index.html          # Everything in one file for simplicity
├── README.md           # How to run/deploy
├── assets/             # For images/visuals (added later)
│   └── .gitkeep
├── SPEC.md             # This file
└── .gitignore
```

## Implementation Notes
- Keep everything in index.html (inline CSS + JS) for maximum portability. One file = works everywhere.
- Use Tailwind CDN, Inter font from Google Fonts
- All animations via CSS transitions + IntersectionObserver (no heavy animation libraries)
- Counters should animate when scrolled into view (count from 0 to target number over ~2 seconds)
- Smooth scroll between sections
- Add subtle parallax effect on hero background
- Mobile responsive — this WILL be demoed on a phone

## Quality Bar
This needs to look like it was built by a professional design agency. No template vibes. No bootstrap feel. Think: Linear.app landing page, Vercel's homepage, Stripe's product pages. Premium, clean, confident.
