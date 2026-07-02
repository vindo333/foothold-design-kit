# Foothold Product Video Plan

Storyboards, scripts, and production notes for the homepage product video
family. Companion to [HOMEPAGE_PLAN.md](HOMEPAGE_PLAN.md) (§3.1 hero, §3.4
HOW IT WORKS) and [MARKETING_DESIGN_SYSTEM.md](MARKETING_DESIGN_SYSTEM.md)
(feed BOTH docs to whatever produces the video). VO and on-screen text
follow `docs/skills/copywriting.md`. **Planning only.**

---

## 1. Strategy: one master, three cuts

Not three videos. **One 40s master designed so shorter cuts fall out of
it**, plus an extended tour assembled from the same footage:

| Cut | Length | Job | Lives where |
|---|---|---|---|
| **Teaser loop** | 3–4s, seamless loop | "I get what this is" before a single word is read | Ambient, muted, autoplaying inside the HOW IT WORKS poster frame (and later: social cards, ads) |
| **Master: "How it works"** | 30–45s | The full arc: question → model → blind spots → Clarity Brief | The homepage video player (§3.4); the "See how it works" target |
| **Extended tour** | ≤120s | Consideration-stage depth: the master + three feature chapters | NOT autoplaying on the homepage. End-screen of the master ("Watch the full tour"), /pricing, onboarding emails |

Rules that make the nesting work:

- The teaser is the master's **first shot family compressed**, not new
  footage.
- Every shot is **sound-off-first**: on-screen text carries 100% of the
  meaning (homepage video autoplays muted; most viewers never unmute).
  Voiceover is a reinforcement layer, not the spine.
- One continuous visual thread: **the same question** ("Should we build
  the new warehouse?" or "Should we make this hire?", organizational
  stakes per POSITIONING.md V4) flows through every cut. Never switch
  example questions mid-video.

---

## 2. The 3-second teaser (the hardest one)

3 seconds = one idea, one motion, zero cuts. The idea that survives:

> **A hard question goes in → structure blooms around it → a solid answer
> comes out.**

**Single continuous shot (3.5s, seamless loop):**

1. **0.0–1.0s**: the glass composer on the dark atmosphere. The question
   types itself (fast, real cursor): *"Should we build the new
   warehouse?"* with the orange `_`.
2. **1.0–2.3s**: the question card recedes to center; **four thinking
   nodes bloom** around it with drawn-on connectors (the app's 4 angles,
   labels flashing just long enough to register: *working for you / could
   sink it / the win / first moves*). One node pulses orange: a blind spot
   flagged.
3. **2.3–3.5s**: the node map collapses inward into a single **Clarity
   Brief card** that settles (fh-settle motion) with a soft shadow. Beat.
   Loop back to the empty composer.

On-screen text (one line max, Lora, appears ~1.2s): **"You think. It
holds."** Or no text at all; the motion alone answers "what is this."

No music dependency, no VO. It must work as a silent GIF-like loop.
This cut is buildable as a standalone `/motion-graphics` piece from pure
brand-styled HTML (no screen recording needed), which makes it the
cheapest thing to produce first and validates the whole visual language.

---

## 3. The 30–45s master: storyboard + script

Structure mirrors the copy's three moves. ~40s, 7 shots. VO budget at a
calm ~130 wpm ≈ 85 words (script below is 83). Captions ≈ shortened VO.

| # | Time | Visual (all real UI unless noted) | On-screen text | VO (optional layer) |
|---|---|---|---|---|
| 1 | 0–4s | The teaser's shot 1: composer, question types itself on the dark atmosphere | (none) | "Some questions sit with you for weeks." |
| 2 | 4–9s | Cut to the real session: the guided start, no blank page, the first prompt appears, user answer flows in | "No blank page." | "Bring one to Foothold. It starts you off." |
| 3 | 9–17s | The 4-angle model filling with real content (screen recording, sped ~2×); nodes/connectors overlay drawn on top linking entries | "Build the whole picture." | "You map what's working, what could sink it, and the win, reverse-engineered." |
| 4 | 17–24s | The diagnostic: thinking-wash sweep, then an assumption gets flagged (orange), contradiction lines drawn between two of the user's own ideas | "It hunts your blind spots." | "Then it pressure-tests what you built. The assumptions you didn't notice. You decide what's real." |
| 5 | 24–31s | The Clarity Brief assembling (the app's stepped narration is inherently cinematic; record it real) | "Walk out with a Clarity Brief." | "You walk out with one clear read: what you decided, and the first real moves." |
| 6 | 31–36s | Zoom out: brief card joins a small stack of past briefs (compounding); export flourish (→ Notion/Obsidian glyphs, subtle) | "Session fifty: a record of how you think." | "And it compounds." |
| 7 | 36–41s | Logo asset on dark atmosphere, grain, orange `_` blinking; CTA | "foothold_ · No account needed to start thinking." | "Foothold. You do the thinking. It makes sure it holds." |

Notes:

- Shots 1–2 double as the **10s cutdown** if ads ever need one.
- The teaser (§2) is shots 1+3+5 compressed, same motion vocabulary.
- Music: one calm, warm bed (no build-drop EDM); grain-era analog feel,
  low in the mix. VO voice if used: measured, dry-warm, mid-register,
  never announcer-energy.
- Register guard: no feature-name soup, no "revolutionary," no speed
  claims beyond "30 minutes" if it appears at all.

---

## 4. The ≤2min extended tour

Master (40s) + three chapters (~25s each), same visual system, chapter
cards using the mono `[BRACKET]` eyebrows:

1. `[THE MODEL]`: deeper on the four angles + the guided starters
   (the "stuck?" nudges, ranked questions).
2. `[THE DIAGNOSTIC]`: deeper on blind-spot hunting: bias flags,
   contradictions between your own ideas, the negation test.
3. `[THE RECORD]`: history, themes across sessions, privacy/export,
   BYOK ("your key, your data relationship").

Ends on the same CTA shot as the master. This cut is assembled, not
re-produced: chapters are additional screen recordings styled identically.

## 5. Production paths

**Path A: Claude Design (video function).** Feed it, in order:
MARKETING_DESIGN_SYSTEM.md → this doc → the specific cut you want, one at a
time, starting with the teaser (smallest, validates the language). Instruct
it to use the `--mk-*` tokens verbatim and the §2/§3 storyboard as a hard
shot list, and to treat on-screen text as primary (sound-off-first).

**Path B: hyperframes pipeline (in this repo, via Claude Code).** The
`/motion-graphics` workflow builds the teaser from brand-styled HTML (no
recordings needed); `/product-launch-video` or `/general-video` builds the
master/tour from the screen recordings + this storyboard, with music and
optional TTS VO. Renders real MP4/WebM deterministically with the exact
brand tokens.

Recommended order regardless of path: **teaser first** (cheap, no
dependencies, proves the visual language) → master once recordings exist →
extended tour last.

## 6. Capture kit (stills done 2026-07-02, recordings pending)

A complete warehouse session now exists as a dev fixture:
`apps/web/app/(public)/dev/fixtures/warehouse.ts`, wired into the three
dev preview routes via `?q=warehouse` (dev-only, 404s in production).
Anyone can re-capture stills or record video from these routes with the
run-web skill's CDP driver; no auth, no AI keys needed. Stills live in
`docs/temp-working-assets/video-shots/`.

| Storyboard shot | Still(s) | Route to capture/record |
|---|---|---|
| Shot 1 (composer) | `shot1a/1b-composer-*.png` | `/start`, type into the question input |
| Shot 2 (guided start) | `shot2-guided-start-specify.png` | `/dev/journey-preview?q=warehouse&step=specify` |
| Shot 3 (model filling) | `shot3a-angles-bottomup.png` | `/dev/journey-preview?q=warehouse&step=topdown\|bottomup` |
| Shot 4 (blind spots) | `shot4a-review-themes.png`, `shot4b-thinking-wash.png` | `/dev/review-preview?q=warehouse` and `&generating=1` |
| Shot 5 (Clarity Brief) | `shot5-brief-step0..6.png`, `shot5-brief-full.png` | `/dev/brief-preview?q=warehouse&step=0..6`, `&full=1` |
| Shot 6 (history/export) | not captured yet | needs the authed path (`seed-session.mjs` × several) |

What the capture taught us (plan ↔ reality sync):

- The UI's real stage names: the sharpening chat is `specify`, the risk
  angle is "Bottlenecks", the review checks are "Resolve the tensions /
  Settle what you deferred / Check your blind spots", and the brief's six
  chapters are "The gist / Where you are now / Minimum critical advantage /
  What to avoid / What's ahead / Carry it forward". Use these names in
  on-screen text where the video shows the UI; invented labels would
  contradict what viewers then see in the product.
- **Shot 4's best frame is the brain-node loading screen** ("Weighing the
  1 claim you settled…"): orange nodes lighting on the node-mesh brain.
  It is simultaneously the thinking-wash beat AND the brand's node motif.
  Record `?q=warehouse&generating=1` for it.
- **Poster frame candidates**: brief step 1 ("Don't commit to the build
  yet…" in display Lora on dark atmosphere) or brief step 0 (the
  six-chapter contents under the question). Both beat the §7 suggestion
  of the settled-card frame; §7 updated.
- The hero micro-trust line already exists in the product verbatim ("No
  account needed to start thinking" sits inside the composer card), so
  shot 7's CTA text matches reality as written.
- The review screen's tension cards ARE the "contradiction between your
  own ideas" visual from shot 4, with quoted claims and an AI-suggested
  resolution; no motion-graphics invention needed.

### Recordings still to gather (for the master/tour)

Screen recordings of the same fixture routes (per the logo/imagery rule:
never fake the UI), 1920×1080+ browser, dark theme:

1. Composer: typing the question, sending (hero + shot 1) — `/start`
2. Guided start: prompt appearing, answering (shot 2)
3. 4-angle model filling (shot 3); type 1–2 extra items live so motion
   shows the model growing
4. Review: tensions + the `generating=1` brain-node run (shot 4)
5. Clarity Brief chapter walk, step 0 → 6 (shot 5)
6. Dashboard/history with several sessions (shot 6) — authed path
7. Export action (shot 6) — authed path

## 7. Delivery specs

- Master format 16:9 1920×1080 (record at this or higher); teaser also
  cropped 1:1 and 4:5 later for social.
- Homepage teaser loop: H.264 + WebM, muted, `playsinline preload="none"`,
  target < 4 MB; poster frame = the brief's "gist" chapter (see §6 poster
  candidates: `shot5-brief-step1.png` or `step0.png`).
- Master: streamed or self-hosted MP4 ≤ 15 MB; captions burned-in (design
  system type, not player-default subtitles); `motion-reduce` → poster.
- Every cut ends on a frame that works as a still (poster discipline).
