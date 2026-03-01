# Modern Web Design Patterns — 2025–2026

> Synthesized from godly.website featured sites: AuthKit, Amie, Linear, Lusion, Notion, Vercel,
> Phantom, Cosmos, Height, Reflect, and 40+ others. These are patterns that actually work.

---

## Hero Section Patterns (7 Variants)

### 1. Centered Text + Gradient Background (Most Common)
**Seen on:** AuthKit, Linear, Reflect, Superpower, Shuttle
```
Layout: Full viewport. Content centered vertically and horizontally.
Headline: 1–2 lines, 57–72px, tight letter-spacing (-0.02em to -0.04em)
Subheadline: 18–20px, max-width: 540px, muted color, ~60% opacity
CTA buttons: 2 buttons — primary (filled) + secondary (outline/ghost)
Background: Multi-stop gradient, subtle animated mesh, or dark with grain texture
Badge/tag: Small "Now in beta" or "Introducing X" chip above headline
```

### 2. Split Layout — Text Left, Visual Right
**Seen on:** Opal Camera, Amie, Height, Desktop.fm
```
Layout: CSS Grid 1fr / 1fr at ≥768px, stacks on mobile
Text side: Headline, subtext, CTA(s), social proof row (avatars + "X users")
Visual side: Product screenshot in device mockup, floating UI elements, 3D render
Animation: Visual slides in from right on load (400ms ease-out)
Background: White or very light gray — contrast comes from visuals
```

### 3. Full-Width Video/3D Background
**Seen on:** Lusion, KidSuper World, Spring/Summer
```
Video: Autoplay, muted, loop, object-fit: cover. Poster image fallback.
Overlay: 40–60% dark overlay for text readability
Text: White, large, minimal — usually just headline + single CTA
Controls: No video controls visible
Performance: Load video lazily, show poster until interaction
```

### 4. Bento Grid Hero
**Seen on:** Notion, Cosmos, Paste
```
Layout: Asymmetric grid of cards showing product features
Main card: Spans 2 columns, has headline + CTA
Feature cards: Each shows one feature with icon + 1-line description
Colors: Each card may have a unique accent color or be unified
Animation: Cards animate in with stagger delay (50ms apart)
```

### 5. Minimal Typographic
**Seen on:** Pedro Duarte, Max Yinger, Logan Liffick, Endless
```
Background: Pure white or black
Headline: Massive, fills viewport width (fluid: clamp(48px, 10vw, 120px))
No images: Typography IS the design
Subtle texture: Grain overlay (5–8% opacity) on background
Interaction: Cursor tracking effects, text scramble animations
```

### 6. Scroll-Reveal Feature Showcase
**Seen on:** Height, Phantom, Family
```
Pin the page: Hero sticks, product UI animates in as user scrolls
Progress: Scroll position drives animation (IntersectionObserver or GSAP ScrollTrigger)
Transitions: Product screens change to show different features
```

### 7. Dark Mode First
**Seen on:** Phantom, Cosmos, ChainZoku, Daniel Sun
```
Background: #0a0a0a or #080808 — not pure black
Text: #f0f0f0 — not pure white (reduces eye strain)
Accent: Electric blue, purple, or green — high contrast on dark
Glow effects: Box-shadow glow on key elements (blur: 40–80px)
```

---

## Navigation Patterns

### 1. Transparent → Frosted Glass on Scroll
**The 2025 standard. Used by 70%+ of Godly sites.**
```css
nav {
  position: fixed;
  top: 0;
  width: 100%;
  padding: 16px 24px;
  transition: all 300ms cubic-bezier(0.2, 0, 0, 1);
  z-index: 100;
}
nav.scrolled {
  background: rgba(255, 255, 255, 0.8);
  backdrop-filter: blur(20px) saturate(180%);
  -webkit-backdrop-filter: blur(20px) saturate(180%);
  border-bottom: 1px solid rgba(0, 0, 0, 0.08);
}
```

### 2. Centered Logo / Balanced Nav
```
Logo: Center or left
Links: 4–6 items, 14px, medium weight
CTA: Right-aligned button (primary color, small, pill shape)
Mobile: Hamburger → full-screen overlay menu
```

### 3. Sidebar / Tab Navigation (App-style)
```
Left sidebar: 240px wide, collapsible to 64px (icon-only)
Items: Icon + label, 48px touch target
Active state: Background pill highlight (primary-container color)
```

---

## Feature / Services Section Patterns

### 1. Icon + Card Grid (3 or 4 columns)
```
Each card: Icon (40–48px), title (18–20px bold), description (14–16px body)
Grid: 3 columns desktop, 2 tablet, 1 mobile
Hover: Card lifts (box-shadow increase) + subtle background shift
Spacing: 32–48px gap between cards
```

### 2. Alternating Feature Rows
```
Row 1: Text left, screenshot right
Row 2: Screenshot left, text right
Each row: 80–120px top padding for breathing room
Mobile: Stack text above image always
```

### 3. Tab-Switched Feature Display
```
Tabs: Horizontal pills (3–5 items)
Content: Product screenshot/UI changes with tab selection
Transition: Fade (200ms) between content
Active tab: Filled background, white text
```

### 4. Bento Grid Features
```
Grid: CSS Grid, mixed card sizes (some span 2 cols)
Cards: Each demonstrates ONE feature with live-ish UI preview
Colors: Alternating light/dark cards for visual interest
```

---

## Testimonials / Social Proof Patterns

### 1. Quote Cards — Masonry/Grid
```
Layout: 3-column grid (2 on tablet, 1 on mobile)
Card: Avatar + name + role/company + quote (2–4 lines)
Style: White card, subtle border, elevation-1 shadow
Stagger: Animate in with 50–100ms delay between cards
```

### 2. Logo Strip
```
Usage: "Trusted by" section — shows company logos
Layout: Flex row, overflow hidden, CSS scroll animation (marquee)
Style: Grayscale logos (or adjust opacity to 50%) — equal visual weight
Speed: 30–60s linear scroll loop
```

### 3. Tweet/Social Embeds Grid
```
Embed real testimonial tweet cards in a masonry grid
Show: Name, handle, avatar, tweet text, date
Platform badge: Twitter/X icon
```

### 4. Single Featured Quote (Hero-level)
```
Large pull quote: 32–40px, italic, centered
Attribution: Name + photo + role below
Background: Light gray or brand color section
```

---

## Footer Patterns

### 1. Multi-Column Footer (Standard)
```
Columns: Logo+description | Product links | Company links | Social+Legal
Logo column: Logo, 2-line description, social icons row
Link columns: 5–8 links each, 14px, hover underline animation
Bottom bar: Copyright + privacy/terms links
```

### 2. Minimal Footer
```
Single row: Logo | links (4–6) | copyright
Used by: Portfolio sites, single-product apps
Height: 60–80px
```

### 3. CTA Footer
```
Large section: "Ready to get started?" + primary CTA button
Then: Standard multi-column links below
Background: Dark or brand color for contrast
```

---

## Animation Patterns (What Makes Sites "Godly")

### 1. Scroll-Triggered Fade + Rise
```css
/* The #1 most used animation on Godly sites */
[data-animate] {
  opacity: 0;
  transform: translateY(32px);
  transition: opacity 0.6s ease, transform 0.6s cubic-bezier(0.16, 1, 0.3, 1);
}
[data-animate].in-view {
  opacity: 1;
  transform: translateY(0);
}
/* JS: IntersectionObserver adds .in-view when element enters viewport */
```

### 2. Stagger Children
```css
/* Parent has stagger effect on children */
.stagger-container > * {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.5s ease, transform 0.5s ease;
}
.stagger-container.in-view > *:nth-child(1) { transition-delay: 0ms; }
.stagger-container.in-view > *:nth-child(2) { transition-delay: 100ms; }
.stagger-container.in-view > *:nth-child(3) { transition-delay: 200ms; }
.stagger-container.in-view > * { opacity: 1; transform: translateY(0); }
```

### 3. Hover Lift (Cards)
```css
.card {
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}
.card:hover {
  transform: translateY(-4px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.12);
}
```

### 4. Gradient Text (Trending 2025)
```css
.gradient-text {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
```

### 5. Mesh/Aurora Background
```css
.aurora-bg {
  background: 
    radial-gradient(ellipse at 20% 50%, rgba(120, 119, 198, 0.3) 0%, transparent 50%),
    radial-gradient(ellipse at 80% 20%, rgba(255, 119, 198, 0.3) 0%, transparent 50%),
    radial-gradient(ellipse at 50% 80%, rgba(119, 198, 255, 0.3) 0%, transparent 50%),
    #fafafa;
}
```

### 6. Button Shimmer Hover
```css
.btn {
  position: relative;
  overflow: hidden;
}
.btn::after {
  content: '';
  position: absolute;
  top: -50%; left: -75%;
  width: 50%; height: 200%;
  background: rgba(255, 255, 255, 0.3);
  transform: skewX(-20deg);
  transition: left 0.6s ease;
}
.btn:hover::after { left: 125%; }
```

### 7. Smooth Reveal Underline
```css
.nav-link {
  position: relative;
  text-decoration: none;
}
.nav-link::after {
  content: '';
  position: absolute;
  bottom: -2px; left: 0;
  width: 0; height: 2px;
  background: currentColor;
  transition: width 0.3s ease;
}
.nav-link:hover::after { width: 100%; }
```

---

## Color Palette Trends 2025–2026

### Trending Combinations
1. **Dark + Electric Purple** — Phantom, ChainZoku (`#0a0a0a` + `#8B5CF6`)
2. **Off-White + Deep Indigo** — Linear, Height (`#FAFAFA` + `#3730A3`)
3. **Warm Neutral + Sage Green** — Samara, nature brands (`#F5F0E8` + `#4A7C59`)
4. **Matte Black + Coral** — Bold brand sites (`#111111` + `#FF6B6B`)
5. **Light Gray + Amber** — Dashboard/SaaS tools (`#F8F8F8` + `#F59E0B`)
6. **White + Vibrant Blue** — AuthKit, Vercel (`#FFFFFF` + `#0070F3`)
7. **Dark Navy + Gold** — Luxury/premium (`#0D1117` + `#D4AF37`)
8. **Soft Beige + Terracotta** — Lifestyle brands (`#FDF8F3` + `#C4714E`)

### What's Out
- Flat pastel palettes (they look 2018)
- Bootstrap blue (#007bff)
- Pure white + pure black (too harsh)
- Neon gradients without restraint

---

## Typography Pairings (Godly Standard)

| Heading | Body | Personality |
|---------|------|-------------|
| Cal Sans / Geist | Inter | Tech startup (Linear, Vercel) |
| Playfair Display | Source Sans 3 | Editorial, luxury |
| Space Grotesk | DM Sans | Modern, geometric |
| Syne | Manrope | Creative agency |
| Clash Display | Satoshi | Bold brand |
| Plus Jakarta Sans | Plus Jakarta Sans | Clean versatile |

### Key Typography Decisions from Godly Sites
- **Tight tracking on headlines:** `-0.02em` to `-0.05em` (makes large text look premium)
- **Generous line-height on body:** `1.6`–`1.75`
- **Max-width on paragraphs:** 60–75 characters (`max-width: 65ch`)
- **Optical sizing:** Use `font-optical-sizing: auto` with variable fonts
- **Weight contrast:** Headlines bold (700–900), body regular (400–450)

---

## Layout Whitespace Standards

- **Section padding:** `80–120px` top/bottom on desktop, `60px` on mobile
- **Max content width:** `1200–1280px` (centered with auto margins)
- **Card padding:** `24–32px` internal padding
- **Between-element spacing:** Use 8px grid (`8, 16, 24, 32, 48, 64, 80, 96px`)
- **Text blocks:** Never wider than `65ch` for readability

## What Separates Godly from Generic
1. **Intentional whitespace** — more breathing room than you think you need
2. **Micro-interactions** — every clickable element has a state change
3. **Typography hierarchy** — 3+ distinct type sizes with clear visual order
4. **One accent color** — used sparingly, not everywhere
5. **Mobile-first actual implementation** — not just responsive but DESIGNED for mobile
6. **Performance** — fast loads, no layout shift, images are WebP/AVIF
