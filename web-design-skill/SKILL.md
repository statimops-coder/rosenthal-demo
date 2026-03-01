---
name: web-design
description: Modern web design system for building beautiful, current websites. Use BEFORE any website build task. Provides Material Design 3 specs, modern layout patterns from godly.website, pre-built components (hero, nav, bento, cards, pricing, CTA, footer), 10 color palettes, typography pairings, and animation patterns. Ensures Codex builds sites that look like 2026, not 2019.
---

# Web Design Skill — Modern Website System

You are building a website. Before writing a single line of HTML, follow this skill.
The difference between a site that looks generic and one that looks premium is almost entirely
about **typography, spacing, color discipline, and micro-interactions** — not complexity.

---

## Quick Start Workflow

Every website build follows this order:

1. **Identify the client type** → pick a color palette from `references/color-palettes.md`
2. **Pick a typography pairing** → from `references/typography.md`
3. **Choose a hero variant** → from `references/components.md` (section 1–3)
4. **Assemble sections** using the component kit (copy → customize text/colors → combine)
5. **Apply MD3 spacing/motion tokens** from `references/material-design-3.md` for polish
6. **Review against the Modern Patterns checklist** below before delivering

---

## The Non-Negotiables (Read These First)

```
✅ Typography: Load a Google Font. Never use system fonts for headings on a real site.
✅ Spacing: All spacing on 8px grid (8, 16, 24, 32, 48, 64, 80, 96px). No random values.
✅ Color: Pick ONE palette. Max 3 colors in the design (primary, secondary, accent).
✅ Responsive: Mobile-first. Test at 375px, 768px, 1280px.
✅ Animations: Every interactive element has a hover/focus state. No static buttons.
✅ Max-width: Body text never wider than 65ch. Container max: 1200px.
✅ Sections: 80–120px padding top/bottom (desktop), 60px (mobile). Breathe.
✅ Accessibility: 4.5:1 contrast ratio for text. 48px minimum touch targets.
✅ No Bootstrap. No jQuery. Vanilla CSS + HTML. Tailwind only if explicitly requested.
```

---

## Layout Pattern Decision Tree

**What type of site is it?**

```
├── SaaS / Product landing page
│   ├── Complex product with many features → Bento Grid Hero + Bento Features
│   └── Simple product / one idea → Centered Hero (Aurora) + Feature Cards 3-col
│
├── Portfolio / Agency
│   ├── Creative / bold personality → Dark Hero + Typographic sections
│   └── Professional / corporate → Split Hero + Alternating Feature Rows
│
├── Service business (plumber, clinic, consultant)
│   → Split Hero + Feature Cards + Testimonials + CTA + Footer
│
├── E-commerce / Product showcase
│   → Full-width visual hero + bento cards for products
│
└── Personal / Blog
    → Minimal typographic hero + single column content
```

---

## Component Usage Guide

All components are in `references/components.md`. Here's when to use each:

| Component | When to Use | Notes |
|-----------|-------------|-------|
| **Shared Base CSS** | Every project | Copy verbatim. Override `:root` variables only. |
| **Hero A (Aurora)** | SaaS, apps, most projects | Most versatile. Works dark OR light. |
| **Hero B (Split)** | Product with screenshot to show | Needs real product image to shine. |
| **Hero C (Dark Glow)** | Dev tools, AI, gaming, crypto | Dark background required. Electric feel. |
| **Nav (Glass)** | Every project | Universal. Adapts to any background. |
| **Bento Grid** | 4–6 features to highlight | 2025's most-used layout pattern. Steal it. |
| **Feature Cards** | Detailed features with explanations | 3-col grid, glassmorphism effect. |
| **Testimonials** | When social proof matters | Always 3+ quotes. 1 looks planted. |
| **Pricing** | SaaS with tiers | Include the toggle — it looks professional. |
| **CTA Section** | Every project — always last before footer | Gradient card. High conversion. |
| **Footer** | Every project | Multi-column = credibility signal. |
| **Contact Form** | Any site that needs inquiries | Animated labels. Very polished. |
| **Stats Section** | If you have real numbers | Animated counters. Impressive. |

---

## How to Customize Components

1. **Copy the HTML + CSS** from the component
2. **Override `:root` variables** at the top of your stylesheet (never change hex values inline)
3. **Replace placeholder text** with real, specific, benefit-focused copy
4. **Swap the gradient** — change `--clr-primary` and `--clr-accent` only
5. **Adjust stagger delays** — keep them 50–100ms apart, never more than 400ms total
6. **Test every hover state** — every card, button, and link needs one

### Quick Color Override Example

```css
/* Just change these 3 lines to completely retheme any component */
:root {
  --clr-primary: #0369a1;     /* Your brand primary */
  --clr-accent: #f59e0b;      /* Your accent (used sparingly) */
  --clr-text: #082f49;        /* Your dark text */
}
```

---

## Animation Rules

- **Scroll reveals:** Use the IntersectionObserver script from the Base CSS section. Add `class="reveal"` to any element.
- **Stagger:** Add `style="--delay:100ms"` (increments of 100ms) to stagger siblings.
- **Hover:** Every card gets `transform: translateY(-4px)` on hover. Every button gets lift + shadow boost.
- **Duration:** 200ms for micro (buttons), 400–600ms for reveals, 300ms for state changes.
- **Easing:** Always `cubic-bezier(0.16, 1, 0.3, 1)` for reveals (springy), `ease` for hovers.
- **Reduced motion:** Always include `@media (prefers-reduced-motion: reduce)` — it's already in Base CSS.

---

## Reference Files

| File | Read When |
|------|-----------|
| `references/material-design-3.md` | You need spacing tokens, elevation, motion curves, color semantics, or the shape system. |
| `references/modern-patterns.md` | You're choosing a layout pattern, hero variant, or animation approach. Also for understanding WHAT makes sites look premium. |
| `references/components.md` | You're building any section of the site. Copy the code, don't reinvent. |
| `references/color-palettes.md` | First decision on every project. Pick the palette that fits the client type. |
| `references/typography.md` | Choosing fonts. Always pick from the 10 pairings — don't invent new combinations. |

---

## The Premium Feel Checklist

Before delivering any site, verify:

- [ ] Hero has a badge/tag above the headline ("Introducing", "Now in Beta", "✦ Spring 2026")
- [ ] Headline uses `letter-spacing: -0.025em` or tighter
- [ ] Body text has `max-width: 65ch`
- [ ] Section padding is at least `80px` top/bottom on desktop
- [ ] At least 3 distinct font sizes visible (hierarchy)
- [ ] Every button has a visible hover state
- [ ] Cards have hover lift (`translateY(-4px)`)
- [ ] At least 2 sections have scroll-reveal animations
- [ ] Footer is multi-column (credibility signal)
- [ ] Mobile tested at 375px — nothing overflows
- [ ] CTA section uses the gradient card pattern
- [ ] Color palette is from `color-palettes.md` — no random hex values

---

## What Separates 2026 from 2019

| Old (Bad) | Modern (Good) |
|-----------|--------------|
| Bootstrap grid | CSS Grid + Flexbox, custom |
| `#007bff` blue | Semantic color tokens from palette |
| `font-size: 16px` fixed | `clamp()` fluid type scale |
| Box shadows: `0 2px 4px black` | Layered, low-opacity shadows |
| `margin: 20px` everywhere | 8px grid system |
| No hover states | Every interactive element has one |
| Hero: center text, basic bg | Hero: aurora gradient, badge, trust signals |
| Roboto at 400 weight | Font pairing with weight contrast (400 body, 700+ heading) |
| Responsive via media queries only | Mobile-first + `clamp()` fluid scaling |
| jQuery animations | CSS transitions + IntersectionObserver |
| Generic Lorem ipsum | Specific, benefit-focused copy |
| Static footer | Multi-column footer with social links |
