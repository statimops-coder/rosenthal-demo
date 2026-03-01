# TASK: Rebuild Rosenthal Chiropractic Demo Website

## STEP 1 — READ BOTH SKILLS (mandatory before writing one line of HTML)
Read ALL these files in order:
1. web-design-skill/SKILL.md
2. web-design-skill/references/modern-patterns.md
3. web-design-skill/references/typography.md
4. web-design-skill/references/color-palettes.md
5. web-design-skill/references/components.md
6. web-design-skill/references/material-design-3.md

## STEP 2 — OWNER DESIGN RULES (absolute — violating these = rejected)
- NO rounded corners as default — sharp edges or max 2-4px, intentional only
- NO centering everything by default — left-aligned text, asymmetric layouts
- NO emojis as icons — Lucide Icons CDN only
  Add in <head>: <script src="https://unpkg.com/lucide@latest/dist/umd/lucide.min.js"></script>
  Call lucide.createIcons() at bottom of body
- NO flat cards — real photo backgrounds, overlays, shadows, hover transforms
- NO basic/rounded/sans-serif fonts — use editorial pairing from typography.md
- NO large body text — 14-15px base
- NO generic templates — every section custom-built
- NO em dashes anywhere in copy
- Soft effects only — no flashy, bouncy animations
- Layered depth — use z-index stacking, overlapping elements
- Real data only — no placeholders, no Lorem ipsum

## STEP 3 — REAL BUSINESS DATA (scraped from mrschiro.com)

### BUSINESS
Name: Rosenthal Chiropractic Clinic
Tagline: "Feel Good. Do More."
Phone: (727) 539-0075
Address: 12855 S. Belcher Road, Suite 1, Largo, FL 33773

### MISSION STATEMENT (real, use verbatim)
"The goal of Rosenthal Chiropractic Clinic is to provide effective chiropractic care with kindness, enthusiasm, and integrity. Rosenthal Chiropractic is committed to provide care to patients with a sincere desire for them to achieve their goals for vibrant health."

### ABOUT DR. MARCY L. SMURTHWAITE
- Native Floridian, originally from Miami
- Doctor of Chiropractic from Life University College of Chiropractic, Atlanta GA
- In private practice since 1994 (30+ years)
- Using instrument adjusting since 1987 -- no cracking, no twisting, no popping
- First doctor in Tampa Bay and second in Florida to use Cold Laser Technology
- Certified with American Society of Laser Therapy
- Over 100 hours in Spinal Rehabilitation; studied with ACES (Dr. Vladimir Janda)
- Advanced Proficiency Rated with Activator Method since 1987; upgraded to Impulse iQ in Feb 2013
- Past President 2013-14 Pinellas County Chiropractic Society
- Past Secretary and Treasurer of Pinellas County Chiro Society
- Member: Florida Chiropractic Association, National Institute of Chiropractic Research
- Certified: Florida Workers Compensation, American Society of Laser Therapy

### DR. MARCY -- PERSONAL (warm, human side)
- Married to Robert since 1999, live in Clearwater area
- Cook and eat organic produce
- Active in church -- go on missionary trips to Mexico, treats Mayan people who are now her friends
- Love trout stream fishing in North Carolina
- Enjoys classic movies, bike riding, reading
- Extended family is a priority

### SERVICES

**1. Impulse iQ Chiropractic**
- FDA-registered, over 20 years of research and development
- Advanced micro-circuitry provides precise adjustments with real-time body feedback
- Auto-Sense technology senses when mobility is maximized
- 100 times faster than manual adjustments
- No twisting, no popping, no cracking; safe for all ages
- Different force settings for different body parts

**2. Cold Laser Therapy (Low-Level Laser Therapy / LLLT)**
- Dr. Marcy was FIRST in Tampa Bay area to use this technology
- Non-thermal laser penetrates deep into tissue
- Increases cellular metabolism, expedites cell repair
- Increases blood flow, decongests tissue, promotes healing, decreases pain
- FDA cleared
- Treats: Arthritis, Back Pain, Bursitis, Carpal Tunnel Syndrome, Degenerative Disc Disease, Fibromyalgia, Herniated Discs, Knee Pain, Migraine Headaches, Muscle Spasms, Plantar Fasciitis, Sciatica, Sports Injuries, Sprains, TMJ, Tendonitis, Whiplash

### TOP 10 PATIENT TESTIMONIALS (real quotes, scraped from site)
1. "Dr. Marcy has helped me so much! I thought I would need surgery, but my pain is gone now. I was able to dance at my grandson's wedding!" - D.S., patient since 2025
2. "I feel so much better! I am leaving here a different person than the one who came in." - M.G., patient since 1990
3. "Since my first appointment last week, I feel AMAZING! Dr. Marcy is a magician!" - S.R., patient since 2020
4. "Dr. Marcy turned me from a real skeptic into a believer. She did more for my back in one visit than any of the other doctors I've seen." - D.R.B., patient since 2020
5. "I drive 45 minutes to see Dr. Marcy because I have that much faith in her. I know she can produce results." - P.B., patient since 1998
6. "I had Carpal Tunnel -- tingling and numbness in my hands for six years. I could hardly write or brush my teeth. After cold laser therapy, I felt immediate results." - J.P., patient since 2006
7. "After years and years of agony, the pain is almost gone after seeing Dr. Marcy for just a few weeks. Best money I have ever spent!" - W.M., patient since 2022
8. "I was SO miserable for a month... it is just amazing that my neck has stopped hurting!" - S.B., patient since 2021
9. "After years and years of hip pain, it is gone after just one treatment by Dr. Marcy. It is like a miracle!" - J.S., patient since 2023
10. "At 70 years old, getting regular chiropractic care makes me able to run circles around 40-year-olds." - R.J., patient since 2012

## STEP 4 — IMAGES (all real, scraped from mrschiro.com)
- images/dr-marcy-real.jpg -- Dr. Marcy portrait (hero image)
- images/marcy-robert-real.jpg -- Dr. Marcy with husband Robert at beach
- images/exam-real.jpg -- Hip rotation chiropractic exam with patient
- images/family-real.jpg -- Rosenthal extended family photo
- images/cold-laser-device-real.png -- Cold laser therapy device
- images/impulse-iq-real.jpg -- Patient getting upper back adjustment with Impulse iQ
- images/cold-laser-room.jpg -- Cold laser therapy room
- images/header-real.png -- Site header banner

## STEP 5 — PALETTE
- Cream background: #f9f7f4
- Deep teal primary: #2a7a6e
- Soft gold accent: #d4a843
- Dark text: #1f2d2a
- White cards: #ffffff

## STEP 6 — TYPOGRAPHY (editorial pairing -- NOT basic sans-serif)
- Headings: DM Serif Display weight 400 -- editorial, distinctive
- Body: DM Sans weight 400 -- clean modern, 14-15px base
- Large headings: letter-spacing: -0.025em
- Body line-height: 1.65
- Google Fonts URL: https://fonts.googleapis.com/css2?family=DM+Serif+Display&family=DM+Sans:wght@300;400;500&display=swap

## STEP 7 — SECTIONS TO BUILD

### NAV (Glass)
- position: fixed, top: 0, width: 100%, z-index: 1000
- Transparent on load; when scrolled add class "scrolled": background rgba(255,255,255,0.85), backdrop-filter: blur(20px), border-bottom 1px solid rgba(0,0,0,0.08)
- Logo left: "Rosenthal Chiropractic" in DM Serif Display, 18px
- Links right: About, Services, Testimonials, Contact -- 14px DM Sans, hover underline reveal
- CTA right: "Call Now" button -- teal fill #2a7a6e, white text, border-radius: 0 (sharp), shimmer hover
- Mobile: hamburger (Lucide "menu" icon) -- toggles nav-open class to show mobile menu

### HERO -- Split Layout (left text / right image)
- display: grid; grid-template-columns: 55fr 45fr; min-height: 100vh
- No padding-top on hero -- nav overlays it
- LEFT panel background: #f9f7f4 cream, padding: 0 64px, display flex align-center
  - Badge: "Boutique Practice Since 1994" -- teal bg, white text, 11px uppercase, letter-spacing: 0.08em, padding: 4px 12px, border-radius: 0, margin-bottom: 24px
  - H1: "Feel Good." then <br> "Do More." -- DM Serif Display, 72px desktop/42px mobile, line-height: 1.1, letter-spacing: -0.025em, color: #1f2d2a
  - Subtext: "Gentle, computerized chiropractic care in Largo, FL. No cracking. No twisting. Just results." -- 15px DM Sans, color: #4a5568, max-width: 440px, margin: 24px 0 32px
  - Buttons row:
    - Primary: "Schedule a Visit" -- teal fill, white, border-radius: 0, shimmer ::after hover
    - Secondary: "Our Services" -- teal border, teal text, transparent bg, border-radius: 0
  - Social proof: small icon (Lucide "users") + "Serving Pinellas County since 1994" -- 13px muted, margin-top: 24px
- RIGHT panel:
  - background-image: url(images/dr-marcy-real.jpg), background-size: cover, background-position: center top
  - height: 100vh, position: relative
  - Subtle teal overlay: ::before pseudo, background: rgba(42,122,110,0.08)
- Mobile: stack, hero image 60vw height above text

### TRUST BAR
- Background: #2a7a6e teal, padding: 32px 0
- 3 items in flex row with gap: 48px, centered
- Each: Lucide icon (white, 20px) + text (white, 14px DM Sans)
  - shield-check: "No Cracking. No Twisting."
  - clock: "Private Practice Since 1994"
  - zap: "First Cold Laser in Tampa Bay"
- Border-top: 1px solid rgba(255,255,255,0.15)

### ABOUT -- Asymmetric Split
- 2 columns: left image / right text, gap: 64px, align-items: center
- Background: white #ffffff, padding: 96px 0
- LEFT: images/marcy-robert-real.jpg -- width 100%, max-height: 520px, object-fit: cover, object-position: center top, slight negative margin-bottom: -24px (z-stacking feel)
- RIGHT:
  - Label: "About Dr. Marcy" -- teal, uppercase, 11px, letter-spacing: 0.1em, DM Sans
  - H2: "30+ Years of Gentle, Life-Changing Care" -- DM Serif Display, 40px
  - Bio (3 sentences from real data): "Dr. Marcy L. Smurthwaite has been in private chiropractic practice since 1994. A native Floridian trained at Life University in Atlanta, she uses only computerized adjusting instruments -- no manual cracking, no twisting, no popping. She was the first doctor in the Tampa Bay area to use Cold Laser Therapy, and she brings the same pioneering spirit to every patient she treats."
  - Credential tags (flex wrap, gap: 8px, margin-top: 16px):
    Each tag: border: 1px solid #2a7a6e, color: #2a7a6e, padding: 4px 12px, border-radius: 0, 12px DM Sans
    Tags: "Life University DC" | "CIA Certified" | "Cold Laser Certified" | "Spinal Rehab 100+ hrs" | "FL Workers Comp Certified" | "Past County Chiro President"
  - Personal line (italic, muted, 14px, margin-top: 20px): "She and her husband Robert go on missionary trips to Mexico, love fly fishing in North Carolina, and eat organic. A doctor who lives what she preaches."

### SERVICES -- 2 Photo Cards
- H2 label above: "Our Services" -- DM Serif Display, 40px, left-aligned, padding-bottom: 8px
- Subheading: "Two powerful technologies. One gentle practice." -- 15px muted DM Sans
- 2 cards side by side (desktop), stacked (mobile)
- Each card min-height: 440px, position: relative, overflow: hidden
- Card 1 (Impulse iQ):
  - background-image: url(images/impulse-iq-real.jpg); background-size: cover; background-position: center
  - Dark overlay: ::before { background: rgba(15,30,28,0.65); position:absolute; inset:0; }
  - Content (position: absolute, bottom: 0, left: 0, padding: 32px, color: white):
    - Lucide icon "activity" -- white, 24px, margin-bottom: 16px
    - H3: "Impulse iQ Chiropractic" -- DM Serif Display, 28px
    - P: "FDA-registered computerized adjusting instrument. Real-time body feedback. 100x faster than manual. Safe for all ages." -- 14px
    - Italic gold span: "No cracking. No twisting." -- color: #d4a843
  - Hover: transform: scale(1.02) on the background-image (use img or ::before scale), shadow increase
- Card 2 (Cold Laser):
  - background-image: url(images/cold-laser-room.jpg); background-size: cover; background-position: center
  - Same overlay structure
  - Lucide icon "zap" -- white, 24px
  - H3: "Cold Laser Therapy" -- DM Serif Display, 28px
  - P: "Non-thermal laser penetrates deep tissue. Reduces inflammation, accelerates healing. FDA cleared. First in Tampa Bay." -- 14px
  - Italic gold span: "First in Tampa Bay." -- color: #d4a843

### CONDITIONS TREATED
- Background: #f9f7f4 cream, padding: 96px 0
- Left-aligned H2: "Conditions We Treat" -- DM Serif Display, 40px
- Subheading: "Cold Laser and Impulse iQ together address a wide spectrum of pain and injury."
- Flex wrap left-aligned tags, gap: 8px, margin-top: 32px
- Each tag: border: 1px solid rgba(42,122,110,0.4), color: #2a7a6e, padding: 6px 16px, border-radius: 0, 13px DM Sans
- Tags: Arthritis | Back Pain | Bursitis | Carpal Tunnel | Degenerative Disc | Fibromyalgia | Headaches | Herniated Discs | Hip Pain | Knee Pain | Migraine | Muscle Spasms | Neck Pain | Plantar Fasciitis | Sciatica | Shoulder Pain | Sports Injuries | TMJ | Tendonitis | Whiplash | Work Injuries

### TESTIMONIALS -- Dual Marquee
- Section: background: white, padding: 80px 0
- Left-aligned label above: "What Our Patients Say" -- uppercase 11px teal letter-spacing: 0.1em
- H2: "Real results. Real patients." -- DM Serif Display, 40px
- Two rows of cards:
  Row 1: scrolls left (animation: scrollLeft linear infinite 40s)
  Row 2: scrolls right (animation: scrollRight linear infinite 45s)
- Each row is overflow: hidden with a flex container that has the cards duplicated
- Card style: background: white, border: 1px solid rgba(0,0,0,0.08), padding: 24px 28px, min-width: 320px, max-width: 380px, margin-right: 16px
  - Quote text: 15px DM Sans, color: #1f2d2a, line-height: 1.6, NOT centered
  - Attribution: "- D.S., patient since 2025" -- 13px, color: #6b7280, margin-top: 12px
- Use all 10 testimonials in each row, duplicated for seamless loop
- CSS keyframes:
  @keyframes scrollLeft { from { transform: translateX(0); } to { transform: translateX(-50%); } }
  @keyframes scrollRight { from { transform: translateX(-50%); } to { transform: translateX(0); } }

### CTA SECTION
- Full width, background: linear-gradient(135deg, #2a7a6e 0%, #1a4d45 100%)
- Padding: 80px 0
- 2 columns: text left / button right (desktop); stacked (mobile)
- Left: H2 white "Ready to Feel Good and Do More?" -- DM Serif Display, 40px | P white 15px "Call today to schedule your first gentle adjustment. No cracking, no pressure, no packages."
- Right: Large CTA button "Call (727) 539-0075" -- gold background #d4a843, dark text #1f2d2a, border-radius: 0, padding: 16px 32px, shimmer hover, font-size: 18px

### CONTACT SECTION
- Background: #f9f7f4, padding: 96px 0
- 2 columns: left info / right map
- Left:
  - Label: "Find Us" -- uppercase teal 11px
  - H2: "Visit Rosenthal Chiropractic" -- DM Serif Display, 36px
  - Address with Lucide "map-pin" icon: 12855 S. Belcher Road, Suite 1, Largo, FL 33773
  - Phone with Lucide "phone" icon, large gold text: (727) 539-0075
  - Hours note (italic muted): "Call to confirm current hours"
- Right: Google Maps iframe
  src="https://maps.google.com/maps?q=12855+S+Belcher+Rd+Suite+1+Largo+FL+33773&output=embed"
  width="100%" height="400" style="border:0;display:block;" allowfullscreen loading="lazy"

### FOOTER -- Multi-column
- Background: #1f2d2a dark, color: white, padding: 64px 0 32px
- 3 columns:
  Col 1: "Rosenthal Chiropractic" in DM Serif Display + "Feel Good. Do More." italic 14px muted + full address 13px muted
  Col 2 header "Quick Links": Home | About | Services | Testimonials | Contact -- 14px, hover underline
  Col 3 header "Contact": phone, note "New patients welcome"
- Bottom bar: 1px solid rgba(255,255,255,0.1), padding-top 24px, "2026 Rosenthal Chiropractic Clinic. All rights reserved." 12px muted

## STEP 8 -- SCROLL REVEAL (IntersectionObserver)
Add this JS -- all sections with class "reveal" fade+rise when entering viewport:
```js
const observer = new IntersectionObserver((entries) => {
  entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('in-view'); } });
}, { threshold: 0.1 });
document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
```
CSS:
```css
.reveal { opacity: 0; transform: translateY(32px); transition: opacity 0.6s ease, transform 0.6s cubic-bezier(0.16,1,0.3,1); }
.reveal.in-view { opacity: 1; transform: translateY(0); }
.reveal:nth-child(2) { transition-delay: 100ms; }
.reveal:nth-child(3) { transition-delay: 200ms; }
```
Add class "reveal" to: trust bar items, about section, service cards, condition tags container, CTA section, contact section, footer columns.

## STEP 9 -- NAV SCROLL BEHAVIOR JS
```js
window.addEventListener('scroll', () => {
  document.querySelector('nav').classList.toggle('scrolled', window.scrollY > 50);
});
```

## STEP 10 -- MOBILE HAMBURGER JS
```js
document.querySelector('.hamburger').addEventListener('click', () => {
  document.querySelector('nav').classList.toggle('nav-open');
});
```

## STEP 11 -- SHIMMER BUTTON CSS
```css
.btn { position: relative; overflow: hidden; }
.btn::after { content: ''; position: absolute; top: -50%; left: -75%; width: 50%; height: 200%; background: rgba(255,255,255,0.25); transform: skewX(-20deg); transition: left 0.5s ease; }
.btn:hover::after { left: 125%; }
```

## DELIVERABLES
1. Replace existing index.html completely (single file, all CSS in <style>, all JS in <script>)
2. Run: git add -A && git commit -m "rebuild: full research + dual skills -- DM Serif, split hero, dual marquee, Lucide, real scraped photos"
3. Run: git push
4. Run: openclaw system event --text "Done: Rosenthal rebuilt from zero with real scraped data. DM Serif Display, split hero, dual scrolling marquee, Lucide icons, 8 real images, MD3 spacing, glass nav. Pushed." --mode now
