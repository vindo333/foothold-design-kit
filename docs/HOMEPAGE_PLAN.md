# Foothold Homepage Plan (logged-out marketing site)

Structure and layout plan for the logged-out homepage. **Planning only,
nothing built yet.** Design language: [MARKETING_DESIGN_SYSTEM.md](MARKETING_DESIGN_SYSTEM.md).
Positioning: [POSITIONING.md](POSITIONING.md). Copy rules:
`docs/skills/copywriting.md`. Copy source: v6 draft in
`docs/temp-working-assets/homepage-copy-draft.md` (Drive doc is the editing
source of truth); an audited v7 working rewrite lives at
`docs/temp-working-assets/homepage-copy-v7-draft.md`.

---

## 1. What the research says (and what we take)

Eight sites studied (2026-07): Arcade, Billow, Sanity, Gainbridge
(structure); Nolla, Apple, Solo Stove, Skoll (brand/atmosphere).

**Cross-site skeleton** (all four SaaS sites): nav → hero → proof → 3–5
alternating feature sections → testimonial → full-width CTA → dense footer.
**None put pricing tables on the homepage**; at most a teaser linking out.

What we adopt, per site:

| Site | Steal | Foothold application |
|---|---|---|
| **Arcade** | Hero is a *live product widget* (type your URL → instant demo), real product embedded on the page; muted looping MP4s per feature instead of screenshots | Hero composer = the real anonymous session entry. Short app-UI loops in HOW IT WORKS |
| **Billow** | Antithesis headline ("Run on facts, not guesswork"); hyper-specific fake data in mockups; "Totally fair to ask." FAQ; 0.3–0.5px hairlines | Copy already has the antithesis ("You do the thinking. Foothold makes sure it holds."). Product frames show a *real* filled-in session, not lorem. Consider FAQ with that disarming tone |
| **Sanity** | Giant type (up to 112px, `max-w-[12ch]`) as the hero visual; seeded interactive cards with starter questions; `motion-reduce` guards; dot-grid textures; `[bracket]` mono labels | Oversized Lora hero; starter-question chips that pre-fill the composer; mono eyebrow labels |
| **Gainbridge** | GSAP scroll-driven background **theme morphing** between sections; semi-mono for numbers; stat row under hero; warm paper + one accent (not category-default blue) | Light→dark chapter transitions animate the bg color; Geist Mono numerals; warm parchment + orange validated |
| **Nolla** | Near-identical palette (cream + espresso `#2b1809`), validation that our warm two-tone works for a trust product; hero = question + immediate action ("How are you feeling?" → analyze); AI claims always anchored by human proof | Hero headline is a question-led action; "you decide" human-anchor next to every AI claim |
| **Apple** | Two-line hero formula; tile-size-as-hierarchy; alternating light/dark backgrounds as the entire pacing device; shadow discipline | Section pacing = light/dark alternation; Apple shadow formula (already in design system §6) |
| **Solo Stove** | Strict rhythm: *full-bleed emotion → contained utility → repeat*; practical micro-tables inside emotional cards; ambient video backgrounds | Nature interstitials between chapters, each followed by a concrete utility block |
| **Skoll** | Full-width unornamented statement section; documentary (non-stock) photography as the only color on monochrome chrome | THE STAKES chapter = full-width typographic statement, no UI, no decoration |

**Motion consensus** across all eight: opacity/translate scroll reveals +
muted autoplay product loops. No parallax theatrics, no carousels-as-hero.
Ambient, never decorative. This matches the design system's choreography
rules.

### Adjacent-audience audit: Overnight Strategist (overnightstrategist.com)

Named first in the positioning brief's "existing audiences". Same hunger
("become a better strategist"), very different product and register. It
sells a **$39 downloadable PDF toolkit** (50 frameworks, listed $89) through
a classic sales funnel: founder-story authority ("Hi there, I'm Shehraz,"
17+ years, McKinsey peers), bonus stacking ("$1,273 of bonuses free"),
urgency ("price goes up when the launch sale ends"), keep-the-materials
guarantee. Headline: "Clear Thinking & Visual Storytelling That Inspires
Action."

What this tells us:

- **The demand is validated**: people pay for structured strategic thinking
  even as static PDFs. Foothold's pitch against it writes itself:
  *frameworks don't push back; Foothold does.* Their method is manual and
  un-personalized: no memory, no diagnostic, no compounding record. Exactly
  moat layers 2, 3, 5.
- **Their funnel mechanics are what we must NOT sound like**: crossed-out
  prices, countdown urgency, bonus-value inflation. Foothold's founding-
  member pricing is a launch offer too, but rendered in our register it's
  a quiet mono badge and a plain sentence, never theatrics (see §3.8).
- **What they do well and we keep**: objection-handling FAQ, peer
  endorsements over academic credentials, one concrete artifact promise
  (their "One Page Strategy" ≈ our Clarity Brief; ours is generated from
  YOUR thinking, not a blank template).

---

## 2. The two big placement decisions

### Product video AND live product: who gets the hero?

Both in the hero would compete. Recommendation:

- **The live composer wins the hero.** Foothold is anonymous-first (users
  can run a whole session up to the Clarity Brief gate without signing up;
  see engineering plan phases 9–11. With the paid-only pricing model this
  anonymous run IS the trial). That makes the Arcade/Nolla pattern
  available to us at full strength: the hero *is* the product's first
  input. Typing a question and pressing enter starts a real session.
  Zero-friction, states the point of view (you think first), and no fake
  demo to maintain.
- **The product video anchors HOW IT WORKS** (section 4 below). The hero's
  secondary link "See how it works" smooth-scrolls to it. People who want
  to watch before touching get a one-scroll path; people who want to act
  act immediately.

### Where the signed-out product surfaces beyond the hero

Three touchpoints, one mechanism: hero composer → starter-question chips
(pre-fill the composer) → CLOSE section repeats the composer with the
"question you've been avoiding" framing. All three feed the same
`/session` anonymous flow.

---

## 3. Page structure (top → bottom)

Pacing follows Apple/Solo Stove: **light utility ↔ dark emotion**, with
grainy nature interstitials as the breaths between chapters. Scroll-driven
background morphing (Gainbridge) glues the transitions.

Copy references = v6 sections in the draft (v7 working rewrite in temp
assets). Eyebrows use mono `[BRACKET]` labels.

### 0. NAV
Dark glass bar floating over the hero (north-star mock:
`foothold-hero-mock-glass-nav-forest.png`): logo asset + orange `_`,
links "How it works · Pricing · Log in", ghost "Log in" + primary
"Start a session" (no "Start free": there is no free plan; the anonymous
session is the trial). Transparent-dark at top → frosted light glass once
scrolled past the hero.

### 1. HERO: *the product is the input* (dark, atmospheric)
- Background: grainy, slightly overexposed forest/sun-flare photo (POV,
  full-bleed), heavier recess toward the composer for legibility. Slow
  30s+ Ken-Burns drift.
- Headline (Lora, display-xl, white): **"Great decision making has a
  structure."** + second line resolving to the product. Optional Sparktoro-
  style rotating tail from the draft's loose ideas ("Foothold is how
  [smart people think smarter | you see around corners | …]"). Decide in
  copy round; the layout reserves one rotating line either way.
- Lead: 1–2 sentences from the copy draft.
- **The composer**: a real glass composer card (the app's own component),
  placeholder "What's the question you've been putting off?", with 3
  starter-question chips (Lora italic), 80/20 per POSITIONING.md: *Should
  we build the new warehouse? · Should we make this hire? · Is this
  expansion actually viable?* (a founder-personal variant, *Should I sell
  the company?*, may rotate in as the fourth; never generic life
  questions). Chips pre-fill; Enter starts the anonymous session.
- Below composer: `[ Get clear in 30 minutes ]` primary CTA (AI gradient,
  the page's one pulsing element) · "See how it works" text link (scrolls
  to video).
- Thinking-nodes accent: as the hero settles, 3–4 nodes + connectors draw
  on, linking the starter chips toward the composer. The "structure" made
  visible. Faint column guides visible in this viewport.
- Choreography: headline (24px travel) → lead (+120ms, 14px) → composer
  (+240ms, 12px, glass sheen sweep) → chips stagger (+360ms) → nodes draw
  last. Micro-trust line under CTA: "No account needed to start thinking"
  (the anonymous session is the trial; don't say "free plan", there isn't
  one).

### 2. STAKES: *the point of view* (dark espresso chapter, no UI)
- Copy: "Good judgment is the last thing that's still yours." The Skoll
  full-width statement treatment: pure typography on the app's dark
  Atmosphere (blurred nature + corner glows + grain; ref: Framer
  dark-grain-glow screenshot). No cards, no product, no imagery.
- Body set in measures of ~60ch, generous line breaks; the one pull-quote
  scale moment: "You're still the one who decides."
- 80/20 sharpening (POSITIONING.md): the argument lands as
  **accountability**. You make the call and you own it in front of the
  board, the team, the family. A chatbot's confident answer doesn't stand
  next to you when it counts. Copy pass should fold this in.
- Background morphs from hero-photo-dark into this flat espresso as you
  scroll (Gainbridge theme-morph).

### 3. WHAT IT IS: *category shift* (light parchment, first utility block)
- Copy: "Where your judgment gets room to work." + the not-a-chatbot /
  not-a-notes-app / not-a-decision-matrix triad. Render the triad as three
  small struck-through chips (the app's strike treatment) resolving into
  one solid chip: "a thinking system".
- Right side: first product glimpse, a single glass card from the app
  (a real angle card with real content) floating over a soft nature blur.
- Faint grid guides on. Section eyebrow: `[WHAT IT IS]`.

### 4. HOW IT WORKS: *the video + the three moves* (light, the workhorse)
- Copy: "Months of circling, compressed into one 30-minute session."
- **Product video** in a browser frame (shadow-5), poster = real session
  still, play button orange. This is the "See how it works" anchor.
- Under it, the three steps as cards connected by drawn-on node lines
  (1 Build the model → 2 Hunt the blind spots → 3 Get the Clarity Brief):
  numbered with oversized ghost Lora numerals; each card carries a muted
  looping MP4 crop of the real UI (Arcade pattern): the 4-angle map, the
  diagnostic flagging an assumption, the Brief assembling.
- The four angles ("What's working for you / What could sink it / …")
  listed with the app's icons inside step 1's card. Mono time badges
  (Billow): `~10 MIN` per step, summing to the 30.

### 5. NATURE INTERSTITIAL: *breath* (full-bleed, 60vh)
- POV: hands writing in a notebook, morning light, heavy grain,
  overexposed.
- One Lora line only (from EDGE copy): *"Assumptions are weeds. Leave them
  alone and they choke out the truth."*
- Solo Stove rule: emotion is immediately followed by utility ↓.

### 6. THE EDGE: *think like the greats* (light)
- Copy: Munger/inversion section. Layout: text column + a compact
  node-diagram illustrating the moves (invert → work backward → pre-mortem
  → surface assumptions) as four connected nodes lighting in sequence.
- This is a text-forward section; keep it tight (no cards).

### 7. COMPOUNDING: *the moat* (dark espresso chapter #2)
- Copy: "Session one: a decision. Session fifty: something you can't buy."
- 80/20 sharpening (POSITIONING.md, moat layer 3): at the target audience
  this record is **institutional memory**: how you actually decided
  things, and what happened next. An asset no empty chatbot window can
  rebuild, and (Team) one the organization keeps.
- Visual: a receding stack/timeline of glass Clarity Brief cards (real
  briefs, content softly blurred for privacy) accumulating left→right,
  the record compounding. Nodes connect recurring themes across briefs.
- Trust line: "Private, encrypted, yours to export." with mono badge
  styling. (Nolla pattern: AI claim anchored by concrete guarantees.)
  Confidentiality is a lead argument for this audience: you can't paste
  "should we acquire our competitor" into a consumer chatbot.
- Optional caption row (moat layer 5, positioning brief): Clarity Briefs
  and next steps flow into Notion, Obsidian, Linear. Small muted icons,
  one line, no integration-wall section.

### 8. PRICING TEASER (light, not a full pricing table)
- **Decided model (2026-07-02)**: annual only, two tracks, each Solo/Team:

  | | **Foothold BYOK** (bring your own AI key) | **Foothold with AI included** |
  |---|---|---|
  | Solo | €279/yr · *founding member €199/yr* | €479/yr · *founding member €379/yr* |
  | Team (3 seats) | €699/yr, +€99/seat · *founding €499/yr, +€79/seat* | €1,099/yr, +€179/seat · *founding €799/yr, +€129/seat* |

- Homepage shows a **teaser, not the matrix**: two cards (BYOK ghost card /
  AI-included glass card with subtle glow), each displaying the **Solo
  founding-member price as primary** (Geist Mono numerals) with the
  standard price as muted context. Set as plain fact ("Founding member
  pricing, first cohort"), quiet mono badge `[FOUNDING MEMBER]`. **No
  crossed-out prices, no countdowns, no bonus-stacking.** The calm
  anti-Overnight-Strategist register is the differentiator. Team pricing
  is one caption line; the full matrix lives on `/pricing`.
- Anchor argument (POSITIONING.md): a strategy consultant costs €50K and
  six weeks; a coach €5K+ a month, booked out. One right call on a
  warehouse-sized question pays for a decade of Foothold. One sentence,
  then "See pricing" → `/pricing`.
- BYOK is also a **trust signal**, not just a price tier: your key, your
  data relationship. Worth one caption under the BYOK card.
- ⚠️ The v6 copy's PRICING section ("framework free forever, you only pay
  for the AI, €29/month") **no longer matches this model**. The v7 working
  rewrite in temp assets carries the new version; the Drive doc still
  needs updating.
- FAQ candidates (Billow's "Totally fair to ask." + Gainbridge's "how do
  we make money" candor; Overnight Strategist shows objection-FAQ works on
  this audience): optional 4-item accordion here or on /pricing.

### 9. CLOSE: *the dare* (dark, full atmosphere, mirrors the hero)
- Copy: "Go ahead. Wing it. Copy your peers. Let ChatGPT pick." (Lora,
  display scale, white; the page's second-biggest type moment).
- The composer returns (same component as hero), placeholder now:
  "Bring the question you've been avoiding_" (with the blinking orange
  underscore). Primary CTA: `[ Answer the question you've been avoiding ]`.
- Background: darkest nature yet, a dusk/fog POV shot, heavy grain.

### 10. FOOTER (dark espresso, recessed atmosphere)
- White logo asset, minimal columns (Product / Company / Legal), language
  hint (EN/DE later), compliance/privacy line. Quiet.

**Page rhythm summary**: dark hero → dark statement → light → light →
nature breath → light → dark → light → dark close → dark footer. Two
utility blocks never sit adjacent without a tonal change; every emotional
(dark/nature) moment is followed by a concrete one.

---

## 4. Section-level animation choreography

Global rules live in the design system §9. Per-section specifics:

| Section | Primary (first, biggest) | Secondary | Ambient |
|---|---|---|---|
| Hero | Headline 24px rise | Composer + chips stagger | Ken-Burns drift, CTA glow pulse, node draw-on |
| Stakes | Statement lines reveal per-paragraph on scroll | (none) | Grain shimmer only (near-still, Skoll) |
| What it is | Strike-through chips animate their strikes | Glass card floats in (+2px hover) | (none) |
| How it works | Video frame rises | Step cards stagger L→R +120ms | Muted UI loops; node connectors draw after cards settle |
| Interstitial | Quote fades (opacity only) | (none) | Slow drift |
| Edge | Node diagram lights node-by-node on scroll | Text reveals | (none) |
| Compounding | Brief stack accumulates on scroll (one card per ~80px scroll, capped) | Trust badges fade | Corner glows breathe |
| Pricing | Cards rise | Numerals count up once (mono) | Featured-card glow |
| Close | Headline rises big | Composer mirrors hero entrance | Blinking `_`, darkest atmosphere |

Scroll-driven **background theme morphing** (light↔dark) implemented as one
page-level controller (GSAP or CSS `animation-timeline`), not per-section
hacks. All reveals `once`, all guarded by `prefers-reduced-motion`.

---

## 5. Technical shape (when we build)

- `apps/web/app/(public)/page.tsx` is the homepage; sections as components
  under `apps/web/features/marketing/` (marketing components stay in the
  app, shared tokens come from `@foothold/ui`).
- Hero/CLOSE composer reuses the real composer component against the
  anonymous-draft flow (`/start` → localStorage draft), engineering plan
  phases 9–11. Until that flow ships, the composer can route to `/start`
  with the question as a param.
- Video: self-hosted MP4/WebM, `muted playsinline preload="none"`, poster
  frame, `motion-reduce:hidden` fallback poster (Sanity pattern). Product
  video production can go through the hyperframes pipeline later.
- Imagery: source grainy nature photos into `apps/web/public/marketing/`
  (AVIF + JPEG fallback); grain applied in-asset, not runtime, for the
  full-bleed shots (runtime SVG grain reserved for atmosphere layers).
- SEO: this page is the one place plain-HTML text matters most. Reveals
  must be CSS-only-enhanced (content present without JS).

---

## 6. Brand audit (the 5 world-building questions)

**1. Does it have a point of view? YES, but put it higher.**
"Your judgment is the last thing that's still yours, and most people are
quietly outsourcing it" is a genuine contrarian belief (the whole market
shouts "let AI do it"). It currently lives in STAKES, one scroll down. The
5-second test fails if the hero says only "Great decision making has a
structure." **Recommendation**: the hero's rotating line or lead must carry
the anti-outsourcing edge explicitly (e.g. keep "You do the thinking.
Foothold makes sure it holds." visible in the hero viewport).

**2. Does everything speak the same language? MOSTLY; leaks being closed.**
(a) *Naming*: **RESOLVED (2026-07-02): it is the Clarity Brief**, never
"Outcome Brief". Sweep engineering plan / older docs when touched.
(b) *Pricing story*: **RESOLVED (2026-07-02)**: annual-only, two tracks
(BYOK / AI included), Solo + Team, founding-member launch pricing; see
§3.8. This retires the copy's "framework free forever / €29 per month"
story. CONTEXT.md has been updated. The anonymous session up to the
Clarity Brief gate is the trial.
(c) *Register wobble*: v6 mixes calm gravity with jokey asides ("that's for
sure", "boom"-adjacent). The register that matches the visual world is dry
warmth: confident, a little wry, never jokey. The v7 working rewrite runs
the draft through `docs/skills/copywriting.md`. The Overnight Strategist
audit sharpens this: their funnel urgency is the exact voice this audience
is already being sold in. Foothold's calm is positioning, not just taste.

**3. Do I feel something specific? YES.**
"A quiet room with the lights on": espresso dark + grain + warm glow +
serif = calm with quiet tension. The named feeling survives the logo strip
test because no mainstream SaaS occupies warm-analog-dark (they're all
white/blue/purple-gradient).

**4. Would I know it without the logo? YES, with discipline.**
Signature stack: grainy overexposed POV nature + espresso glass + Lora
judgment voice + single orange + thinking nodes + visible guides. Caveat
from research: Nolla runs nearly the same cream/espresso palette. Our
differentiators are the **serif voice, the grain, the orange, and the
nodes**, so those four must appear in every asset (social cards included).

**5. Is the audience visible? YES, resharpened 2026-07 (POSITIONING.md V4).**
The audience is the person who owns the call: 80% organizational stakes,
20% the same person's personal high-stakes. POV imagery casts the visitor
as the thinker (their hands, their notebook, their view;
reMarkable-adjacent, which is exactly this buyer's aesthetic). The starter
chips name their actual questions ("Should we build the new warehouse?").
The pricing respects their self-image (annual, plain-stated, "if your work
runs on your judgment"). The wrong audiences, answer-machine seekers and
generic life-clarity browsers, correctly feel nothing here. Note: v6 copy
examples still skew personal ("Should I leave this job?" leads its
question list); the v7 rewrite flips the lead set per POSITIONING.md.

---

## 7. Open decisions (need Vincent)

1. ~~Free-tier promise~~ **Resolved**: annual two-track pricing (§3.8);
   anonymous session = trial. Remaining sub-decision: exactly what the
   anonymous run includes before the Clarity Brief gate, and whether the
   founding-member window has a stated end condition (cohort size or date,
   stated plainly if so, never as a countdown).
2. **Review the v7 copy rewrite** (temp assets) and carry it back into the
   Drive doc, which still holds v6.
3. **Rotating hero headline**: in or out (layout reserves the line).
   Candidate H1 floated 2026-07-02 alongside the refreshed POSITIONING.md
   "What it is" copy (DECISION-088): **"A new way of thinking."** Tentative,
   not decided; would replace or precede "Great decision making has a
   structure." in the v7 draft — test against the 5-second test (§6.1)
   before committing, since it's more identity-forward and less
   mechanism-forward than the current lead.
4. **Hero photo**: source the actual forest/POV shot (license or shoot);
   the mock's sun-flare forest is the reference.
5. **Product video**: storyboards, scripts, and production paths live in
   [PRODUCT_VIDEO_PLAN.md](PRODUCT_VIDEO_PLAN.md) (3s teaser loop / 30–45s
   master / ≤2min tour; one master, cuts fall out of it). Homepage ships
   with a styled poster + "coming" state if video isn't ready.
6. **FAQ on homepage** vs pricing page only (Overnight Strategist confirms
   objection-FAQ works on this audience).
7. **Testimonial slot**: skeleton reserves none (pre-launch); Jan's DE
   quote exists; Overnight Strategist's peer-endorsement pattern (named
   operators, not logos) is the model when proof arrives.
