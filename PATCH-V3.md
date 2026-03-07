# V3 Patch — Remove Motivational Language + Add Interactivity

## Content Changes — Remove These
1. **Hero subtitle:** Remove "How a PE fundraiser built a 24/7 AI ecosystem from scratch" — replace with something neutral like "A personal AI operating system"
2. **Hero byline:** Remove "Built by Andres Perez — PE Fundraiser, Zero Technical Background" — replace with just "Built by Andres Perez"
3. **Footer:** Remove "Built with AI. By a human who'd never coded before." — replace with "Built by Andres Perez with Homer AI"
4. **Remove ALL motivational/inspirational quotes** including:
   - "The question isn't whether AI changes everything. It's whether you're building while others are waiting." — DELETE this entirely
   - Any other "inspirational" sounding language throughout
5. **Section descriptions** — make them factual, not pitchy. Examples:
   - NOT "Measured output in 5 weeks of focused AI system building" → YES "System metrics since January 27, 2026"
   - NOT "Core capabilities that run daily without manual intervention" → YES "Daily automated capabilities"
   - NOT "A 5-week build sprint from setup to autonomous operation" → YES "Build timeline"
6. **"What's Next" section:** Remove "This is week 5. Imagine week 50." — replace with "Roadmap" as header. Keep Scale/Integrate/Compound cards but rewrite descriptions to be matter-of-fact, not inspirational.

## Interactivity — Add These

### 1. Capability Cards — Click to Expand
- Cards start showing just icon + title
- On click/tap: card expands smoothly (CSS transition, max-height trick) to reveal the full description
- Add a subtle "+" indicator that rotates to "×" when expanded
- Multiple cards can be open at once

### 2. Stats — Hover/Tap Detail
- Each stat number is tappable
- On tap: a small tooltip/popover appears below with a one-line detail:
  - 31 Skills → "Custom automation scripts covering research, voice, security, family ops, and more"
  - 293 Documents → "Obsidian vault with notes, references, project docs, and daily logs"
  - 18 Integrations → "WhatsApp, Gmail, Calendar, Todoist, Spotify, GitHub, Supabase, and more"
  - 40+ Days → "Running 24/7 since January 27, 2026 on a Mac mini"
  - 1,500+ Chunks → "Vector-embedded knowledge searchable by any MCP-compatible AI"
  - 6 Workflows → "Morning brief, HN digest, research briefs, sync jobs, evening check-in, overnight coding"
- Tap again to dismiss

### 3. Timeline — Tap to Reveal
- On desktop: horizontal timeline already works
- Make the week cards COLLAPSED by default — show just the week number, title, and date range
- Tap to expand and show the bullet points
- Smooth accordion animation

### 4. Architecture Diagram — Animated Build
- When scrolled into view, the layers appear one by one (staggered, top to bottom)
- Each layer slides in from the left with a slight bounce
- Connection arrows draw themselves (CSS animation on border/line)
- After all layers appear, a subtle pulse ripples through the whole diagram once

### 5. Hero — Floating Pills Animation
- The skill/integration pills in the hero should gently float/drift (CSS animation with different speeds and directions per pill)
- On tap, each pill should briefly glow its color and show a tiny tooltip with one more detail
- Stagger the initial appearance of pills (fade in one by one over 2 seconds)

### 6. Always On — Live Clock
- Add a real-time clock display somewhere in the "Always On" section showing current time
- The activity closest to the current time should have a subtle highlight/glow to show "this is happening now" or "this happened most recently"
- Makes it feel alive, not static

### 7. Smooth Section Transitions
- When scrolling between sections, add a subtle parallax offset to section headers (they scroll slightly slower than content)
- Cards should have a very subtle tilt on hover (CSS transform: perspective + rotateX/Y, like 1-2 degrees max) — gives that 3D interactive feel

### 8. Mobile Gestures
- The timeline section should be horizontally swipeable on mobile (CSS overflow-x: auto with snap points)
- Add subtle haptic-style visual feedback on taps (brief scale pulse: 0.97 → 1.0)

## Technical Notes
- Keep everything in single index.html
- No external JS libraries (vanilla JS only + Lucide CDN)
- All animations via CSS transitions/keyframes + IntersectionObserver
- Tooltips: use absolute-positioned divs toggled via JS click handlers
- Accordion: use max-height transition trick (max-height: 0 → max-height: 500px with overflow: hidden)
- Keep it performant — no heavy animations that jank on mobile
