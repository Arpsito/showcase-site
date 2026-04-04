# Showcase Site Upgrade: 3D Animations & Interactive Polish

## Context
Single-page showcase site (`index.html`, ~1500 lines) built with Tailwind CDN + Lucide icons + vanilla JS. Light theme with pastel accents (coral, teal, gold, lavender, sky, mint). Already has basic `.section-fade` scroll reveal (opacity + translateY).

## Goals
Add premium interactive polish inspired by modern 3D animated sites. Keep it a single `index.html` — no build tools, no frameworks. All CSS/JS stays inline.

## Upgrades to Implement

### 1. Enhanced Scroll Animations (replace basic section-fade)
- **Staggered reveals**: Child elements within sections animate in sequence (100-150ms delay between items)
- **Varied directions**: Some sections slide from left, others from right, stats count up
- **Parallax depth**: Subtle parallax on hero section background elements (gradients shift at different scroll speeds)
- **Stats counter animation**: Numbers in stats section count up from 0 when they scroll into view

### 2. 3D Card Hover Effects
- **Capability/feature cards**: Add CSS perspective + rotateX/rotateY on mousemove, creating a tilt effect
- **Shine overlay**: Subtle light reflection that follows cursor position on hover
- **Spring-back animation**: Cards smoothly return to flat when mouse leaves
- **Touch-friendly**: On mobile, use a subtle scale(1.02) on tap instead of tilt

### 3. Animated Gradient Backgrounds
- **Hero section**: Slow-moving gradient animation (coral → lavender → sky, 8s cycle)
- **Section dividers**: Thin gradient lines between sections that shimmer/flow

### 4. Micro-interactions
- **Nav scroll progress**: Thin colored progress bar at top of page showing scroll position
- **Button hover**: Subtle lift + shadow expansion on CTA buttons
- **Link underlines**: Animated underline that slides in from left on hover

### 5. Performance Guardrails
- Use `will-change` sparingly (only on actively animating elements)
- Respect `prefers-reduced-motion` — disable all animations if user prefers reduced motion
- Use `IntersectionObserver` for scroll triggers (no scroll event listeners)
- Keep total added JS under 3KB
- 60fps target — no heavy repaints

## Design Constraints
- Keep the existing light theme and color palette
- Don't change content or layout structure
- Don't add external dependencies (no GSAP, no Three.js — pure CSS + vanilla JS)
- Must work well on mobile Safari (iPhone) since demos happen on phone
- Preserve existing Lucide icon initialization

## Test
Open in browser and verify:
1. Sections reveal smoothly on scroll with staggered children
2. Cards tilt on hover with shine effect
3. Hero gradient animates
4. Stats count up when visible
5. Progress bar works at top of page
6. Everything works on mobile viewport (375px)
7. `prefers-reduced-motion` disables animations
