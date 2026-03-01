# Color Palettes — 10 Modern Ready-to-Use Themes

> Each palette = complete CSS custom property set. Copy the `:root` block, done.
> Every palette includes light + dark mode variants.

---

## Category: Corporate / Professional

### 1. Indigo Professional (default)
**Personality:** Trustworthy SaaS, tech startup, developer tools
**Seen on:** Linear, Vercel, AuthKit

```css
:root {
  --clr-primary: #6366f1;
  --clr-primary-dark: #4f46e5;
  --clr-primary-light: #a5b4fc;
  --clr-secondary: #8b5cf6;
  --clr-accent: #06b6d4;
  --clr-bg: #ffffff;
  --clr-surface: #f8fafc;
  --clr-surface-alt: #f1f5f9;
  --clr-text: #0f172a;
  --clr-text-muted: #64748b;
  --clr-border: rgba(0, 0, 0, 0.08);
  --clr-border-strong: rgba(0, 0, 0, 0.15);
  --gradient-hero: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
}

@media (prefers-color-scheme: dark) {
  :root {
    --clr-bg: #0a0a0f;
    --clr-surface: #111118;
    --clr-surface-alt: #1a1a24;
    --clr-text: #f0f0ff;
    --clr-text-muted: #7c7c9a;
    --clr-border: rgba(255, 255, 255, 0.08);
    --clr-border-strong: rgba(255, 255, 255, 0.15);
    --clr-primary: #818cf8;
    --clr-primary-light: #6366f1;
  }
}
```

---

### 2. Midnight Blue (Corporate)
**Personality:** Finance, consulting, enterprise software
**Use for:** B2B services, law firms, financial apps

```css
:root {
  --clr-primary: #1e40af;
  --clr-primary-dark: #1e3a8a;
  --clr-primary-light: #93c5fd;
  --clr-secondary: #0891b2;
  --clr-accent: #f59e0b;
  --clr-bg: #ffffff;
  --clr-surface: #f8faff;
  --clr-surface-alt: #eff6ff;
  --clr-text: #0c1a3a;
  --clr-text-muted: #4b5e8a;
  --clr-border: rgba(30, 64, 175, 0.1);
  --gradient-hero: linear-gradient(135deg, #1e40af 0%, #0891b2 100%);
}

@media (prefers-color-scheme: dark) {
  :root {
    --clr-bg: #080c18;
    --clr-surface: #0e1520;
    --clr-surface-alt: #141e2e;
    --clr-text: #e8f0ff;
    --clr-text-muted: #5e7aad;
    --clr-border: rgba(255, 255, 255, 0.07);
    --clr-primary: #60a5fa;
    --clr-accent: #fbbf24;
  }
}
```

---

## Category: Creative / Bold

### 3. Electric Purple (Bold Brand)
**Personality:** Creative agencies, AI startups, gaming, crypto
**Seen on:** Phantom, ChainZoku, bold SaaS

```css
:root {
  --clr-primary: #7c3aed;
  --clr-primary-dark: #6d28d9;
  --clr-primary-light: #c4b5fd;
  --clr-secondary: #db2777;
  --clr-accent: #10b981;
  --clr-bg: #ffffff;
  --clr-surface: #faf5ff;
  --clr-surface-alt: #f3e8ff;
  --clr-text: #1a0533;
  --clr-text-muted: #6b5b8b;
  --clr-border: rgba(124, 58, 237, 0.12);
  --gradient-hero: linear-gradient(135deg, #7c3aed 0%, #db2777 100%);
}

@media (prefers-color-scheme: dark) {
  :root {
    --clr-bg: #07030f;
    --clr-surface: #0f0820;
    --clr-surface-alt: #160c2e;
    --clr-text: #f0e8ff;
    --clr-text-muted: #7c6b9e;
    --clr-border: rgba(196, 181, 253, 0.1);
    --clr-primary: #a78bfa;
    --clr-secondary: #f472b6;
  }
}
```

---

### 4. Sunset Coral (Energetic)
**Personality:** Consumer apps, lifestyle brands, creative tools

```css
:root {
  --clr-primary: #f97316;
  --clr-primary-dark: #ea580c;
  --clr-primary-light: #fdba74;
  --clr-secondary: #ec4899;
  --clr-accent: #8b5cf6;
  --clr-bg: #fffbf7;
  --clr-surface: #fff7ed;
  --clr-surface-alt: #ffedd5;
  --clr-text: #1c0a00;
  --clr-text-muted: #78543c;
  --clr-border: rgba(249, 115, 22, 0.12);
  --gradient-hero: linear-gradient(135deg, #f97316 0%, #ec4899 100%);
}

@media (prefers-color-scheme: dark) {
  :root {
    --clr-bg: #0f0800;
    --clr-surface: #1a0e00;
    --clr-surface-alt: #241600;
    --clr-text: #fff3e6;
    --clr-text-muted: #9e7048;
    --clr-border: rgba(249, 115, 22, 0.15);
    --clr-primary: #fb923c;
    --clr-secondary: #f472b6;
  }
}
```

---

## Category: Healthcare / Medical

### 5. Clean Teal (Health & Wellness)
**Personality:** Medical apps, health startups, wellness brands
**Key:** Trust + calm + clean

```css
:root {
  --clr-primary: #0d9488;
  --clr-primary-dark: #0f766e;
  --clr-primary-light: #5eead4;
  --clr-secondary: #0891b2;
  --clr-accent: #22c55e;
  --clr-bg: #f8fffe;
  --clr-surface: #f0fdfa;
  --clr-surface-alt: #ccfbf1;
  --clr-text: #042f2e;
  --clr-text-muted: #3d7872;
  --clr-border: rgba(13, 148, 136, 0.12);
  --gradient-hero: linear-gradient(135deg, #0d9488 0%, #0891b2 100%);
}

@media (prefers-color-scheme: dark) {
  :root {
    --clr-bg: #020f0e;
    --clr-surface: #041a19;
    --clr-surface-alt: #062a28;
    --clr-text: #e0fff8;
    --clr-text-muted: #3f8f8a;
    --clr-border: rgba(94, 234, 212, 0.1);
    --clr-primary: #2dd4bf;
    --clr-accent: #4ade80;
  }
}
```

---

## Category: Tech / Startup

### 6. Vercel Dark (Developer Tools)
**Personality:** Dev tools, CLI products, infrastructure, open source
**Seen on:** Vercel, Linear (dark mode), Shuttle

```css
:root {
  --clr-primary: #000000;
  --clr-primary-dark: #171717;
  --clr-primary-light: #404040;
  --clr-secondary: #6366f1;
  --clr-accent: #ffffff;
  --clr-bg: #ffffff;
  --clr-surface: #fafafa;
  --clr-surface-alt: #f5f5f5;
  --clr-text: #0a0a0a;
  --clr-text-muted: #737373;
  --clr-border: rgba(0, 0, 0, 0.09);
  --gradient-hero: linear-gradient(180deg, #ffffff 0%, #f5f5f5 100%);
}

@media (prefers-color-scheme: dark) {
  :root {
    --clr-bg: #000000;
    --clr-surface: #111111;
    --clr-surface-alt: #1a1a1a;
    --clr-text: #ededed;
    --clr-text-muted: #888888;
    --clr-border: rgba(255, 255, 255, 0.08);
    --clr-primary: #ffffff;
    --clr-primary-dark: #ededed;
  }
}
```

---

### 7. Electric Green (AI / Futuristic)
**Personality:** AI tools, hacker culture, terminal aesthetic, crypto

```css
:root {
  --clr-primary: #16a34a;
  --clr-primary-dark: #15803d;
  --clr-primary-light: #4ade80;
  --clr-secondary: #0ea5e9;
  --clr-accent: #facc15;
  --clr-bg: #f0fdf4;
  --clr-surface: #dcfce7;
  --clr-surface-alt: #bbf7d0;
  --clr-text: #052e16;
  --clr-text-muted: #166534;
  --clr-border: rgba(22, 163, 74, 0.15);
  --gradient-hero: linear-gradient(135deg, #16a34a 0%, #0ea5e9 100%);
}

@media (prefers-color-scheme: dark) {
  :root {
    --clr-bg: #000a02;
    --clr-surface: #00110a;
    --clr-surface-alt: #001a10;
    --clr-text: #d1fae5;
    --clr-text-muted: #22703c;
    --clr-border: rgba(74, 222, 128, 0.1);
    --clr-primary: #4ade80;
    --clr-secondary: #38bdf8;
  }
}
```

---

## Category: Luxury

### 8. Black Gold (Premium)
**Personality:** Luxury brands, high-end services, premium SaaS, fashion

```css
:root {
  --clr-primary: #b45309;
  --clr-primary-dark: #92400e;
  --clr-primary-light: #fcd34d;
  --clr-secondary: #78716c;
  --clr-accent: #d4af37;
  --clr-bg: #fffef8;
  --clr-surface: #fdf7e3;
  --clr-surface-alt: #faebc2;
  --clr-text: #1c1108;
  --clr-text-muted: #6b5a3a;
  --clr-border: rgba(180, 83, 9, 0.1);
  --gradient-hero: linear-gradient(135deg, #1c1108 0%, #4a3520 50%, #b45309 100%);
}

@media (prefers-color-scheme: dark) {
  :root {
    --clr-bg: #0c0800;
    --clr-surface: #161000;
    --clr-surface-alt: #201800;
    --clr-text: #fff8e1;
    --clr-text-muted: #7a6030;
    --clr-border: rgba(212, 175, 55, 0.12);
    --clr-primary: #fbbf24;
    --clr-accent: #fde68a;
  }
}
```

---

## Category: Nature / Eco

### 9. Earth Sage (Sustainable / Nature)
**Personality:** Eco brands, sustainability, organic products, outdoor apps

```css
:root {
  --clr-primary: #4a7c59;
  --clr-primary-dark: #3a6147;
  --clr-primary-light: #86b899;
  --clr-secondary: #8b7355;
  --clr-accent: #c4714e;
  --clr-bg: #fdf8f3;
  --clr-surface: #f5f0e8;
  --clr-surface-alt: #ece5d8;
  --clr-text: #1a2a1c;
  --clr-text-muted: #5a6b5c;
  --clr-border: rgba(74, 124, 89, 0.12);
  --gradient-hero: linear-gradient(135deg, #4a7c59 0%, #8b7355 100%);
}

@media (prefers-color-scheme: dark) {
  :root {
    --clr-bg: #080e09;
    --clr-surface: #0e1810;
    --clr-surface-alt: #142018;
    --clr-text: #e0f0e3;
    --clr-text-muted: #4a6b50;
    --clr-border: rgba(134, 184, 153, 0.1);
    --clr-primary: #86b899;
    --clr-accent: #d4856a;
  }
}
```

---

### 10. Ocean Blue (Clean / Calm)
**Personality:** Travel, wellness, productivity, educational platforms

```css
:root {
  --clr-primary: #0369a1;
  --clr-primary-dark: #075985;
  --clr-primary-light: #7dd3fc;
  --clr-secondary: #0891b2;
  --clr-accent: #f0abfc;
  --clr-bg: #f0f9ff;
  --clr-surface: #e0f2fe;
  --clr-surface-alt: #bae6fd;
  --clr-text: #082f49;
  --clr-text-muted: #2c5f7a;
  --clr-border: rgba(3, 105, 161, 0.12);
  --gradient-hero: linear-gradient(135deg, #0369a1 0%, #0891b2 100%);
}

@media (prefers-color-scheme: dark) {
  :root {
    --clr-bg: #020c14;
    --clr-surface: #04141f;
    --clr-surface-alt: #071e2e;
    --clr-text: #e0f2fe;
    --clr-text-muted: #2a6a8a;
    --clr-border: rgba(125, 211, 252, 0.1);
    --clr-primary: #38bdf8;
    --clr-accent: #e879f9;
  }
}
```

---

## How to Pick a Palette

| Client Type | Use Palette |
|-------------|-------------|
| SaaS / Developer tools | #1 Indigo Professional or #6 Vercel Dark |
| Finance / Legal / Enterprise | #2 Midnight Blue |
| Creative agency / Bold startup | #3 Electric Purple |
| Consumer app / Lifestyle | #4 Sunset Coral |
| Healthcare / Medical | #5 Clean Teal |
| AI / Crypto / Gaming | #7 Electric Green or #3 Electric Purple |
| Luxury brand / Premium SaaS | #8 Black Gold |
| Eco / Sustainability | #9 Earth Sage |
| Travel / Education | #10 Ocean Blue |

## Rules for Using Palettes
1. **Never add a 4th color** — 3 is the max (primary, secondary, accent used sparingly)
2. **Accent color = 5% of design** — use it on 1 key CTA, not everywhere
3. **Test contrast** — ensure 4.5:1 ratio for body text (use webaim.org/resources/contrastchecker)
4. **Gradients = primary → secondary** (same palette row)
5. **Dark mode** — don't just flip colors; darken backgrounds to near-black, reduce saturation on primary
