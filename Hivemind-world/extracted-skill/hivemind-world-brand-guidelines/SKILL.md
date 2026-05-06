---
name: hivemind-world-brand-guidelines
description: Apply Hivemind World's official brand identity to any asset. Use this skill whenever creating or styling any document, presentation, web UI, social media graphic, email template, or visual content for Hivemind World or any of its mixer sub-brands (London Mixer, Barcelona Mixer, Limassol Mixer, etc.). Also use when generating copy, event descriptions, or team bios that must match Hivemind World's voice and tone. Trigger on any mention of "Hivemind", "mixer", "B2B gaming events", or requests to create materials for Harry Phokou's events business.
---

# Hivemind World — Brand Guidelines

Hivemind World is a global series of curated B2B gaming industry mixers, summits, and conferences. The brand aesthetic is dark, premium, and futuristic — think high-end gaming conference meets exclusive members club. Every asset should feel like it belongs on a stage.

---

## 1. Brand Identity

**Full name:** Hivemind World  
**Tagline:** Powering the Future of B2B Gaming Events  
**Legal entity:** Hivemind Trading Ltd  
**Website:** hivemind.world  
**Contact:** info@hivemind.world  

**Sub-brand naming convention:** [City] Mixer  
Examples: London Mixer, Barcelona Mixer, Limassol Mixer, Malmö Mixer, Brighton Mixer, Cologne Mixer

---

## 2. Color System

All colors are extracted directly from the Figma design file (R0GyLoQrjHyGesJZFpJkYD).

### Core Palette

| Token | Hex | Usage |
|---|---|---|
| `--hm-dark` | `#070725` | Primary background, button text, overlays |
| `--hm-text-primary` | `#f8fafc` | Large display text, stat numbers |
| `--hm-text-secondary` | `#e2e8f0` | Headings, body copy on dark |
| `--hm-glow` | `#4d7eff` | Electric blue — inner glow on all buttons, accent highlight |
| `--hm-cyan` | `#00cbff` | Secondary CTA button fill (Become a Sponsor / sponsor-facing CTAs) |
| `--hm-cyan-border` | `#3fd6ff` | Border on cyan CTA buttons |
| `--hm-surface` | `#e7e7e7` | Primary CTA button fill (Get Tickets / attendee-facing CTAs) |

### Background Overlay System

The hero background uses a layered dark overlay approach:
```css
background-image:
  linear-gradient(180deg, rgba(7, 7, 37, 0.2) 0%, rgba(7, 7, 37, 0) 100%),
  linear-gradient(90deg, rgba(7, 7, 37, 0.4) 0%, rgba(7, 7, 37, 0.4) 100%);
```

Section backgrounds are solid `#070725`. Light/glow decorative effects are photographic PNG elements placed at section edges (see "Light Effects" section below).

### Text Shadow on Stats

Large stat numbers use a white text shadow for a luminous "neon glow" effect:
```css
text-shadow: 4px 4px 200px white;
```

---

## 3. Typography

### Typefaces

| Role | Font | Weight | Notes |
|---|---|---|---|
| Section headings | Scandia | Bold | All major section titles — confirmed from Figma |
| Sub-headings | Helvetica | Bold | Secondary headings, event names, stat labels |
| Body copy | Helvetica | Regular | Paragraphs, descriptions, metadata |
| Buttons | Helvetica | Bold | All CTA buttons |
| Nav links (active) | Helvetica | Bold | Active nav item with bottom border indicator |
| Nav links (default) | Helvetica | Regular | Inactive nav items, slightly transparent |

**Fallback stack:** `Scandia, sans-serif` for headings; `Helvetica, Arial, sans-serif` for everything else

**Note on Scandia:** Scandia is a licensed typeface (by TypeTogether). It must be purchased and installed — it cannot be substituted with a system font without a noticeable difference. Fallback is Arial Bold but this should only be used in emergencies.

### Type Scale (from Figma)

| Role | Font | Size | Line Height | Color |
|---|---|---|---|---|
| Section heading | Scandia Bold | 60px | normal | `#ffffff` with `text-shadow: 0px 4px 4px rgba(0,0,0,0.25)` |
| Display stat | Helvetica Bold | 80px | normal | `#f8fafc` with `text-shadow: 4px 4px 200px white` |
| Hero heading | Scandia Bold | 45px | 52px | `#e2e8f0` |
| Sub-heading | Helvetica Bold | 26–28px | normal | `#e2e8f0` |
| Body | Helvetica Regular | 16–18px | 1.5 | `#e2e8f0` |
| Nav links | Helvetica Bold/Regular | 22px | 22px | `#e7e7e7` / `rgba(231,231,231,0.9)` |
| Small / metadata | Helvetica Regular | 13–16px | normal | `#e2e8f0` |

---

## 4. Button System

There are **two button families** and **four button variants** in total — all confirmed from Figma nodes.

---

### Family 1: Filled Pill Buttons (Inner Glow)

Used over dark backgrounds, photos, and event cards. The defining signature is an **inner blue glow** on the button edge.

#### Button Type 1A — Primary CTA ("Get Tickets" — standard)
Used in the hero section.
```css
background: #e7e7e7;
color: #070725;
font: bold 20px Helvetica;
border-radius: 96px;
padding: 16px 24px;
box-shadow:
  0px 4px 4px rgba(0,0,0,0.25),          /* drop shadow */
  inset -1.2px 0px 7.2px 0px #4d7eff;   /* inner blue glow */
```

#### Button Type 1B — Primary CTA ("Get Tickets" — card size)
Used inside event cards. Same style, slightly larger.
```css
background: #e7e7e7;
color: #070725;
font: bold 24px Helvetica;
border-radius: 96px;
padding: 19.2px 28.8px;
box-shadow:
  0px 4px 4px rgba(0,0,0,0.25),
  inset -1.2px 0px 7.2px 0px #4d7eff;
```

#### Button Type 1C — Sponsor CTA ("Become a Sponsor")
Used alongside the primary CTA in the hero. Cyan fill with border.
```css
background: #00cbff;
color: #070725;
font: bold 20px Helvetica;
border: 1.2px solid #3fd6ff;
border-radius: 96px;
padding: 16px 24px;
box-shadow:
  inset 0px 4px 4px rgba(0,0,0,0.25),
  inset -1.2px 0px 7.2px 0px #4d7eff;
```

---

### Family 2: White Outlined Pill Button (Outer Glow)

Used in the standalone CTA strip at the bottom of the page ("Explore our upcoming events"). Key difference: **white fill** + **outer blue glow** instead of inner.

#### Button Type 2 — White CTA ("Get Tickets" — bottom strip)
```css
background: white;
color: #070725;
font: bold 26px Helvetica;
border: 1px solid #4d7eff;
border-radius: 80px;
padding: 16px 24px;
box-shadow: -1px 0px 7px 0px rgba(77, 126, 255, 0.88); /* outer glow */
```

---

### When to Use Which Button

| Context | Button Type |
|---|---|
| Hero section — attendee action | 1A (standard primary) |
| Event cards — register/ticket | 1B (card size primary) |
| Hero section — sponsor action | 1C (cyan sponsor) |
| Standalone CTA strip / dark section footer | 2 (white outer glow) |

---

### Navigation Links (not buttons — for reference)

The nav uses link components, not buttons. Two states:

**Active/current page:**
```css
font: bold 22px Helvetica;
color: #e7e7e7;
border-bottom: 1px solid #e7e7e7;
backdrop-filter: blur(50px);
padding: 12px 16px;
```

**Default/inactive:**
```css
font: normal 22px Helvetica;
color: rgba(231, 231, 231, 0.9);
backdrop-filter: blur(50px);
padding: 12px 16px;
/* Contact link adds text-decoration: underline */
```

---

## 5. Cards & Layout

### Event Cards
```css
border-radius: 16px;
overflow: hidden;
background: photo-fill over #070725;
```
Cards contain: event logo (city branding), date, location, and a CTA button. They use a dark linear gradient overlay on the photo for text legibility.

### Section Layout
- Max content width: 1200px (desktop)
- Section padding: 120px horizontal on desktop, 16px on mobile
- Grid: Event cards in 4-column grid (desktop), 2-column (tablet), 1-column (mobile)

---

## 6. Visual Effects — Signature "Light Streaks"

A defining visual element of the Hivemind World brand is atmospheric stage-light bokeh effects — long soft light streaks that appear at section edges and behind content. These are PNG image overlays placed at section corners/edges:

- **light-left.png** — placed left side of dark sections
- **light-right.png** — placed right side of dark sections  
- **neon-light.png** — small neon glow divider element between stat numbers

**Usage rule:** At least one light streak effect per full-page dark section. Never use flat dark backgrounds without some atmospheric lighting element.

---

## 7. Logo System

### Main Logo

The Hivemind World logo is a horizontal lockup: blue/teal honeycomb-shield icon + "hivemind" wordmark in white. Always use on dark (`#070725`) backgrounds only.

**Two logo variants — both transparent PNGs hosted permanently on hivemind.world:**

| Variant | URL | Use when |
|---|---|---|
| Horizontal (landscape) | `https://hivemind.world/wp-content/uploads/2025/11/Hivemind.png` | Navigation bar, email headers, banners, horizontal layouts |
| Vertical (stacked) | `https://hivemind.world/wp-content/uploads/2025/11/Hivemind_B2B-Gaming-Events.png` | Footer, social media, square formats, vertical layouts |

**HTML usage:**
```html
<!-- Horizontal — nav/header -->
<img src="https://hivemind.world/wp-content/uploads/2025/11/Hivemind.png"
     alt="Hivemind World" height="40" />

<!-- Vertical — footer/social -->
<img src="https://hivemind.world/wp-content/uploads/2025/11/Hivemind_B2B-Gaming-Events.png"
     alt="Hivemind World" height="80" />
```

Both logos are transparent PNGs — always place on `#070725` dark background. Never on white or light surfaces.

**Figma source node:** `694:1604` in file `R0GyLoQrjHyGesJZFpJkYD`

---

### Event Sub-Brand Logos (SVG — scalable, permanent URLs)

Each mixer city has its own SVG logo. These are the canonical files:

| Event | URL |
|---|---|
| London Mixer | `https://hivemind.world/wp-content/uploads/2025/11/Hivemind-London-Mixer.svg` |
| London Mixer (variant) | `https://hivemind.world/wp-content/uploads/2025/11/Hivemind-London-Mixer-1.svg` |
| Barcelona Mixer | `https://hivemind.world/wp-content/uploads/2025/11/Hivemind-Barcelona-Mixer.svg` |
| Limassol Mixer | `https://hivemind.world/wp-content/uploads/2025/11/Hivemind-Limassol-Mixer.svg` |
| Brighton Mixer | `https://hivemind.world/wp-content/uploads/2025/11/Hivemind-Brighton-Mixer.svg` |
| Cologne Mixer | `https://hivemind.world/wp-content/uploads/2025/11/Hivemind-Cologne-Mixer.svg` |
| Malmö Mixer | `https://hivemind.world/wp-content/uploads/2025/11/Hivemind-London-Mixer-1.svg` *(check for dedicated file)* |

**Sub-brand logo structure:** small city photo thumbnail on left + HIVEMIND wordmark top + "[City] / Mixer" label bottom. SVG format, fully scalable, white on transparent.

---

### Logo Usage Rules
- Always on `#070725` dark background — never on white or light
- Never separate the icon from the wordmark
- Never recolour — icon is always blue/teal, wordmark always white
- Maintain clear space equal to the height of the "h" in "hivemind" on all four sides
- For new city events not yet in WordPress: export from Figma node structure following the same icon + wordmark + city/Mixer pattern

---

## 8. Brand Voice & Tone

Hivemind World's voice is **confident, direct, and industry-insider**. It speaks to senior gaming professionals — founders, executives, investors, publishers — as peers.

### Voice Principles
- **Authoritative but not arrogant.** Hivemind World knows its audience well and respects their time.
- **Specific over vague.** Name real companies, real cities, real numbers. "1500+ attendees including CEOs from Ubisoft, Amazon, and Google" not "a great crowd of industry leaders."
- **Energy without hype.** The events are genuinely exclusive — the copy doesn't need to shout.
- **Community-first framing.** Hivemind is about the collective intelligence of the room, not a conference stage.

### Tone by Context

| Context | Tone | Example |
|---|---|---|
| Event headlines | Bold, declarative | "Powering the Future of B2B Gaming Events" |
| Event descriptions | Warm, inviting | "Each activity is designed to turn conversations into collaborations." |
| CTA copy | Direct, action-first | "Get Tickets" / "Become a Sponsor" |
| Social/testimonial | Authentic, peer-to-peer | "Simply one of the best side-events of the year." |
| Stats/proof points | Confident, factual | "70% Executives & Founders / 1500+ Attendees / 12+ Events" |

### Copy Patterns to Use
- "Curated" (not "exclusive" — curated implies craft, not gatekeeping)
- "Connecting the B2B games industry" (the core mission, always accurate)
- "Free and paid mixers" (transparency about access)
- "Conversations into collaborations" (the key outcome)

### Words to Avoid
- "World-class" (generic)
- "Networking event" (too transactional, prefer "mixer")
- "Amazing opportunity" (filler)
- "State-of-the-art" (irrelevant to the brand)

---

## 9. Proof Points & Brand Stats

Always use these verified figures in brand materials (update as events are added):

- **12+ Events** held globally
- **1500+ Attendees** across all events
- **70% Executives & Founders** attendee breakdown

Past notable partners/attendees: Ubisoft, Amazon Web Services, Google, Metacore, Supercell, Airship, Lurkit, Metaplay, Dreamloop Games.

---

## 10. Team

| Name | Role | Contact |
|---|---|---|
| Harry Phokou | Founder & CEO | harry@hivemind.world |
| Zhanna Tushkina | Event Manager | zhanna@hivemind.world |
| Theo Phokou | Partnership Manager | theo@hivemind.world |

---

## 11. Asset Application Checklist

Before finalising any Hivemind World branded asset, verify:

- [ ] Background is `#070725` or a photo over `#070725`
- [ ] All text is `#ffffff`, `#f8fafc`, or `#e2e8f0` (never dark text on dark background)
- [ ] Section headings use **Scandia Bold**
- [ ] Sub-headings, body, and buttons use **Helvetica Bold or Regular**
- [ ] At least one atmospheric light streak effect is present on full dark sections
- [ ] Attendee CTAs use Button Type 1A or 1B (grey fill, inner blue glow)
- [ ] Sponsor CTAs use Button Type 1C (cyan fill, inner blue glow)
- [ ] Standalone strip CTAs use Button Type 2 (white fill, outer blue glow)
- [ ] The `#4d7eff` blue glow appears on ALL button types
- [ ] Event cards use 16px border radius
- [ ] All pill buttons use 96px (or 80px for Type 2) border radius
- [ ] Logo is white version, never isolated from wordmark for event sub-brands
- [ ] Copy uses the Hivemind voice — direct, specific, insider-tone
