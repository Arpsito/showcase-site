# Showcase Site Redesign — V2

## The Problem
V1 looks like every other AI-generated website: purple gradients, glassmorphism, emoji icons, dark futuristic vibe. We need to look like a human designer built this — distinctive, colorful, confident.

## Design Direction
Think: **Stripe meets Notion meets a premium pitch deck.** Clean, editorial, colorful but restrained. NOT dark-mode-purple-gradient-AI-website.

## Color Palette — Bright Pastels + Bold
- **Background:** Off-white (#FAFAF9) with subtle warm tone — NOT pure black
- **Text:** Near-black (#1a1a2e) for headers, dark gray (#4a4a5a) for body
- **Primary accent:** Coral/Salmon (#FF6B6B)
- **Secondary:** Electric teal (#2EC4B6)  
- **Tertiary:** Warm gold (#FFD166)
- **Quaternary:** Soft lavender (#A78BFA)
- **Supporting:** Sky blue (#60A5FA), Mint (#34D399)
- **Cards:** White (#FFFFFF) with subtle shadow, NO glassmorphism
- **Borders:** Light gray (#E5E7EB), clean and subtle

## Typography
- **Headlines:** "Space Grotesk" from Google Fonts — bold, geometric, distinctive
- **Body:** "Inter" — clean readability
- **Accent text:** Consider monospace for stats/numbers (JetBrains Mono or similar)

## Logo — Homer
Create an inline SVG logo for "Homer" that feels like a real brand:
- Concept: A stylized amphora (Greek vase) integrated with a tech/circuit motif
- OR: A clean wordmark "HOMER" with the O replaced by a small amphora silhouette
- Colors: Use the coral (#FF6B6B) as primary logo color
- Should work at small sizes (nav) and large sizes (hero)
- Place in top-left nav area

## Icons — NO EMOJI
Replace ALL emoji with proper SVG icons. Use Lucide Icons (https://unpkg.com/lucide@latest/dist/umd/lucide.min.js):
- Skills Built → `wrench` icon
- Knowledge Base → `book-open` icon
- Integrations → `plug` icon
- Days Running → `clock` icon
- Knowledge Chunks → `puzzle` icon
- Workflows → `settings` icon
- Morning Brief → `sun` icon
- Research → `search` icon
- Voice → `mic` icon
- Knowledge Base → `brain` icon
- Security → `shield` icon
- Family → `users` icon
- Coding → `code` icon
- Content → `newspaper` icon

Each icon should be in a colored circle/rounded-square background using the pastel palette.

## Layout Changes

### Navigation
- Sticky top nav with: Homer logo (left), section links (center), "Andres Perez" (right)
- Clean white background with subtle bottom border
- Nav links in subtle gray, active section highlighted

### Hero
- LEFT-aligned text (not centered) with a colorful abstract graphic on the right
- "5 Weeks. Zero Code. One AI Agent." in Space Grotesk, near-black
- Below: "Built by Andres Perez — PE Fundraiser, Zero Technical Background"
- The right side: a colorful arrangement of floating skill/integration badges in pastel colors (like a tag cloud made of rounded pills)
- NO gradient mesh background. Clean off-white with maybe one subtle geometric accent

### Stats Section ("By The Numbers")
- Horizontal layout with large numbers
- Each stat number in a different pastel color from the palette
- Numbers in monospace font for that data-dashboard feel
- Clean dividers between stats, no cards needed
- Still animated count-up on scroll

### Timeline ("The Journey")
- Horizontal timeline on desktop (scrollable if needed), vertical on mobile
- Each week gets a colored dot from the palette (coral → teal → gold → lavender → mint)
- Clean cards below each dot with white background and colored left border
- Week number in the colored dot

### Capability Cards
- 2x4 grid on desktop, single column mobile
- White cards with colored left border (each card gets a unique pastel)
- Icon in a colored rounded square (40x40px) top-left of card
- Title + short description
- Subtle hover: lift + colored shadow

### The Stack
- Redesign as a proper architecture diagram
- Use colored boxes connected by lines/arrows (drawn with CSS/SVG)
- Layer labels in clean sans-serif
- Color each layer differently:
  - You (coral) → WhatsApp/Voice (teal) → Homer (gold) → OpenClaw (lavender) → Skills (sky blue) → Outputs (mint)
- Make it look like an actual engineering diagram, not ASCII art

### Always On
- Redesign as a "daily rhythm" visual
- Use a clock/timeline metaphor — 24hr circular layout OR clean horizontal timeline
- Each activity gets an icon + time + description
- Use the pastel dots for each time marker
- Feel: "This system never sleeps"

### Enterprise Potential
- Keep the locked/placeholder concept
- Cards with dashed borders and a subtle lock icon (from Lucide)
- Muted colors (grayed-out pastels) to show these are coming
- Small banner: "Confidential business applications — details available in person"

### What's Next
- Keep the "This is week 5. Imagine week 50." headline
- Three cards with icons for Scale, Integrate, Compound
- Each card gets a pastel accent
- Closing quote in italic Space Grotesk

### Footer
- Clean, minimal
- "Built by Andres Perez with Homer AI"
- Small "Powered by OpenClaw + Claude" below
- Year: 2026

## Technical Requirements
- Keep everything in ONE index.html file (inline CSS + JS)
- Load Lucide icons from CDN: `<script src="https://unpkg.com/lucide@latest/dist/umd/lucide.min.js"></script>` then call `lucide.createIcons()` after DOM ready
- Load fonts: Space Grotesk + Inter + JetBrains Mono from Google Fonts
- Keep Tailwind CDN
- Keep all scroll animations (IntersectionObserver) but make them subtler (less translateY, shorter duration)
- Keep counter animations
- Responsive — test on narrow viewport
- The Homer amphora logo should be an inline SVG (not an external file)

## What to Keep from V1
- All the CONTENT (text, stats, descriptions) — don't change the words
- The section order
- The counter animation logic
- The IntersectionObserver pattern
- The parallax concept (but toned down)

## What to Change from V1
- EVERYTHING visual: colors, fonts, layout, icons, spacing, cards
- Remove all glassmorphism
- Remove purple/blue/cyan gradient theme
- Remove emoji icons
- Add navigation bar
- Add Homer logo
- Add "Andres Perez" name prominently
- Light background instead of dark
- Editorial/premium feel instead of "AI startup landing page"
