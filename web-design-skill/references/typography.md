# Typography Reference — Modern Google Fonts Pairings

> All pairings: Google Fonts (free). Each includes import, CSS variables, and type scale.
> The responsive type scale uses `clamp()` — no media queries needed for font sizes.

---

## Universal Responsive Type Scale

```css
/* Use these everywhere. Adjust --type-base-size to shift all sizes proportionally. */
:root {
  --type-base-size: 1rem; /* = 16px */
  --type-scale-ratio: 1.25; /* major third */

  /* Fluid sizes using clamp(min, preferred, max) */
  --text-xs:    clamp(0.64rem, 0.5vw + 0.5rem, 0.75rem);
  --text-sm:    clamp(0.80rem, 0.8vw + 0.6rem, 0.875rem);
  --text-base:  clamp(0.9375rem, 1vw + 0.7rem, 1rem);
  --text-md:    clamp(1.0625rem, 1.2vw + 0.75rem, 1.125rem);
  --text-lg:    clamp(1.125rem, 1.5vw + 0.8rem, 1.25rem);
  --text-xl:    clamp(1.25rem, 2vw + 0.8rem, 1.5rem);
  --text-2xl:   clamp(1.5rem, 3vw + 0.5rem, 2rem);
  --text-3xl:   clamp(1.75rem, 4vw + 0.5rem, 2.5rem);
  --text-4xl:   clamp(2rem, 5vw + 0.5rem, 3.25rem);
  --text-5xl:   clamp(2.5rem, 7vw + 0.25rem, 4.5rem);
  --text-6xl:   clamp(3rem, 10vw, 6rem);

  /* Line heights */
  --leading-tight:  1.1;
  --leading-snug:   1.3;
  --leading-normal: 1.5;
  --leading-relaxed: 1.65;
  --leading-loose:  1.8;

  /* Letter spacing */
  --tracking-tight: -0.04em;
  --tracking-snug:  -0.025em;
  --tracking-normal: 0;
  --tracking-wide:  0.05em;
  --tracking-caps:  0.1em;
}

/* Heading defaults */
h1, h2, h3, h4, h5, h6 {
  font-family: var(--font-heading);
  font-weight: 700;
  line-height: var(--leading-tight);
  letter-spacing: var(--tracking-snug);
  color: var(--clr-text);
}

h1 { font-size: var(--text-5xl); }
h2 { font-size: var(--text-4xl); }
h3 { font-size: var(--text-3xl); }
h4 { font-size: var(--text-2xl); }
h5 { font-size: var(--text-xl); }
h6 { font-size: var(--text-lg); }

/* Body defaults */
body {
  font-family: var(--font-body);
  font-size: var(--text-base);
  line-height: var(--leading-relaxed);
  color: var(--clr-text);
}

p { max-width: 65ch; }  /* Critical for readability */
```

---

## Pairing 1 — Inter + Inter (The Modern Default)
**Personality:** Clean, professional, highly legible. Used by Linear, Notion, Vercel.

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
```

```css
:root {
  --font-heading: 'Inter', system-ui, sans-serif;
  --font-body: 'Inter', system-ui, sans-serif;
}
/* Headings: weight 700-800, tracking -0.03em */
/* Body: weight 400-450, tracking 0 */
/* Works at ALL sizes — the workhorse font of the web */
```

**Best for:** SaaS, dev tools, dashboards, corporate sites

---

## Pairing 2 — Plus Jakarta Sans + DM Sans
**Personality:** Friendly, modern, versatile. Startup energy without being trendy.

```html
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&family=DM+Sans:wght@400;500&display=swap" rel="stylesheet">
```

```css
:root {
  --font-heading: 'Plus Jakarta Sans', sans-serif;
  --font-body: 'DM Sans', sans-serif;
}
/* Headings: 700-800, -0.025em tracking */
/* Body: 400, 1.65 line-height */
```

**Best for:** Consumer apps, startups, product landing pages

---

## Pairing 3 — Space Grotesk + Manrope
**Personality:** Geometric, technical, slightly quirky. Strong personality.

```html
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Manrope:wght@400;500;600&display=swap" rel="stylesheet">
```

```css
:root {
  --font-heading: 'Space Grotesk', sans-serif;
  --font-body: 'Manrope', sans-serif;
}
/* Headings: 600-700, -0.02em tracking */
/* Body: 400, 1.7 line-height */
/* Note: Space Grotesk is distinctive — don't use for generic corporate sites */
```

**Best for:** Tech brands, creative agencies, AI/crypto startups

---

## Pairing 4 — Playfair Display + Source Sans 3
**Personality:** Editorial, premium, sophisticated. Classic contrast.

```html
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;800;900&family=Source+Sans+3:wght@300;400;600&display=swap" rel="stylesheet">
```

```css
:root {
  --font-heading: 'Playfair Display', Georgia, serif;
  --font-body: 'Source Sans 3', sans-serif;
}
/* Headings: 700-900, serif luxury feel */
/* Body: 300-400, very readable at small sizes */
/* Contrast is the design — don't use same weight for both */
```

**Best for:** Luxury brands, editorial sites, restaurants, agencies

---

## Pairing 5 — Syne + Nunito Sans
**Personality:** Bold, expressive, creative. For brands with strong identity.

```html
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@600;700;800&family=Nunito+Sans:wght@300;400;600&display=swap" rel="stylesheet">
```

```css
:root {
  --font-heading: 'Syne', sans-serif;
  --font-body: 'Nunito Sans', sans-serif;
}
/* Headings: 700-800, very tight tracking (-0.04em) */
/* Body: 300-400, rounded and friendly */
/* Syne = wide, bold. Contrasts perfectly with Nunito's roundness */
```

**Best for:** Creative portfolios, design agencies, fashion brands

---

## Pairing 6 — Fraunces + General Sans
**Personality:** Warm, artisanal, trustworthy. The 2025 craft/editorial choice.

```html
<link href="https://fonts.googleapis.com/css2?family=Fraunces:wght@700;800;900&family=DM+Sans:wght@400;500&display=swap" rel="stylesheet">
```

```css
:root {
  --font-heading: 'Fraunces', serif;
  --font-body: 'DM Sans', sans-serif;
}
/* Fraunces = optical size aware, beautiful at large sizes */
/* font-optical-sizing: auto; on headings for best results */
```

**Best for:** Food brands, artisan products, indie SaaS with warm personality

---

## Pairing 7 — Outfit + Inter
**Personality:** Clean, geometric, slightly friendly. Modern minimalist.

```html
<link href="https://fonts.googleapis.com/css2?family=Outfit:wght@400;600;700;800&family=Inter:wght@400;500&display=swap" rel="stylesheet">
```

```css
:root {
  --font-heading: 'Outfit', sans-serif;
  --font-body: 'Inter', system-ui, sans-serif;
}
/* Outfit = clean geometric at large sizes */
/* Inter = ultra legible at small sizes */
/* Best of both worlds */
```

**Best for:** General purpose — works for almost any project type

---

## Pairing 8 — Clash Display + Satoshi
**Personality:** Bold, contemporary, high-impact. Maximum personality.
> Note: These are not on Google Fonts — use from Fontshare (free)

```html
<!-- Fontshare CDN (free, no API key needed) -->
<link href="https://api.fontshare.com/v2/css?f[]=clash-display@600,700,800&f[]=satoshi@400,500,700&display=swap" rel="stylesheet">
```

```css
:root {
  --font-heading: 'Clash Display', sans-serif;
  --font-body: 'Satoshi', sans-serif;
}
/* Clash Display = ultra bold, very large headlines only */
/* Satoshi = clean, modern, excellent body font */
/* 2025 trend pairing — used on many Godly sites */
```

**Best for:** Bold brand sites, agency portfolios, premium apps

---

## Pairing 9 — Cormorant Garamond + Mulish
**Personality:** Elegant, sophisticated, high-fashion. Maximum luxury.

```html
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@500;600;700&family=Mulish:wght@300;400;500&display=swap" rel="stylesheet">
```

```css
:root {
  --font-heading: 'Cormorant Garamond', serif;
  --font-body: 'Mulish', sans-serif;
}
/* Cormorant = thin strokes, very elegant at 60px+ */
/* Use for hero headlines only — not body or UI text */
/* Body in Mulish: weight 300 for maximum refinement */
```

**Best for:** Luxury brands, high fashion, premium hospitality, jewelry

---

## Pairing 10 — JetBrains Mono + Inter
**Personality:** Technical, developer-focused, terminal aesthetic.

```html
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
```

```css
:root {
  --font-heading: 'JetBrains Mono', monospace;
  --font-body: 'Inter', system-ui, sans-serif;
  --font-code: 'JetBrains Mono', monospace;
}
/* Mono heading = strong developer tool identity signal */
/* Use sparingly for headings — works on dark backgrounds especially */
```

**Best for:** Dev tools, CLIs, terminal apps, cybersecurity, hacker culture

---

## Typography Best Practices

### The Rules That Actually Matter

```css
/* 1. NEVER use system fonts for headlines on premium sites */
/* Always load at minimum a variable Google font */

/* 2. Optical sizing for large text */
.hero-title {
  font-optical-sizing: auto;
  font-variation-settings: 'opsz' 72;
}

/* 3. Balance text on last line */
h1, h2, h3 { text-wrap: balance; }
p { text-wrap: pretty; } /* Prevents orphaned last words */

/* 4. Never let body text exceed 75 characters */
.prose { max-width: 65ch; }

/* 5. Establish clear hierarchy with 3+ size jumps */
/* ✅ Good: body 16px → subtitle 20px → headline 48px (3× jump) */
/* ❌ Bad: body 16px → subtitle 18px → headline 22px (too close) */

/* 6. Weight contrast matters more than size alone */
/* ✅ Good: headline 700 weight vs body 400 weight */
/* ❌ Bad: headline 600 weight vs body 500 weight */

/* 7. Negative letter-spacing on large text */
.display-text {
  letter-spacing: -0.03em; /* essential for premium feel at 60px+ */
}
```

### Mobile Typography Checklist
- [ ] Minimum body font size: 16px (never go below — Safari zoom triggers at <16px)
- [ ] Touch target labels: minimum 14px with 4px padding
- [ ] Line height on mobile body: 1.6 minimum
- [ ] Hero headline on mobile: clamp() ensures it scales, test at 375px wide
- [ ] Dark mode: slightly reduce weight (use 500 where desktop uses 700)

### Font Loading Best Practice

```html
<!-- In <head> — optimized font loading -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<!-- Load only the weights you use. 400,500,700 covers 90% of designs -->
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&display=swap" rel="stylesheet">
```

```css
/* Font fallback stack — prevents invisible text during load */
body {
  font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
}
/* -apple-system matches San Francisco on Mac/iOS */
/* BlinkMacSystemFont for older Chrome on Mac */
```
