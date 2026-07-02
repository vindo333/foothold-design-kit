# Foothold Marketing Design System

Design system for the logged-out marketing site (homepage first). Written to
be **self-contained**: paste the whole doc (or just §2–§9) into Claude Design
or any design tool and it carries everything needed to produce on-brand
screens without re-deriving decisions. The app's own system (globals.css
`--fh-*` tokens, DECISION-065 atmosphere) is the parent; this extends it for
marketing scale.

**Status**: planning (nothing built). Companions: [HOMEPAGE_PLAN.md](HOMEPAGE_PLAN.md),
[POSITIONING.md](POSITIONING.md), copy rules in `docs/skills/copywriting.md`.

---

## 1. Point of view (what the brand believes)

> **Your judgment is the last thing that's still yours, and most people are
> quietly outsourcing it.** Foothold exists for people who refuse to. AI
> holds the guardrails; the human decides.

The positioning-brief version of the same belief ([POSITIONING.md](POSITIONING.md)):
Foothold's differentiation is **epistemic ownership**, not "AI
productivity." AI structures, sharpens, pressure-tests, synthesizes; you
shape the answer. For **decision-makers whose calls move real money**, the
person who owns the question ("Should we build the new warehouse?"):
founders, owners, executives, senior operators. 80% organizational stakes,
20% the same person's personal high-stakes questions; the business-stakes
frame always leads. For this buyer the belief lands as accountability:
**you make the call and you own it in front of the board.** A chatbot's
confident answer doesn't stand next to you when it counts. Keyline that may
close any page or asset: *"Because some questions deserve more than a
generic AI chat."*

Everything downstream expresses this one belief:

- The **serif (Lora)** is the human thinking voice; it always carries the
  judgment. The **sans (Geist)** is the system; it only ever labels,
  guides, and holds structure. The typographic hierarchy IS the product
  philosophy.
- **Nature imagery** = where clear thinking actually happens (the walk,
  the notebook, the window). **Glass UI** = the structure that holds it.
  The homepage alternates between the two the way a session alternates
  between your mind and the framework.
- The named feeling: **"a quiet room with the lights on."** Calm, warm,
  slightly serious. Not productivity-energetic, not wellness-soft, not
  corporate-slick. If a screen feels busy or hypey, it's off-brand.
- Audience made visible: the imagery is first-person POV (your hands, your
  notebook, your view). The visitor is cast as the thinker, never shown a
  stock model "being productive."

---

## 2. Color

Light-first marketing palette (the app is atmospheric-dark; the marketing
site leads warm-light and dips into the app's espresso dark for emotional
chapters and product frames; that contrast is the rhythm).

### Core tokens

| Token | Value | Use |
|---|---|---|
| `--mk-bg` | `#F4F1EC` | Page background (warm parchment; never pure white pages) |
| `--mk-surface` | `#FFFFFF` | Cards, contained blocks |
| `--mk-ink` | `#191110` | Headlines, primary text (espresso, never #000) |
| `--mk-body` | `#4A4543` | Body text |
| `--mk-muted` | `#8C8580` | Captions, meta |
| `--mk-brand` | `#f6590b` | THE accent. CTAs, connector lines, highlights. One bold color, used sparingly (≤5% of any viewport) |
| `--mk-brand-deep` | `#e8431e` | Brand hover/pressed, gradient stop |
| `--mk-border-warm` | `#EAD9C2` | Hairline borders, dividers |
| `--mk-gold` | `#EDD3B2` | Warm tint fills, subtle highlights |
| `--mk-dark-bg` | `#0F0908` | Dark chapter background |
| `--mk-dark-surface` | `#191110` | Dark chapter cards |
| `--mk-dark-text` | `#E7E2DF` | Body on dark |
| `--mk-focus` | `#0496FF` | Focus rings only; never decorative |

### Rules

- **One bold color.** Orange is the only saturated hue on the page. Blue is
  functional (focus) only. If two orange elements compete in one viewport,
  demote one.
- Dark sections use the app's dark-theme glow recipe: `rgba(246,89,11,0.16)`
  warm glow + `rgba(107,75,144,0.11)` mauve glow, radial, from corners,
  **with the grain layer on top** so the glow reads as burnt/analog, not
  neon (reference:
  `docs/temp-working-assets/ref-framer-dark-grain-orange-glow.png`).
- Gradients, two tiers: (a) the **AI-action gradient** (brand → brand-deep,
  135°), the only saturated gradient, reserved for primary CTAs, matching
  the app's AI buttons; (b) **subtle atmospheric washes**, the corner-glow
  radials and faint warm `--mk-gold` tints on surfaces. These soft
  gradients are a brand signature (the app's atmosphere); hard two-color
  decorative gradients are not.

---

## 3. Typography

Two voices by ROLE (same law as the app; see packages/ui typography.ts):

- **Lora (serif)** → judgment voice: headlines, pull quotes, the questions
  ("Should we build the new warehouse?"), Clarity Brief excerpts. Dominates
  emotionally.
- **Geist (sans)** → system voice: nav, eyebrows, buttons, feature labels,
  captions, pricing tables, footer.

A headline set in Geist or a button set in Lora is a system violation.

### Marketing type scale (extends the app scale upward)

| Step | Size (clamp) | Font | Use |
|---|---|---|---|
| `display-xl` | `clamp(2.75rem, 6vw, 4.5rem)` / 1.05 | Lora 500, -0.02em | Hero headline only |
| `display` | `clamp(2.25rem, 4.5vw, 3.5rem)` / 1.1 | Lora 500 | Section (chapter) headlines |
| `title` | `clamp(1.5rem, 2.5vw, 1.875rem)` / 1.2 | Lora 500 | Sub-section, step titles |
| `quote` | `clamp(1.375rem, 2.2vw, 1.75rem)` / 1.4 | Lora 500 italic | Pull quotes |
| `lead` | `1.25rem` / 1.6 | Geist 400 | Intro paragraph under headlines |
| `body-lg` | `1.125rem` / 1.65 | Geist 400 | Marketing body (larger than app body) |
| `body` | `1rem` / 1.6 | Geist 400 | Dense sections, cards |
| `eyebrow` | `0.75rem` / 1, +0.14em tracking, uppercase | Geist 600 | Section labels ("THE STAKES") |
| `caption` | `0.8125rem` / 1.5 | Geist 400 | Image captions, fine print |

- Eyebrows are Geist uppercase in `--mk-muted`, with a 16px orange rule
  (2px tall bar) to their left. This is the "orange bars" motif from the CI
  doc, used consistently as the section marker.
- **Geist Mono** (third voice, tiny doses): numerals, timestamps, and
  `[bracket]` meta labels, e.g. `[THE STAKES]`, `~30 MIN`, `€199/YR`.
  Reference: the Sanity orange-editorial promo
  (`docs/temp-working-assets/ref-sanity-orange-editorial-dotgrid.png`).
  Mono = measured/technical precision; never for sentences.
- Max headline width ~18ch, body ~65ch.

---

## 4. Layout & grid

- **12-column grid**, max-width `1200px` content / `1440px` wide frames,
  gutter `24px`, side padding `24px` mobile / `48px` desktop.
- **Section rhythm**: vertical padding `clamp(96px, 12vh, 160px)` between
  chapters. Generous; emptiness is part of the calm.
- **Visible grid (the "transparent shell")**: on light sections, render
  faint vertical column guides (1px lines at `rgba(25,17,16,0.045)`) plus
  the occasional dimension tick or crop mark at `rgba(25,17,16,0.08)`.
  Restricted to: hero, HOW IT WORKS diagram, pricing. Never on nature
  imagery or dark chapters. It should read as "thinking in progress,"
  not decoration; if a section already has a diagram, skip the guides.
- **Thinking nodes (signature motif)**: the app's brain-node visual. Small
  orange node dots (6–8px, `--mk-brand`, soft glow halo) joined by 1.5px
  hairline connectors (brand on light, `rgba(246,89,11,0.5)` on dark) that
  draw on with a stroke animation. This is the marketing site's diagram
  language: ideas as nodes, structure as the lines between them. Use it for
  the hero flow reveal, the HOW IT WORKS map, and the blind-spot diagnostic
  illustration. Max one node system per viewport; nodes connect *content*
  (a question chip to its angle card), never float as pure decoration.

## 5. Radius & borders

Reuse the app's four radii exactly: `4px` chips · `8px` controls/buttons ·
`12px` cards/panels · `9999px` pills. Product frames (browser mockups) get
`16px` outer. Hairlines: `1px solid --mk-border-warm` on light,
`rgba(255,255,255,0.085)` on dark.

---

## 6. Shadows (Apple formula)

All shadows: **straight 180° (x = 0), blur = 2.5–3× the y-offset, low
opacity, espresso-tinted** (`25,17,16`, never pure black on light bg).
Most elements also carry a hairline ring for edge definition.

| Token | Value | Use |
|---|---|---|
| `--mk-shadow-1` | `0 2px 6px rgba(25,17,16,0.06)` | Chips, small controls |
| `--mk-shadow-2` | `0 4px 12px rgba(25,17,16,0.07)` | Buttons, inputs |
| `--mk-shadow-3` | `0 8px 20px rgba(25,17,16,0.08)` | Cards |
| `--mk-shadow-4` | `0 16px 40px rgba(25,17,16,0.10)` | Floating panels, nav on scroll |
| `--mk-shadow-5` | `0 32px 80px rgba(25,17,16,0.14)` | Hero product frame, video player |

- Hover lift = move up one shadow step + `translateY(-2px)`, 260ms.
- On dark sections, swap to the app's recessed glass shadows
  (`0 40px 100px -52px rgba(0,0,0,0.7)`). Dark chapters use the app's own
  `.fh-glass` recipes verbatim, not the marketing scale.

---

## 7. Imagery

Two image worlds, never blended in one frame:

### A. Dream-nature (the mind)

- **Content**: POV, first person. Hands writing in a notebook. A path
  ahead. Morning light through trees. Looking out over water/fog. A mug
  beside a notepad by a window. The viewer IS the thinker.
- **Treatment**: slightly overexposed (+0.5 EV feel, lifted blacks, soft
  highlights allowed to bloom), visible film grain, warm white balance,
  shallow depth of field. Never HDR-crisp, never blue-toned, never stocky
  (no faces to camera, no laptops-in-cafés clichés).
- **Recipe (CSS/Claude Design)**: `filter: brightness(1.06) contrast(0.94)
  saturate(0.9)` + grain overlay (SVG turbulence, `mix-blend-mode:
  soft-light`, opacity 0.3, same grain as the app's Atmosphere layer 4) +
  very subtle warm wash `rgba(237,211,178,0.08)`.
- **Usage**: full-bleed interstitial bands between chapters (60–75vh), hero
  background at heavy recess (blurred/dimmed like the app's Atmosphere),
  and inside glass cards as recessed context.

### B. Product UI (the structure)

- Real app screenshots/recordings only; the app already carries the brand
  (espresso glass over nature haze). Never redraw fake UI.
- Framed in a minimal browser chrome: `16px` radius, hairline border,
  `--mk-shadow-5`, on light bg. Or floating glassmorphic over a nature
  band (the "glassmorphic card over nature" premium shot from the CI doc).
- Product video player uses the same frame treatment.

**Logo rule (hard)**: never recreate the Foothold logo in code. Use
`assets/brand` files only; plain-text "Foothold" fallback.

---

## 8. Glass primitives (a brand hallmark, not just dark chapters)

Glassmorphic cards are core Foothold branding. The app UI is the look, and
the marketing site reuses its recipes verbatim so marketing and product are
one world:

- `.fh-glass`: hero cards on dark. Sheen gradient + corner glow +
  `blur(30px) saturate(1.35)`, hairline `rgba(255,255,255,0.085)` border.
- `.fh-glass-soft`: secondary cards. `blur(20px)`, lighter shadow.
- **Glass over nature**, the premium shot: a frosted glass card or nav bar
  floating directly on a grainy nature photo (north star:
  `docs/temp-working-assets/foothold-hero-mock-glass-nav-forest.png`, the
  dark glass `foothold_` bar with orange underscore over a sun-flared
  forest). Glass on light parchment sections is allowed but subtle (white
  glass at 0.55–0.62 alpha, warm hairline).
- Dark chapter backgrounds rebuild the app's Atmosphere: blurred nature
  base (opacity ~0.16) + bottom vignette + corner glows + grain. This is
  the signature; a dark marketing chapter should be indistinguishable in
  atmosphere from the app itself.
- **The `_` cursor**: the orange underscore from the logo lockup can appear
  as a blinking-cursor accent after key headlines (2.8s slow blink, one per
  page max). Thinking as something still being written.

---

## 9. Motion

Motion states the hierarchy: **the important thing moves first and biggest;
supporting elements follow, later and smaller.**

### Tokens

| Token | Value |
|---|---|
| `--mk-ease` | `cubic-bezier(0.22, 1, 0.36, 1)` (app's --fh-ease) |
| `--mk-fast` | `150ms` (hover, press) |
| `--mk-standard` | `260ms` (state changes) |
| `--mk-reveal` | `700ms` (scroll entrances, primary) |
| `--mk-reveal-slow` | `900ms` (imagery, atmosphere) |
| `--mk-stagger` | `120ms` (delay step between siblings) |

### Choreography rules

1. **Primary-first stagger**: headline enters first (`translateY(24px)→0`,
   700ms), lead follows +120ms with 14px travel, CTAs +240ms with 10px,
   decorative elements (guides, connectors) last at +360ms with
   opacity-only. Distance shrinks with importance; never uniform.
2. **Scroll reveals**: trigger at 20% viewport entry, once only. Whole
   sections never slide; children stagger inside a static section.
3. **Connector lines draw on** (stroke-dashoffset) after their endpoints
   have settled.
4. **Continuous motion**: at most one slow ambient loop per viewport (the
   app's `fhd-glow` 2.8s CTA pulse, or a 30s+ Ken-Burns drift on nature
   bands at ≤4% scale). Nothing else loops.
5. **Micro**: buttons press `scale(0.97)` (app convention), hover lifts
   2px + one shadow step.
6. `prefers-reduced-motion`: all reveals become opacity-only, loops off.

---

## 10. Component inventory (marketing)

| Component | Spec |
|---|---|
| **Nav** | Transparent over hero → frosted glass bar on scroll (`blur(22px)`, hairline bottom, shadow-4). Logo asset left; "How it works · Pricing · Log in" Geist; primary CTA button right |
| **Button / primary** | AI gradient (brand→brand-deep 135°), white Geist 600, 8px radius, shadow-2, `fhd-glow` pulse allowed on the single most important CTA per page |
| **Button / secondary** | Ghost: ink text, hairline warm border, bg white; hover → gold tint fill |
| **Button / tertiary** | Text + "·" separator pattern from the copy ("[ Get clear ] · See how it works"); the "See how it works" is an underlined text link |
| **Eyebrow** | Orange 16×2px bar + Geist uppercase tracked label |
| **Question chip** | Lora italic in a pill on glass; used for the rotating real questions ("Should we make this hire?") |
| **Step card** | Numbered (oversized Lora numeral at 8% opacity behind), title Lora, body Geist, on `--mk-surface` with shadow-3 |
| **Product frame** | Browser chrome mockup, 16px radius, shadow-5; dark variant floats on nature band as glass |
| **Video player** | Product frame + centered play affordance (orange circle, shadow-3); poster = real app still |
| **Pull quote** | Lora italic `quote` size, orange left bar, generous whitespace |
| **Pricing card** | White surface, hairline, shadow-3; featured plan gets glass treatment + glow |
| **Footer** | Dark espresso chapter, recessed nature atmosphere, minimal links, logo-white asset |

---

## 11. Voice (so design and copy stay one language)

All marketing copy runs through **`docs/skills/copywriting.md`** (Rule of
One, Three-Question Test, Two-Second Test, anti-AI filters). Where that file
and this section overlap, it wins on language mechanics; this section wins
on brand register. Non-negotiables repeated here:

- **No em dashes.** Periods, commas, colons, or restructure.
- **Show stakes, don't label them.** Never call a question "expensive" or
  "teuer". A concrete question ("Should we build the new warehouse?") or a
  number ("a €50K consultant, six weeks") carries the stakes. Compact
  fallback where unavoidable: "costly" or "high-stakes".
- Headlines: declarative Lora sentences with a period. ("Good judgment is
  the last thing that's still yours.")
- Second person, present tense. Short sentences land the punch.
- Named enemy: outsourced judgment / confident-sounding chatbot answers.
  Never "productivity" framing, never "10x faster."
- Named artifact: **the Clarity Brief** (never "Outcome Brief").
- The audience is the person who **owns the call**: founders, owners,
  executives, fractional CxOs, consultants (the All-In/Acquisition.com/
  Naval-reading crowd; reMarkable owners are the aesthetic existence
  proof). Write to someone who'd rather feel sharp than feel busy, and who
  answers for the call afterwards. Example questions lead 80/20:
  organizational stakes first (*Should we build the new warehouse? Should
  we make this hire? Is this expansion actually viable?*), the same
  person's personal high-stakes second (*Should I sell the company?*),
  never generic life-clarity.
- **Calm is positioning, not just taste**: this audience is currently sold
  strategy via launch-funnel urgency (crossed-out prices, countdown sales,
  "$1,273 of bonuses"). Foothold never does urgency theatrics. Founding-
  member pricing is stated as plain fact with a quiet mono badge. Emotional
  payoff we sell: *the moment of clarity*, solid footholds while others
  copy and worry.
- German-market aware (€ pricing, DE audience) but EN-first site.
- Words we use: judgment, structure, clarity, stand on, blind spots, hold,
  pressure-test, see more.
- Words we don't: supercharge, unlock, seamless, revolutionary, magic,
  hack, secret, limited-time, expensive.

---

## 12. Paste-ready CSS tokens

```css
:root {
  /* color */
  --mk-bg: #F4F1EC; --mk-surface: #FFFFFF;
  --mk-ink: #191110; --mk-body: #4A4543; --mk-muted: #8C8580;
  --mk-brand: #f6590b; --mk-brand-deep: #e8431e;
  --mk-border-warm: #EAD9C2; --mk-gold: #EDD3B2;
  --mk-dark-bg: #0F0908; --mk-dark-surface: #191110; --mk-dark-text: #E7E2DF;
  --mk-focus: #0496FF;
  /* type */
  --mk-font-judgment: "Lora", Georgia, serif;
  --mk-font-system: "Geist", system-ui, sans-serif;
  /* shadows: x=0, blur = 2.5–3 × y, espresso tint */
  --mk-shadow-1: 0 2px 6px rgba(25,17,16,0.06);
  --mk-shadow-2: 0 4px 12px rgba(25,17,16,0.07);
  --mk-shadow-3: 0 8px 20px rgba(25,17,16,0.08);
  --mk-shadow-4: 0 16px 40px rgba(25,17,16,0.10);
  --mk-shadow-5: 0 32px 80px rgba(25,17,16,0.14);
  /* radius */
  --mk-r-chip: 4px; --mk-r-control: 8px; --mk-r-card: 12px; --mk-r-frame: 16px;
  /* motion */
  --mk-ease: cubic-bezier(0.22, 1, 0.36, 1);
  --mk-fast: 150ms; --mk-standard: 260ms;
  --mk-reveal: 700ms; --mk-reveal-slow: 900ms; --mk-stagger: 120ms;
  /* atmosphere */
  --mk-glow-warm: rgba(246,89,11,0.16);
  --mk-glow-mauve: rgba(107,75,144,0.11);
  --mk-grid-line: rgba(25,17,16,0.045);
}
```
