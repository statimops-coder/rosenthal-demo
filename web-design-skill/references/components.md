# Component Kit — Copy-Paste Ready Modern Components

> All components: vanilla HTML + CSS, mobile-first, responsive, animated.
> CSS custom properties used throughout — override in `:root` to theme.
> Add the IntersectionObserver script once per page for `.reveal` animations.

---

## Shared Base CSS

```css
/* Add this once at the top of your stylesheet */
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --clr-primary: #6366f1;
  --clr-primary-dark: #4f46e5;
  --clr-accent: #8b5cf6;
  --clr-bg: #ffffff;
  --clr-surface: #f8fafc;
  --clr-text: #0f172a;
  --clr-text-muted: #64748b;
  --clr-border: rgba(0, 0, 0, 0.08);
  --radius-sm: 8px;
  --radius-md: 16px;
  --radius-lg: 24px;
  --radius-full: 9999px;
  --shadow-sm: 0 1px 3px rgba(0,0,0,.08), 0 1px 2px rgba(0,0,0,.06);
  --shadow-md: 0 4px 16px rgba(0,0,0,.10), 0 2px 6px rgba(0,0,0,.06);
  --shadow-lg: 0 20px 40px rgba(0,0,0,.12), 0 8px 16px rgba(0,0,0,.08);
  --transition: 0.25s cubic-bezier(0.2, 0, 0, 1);
  --section-py: clamp(60px, 8vw, 120px);
  --container-max: 1200px;
}

.container {
  width: 100%;
  max-width: var(--container-max);
  margin-inline: auto;
  padding-inline: clamp(16px, 4vw, 48px);
}

/* Scroll reveal */
.reveal {
  opacity: 0;
  transform: translateY(24px);
  transition: opacity 0.6s ease, transform 0.6s cubic-bezier(0.16, 1, 0.3, 1);
}
.reveal.visible { opacity: 1; transform: none; }

@media (prefers-reduced-motion: reduce) {
  .reveal { transition: none; opacity: 1; transform: none; }
}
```

```html
<!-- Add before </body> — powers all .reveal animations -->
<script>
const observer = new IntersectionObserver(
  (entries) => entries.forEach(e => e.isIntersecting && e.target.classList.add('visible')),
  { threshold: 0.1, rootMargin: '0px 0px -40px 0px' }
);
document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
</script>
```

---

## 1. HERO — Variant A: Centered Text + Aurora Gradient

```html
<section class="hero-aurora">
  <div class="container">
    <div class="hero-badge">✦ Launching Spring 2026</div>
    <h1 class="hero-title">
      Build faster.<br>
      <span class="gradient-text">Ship smarter.</span>
    </h1>
    <p class="hero-sub">
      The platform modern teams use to design, build, and scale products
      without the overhead. Join 12,000+ developers who ship daily.
    </p>
    <div class="hero-cta">
      <a href="#" class="btn btn-primary">Get started free</a>
      <a href="#" class="btn btn-ghost">Watch demo →</a>
    </div>
    <div class="hero-trust">
      <div class="avatar-stack">
        <img src="https://i.pravatar.cc/32?img=1" alt="">
        <img src="https://i.pravatar.cc/32?img=2" alt="">
        <img src="https://i.pravatar.cc/32?img=3" alt="">
        <img src="https://i.pravatar.cc/32?img=4" alt="">
      </div>
      <span>Trusted by <strong>12,000+</strong> teams worldwide</span>
    </div>
  </div>
</section>
```

```css
.hero-aurora {
  min-height: 100svh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  background:
    radial-gradient(ellipse at 20% 40%, rgba(99, 102, 241, 0.2) 0%, transparent 55%),
    radial-gradient(ellipse at 80% 20%, rgba(139, 92, 246, 0.2) 0%, transparent 55%),
    radial-gradient(ellipse at 60% 80%, rgba(59, 130, 246, 0.15) 0%, transparent 55%),
    #fafafa;
  padding: clamp(80px, 12vw, 140px) 0;
}

.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  font-size: 0.8125rem;
  font-weight: 500;
  color: var(--clr-primary);
  background: rgba(99, 102, 241, 0.08);
  border: 1px solid rgba(99, 102, 241, 0.2);
  padding: 5px 14px;
  border-radius: var(--radius-full);
  margin-bottom: 24px;
}

.hero-title {
  font-size: clamp(2.5rem, 7vw, 4.5rem);
  font-weight: 700;
  line-height: 1.1;
  letter-spacing: -0.03em;
  color: var(--clr-text);
  margin-bottom: 20px;
}

.gradient-text {
  background: linear-gradient(135deg, var(--clr-primary) 0%, var(--clr-accent) 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero-sub {
  font-size: clamp(1rem, 2vw, 1.25rem);
  color: var(--clr-text-muted);
  max-width: 560px;
  margin-inline: auto;
  line-height: 1.65;
  margin-bottom: 36px;
}

.hero-cta {
  display: flex;
  gap: 12px;
  justify-content: center;
  flex-wrap: wrap;
  margin-bottom: 48px;
}

.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  padding: 12px 24px;
  border-radius: var(--radius-full);
  font-size: 0.9375rem;
  font-weight: 500;
  text-decoration: none;
  transition: all var(--transition);
  cursor: pointer;
  border: none;
  white-space: nowrap;
}

.btn-primary {
  background: var(--clr-primary);
  color: white;
  box-shadow: 0 4px 14px rgba(99, 102, 241, 0.35);
}
.btn-primary:hover {
  background: var(--clr-primary-dark);
  transform: translateY(-2px);
  box-shadow: 0 8px 20px rgba(99, 102, 241, 0.4);
}

.btn-ghost {
  background: transparent;
  color: var(--clr-text);
  border: 1px solid var(--clr-border);
}
.btn-ghost:hover {
  background: var(--clr-surface);
  border-color: rgba(0,0,0,0.15);
}

.hero-trust {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  color: var(--clr-text-muted);
  font-size: 0.875rem;
}

.avatar-stack {
  display: flex;
}
.avatar-stack img {
  width: 28px;
  height: 28px;
  border-radius: 50%;
  border: 2px solid white;
  margin-left: -8px;
  object-fit: cover;
}
.avatar-stack img:first-child { margin-left: 0; }
```

---

## 2. HERO — Variant B: Split Layout

```html
<section class="hero-split">
  <div class="container hero-split__inner">
    <div class="hero-split__text">
      <div class="hero-badge">New in 2026</div>
      <h1>Your work,<br><span class="gradient-text">supercharged.</span></h1>
      <p>Stop juggling 12 tools. Velocity brings your team's projects, docs, and conversations into one fast, beautiful workspace.</p>
      <div class="hero-cta">
        <a href="#" class="btn btn-primary">Start free trial</a>
        <a href="#" class="btn btn-ghost">See features</a>
      </div>
      <p class="hero-footnote">No credit card required · 14-day free trial · Cancel anytime</p>
    </div>
    <div class="hero-split__visual">
      <div class="product-mockup">
        <!-- Replace with actual screenshot or SVG illustration -->
        <div class="mockup-placeholder">🖥️ Product Screenshot</div>
      </div>
    </div>
  </div>
</section>
```

```css
.hero-split { padding: var(--section-py) 0; background: var(--clr-bg); }

.hero-split__inner {
  display: grid;
  gap: clamp(40px, 6vw, 80px);
  align-items: center;
}
@media (min-width: 768px) {
  .hero-split__inner { grid-template-columns: 1fr 1fr; }
}

.hero-split__text h1 {
  font-size: clamp(2.25rem, 5vw, 3.75rem);
  font-weight: 700;
  line-height: 1.1;
  letter-spacing: -0.025em;
  margin-block: 16px 20px;
}
.hero-split__text p {
  font-size: 1.0625rem;
  color: var(--clr-text-muted);
  line-height: 1.65;
  max-width: 48ch;
  margin-bottom: 32px;
}

.hero-footnote {
  margin-top: 16px;
  font-size: 0.8125rem;
  color: var(--clr-text-muted);
}

.product-mockup {
  border-radius: var(--radius-lg);
  overflow: hidden;
  box-shadow: var(--shadow-lg);
  background: var(--clr-surface);
  aspect-ratio: 4/3;
}
.mockup-placeholder {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2rem;
  background: linear-gradient(135deg, #f0f4ff 0%, #e8e8ff 100%);
}
```

---

## 3. HERO — Variant C: Dark + Glow

```html
<section class="hero-dark">
  <div class="hero-dark__glow"></div>
  <div class="container" style="position:relative;z-index:1;text-align:center">
    <h1 class="hero-dark__title">The future of<br><span class="glow-text">AI-powered dev.</span></h1>
    <p class="hero-dark__sub">Built for engineers who refuse to slow down. Deploy, monitor, and scale with one command.</p>
    <a href="#" class="btn btn-glow">Get early access</a>
  </div>
</section>
```

```css
.hero-dark {
  position: relative;
  min-height: 100svh;
  display: flex;
  align-items: center;
  background: #080808;
  overflow: hidden;
  padding: clamp(80px, 12vw, 140px) 0;
}

.hero-dark__glow {
  position: absolute;
  top: 50%; left: 50%;
  transform: translate(-50%, -50%);
  width: 800px; height: 500px;
  background: radial-gradient(ellipse, rgba(99,102,241,0.3) 0%, transparent 70%);
  pointer-events: none;
}

.hero-dark__title {
  font-size: clamp(2.5rem, 7vw, 5rem);
  font-weight: 700;
  line-height: 1.05;
  letter-spacing: -0.03em;
  color: #f0f0f0;
  margin-bottom: 20px;
}

.glow-text {
  background: linear-gradient(135deg, #818cf8, #c084fc);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero-dark__sub {
  color: rgba(240,240,240,0.55);
  font-size: clamp(1rem, 2vw, 1.2rem);
  max-width: 520px;
  margin-inline: auto;
  line-height: 1.7;
  margin-bottom: 36px;
}

.btn-glow {
  display: inline-flex;
  align-items: center;
  padding: 14px 32px;
  border-radius: var(--radius-full);
  background: var(--clr-primary);
  color: white;
  font-size: 1rem;
  font-weight: 500;
  text-decoration: none;
  box-shadow: 0 0 40px rgba(99,102,241,0.5);
  transition: all var(--transition);
}
.btn-glow:hover {
  box-shadow: 0 0 60px rgba(99,102,241,0.7);
  transform: translateY(-2px);
}
```

---

## 4. NAVIGATION — Glassmorphism Sticky

```html
<nav class="nav-glass" id="mainNav">
  <div class="container nav-glass__inner">
    <a href="/" class="nav-logo">Velocity</a>
    <ul class="nav-links">
      <li><a href="#features">Features</a></li>
      <li><a href="#pricing">Pricing</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#blog">Blog</a></li>
    </ul>
    <div class="nav-actions">
      <a href="#" class="btn-nav-ghost">Sign in</a>
      <a href="#" class="btn btn-primary" style="padding:8px 20px;font-size:.875rem">Get started</a>
    </div>
    <button class="nav-hamburger" aria-label="Menu">☰</button>
  </div>
</nav>
```

```css
.nav-glass {
  position: fixed;
  top: 0; left: 0; right: 0;
  z-index: 1000;
  transition: background var(--transition), border-color var(--transition), backdrop-filter var(--transition);
}

.nav-glass.scrolled {
  background: rgba(255, 255, 255, 0.85);
  backdrop-filter: blur(20px) saturate(180%);
  -webkit-backdrop-filter: blur(20px) saturate(180%);
  border-bottom: 1px solid rgba(0, 0, 0, 0.08);
  box-shadow: 0 1px 20px rgba(0,0,0,.05);
}

.nav-glass__inner {
  display: flex;
  align-items: center;
  gap: 32px;
  height: 64px;
}

.nav-logo {
  font-size: 1.125rem;
  font-weight: 700;
  text-decoration: none;
  color: var(--clr-text);
  letter-spacing: -0.02em;
  margin-right: auto;
}

.nav-links {
  display: none;
  list-style: none;
  gap: 4px;
}
@media (min-width: 768px) {
  .nav-links { display: flex; }
}

.nav-links a {
  padding: 6px 12px;
  border-radius: var(--radius-sm);
  text-decoration: none;
  color: var(--clr-text-muted);
  font-size: 0.9375rem;
  font-weight: 450;
  transition: color var(--transition), background var(--transition);
}
.nav-links a:hover { color: var(--clr-text); background: rgba(0,0,0,.05); }

.btn-nav-ghost {
  text-decoration: none;
  color: var(--clr-text-muted);
  font-size: 0.9375rem;
  padding: 8px 16px;
  transition: color var(--transition);
}
.btn-nav-ghost:hover { color: var(--clr-text); }

.nav-hamburger {
  display: flex;
  background: none;
  border: none;
  cursor: pointer;
  font-size: 1.25rem;
  margin-left: auto;
}
@media (min-width: 768px) {
  .nav-hamburger { display: none; }
  .nav-actions { display: flex; align-items: center; gap: 8px; }
}
```

```html
<script>
const nav = document.getElementById('mainNav');
window.addEventListener('scroll', () => {
  nav.classList.toggle('scrolled', window.scrollY > 20);
});
</script>
```

---

## 5. BENTO GRID

```html
<section class="bento-section">
  <div class="container">
    <h2 class="reveal" style="text-align:center;font-size:clamp(1.75rem,4vw,2.75rem);font-weight:700;letter-spacing:-0.02em;margin-bottom:48px">
      Everything you need, nothing you don't.
    </h2>
    <div class="bento-grid">
      <div class="bento-card bento-card--wide reveal">
        <div class="bento-icon">⚡</div>
        <h3>Blazing fast deploys</h3>
        <p>Push to git, live in 30 seconds. Zero config, automatic scaling.</p>
        <div class="bento-visual bento-visual--speed"></div>
      </div>
      <div class="bento-card reveal" style="--delay:100ms">
        <div class="bento-icon">🔒</div>
        <h3>Enterprise security</h3>
        <p>SOC 2 Type II, SSO, audit logs. Built-in, not bolted on.</p>
      </div>
      <div class="bento-card reveal" style="--delay:150ms">
        <div class="bento-icon">🌍</div>
        <h3>Global edge network</h3>
        <p>Deployed to 40+ regions. Sub-50ms response worldwide.</p>
      </div>
      <div class="bento-card bento-card--tall reveal" style="--delay:200ms">
        <div class="bento-icon">📊</div>
        <h3>Real-time analytics</h3>
        <p>See exactly what's happening. Every request, every error, in real time.</p>
      </div>
      <div class="bento-card reveal" style="--delay:250ms">
        <div class="bento-icon">🤝</div>
        <h3>Team collaboration</h3>
        <p>Comments, reviews, shared environments built in.</p>
      </div>
    </div>
  </div>
</section>
```

```css
.bento-section { padding: var(--section-py) 0; background: var(--clr-bg); }

.bento-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 16px;
}

@media (min-width: 640px) {
  .bento-grid { grid-template-columns: repeat(2, 1fr); }
  .bento-card--wide { grid-column: span 2; }
}

@media (min-width: 1024px) {
  .bento-grid { grid-template-columns: repeat(3, 1fr); }
  .bento-card--wide { grid-column: span 2; }
  .bento-card--tall { grid-row: span 2; }
}

.bento-card {
  background: var(--clr-surface);
  border: 1px solid var(--clr-border);
  border-radius: var(--radius-lg);
  padding: 28px;
  transition: transform var(--transition), box-shadow var(--transition);
  transition-delay: var(--delay, 0ms);
  min-height: 200px;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.bento-card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-md);
  border-color: rgba(99, 102, 241, 0.2);
}

.bento-icon {
  font-size: 2rem;
  margin-bottom: 4px;
}

.bento-card h3 {
  font-size: 1.125rem;
  font-weight: 600;
  color: var(--clr-text);
  letter-spacing: -0.01em;
}

.bento-card p {
  font-size: 0.9375rem;
  color: var(--clr-text-muted);
  line-height: 1.6;
}
```

---

## 6. FEATURE CARDS — Glassmorphism

```html
<section class="features-section">
  <div class="container">
    <div class="section-header reveal">
      <h2>Built for builders</h2>
      <p>Every feature designed to get out of your way and let you ship.</p>
    </div>
    <div class="features-grid">
      <div class="feature-card reveal">
        <div class="feature-card__icon" style="--icon-color:#6366f1">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M13 2L3 14h9l-1 8 10-12h-9l1-8z"/></svg>
        </div>
        <h3>Instant deploys</h3>
        <p>Git push triggers an automatic build and deployment. Live in under 30 seconds, every time.</p>
        <a href="#" class="feature-card__link">Learn more →</a>
      </div>
      <div class="feature-card reveal" style="--delay:100ms">
        <div class="feature-card__icon" style="--icon-color:#8b5cf6">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="11" width="18" height="11" rx="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/></svg>
        </div>
        <h3>Zero-trust security</h3>
        <p>Every request verified, every secret encrypted. SOC 2 compliance built in, not added later.</p>
        <a href="#" class="feature-card__link">Learn more →</a>
      </div>
      <div class="feature-card reveal" style="--delay:200ms">
        <div class="feature-card__icon" style="--icon-color:#06b6d4">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><path d="M2 12h20M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>
        </div>
        <h3>Global edge network</h3>
        <p>Serve from 40+ PoPs worldwide. Your users get sub-50ms responses regardless of location.</p>
        <a href="#" class="feature-card__link">Learn more →</a>
      </div>
    </div>
  </div>
</section>
```

```css
.features-section { padding: var(--section-py) 0; background: var(--clr-surface); }

.section-header {
  text-align: center;
  max-width: 600px;
  margin-inline: auto;
  margin-bottom: 56px;
}
.section-header h2 {
  font-size: clamp(1.75rem, 4vw, 2.5rem);
  font-weight: 700;
  letter-spacing: -0.025em;
  color: var(--clr-text);
  margin-bottom: 12px;
}
.section-header p {
  font-size: 1.0625rem;
  color: var(--clr-text-muted);
  line-height: 1.65;
}

.features-grid {
  display: grid;
  gap: 20px;
  grid-template-columns: 1fr;
}
@media (min-width: 640px) { .features-grid { grid-template-columns: repeat(2, 1fr); } }
@media (min-width: 1024px) { .features-grid { grid-template-columns: repeat(3, 1fr); } }

.feature-card {
  background: rgba(255, 255, 255, 0.7);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  border: 1px solid rgba(255, 255, 255, 0.8);
  border-radius: var(--radius-lg);
  padding: 28px;
  display: flex;
  flex-direction: column;
  gap: 12px;
  transition: transform var(--transition), box-shadow var(--transition);
  transition-delay: var(--delay, 0ms);
}
.feature-card:hover { transform: translateY(-4px); box-shadow: var(--shadow-md); }

.feature-card__icon {
  width: 48px; height: 48px;
  border-radius: var(--radius-sm);
  background: rgba(from var(--icon-color) r g b / 0.12);
  color: var(--icon-color);
  display: flex;
  align-items: center;
  justify-content: center;
}

.feature-card h3 {
  font-size: 1.0625rem;
  font-weight: 600;
  color: var(--clr-text);
}

.feature-card p {
  font-size: 0.9375rem;
  color: var(--clr-text-muted);
  line-height: 1.6;
  flex: 1;
}

.feature-card__link {
  font-size: 0.875rem;
  color: var(--clr-primary);
  text-decoration: none;
  font-weight: 500;
  transition: gap var(--transition);
  align-self: flex-start;
}
.feature-card__link:hover { text-decoration: underline; }
```

---

## 7. TESTIMONIALS — Card Grid

```html
<section class="testimonials-section">
  <div class="container">
    <h2 class="reveal" style="text-align:center;font-size:clamp(1.75rem,4vw,2.5rem);font-weight:700;letter-spacing:-0.025em;margin-bottom:48px">
      Loved by teams at every stage
    </h2>
    <div class="testimonials-grid">
      <blockquote class="testimonial-card reveal">
        <p>"Velocity cut our deployment time from 45 minutes to under 60 seconds. It's the single best infrastructure decision we've made this year."</p>
        <footer>
          <img src="https://i.pravatar.cc/48?img=10" alt="Sarah Chen">
          <div>
            <cite>Sarah Chen</cite>
            <span>CTO at Meridian Health</span>
          </div>
        </footer>
      </blockquote>
      <blockquote class="testimonial-card reveal" style="--delay:100ms">
        <p>"The DX is unreal. I went from 'I'll try it' to 'we're migrating everything' in one afternoon. The team just gets what developers actually need."</p>
        <footer>
          <img src="https://i.pravatar.cc/48?img=20" alt="Marcus Rivera">
          <div>
            <cite>Marcus Rivera</cite>
            <span>Lead Engineer at Flux Systems</span>
          </div>
        </footer>
      </blockquote>
      <blockquote class="testimonial-card reveal" style="--delay:200ms">
        <p>"We evaluated five platforms. Velocity was the only one where our junior devs could deploy confidently on day one. The guardrails are invisible but effective."</p>
        <footer>
          <img src="https://i.pravatar.cc/48?img=30" alt="Priya Nair">
          <div>
            <cite>Priya Nair</cite>
            <span>VP Engineering at Strata</span>
          </div>
        </footer>
      </blockquote>
    </div>
  </div>
</section>
```

```css
.testimonials-section { padding: var(--section-py) 0; background: var(--clr-bg); }

.testimonials-grid {
  display: grid;
  gap: 20px;
  grid-template-columns: 1fr;
}
@media (min-width: 640px) { .testimonials-grid { grid-template-columns: repeat(2, 1fr); } }
@media (min-width: 1024px) { .testimonials-grid { grid-template-columns: repeat(3, 1fr); } }

.testimonial-card {
  background: var(--clr-surface);
  border: 1px solid var(--clr-border);
  border-radius: var(--radius-lg);
  padding: 28px;
  transition-delay: var(--delay, 0ms);
}

.testimonial-card p {
  font-size: 1rem;
  color: var(--clr-text);
  line-height: 1.7;
  font-style: italic;
  margin-bottom: 20px;
}

.testimonial-card footer {
  display: flex;
  align-items: center;
  gap: 12px;
}
.testimonial-card footer img {
  width: 40px; height: 40px;
  border-radius: 50%;
  object-fit: cover;
}
.testimonial-card cite {
  display: block;
  font-style: normal;
  font-weight: 600;
  font-size: 0.875rem;
  color: var(--clr-text);
}
.testimonial-card span {
  font-size: 0.8125rem;
  color: var(--clr-text-muted);
}
```

---

## 8. PRICING TABLE

```html
<section class="pricing-section">
  <div class="container">
    <div class="pricing-header reveal">
      <h2>Simple, transparent pricing</h2>
      <p>Start free. Scale as you grow. No surprise bills.</p>
      <div class="pricing-toggle">
        <span>Monthly</span>
        <label class="toggle-switch">
          <input type="checkbox" id="billingToggle">
          <span class="toggle-thumb"></span>
        </label>
        <span>Annual <span class="save-badge">Save 20%</span></span>
      </div>
    </div>
    <div class="pricing-grid">
      <div class="pricing-card reveal">
        <div class="pricing-card__name">Starter</div>
        <div class="pricing-card__price">
          <span class="price-amount" data-monthly="0" data-annual="0">$0</span>
          <span class="price-period">/month</span>
        </div>
        <p class="pricing-card__desc">Perfect for side projects and personal portfolios.</p>
        <a href="#" class="btn btn-ghost" style="width:100%;justify-content:center;margin:20px 0">Get started free</a>
        <ul class="pricing-features">
          <li>✓ 3 projects</li>
          <li>✓ 1GB storage</li>
          <li>✓ 100GB bandwidth</li>
          <li>✓ Community support</li>
        </ul>
      </div>
      <div class="pricing-card pricing-card--featured reveal" style="--delay:100ms">
        <div class="pricing-card__badge">Most Popular</div>
        <div class="pricing-card__name">Pro</div>
        <div class="pricing-card__price">
          <span class="price-amount" data-monthly="29" data-annual="23">$29</span>
          <span class="price-period">/month</span>
        </div>
        <p class="pricing-card__desc">For growing teams shipping products that matter.</p>
        <a href="#" class="btn btn-primary" style="width:100%;justify-content:center;margin:20px 0">Start Pro trial</a>
        <ul class="pricing-features">
          <li>✓ Unlimited projects</li>
          <li>✓ 100GB storage</li>
          <li>✓ 1TB bandwidth</li>
          <li>✓ Priority support</li>
          <li>✓ Custom domains</li>
          <li>✓ Analytics dashboard</li>
        </ul>
      </div>
      <div class="pricing-card reveal" style="--delay:200ms">
        <div class="pricing-card__name">Enterprise</div>
        <div class="pricing-card__price">
          <span class="price-amount">Custom</span>
        </div>
        <p class="pricing-card__desc">Dedicated infrastructure, compliance, and SLAs.</p>
        <a href="#" class="btn btn-ghost" style="width:100%;justify-content:center;margin:20px 0">Contact sales</a>
        <ul class="pricing-features">
          <li>✓ Unlimited everything</li>
          <li>✓ Dedicated infrastructure</li>
          <li>✓ SOC 2 & HIPAA</li>
          <li>✓ SSO / SAML</li>
          <li>✓ 99.99% SLA</li>
          <li>✓ Dedicated support</li>
        </ul>
      </div>
    </div>
  </div>
</section>
```

```css
.pricing-section { padding: var(--section-py) 0; background: var(--clr-surface); }

.pricing-header {
  text-align: center;
  margin-bottom: 48px;
}
.pricing-header h2 {
  font-size: clamp(1.75rem, 4vw, 2.5rem);
  font-weight: 700;
  letter-spacing: -0.025em;
  margin-bottom: 12px;
}
.pricing-header > p { color: var(--clr-text-muted); font-size: 1.0625rem; margin-bottom: 24px; }

.pricing-toggle {
  display: inline-flex;
  align-items: center;
  gap: 12px;
  font-size: 0.9375rem;
  color: var(--clr-text-muted);
}
.toggle-switch {
  position: relative;
  display: inline-block;
  width: 44px; height: 24px;
  cursor: pointer;
}
.toggle-switch input { opacity: 0; width: 0; height: 0; }
.toggle-thumb {
  position: absolute;
  inset: 0;
  background: #cbd5e1;
  border-radius: var(--radius-full);
  transition: background var(--transition);
}
.toggle-thumb::after {
  content: '';
  position: absolute;
  top: 3px; left: 3px;
  width: 18px; height: 18px;
  background: white;
  border-radius: 50%;
  transition: transform var(--transition);
}
input:checked ~ .toggle-thumb { background: var(--clr-primary); }
input:checked ~ .toggle-thumb::after { transform: translateX(20px); }

.save-badge {
  display: inline-block;
  font-size: 0.75rem;
  font-weight: 600;
  color: #16a34a;
  background: #dcfce7;
  padding: 2px 8px;
  border-radius: var(--radius-full);
}

.pricing-grid {
  display: grid;
  gap: 20px;
  grid-template-columns: 1fr;
  align-items: start;
}
@media (min-width: 640px) { .pricing-grid { grid-template-columns: repeat(2, 1fr); } }
@media (min-width: 1024px) { .pricing-grid { grid-template-columns: repeat(3, 1fr); } }

.pricing-card {
  background: var(--clr-bg);
  border: 1px solid var(--clr-border);
  border-radius: var(--radius-lg);
  padding: 32px;
  transition-delay: var(--delay, 0ms);
  position: relative;
}

.pricing-card--featured {
  border-color: var(--clr-primary);
  box-shadow: 0 0 0 1px var(--clr-primary), var(--shadow-md);
  transform: scale(1.02);
}

.pricing-card__badge {
  position: absolute;
  top: -12px; left: 50%;
  transform: translateX(-50%);
  background: var(--clr-primary);
  color: white;
  font-size: 0.75rem;
  font-weight: 600;
  padding: 4px 14px;
  border-radius: var(--radius-full);
}

.pricing-card__name {
  font-size: 0.875rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: var(--clr-text-muted);
  margin-bottom: 8px;
}
.pricing-card__price {
  display: flex;
  align-items: baseline;
  gap: 4px;
  margin-bottom: 8px;
}
.price-amount {
  font-size: 2.5rem;
  font-weight: 700;
  letter-spacing: -0.03em;
  color: var(--clr-text);
}
.price-period { color: var(--clr-text-muted); font-size: 0.9375rem; }
.pricing-card__desc { color: var(--clr-text-muted); font-size: 0.9375rem; line-height: 1.55; }

.pricing-features {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.pricing-features li { font-size: 0.9375rem; color: var(--clr-text); }
```

```html
<script>
document.getElementById('billingToggle').addEventListener('change', function() {
  const annual = this.checked;
  document.querySelectorAll('.price-amount[data-monthly]').forEach(el => {
    const val = annual ? el.dataset.annual : el.dataset.monthly;
    el.textContent = val === '0' ? '$0' : `$${val}`;
  });
});
</script>
```

---

## 9. CTA SECTION

```html
<section class="cta-section">
  <div class="container">
    <div class="cta-card reveal">
      <div class="cta-card__bg"></div>
      <div class="cta-card__content">
        <h2>Ready to ship faster?</h2>
        <p>Join 12,000+ teams already building with Velocity. Get started in under 5 minutes.</p>
        <div class="cta-card__actions">
          <a href="#" class="btn btn-white">Start for free</a>
          <a href="#" class="btn btn-outline-white">Schedule a demo</a>
        </div>
        <p class="cta-card__footnote">No credit card · 14-day trial · Cancel anytime</p>
      </div>
    </div>
  </div>
</section>
```

```css
.cta-section { padding: var(--section-py) 0; background: var(--clr-bg); }

.cta-card {
  position: relative;
  border-radius: 28px;
  overflow: hidden;
  padding: clamp(48px, 8vw, 80px);
  text-align: center;
}

.cta-card__bg {
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, var(--clr-primary) 0%, var(--clr-accent) 100%);
}

.cta-card__content {
  position: relative;
  z-index: 1;
}

.cta-card h2 {
  font-size: clamp(1.75rem, 4vw, 3rem);
  font-weight: 700;
  color: white;
  letter-spacing: -0.025em;
  margin-bottom: 12px;
}
.cta-card > .cta-card__content > p {
  color: rgba(255,255,255,0.8);
  font-size: 1.0625rem;
  max-width: 520px;
  margin-inline: auto;
  line-height: 1.65;
  margin-bottom: 32px;
}
.cta-card__actions {
  display: flex;
  gap: 12px;
  justify-content: center;
  flex-wrap: wrap;
  margin-bottom: 16px;
}

.btn-white {
  background: white;
  color: var(--clr-primary);
  font-weight: 600;
}
.btn-white:hover { background: rgba(255,255,255,.9); transform: translateY(-2px); }

.btn-outline-white {
  background: transparent;
  color: white;
  border: 1px solid rgba(255,255,255,0.4);
}
.btn-outline-white:hover { background: rgba(255,255,255,.1); }

.cta-card__footnote { color: rgba(255,255,255,0.6); font-size: 0.8125rem; }
```

---

## 10. FOOTER — Multi-Column

```html
<footer class="site-footer">
  <div class="container">
    <div class="footer-main">
      <div class="footer-brand">
        <a href="/" class="nav-logo">Velocity</a>
        <p>The platform modern teams use to build, deploy, and scale without the overhead.</p>
        <div class="footer-social">
          <a href="#" aria-label="Twitter/X">𝕏</a>
          <a href="#" aria-label="GitHub">⌥</a>
          <a href="#" aria-label="LinkedIn">in</a>
        </div>
      </div>
      <nav class="footer-nav">
        <div class="footer-col">
          <h4>Product</h4>
          <a href="#">Features</a>
          <a href="#">Pricing</a>
          <a href="#">Changelog</a>
          <a href="#">Roadmap</a>
          <a href="#">Status</a>
        </div>
        <div class="footer-col">
          <h4>Company</h4>
          <a href="#">About</a>
          <a href="#">Blog</a>
          <a href="#">Careers</a>
          <a href="#">Press</a>
        </div>
        <div class="footer-col">
          <h4>Resources</h4>
          <a href="#">Documentation</a>
          <a href="#">API Reference</a>
          <a href="#">Community</a>
          <a href="#">Support</a>
        </div>
      </nav>
    </div>
    <div class="footer-bottom">
      <p>© 2026 Velocity, Inc. All rights reserved.</p>
      <div class="footer-legal">
        <a href="#">Privacy</a>
        <a href="#">Terms</a>
        <a href="#">Cookies</a>
      </div>
    </div>
  </div>
</footer>
```

```css
.site-footer {
  background: var(--clr-text);
  color: rgba(255,255,255,0.7);
  padding: 64px 0 32px;
}

.footer-main {
  display: grid;
  gap: 48px;
  margin-bottom: 48px;
}
@media (min-width: 768px) {
  .footer-main { grid-template-columns: 1fr 2fr; }
}

.footer-brand { display: flex; flex-direction: column; gap: 12px; }
.footer-brand .nav-logo { color: white; }
.footer-brand > p { font-size: 0.9375rem; line-height: 1.65; max-width: 28ch; }

.footer-social { display: flex; gap: 16px; }
.footer-social a {
  color: rgba(255,255,255,0.5);
  text-decoration: none;
  font-size: 1.1rem;
  transition: color var(--transition);
}
.footer-social a:hover { color: white; }

.footer-nav {
  display: grid;
  gap: 32px;
  grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
}

.footer-col { display: flex; flex-direction: column; gap: 10px; }

.footer-col h4 {
  font-size: 0.875rem;
  font-weight: 600;
  color: white;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  margin-bottom: 4px;
}

.footer-col a {
  color: rgba(255,255,255,0.55);
  text-decoration: none;
  font-size: 0.9375rem;
  transition: color var(--transition);
}
.footer-col a:hover { color: white; }

.footer-bottom {
  border-top: 1px solid rgba(255,255,255,0.1);
  padding-top: 24px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 12px;
  font-size: 0.875rem;
}

.footer-legal { display: flex; gap: 24px; }
.footer-legal a { color: rgba(255,255,255,0.5); text-decoration: none; }
.footer-legal a:hover { color: white; }
```

---

## 11. CONTACT FORM — Animated Labels

```html
<section class="contact-section">
  <div class="container" style="max-width:600px">
    <div class="section-header reveal">
      <h2>Get in touch</h2>
      <p>We typically respond within 2 hours on business days.</p>
    </div>
    <form class="contact-form reveal" style="--delay:100ms">
      <div class="form-row">
        <div class="form-group">
          <input type="text" id="fname" placeholder=" " required>
          <label for="fname">First name</label>
        </div>
        <div class="form-group">
          <input type="text" id="lname" placeholder=" " required>
          <label for="lname">Last name</label>
        </div>
      </div>
      <div class="form-group">
        <input type="email" id="email" placeholder=" " required>
        <label for="email">Email address</label>
      </div>
      <div class="form-group">
        <input type="text" id="company" placeholder=" ">
        <label for="company">Company (optional)</label>
      </div>
      <div class="form-group">
        <textarea id="message" rows="5" placeholder=" " required></textarea>
        <label for="message">Your message</label>
      </div>
      <button type="submit" class="btn btn-primary" style="width:100%;justify-content:center;padding:14px">Send message</button>
    </form>
  </div>
</section>
```

```css
.contact-section { padding: var(--section-py) 0; background: var(--clr-bg); }

.contact-form { display: flex; flex-direction: column; gap: 16px; }

.form-row { display: grid; gap: 16px; grid-template-columns: 1fr; }
@media (min-width: 480px) { .form-row { grid-template-columns: 1fr 1fr; } }

.form-group {
  position: relative;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 16px;
  border: 1px solid var(--clr-border);
  border-radius: var(--radius-sm);
  font-size: 1rem;
  font-family: inherit;
  color: var(--clr-text);
  background: var(--clr-bg);
  outline: none;
  transition: border-color var(--transition);
  resize: vertical;
}
.form-group input:focus,
.form-group textarea:focus { border-color: var(--clr-primary); }

.form-group label {
  position: absolute;
  top: 16px; left: 16px;
  font-size: 1rem;
  color: var(--clr-text-muted);
  pointer-events: none;
  transition: all 0.2s ease;
  background: var(--clr-bg);
  padding: 0 4px;
}

.form-group input:not(:placeholder-shown) ~ label,
.form-group input:focus ~ label,
.form-group textarea:not(:placeholder-shown) ~ label,
.form-group textarea:focus ~ label {
  top: -8px; left: 12px;
  font-size: 0.75rem;
  color: var(--clr-primary);
  font-weight: 500;
}
```

---

## 12. STATS / COUNTER SECTION

```html
<section class="stats-section">
  <div class="container">
    <div class="stats-grid">
      <div class="stat-card reveal">
        <div class="stat-number" data-target="12000">0</div>
        <div class="stat-label">Teams using Velocity</div>
      </div>
      <div class="stat-card reveal" style="--delay:100ms">
        <div class="stat-number" data-target="99.99" data-suffix="%">0</div>
        <div class="stat-label">Uptime SLA</div>
      </div>
      <div class="stat-card reveal" style="--delay:200ms">
        <div class="stat-number" data-target="47" data-suffix="ms">0</div>
        <div class="stat-label">Average response time</div>
      </div>
      <div class="stat-card reveal" style="--delay:300ms">
        <div class="stat-number" data-prefix="$" data-target="2.1" data-suffix="B">0</div>
        <div class="stat-label">In infrastructure managed</div>
      </div>
    </div>
  </div>
</section>
```

```css
.stats-section {
  padding: var(--section-py) 0;
  background: linear-gradient(135deg, var(--clr-primary) 0%, var(--clr-accent) 100%);
}

.stats-grid {
  display: grid;
  gap: 1px;
  background: rgba(255,255,255,0.15);
  border-radius: var(--radius-lg);
  overflow: hidden;
  grid-template-columns: repeat(2, 1fr);
}
@media (min-width: 768px) { .stats-grid { grid-template-columns: repeat(4, 1fr); } }

.stat-card {
  background: transparent;
  padding: 40px 32px;
  text-align: center;
  transition-delay: var(--delay, 0ms);
}

.stat-number {
  font-size: clamp(2rem, 5vw, 3rem);
  font-weight: 700;
  color: white;
  letter-spacing: -0.03em;
  line-height: 1;
  margin-bottom: 8px;
}

.stat-label {
  font-size: 0.9375rem;
  color: rgba(255,255,255,0.75);
  line-height: 1.4;
}
```

```html
<script>
// Animate stats when visible
const statsObserver = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (!entry.isIntersecting) return;
    const el = entry.target.querySelector('.stat-number');
    if (!el) return;
    const target = parseFloat(el.dataset.target);
    const prefix = el.dataset.prefix || '';
    const suffix = el.dataset.suffix || '';
    const decimals = target % 1 !== 0 ? 2 : 0;
    const isLarge = target >= 1000;
    let start = null;
    const duration = 1800;
    const animate = (ts) => {
      if (!start) start = ts;
      const progress = Math.min((ts - start) / duration, 1);
      const eased = 1 - Math.pow(1 - progress, 3);
      const val = target * eased;
      el.textContent = prefix + (isLarge ? Math.round(val).toLocaleString() : val.toFixed(decimals)) + suffix;
      if (progress < 1) requestAnimationFrame(animate);
    };
    requestAnimationFrame(animate);
    statsObserver.unobserve(entry.target);
  });
}, { threshold: 0.5 });

document.querySelectorAll('.stat-card').forEach(el => statsObserver.observe(el));
</script>
```

---

## HOW TO COMBINE THESE COMPONENTS

1. **Start with base CSS** (shared variables + container + reveal)
2. **Add nav** (glassmorphism sticky)
3. **Pick hero** based on project type:
   - SaaS/startup → Variant A (centered aurora)
   - Product showcase → Variant B (split)
   - Gaming/crypto/dark brand → Variant C (dark glow)
4. **Bento grid** for feature overview (modern, 2025 standard)
5. **Feature cards** for detailed feature breakdown
6. **Stats** for social proof numbers
7. **Testimonials** for trust signals
8. **Pricing** if applicable
9. **CTA section** before footer
10. **Footer** always multi-column for credibility

**Color theming:** Override `:root` variables only. Never hard-code hex values in components.
