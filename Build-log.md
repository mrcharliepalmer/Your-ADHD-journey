# Build Log — CareADHD Journey Page Redesign

**Project:** Speculative redesign of careadhd.co.uk/your-journey-with-us
**Date:** 28 February 2026
**Built by:** Charlie Palmer (Red Slash Studio) + Claude
**Status:** Ninth iteration — section transitions unified, watermark removed

---

## 1. What Was Built

A single-page HTML/CSS redesign of CareADHD's "Your Journey With Us" page. The existing page used a 10-step process flowchart and FAQ accordions — operational language aimed at the business. The redesign reframes the same journey as a narrative aimed at the person arriving at the page, anxious and uncertain.

**Deliverable:** `index.html` — single file, embedded CSS, no external dependencies beyond Google Fonts (Inter). ~760 lines. Ready for GitHub Pages or static hosting.

**Key design features:**
- Teal gradient hero with the opening copy line promoted to headline
- Lora (serif) + Inter (sans-serif) font pairing for editorial warmth
- Section-based layout with alternating backgrounds for visual rhythm
- Hand-drawn illustration in Step 3 (hand holding smartphone) replacing the CSS phone mockup
- Detail pills in Step 4 (virtual, 60–90 mins, one-to-one) for scannability
- Italic serif emotional beat in Step 5 at a narrower column width
- Treatment cards with two-column layout (Step 6)
- Watermark numbers (removed — illustrations now carry that visual weight)
- Warm amber accent colour alongside the existing teal/pink brand palette
- Scroll-triggered reveal animations (IntersectionObserver, vanilla JS)
- Staggered text entrance animations in the hero
- CTA strip with three equal-weight options at page end

---

## 2. Process — How This Was Made

### Phase 1: Briefing & framing
The project was pre-framed before any tools were opened. A `CLAUDE.md` file established:
- The strategic intent (speculative pitch to CareADHD leadership)
- The audience (a CMO who cares about their brand)
- The success criteria ("if they think *this is better than what we have* — that's success")
- The tone constraints (warm but not soft, credible healthcare, not a wellness app)
- The copy source (`CareADHD_Journey_Page_Copy.md`) — treated as locked, not to be altered

**This is the most important phase.** The brief did more work than any design decision that followed. Every subsequent choice had a frame to be evaluated against.

### Phase 2: Brand & competitor analysis
Before writing any code, the existing CareADHD site was examined in detail:
- Live journey page — structure, hierarchy, infographic, FAQ section
- Homepage and About page — for broader brand context
- CSS extraction — exact colours (`#3F7174`, `#F0B0C8`), fonts (Familjen Grotesk, Arimo), patterns
- Logo assets — URLs captured from Squarespace CDN
- Platform identification (Squarespace) — informed what constraints the current team operates under

This produced a written analysis identifying the core problem: the page treats the process as an internal operational flow, not a human experience.

### Phase 3: Planning
A structured implementation plan was written before any code, covering:
- Design system (colours, typography scale, spacing)
- Section-by-section layout decisions
- Responsive strategy
- Technical approach (single file, no dependencies)

Three clarifying questions were asked before the plan was finalised:
1. Promo bar (yes/no) → No — keep narrative focus
2. App section treatment (device mockup vs elevated styling) → Elevated styling only
3. Motion (transitions vs static) → Subtle transitions

### Phase 4: First build
The full page was built in a single pass — all HTML structure, all CSS, all copy, all responsive rules. This was previewed in-browser immediately.

**Assessment of v1:** Structurally sound, copy faithful, but visually flat. "A long wall of text" on alternating backgrounds. Functionally correct but not yet a piece of work that makes someone stop and think.

### Phase 5: Visual upgrade
A direction was chosen:
- Timeline journey layout (over card-based or editorial alternatives)
- Warm amber accent colour (over staying within teal/pink only)

The page was substantially rewritten — not tweaked — with:
- New hero treatment (gradient, headline promotion, label)
- Timeline grid layout replacing stacked sections
- Feature cards for the app section
- Treatment cards with amber dot accents
- Stronger typographic hierarchy for emotional moments
- Pull quote styling for Step 7
- Gradient CTA strip with depth

### Phase 6: Verification
- Full desktop scroll-through in browser
- Copy cross-checked against source file (two defensible capitalisation changes noted)
- Scroll animations verified
- Mobile CSS rules reviewed (viewport testing limited by environment constraints)

### Phase 7: Typography & structure overhaul
Charlie's feedback on v2: "The serif font makes a real difference... but the rest of the page lacks visual dynamism. Everything just feels the same."

The page was rebuilt with:
- **Lora serif** paired with Inter sans-serif — editorial warmth, immediate quality gap vs the live site
- **Section-based layout** replacing the rigid timeline grid — each section free to use its own visual treatment
- **Bridge line** ("Whatever brought you here...") in italic serif — warm, human transition from hero to process
- **Alternating background washes** (warm-white, teal-wash, amber-wash, pink-wash) for scroll rhythm
- **SVG line icons** replacing emoji in the app features section
- **Frosted glass nav** with backdrop-filter blur

### Phase 8: Visual dynamism pass
Charlie's feedback on v3: "Everything just feels the same. How do we inject something special into it?"

The core problem: every section was step-num → heading → paragraphs at the same width. Structurally correct, visually monotonous.

Changes made:
- **Hero background fade removed** — the gradient from teal to warm-white at the bottom was replaced with a clean hard edge. More contemporary.
- **Step 3: Phone mockup** — the four app features now render inside a CSS phone frame (dark bezel, notch, rounded screen, tab bar dots). The app stops being a list of features and starts looking like a real product.
- **Step 4: Detail pills** — "Virtual appointment", "60–90 minutes", "One-to-one" as scannable rounded badges with SVG icons, pulling key facts out of the body text.
- **Step 5: Intimate column** — narrower max-width (560px vs 720px), italic serif emotional beat. Creates a genuine pause in the page's rhythm at the emotional peak.
- **Steps 1 & 7: Watermark numbers** — large, faded serif numbers in the background, adding visual depth to the plainest text sections.

The page now has genuine visual variety — each section feels distinct while remaining coherent. The phone mockup is the standout moment; the intimate Step 5 is the emotional one.

---

## 3. Reflections on Working Style

### What Charlie does before opening any tool

The brief (`CLAUDE.md`) was the first artefact — not a wireframe, not a mood board, not code. It established:
- **Who sees this and why** (a CMO evaluating whether to have a conversation)
- **What the emotional state of the end user is** (anxious, uncertain, possibly relieved)
- **What success looks like** in concrete terms
- **What not to do** (no clinical language, no marketing language, no rewriting copy)

This is a consulting habit, not a design habit. The frame comes first. The work is always in service of a clearly articulated intent.

### Copy comes before design

The page copy was written separately, in a standalone Markdown file, before any visual decisions were made. The copy was treated as the primary deliverable — the design exists to serve it, not the other way around.

This is unusual. Most web design processes start with wireframes or templates. Here, the copy *is* the architecture. The design decisions (timeline, card treatments, typographic emphasis) all emerged from the copy's natural rhythm — where it pauses, where it builds, where it lands an emotional beat.

### Opinionated but not prescriptive

Charlie had clear instincts throughout:
- "It's a bit dull to look at" — honest assessment, no hedging
- Immediate selection of the timeline approach and warm accent colour — decisive, confident

But the approach was always *directional* rather than pixel-specific. The brief said "generous white space — it is doing as much work as the content" rather than "32px padding between sections." This gave room for implementation decisions while keeping the intent locked.

### Quality is the argument

The `CLAUDE.md` explicitly states: "The redesigned page is the argument. It should speak for itself before the email does."

This means every decision has to survive the question: *does this make a CMO want to have a conversation?* That's a higher bar than "does this look good" or "does this communicate the steps." The work isn't a deliverable — it's a credential.

### Iterative, not perfectionist

The first version was allowed to exist, was assessed honestly, and was then substantially upgraded. There was no attempt to get it perfect first time — the first pass established the structural foundation, the second pass added the visual personality.

This is a healthy creative rhythm: get the bones right, then dress them. It also means the first version wasn't wasted — the copy placement, semantic structure, and responsive rules all carried through.

---

## 4. Toward Automation — What's Capturable

If the goal is to develop a repeatable process that can be partially automated, here's what this session suggests:

### Already systematisable
- **Brand analysis** — Extracting colours, fonts, layout patterns, and platform from a live URL. This is mechanical and could be scripted or templated.
- **Copy-to-HTML mapping** — Taking a structured Markdown file and producing semantic HTML with the right heading levels, paragraph structure, and section breaks.
- **Design system generation** — Given a set of extracted brand colours, generating an extended palette (light/dark variants, accent options, text colours) is formulaic.
- **Responsive scaffolding** — The breakpoint rules, font scaling, and layout collapse patterns are consistent across projects.

### Partially systematisable (needs judgement)
- **Section-level design decisions** — Which sections get visual elevation, which get cards, which get typographic treatment. This follows the *copy's emotional arc*, which can be signalled (e.g., marking key lines in the Markdown source) but not fully automated.
- **Visual rhythm** — Alternating backgrounds, spacing variation, and timeline vs flat layout. Could be offered as options from a template, with a human choosing.
- **Accent colour selection** — Could be generated algorithmically (complementary/analogous to the primary brand colour) but the final choice needs taste.

### Not systematisable (this is the expertise)
- **The brief itself** — Identifying the strategic frame, the audience, the emotional state of the reader, and the success criteria. This is the consulting layer. It's the reason the work is good, and it can't be templated.
- **Knowing when something is "dull"** — The first version was structurally correct. Knowing it wasn't *enough* — and knowing which direction to push — is pattern recognition built from experience.
- **Tone calibration** — "Warm but not soft" is a judgement call that affects every decision from font weight to background colour to how much whitespace to leave after an emotional paragraph. This is the hardest thing to encode.

### A possible process template

```
1. FRAME    → Write the brief (audience, intent, success criteria, constraints)
2. COPY     → Write the page copy in structured Markdown, locked before design begins
3. ANALYSE  → Extract brand assets from existing site (colours, fonts, logo, patterns)
4. PLAN     → Define design system + section-by-section layout decisions
5. BUILD    → Generate the first structural pass (HTML/CSS from copy + design system)
6. ASSESS   → Review honestly — does it meet the brief's success criteria?
7. ELEVATE  → Apply visual personality (the layer that makes it *good*, not just correct)
8. VERIFY   → Cross-check copy, test responsive, confirm quality bar
```

Steps 3 and 5 are the most automatable. Steps 1, 6, and 7 are where the expertise lives. Steps 2 and 4 are in between — they benefit from structure but require creative judgement.

### Phase 9: Visual richness — hero transition + upcoming enhancements

Charlie's feedback on the current build: "It feels too much like a long text wall with little visual dynamic." The structural variety added in Phase 8 (phone mockup, pills, intimate column, watermark numbers) helped, but the sections between those highlights are still blocks of text on alternating backgrounds. The page needs more visual richness without adding clutter.

**Six options were discussed. Three were selected as the highest-leverage trio:**

1. **Journey thread** — a thin vertical line running down the left side connecting all step numbers, turning seven separate sections into one continuous visual journey. Step numbers become nodes on the line rather than floating labels.

2. **Key-fact callouts** — pull specific details out of body text into visually distinct typographic moments. Candidates: "within 24 hours" (Step 1), "Weeks 4 and 12" (Step 6), and similar concrete details that give scanners something to land on without reading every paragraph.

3. **Section dividers** — subtle curved SVG shapes between sections instead of hard background-colour edges. The hero already uses organic SVG curves; carrying that language through the page would create flow between sections rather than rigid blocks.

**Other options discussed but deferred:**
- Alternating content alignment (offset text, asymmetric layouts)
- Scroll progress indicator showing position in the 7-step journey
- Step-level iconography (hand-drawn illustrations — see below)

**What was completed in this session:**

**Hero-to-bridge transition redesign.** The hard edge between the teal hero and the warm-white body was the most jarring transition on the page. Three techniques were combined:

- **Overlapping bridge card** — the "Whatever brought you here" quote is now inside a white card (rounded corners, layered shadow) that physically overlaps the hero section via negative margin. It acts as a visual stepping stone between the two worlds.
- **Soft vignette** — a 180px gradient fade at the very bottom of the hero, fading teal to warm-white. Starts well below the last paragraph so the copy never feels rushed or faded out. The hero has 16rem of bottom padding to create clear breathing room between the copy and the fade.
- **Extra hero depth** — generous padding below the copy gives the hero's final statement room to land before any visual transition begins.

The bridge card's `z-index: 3` places it above the vignette, so it sits cleanly in the transition zone.

**Hand-drawn illustration style.** Charlie shared examples of ink-sketch illustrations (black line work with red accents) generated for a separate project in a consistent house style. These were discussed as potential per-step illustrations that could replace or augment the existing visual treatments:
- Hand holding a lightbulb (Step 1 — recognition)
- Hand writing/filling a form (Step 2 — questionnaires)
- Hand holding a phone (Step 3 — could replace the CSS phone mockup with something more distinctive)
- Two people in conversation (Step 4 — assessment)
- Hand holding a mirror or lens (Step 5 — diagnosis/self-understanding)
- Hand holding puzzle pieces or adjusting dials (Step 6 — treatment)
- Hand pointing at a chart or holding a compass (Step 7 — long-term plan)

These would be generated externally and added as image assets. The style is warm, human, editorial — not clinical or corporate — which matches the page's tone perfectly. This would be a genuine differentiator vs any competitor in the ADHD assessment space. **Decision deferred until Charlie confirms the illustration style can be generated consistently enough across 7 images.**

### Phase 10: Visual richness — journey thread, key facts, section dividers

All three priorities from Phase 9 were implemented in a single pass.

**1. Journey thread**

A `.journey-thread` wrapper div encloses all seven journey sections. A `::before` pseudo-element draws a continuous 1px vertical line down the left gutter, positioned at `calc(50% - 360px - 2.5rem)` — 2.5rem left of the 720px content edge. The line uses `var(--teal-mid)` at 15% opacity with a linear gradient that fades to transparent at top and bottom.

Each `.step-num` gains a `::before` node dot — a 9px circle with a 2px border in `var(--teal-mid)`, positioned at `left: -2.5rem` to sit on the thread line. The dot's `background` matches the section's background colour (warm-white by default, teal-wash and amber-wash via overrides) so it "punches through" the line cleanly.

Adjustments were needed for sections with non-standard content widths:
- **Step 3 (showcase, 880px):** dot offset increased by 80px (`left: calc(-2.5rem - 80px)`)
- **Step 5 (intimate, 560px):** dot offset decreased by 80px (`left: calc(-2.5rem + 80px)`)

The thread and node dots are hidden on mobile (`display: none` below 768px) — the vertical line doesn't work at narrow widths and the step numbers read fine without it.

**2. Key-fact callouts**

Four editorial-style callout cards were added, each sitting below the relevant paragraph. They use a `.key-fact` class — `inline-flex`, white background, 8px border-radius, 3px amber left border, subtle box shadow. Inside: a `.key-fact-value` (Lora serif, 600 weight, teal-deep) and a `.key-fact-label` (smaller, secondary colour).

The four callouts:
- **Step 1:** "Within 24 hours" — "we'll be in touch after you sign up"
- **Step 2:** "Not a test you pass or fail" — "just a starting point for understanding your story"
- **Step 6:** "Weeks 4 & 12" — "medication reviews to check progress and adjust"
- **Step 7:** "At NHS cost" — "ongoing medication through your GP under shared care"

These are *not* new copy — they're phrases already present in the body text, promoted to scannable highlights. The treatment feels editorial (a magazine pulling out key stats) rather than UI badges or marketing callouts. On mobile, padding and font size reduce slightly for better stacking.

**3. Section dividers**

Six curved SVG dividers replace the hard colour-block edges between journey sections. Each is a `<div class="section-divider">` containing an SVG with a `viewBox="0 0 1440 48"` and `preserveAspectRatio="none"`. The SVG path creates a gentle wave; the `fill` matches the *next* section's background colour, and a `divider-from-*` class sets the div's own background to match the *preceding* section.

Each divider uses a different curve profile so they don't feel repetitive:
- Step 1→2: single S-curve
- Step 2→3: double wave (three control points)
- Step 3→4: asymmetric sweep
- Step 4→5: inverse S-curve
- Step 5→6: steep dip with recovery
- Step 6→7: gentle undulation

The `::before` and `::after` border lines on the step-showcase section (Step 3) were removed since the dividers now handle that transition. Dividers scale to 32px height on mobile.

**What this achieves:**

The page now has three layers of visual richness beyond the copy itself:
1. A *structural* layer (the thread) that ties the seven sections into one continuous journey
2. A *content* layer (the key facts) that gives scanners concrete details to land on without reading every paragraph
3. A *transitional* layer (the dividers) that creates organic flow between sections instead of rigid blocks

None of these add clutter or compete with the copy. They work *with* the existing visual treatments (phone mockup, pills, intimate column, watermark numbers, treatment cards) to create a page with genuine variety at every scroll position.

### Phase 11: Hero curve, bridge restyle, illustrations, timeline removal

Four connected changes in a single session, each following from the last.

**1. Hero-to-body transition: vignette → SVG curve.**

Charlie felt the soft gradient vignette at the bottom of the hero lacked clear demarcation — it faded rather than transitioned. The 180px `::after` linear gradient was replaced with a `.hero-curve` element containing an SVG path (`viewBox="0 0 1440 80"`) that creates an asymmetric wave filled with `var(--warm-white)`. This matches the curved SVG divider language already used between journey sections, giving the page a consistent organic transition style throughout. The curve sits at the bottom of the hero via `position: absolute; bottom: -1px`.

**2. Bridge restyle: card → section header.**

With the curve creating a clean edge, the overlapping white bridge card (which relied on the vignette's ambiguity to work) no longer made sense. The "Whatever brought you here, here's what happens next" line was taken out of its card container and restyled as an italic serif header sitting at the top of the off-white section. The `.bridge-card` wrapper, its `box-shadow`, `border-radius`, and negative margin were all removed. The bridge section now has `background: var(--warm-white)` and `padding: 4.5rem 2rem 4rem`, with the text at `1.875rem` and the amber rule beneath. Simpler, cleaner, more confident.

**3. Hand-drawn illustrations: style development and first integration.**

A significant creative discussion established the illustration approach for the page:

- **Style:** Hand-drawn ink fineliner in CareADHD teal (#3F7174) with CareADHD pink (#F0B0C8) as a sparing accent — not the red accent from a previous project. Warm, editorial, human.
- **Subject matter principle:** Metaphorical at emotional peaks (Steps 1, 4, 5, 7), grounded/literal at practical steps (Steps 2, 3, 6). Each illustration finds its own register; consistency comes from the illustration *style*, not the illustration *approach*.
- **Subjects discussed:**
  - Step 1: A door slightly ajar with warm light spilling through (recognition, arrival)
  - Step 2: Fragments/pieces assembling, a constellation forming (building a picture)
  - Step 3: A companion, a thread connecting (support from day one)
  - Step 4: Two chairs, two cups of tea (conversation, not examination)
  - Step 5: A lens coming into focus, fog clearing (diagnosis, understanding)
  - Step 6: A key cut to fit, ingredients being chosen (bespoke treatment)
  - Step 7: A road continuing, roots growing (long-term continuity)

A Gem (custom GPT-style prompt) was written to generate illustrations consistently in this style, adapted from an existing Steadman.ai illustrator prompt. Key changes from the source: energy shifted from dynamic to still, shading softened from architectural hatching to stippling/cross-hatch, silhouette mode replaced with open line drawings, and explicit subject matter guidance added to avoid clinical imagery.

**Step 1 illustration (door ajar) was generated, refined, and integrated.** The image was placed alongside the Step 1 copy in a two-column grid layout (`.journey-section--illustrated`): copy left, illustration right. A new CSS class handles the grid at `var(--showcase-width)` with `grid-template-columns: 1fr 1fr` and `gap: 3rem`. On mobile, the grid collapses to single-column with the illustration above the copy (`order: -1`).

Background removal was handled manually by Charlie (the AI-generated warm-white background didn't match exactly, and `mix-blend-mode: multiply` didn't produce clean enough results). The pink light wash from the door was preserved through careful manual extraction.

**4. Journey thread removed.**

The vertical timeline (thread line + node dots on step numbers) was introduced in Phase 10 to tie seven separate text sections into one visual journey. With illustrations now serving that connective role — consistent style, recurring placement, visual rhythm — the thread became redundant and created a layout conflict with the two-column illustrated sections. Removed:

- `.journey-thread` wrapper div and its `::before` vertical line
- `.step-num::before` node dots and all section-specific dot offset overrides (showcase, intimate, teal-wash, amber-wash)
- Mobile hide rules for thread and dots
- The step numbers retain their dash (`::after`) and typographic treatment

The illustrations replace the timeline's job better: they're more visually distinctive, carry emotional weight, and don't constrain the layout.

### Phase 12: Step 2 illustration attempts → typographic solution

**The problem:** Step 2 ("We'll ask you to help us build a picture") needed visual treatment. Multiple illustration concepts were attempted:

1. **Torn fragments assembling** — read as destruction, not construction. The pieces looked ripped apart, not gathered together.
2. **Flat collage pieces converging** — still read as debris. Abstract shapes without inherent meaning default to "broken."
3. **Five-piece jigsaw** — the model kept rendering it as a chunky 3D product (thick edges, bevelled surfaces) despite repeated instructions for flatness. The word "jigsaw" triggers a toy-shop mental model.
4. **Constellation forming** (dots and connecting lines) — worked as an illustration but felt too scientific/astronomical on the page. Wrong register.
5. **Mosaic tiles** — again rendered with 3D thickness. Same problem as the jigsaw.

**The decision:** Not every step needs an illustration. The strength of Step 2 is the reassurance in the words — "not a test you pass or fail" — and forcing a visual metaphor for questionnaires was always fighting the copy. The illustration was dropped in favour of a typographic moment.

**What was built:** The section now has three beats — opening copy at content width, then a centred italic serif statement ("Not a test you pass or fail.") at showcase width with a quieter subtitle beneath, then the closing paragraph back at content width. The statement breaks out of the body text rhythm and creates a genuine pause in the scroll. The key-fact callout was removed since the typographic moment replaces it more powerfully.

CSS classes: `.step2-reassurance`, `.step2-reassurance-line` (2.25rem Lora italic, teal-deep), `.step2-reassurance-sub` (body size, secondary colour). Mobile scales the headline to 1.625rem.

**Lesson:** Illustrations earn their place where they carry emotional weight the text can't (Step 1's door). Where the text *is* the emotional moment, the design should serve it typographically rather than compete with it visually.

### Phase 13: Step 2 — simplifying the reassurance

**The problem:** The three-beat structure from Phase 12 (body copy → centred italic breakout → closing paragraph) created a middle element that felt like a standalone decorative moment rather than part of the reading flow. The centred serif statement ("Not a test you pass or fail." / "Just a starting point for understanding your story.") duplicated the sentiment already carried by the final paragraph, and the section didn't need both.

**The decision:** Remove the standalone breakout entirely. Instead, bring attention to the final paragraph — which already contains the reassurance — by shifting its typographic register.

**Three options were considered:**
1. **Typographic shift** — Lora serif italic at 1.2rem in teal-deep, with generous top margin. Relies on the typeface change to signal a shift in register.
2. **Inset card** — white card with amber/pink left border on the teal-wash background. Risked feeling like UI rather than editorial.
3. **Narrowed focus** — 560px max-width, same as Step 5's intimate column. Would use the same trick twice.

**Option A (typographic shift) was chosen** as the simplest and most confident — the copy is strong enough that a typeface change and some space is all it needs.

**What was built:** The `.step2-reassurance` wrapper, `.step2-reassurance-line`, and `.step2-reassurance-sub` were all removed. The final paragraph gained a `.step2-closing` class: `font-family: var(--font-serif)`, `font-size: 1.2rem`, `font-style: italic`, `color: var(--teal-deep)`, `margin-top: 2.5rem`. A 3px amber left border with `padding-left: 1.5rem` was added to give the eye a vertical anchor — drawing attention to the paragraph without competing with it.

The section now has two beats instead of three: body copy (Inter, standard weight), then the reassurance (Lora italic, teal, amber accent line). Simpler, more direct, and the reassurance lands with more presence because it isn't pre-empted by a decorative restatement of the same idea.

### Phase 14: Step 1 & Step 3 — illustration-led refinement

Three connected changes that followed from the hand-drawn illustration style becoming the page's primary visual language.

**1. Step 1: key-fact callout removed.**

The "Within 24 hours — we'll be in touch after you sign up" callout box was removed from Step 1. With the door-ajar illustration now providing the visual interest for the section, the callout was redundant — competing for attention without adding information (the same detail is already in the body copy). The section is cleaner: copy on the left, illustration on the right, nothing else.

**2. Step 3: phone mockup replaced with hand-drawn illustration.**

The CSS phone mockup (dark bezel, notch, screen with four feature cards, tab bar dots) was the most technically elaborate visual element on the page, but it was also the coldest — a dark UI component sitting in the middle of an otherwise warm, editorial design. With the hand-drawn style established, it was the obvious candidate for replacement.

The phone mockup was removed entirely and replaced with a hand-holding-smartphone illustration in the same ink/pink style as the Step 1 door. The section was converted from the centred single-column `.step-showcase` layout to a two-column `.journey-section--illustrated-left` layout — illustration on the left, copy on the right — mirroring Step 1 but on the opposite side for visual alternation. On mobile, the illustration stacks above the copy.

An illustration prompt was written for the Gem (custom GPT illustrator) and added to `Illustrations/Illustration-prompts.md`. Key creative decisions in the prompt: the hand is relaxed (browsing, not urgently checking); the phone screen shows a wash of CareADHD pink rather than a rendered UI; optionally the faintest suggestion of card shapes on screen, removed if they compete with the pink warmth. The pink-screen-as-warmth mirrors the light-through-door concept from Step 1 — support is already here.

**3. Step 3: background changed from pink-wash to warm-white.**

The pink-wash background (`var(--pink-wash)`) was a legacy of the phone mockup era — the pink distinguished the app section as a "showcase" moment. With the illustration now carrying the visual weight, the pink background competed with the pink accent in the illustration and made the section feel heavy. Changed to `var(--warm-white)` to match the surrounding sections.

This required updating the SVG divider entering Step 3 (teal-wash → warm-white instead of teal-wash → pink-wash) and removing the divider exiting Step 3 entirely (both Step 3 and Step 4 are now warm-white, so no transition needed).

**4. Step 3: waiting well line restyled.**

The "waiting well" closing line was inside a `.waiting-well` div — a white card with amber left border and box shadow. This was a UI component where an editorial moment was needed. Changed to use the `.step2-closing` class (Lora serif italic, teal-deep, amber left border) — the same typographic treatment used for Step 2's closing reassurance. Consistent, lighter, and it reads as an emotional punctuation mark rather than a callout card.

**What this achieves:**

The page's visual language is now fully unified around the hand-drawn illustration style. Steps 1 and 3 both use two-column layouts with ink/pink illustrations alternating sides. The CSS phone mockup — the last "tech-y" element — is gone. Every visual moment on the page now feels warm, editorial, and human: illustrations, serif typography, amber accents, and breathing space.

### Phase 15: Sections 4 & 5 — background and typographic refinement

Two sections restyled in preparation for illustration integration.

**Section 4 (assessment):**

Three changes to shift this section from a neutral information block to something with more visual presence and emotional register:

1. **Background changed to pink-wash.** The section was previously warm-white (same as Steps 1, 3, and the surrounding context). Moving it to pink-wash gives it its own identity in the scroll rhythm and creates a better colour sequence: warm-white (Step 3) → pink-wash (Step 4) → warm-white (Step 5) → teal-wash (Step 6). New curved SVG dividers added above (warm-white → pink-wash) and the existing divider below updated (pink-wash → warm-white).

2. **Detail pills removed.** The three pills ("Virtual appointment", "60–90 minutes", "One-to-one") were introduced in Phase 8 as scannable badges. With the section moving toward an illustration-led layout, the pills competed for attention without adding information that isn't already in the opening paragraph. Cleaner without them.

3. **Paragraph 3 given emotional-beat treatment.** The "One thing worth knowing: many people with ADHD became very good at masking..." paragraph is the emotional core of this section. It now uses the `.emotional-beat` class — Lora serif italic at 1.375rem in teal-deep, with amber top and bottom borders — the same treatment previously used in Section 5. This creates a genuine pause in the reading flow at exactly the right moment.

**Section 5 (diagnosis):**

Three changes to prepare this section for a right-column illustration:

1. **Background changed from amber-wash to warm-white.** The amber-wash background was introduced when Step 5 had its own visual identity as the "intimate column" moment. With an illustration coming, the amber competed — and the colour sequence now reads better as pink-wash → warm-white → teal-wash.

2. **Intimate column removed.** The `journey-section--intimate` class (560px max-width) was removed, returning the section to the standard 720px content width. This prepares for a two-column illustrated layout where the copy sits left and the illustration sits right.

3. **Typographic treatments swapped.** The middle paragraph's `.emotional-beat` class was removed — the serif italic with amber borders felt too heavy for this section now that Step 4 uses the same treatment. The final paragraph ("What it does give you is a framework...") gained the `.step2-closing` class — Lora serif italic with amber left border — matching the closing treatment used in Steps 2 and 3. This is lighter and more consistent: every section that ends with a reassuring statement now uses the same typographic register.

**Divider updates:** Four dividers were updated to reflect the new background sequence: warm-white → pink-wash (new, before Step 4), pink-wash → warm-white (updated, after Step 4 into Step 5), warm-white → teal-wash (updated, after Step 5 into Step 6).

**What's next:** Section 5 is now ready for a two-column illustrated layout. The illustration subject (discussed in Phase 11) is a lens coming into focus or fog clearing — representing diagnosis and self-understanding. The layout will mirror Steps 1 and 3, with copy left and illustration right. Section 4 may also take an illustration (two chairs, two cups of tea) on the opposite side for alternation.

### Phase 17: Step 6 — treatment cards stripped, editorial restyle

**The problem:** Step 6's two treatment columns ("On medication" / "On psychological support") were inside white cards — `background: white`, `border-radius: 12px`, `box-shadow`, hover lift effect. These were the most "UI component" feeling elements left on the page. Every other section had moved toward open editorial typography, and the white boxes felt out of place.

**Three options were discussed:**

1. **Strip the cards, keep the columns** — remove white background, border, shadow, border-radius. Two columns of open text, distinguished only by their serif headings.
2. **Amber left border instead of cards** — 3px amber left border with padding, matching the `step2-closing` treatment used elsewhere. No background.
3. **Stack vertically** — drop the two-column grid entirely.

**Option 2 was tried first.** The amber borders were applied — but on reflection, they didn't work. The amber left border earns its place elsewhere (Steps 2 and 3) because it marks a single emotional beat — a short italic serif line. In Step 6, it ran alongside two full paragraphs of practical information, making them feel like pull quotes or callouts when they're really structured body text.

**Option 1 was chosen.** All card styling removed: white background, border, border-radius, box-shadow, hover effect, padding. The two-column grid stays (the parallel structure serves the copy), but the content sits openly on the teal-wash background.

**Additional changes:**
- **Key-fact callout removed.** The "Weeks 4 & 12" callout box below the treatment grid was removed. The same detail is already in the medication paragraph — the callout was redundant and competed with the now-cleaner layout.
- **Amber heading dots restored.** The `h3::before` pseudo-element (6px amber circle) was brought back on the treatment headings. These had been lost when the card styles were stripped. They give each column heading a small visual anchor without adding weight.
- **Mobile override removed.** The treatment-card padding override in the mobile breakpoint was no longer needed.

**What this achieves:** The section now feels consistent with the rest of the page — open, editorial, trusting the typography and structure to do the work. The two-column layout signals "two parallel tracks" without needing boxes to enforce it. The amber dots on the headings provide just enough visual interest to break up the text.

**Design process note:** This phase is a good example of Charlie's approach to subtraction. The instinct when something feels wrong isn't to add — it's to strip back and see what the content needs on its own terms. The first move was to identify what didn't belong (white cards), not to ask what could be added. When the replacement (amber borders) was tried and didn't earn its place, it was removed rather than justified. And when the result felt too bare, the response wasn't to add a new element — it was to restore a small detail (the amber dots) that had been lost in the process. The final state has *less* CSS than any intermediate version. That restraint — the willingness to try something, reject it honestly, and arrive at less rather than more — is the difference between decoration and design.

### Phase 16: Step 5 — mirror illustration integrated

Charlie provided a mirror illustration (`mirror-illustration.png`) — replacing the earlier concept of a lens or fog clearing. A mirror is a stronger metaphor for diagnosis: seeing yourself clearly, perhaps for the first time.

**What was done:**

1. **Image swap.** The placeholder horizon illustration (`horizon-illustration.png`) in Step 5's `.journey-illustration` div was replaced with `mirror-illustration.png`.

2. **Horizontal flip.** The mirror was facing away from the copy column. An inline `transform: scaleX(-1)` was added to the `<img>` element so the mirror faces left toward the copy — visually connecting the illustration to the text it accompanies. The flip is CSS-only; the source image is unchanged.

**Design process note:** The shift from "lens coming into focus" or "fog clearing" to a mirror is worth noting. The earlier concepts were about *clarity arriving* — something external changing so you can see better. A mirror reframes it: the clarity was always there, you just weren't looking at yourself with the right frame. That's a much closer match to what a diagnosis actually does. It doesn't reveal something new — it gives you a name for something you've always lived with.

This is the same instinct that drove Phase 17's subtraction — Charlie doesn't settle on the first metaphor that fits the brief, he keeps pressing until the metaphor fits the *feeling*. A lens is technically correct (diagnosis brings focus). A mirror is emotionally correct (diagnosis brings self-recognition). The difference is the gap between a page that explains the process and a page that understands the person going through it.

The CSS flip is a small detail but it follows the same logic. The illustration isn't decoration sitting next to the text — it's facing the text, oriented toward it, as if the mirror is being offered to the reader through the copy. Composition serves narrative even at the level of `scaleX(-1)`.

### Phase 18: Step 7 — window illustration, layout and typographic refinement

Charlie provided a window illustration (`window-illustration.png`) for Step 7. A window looking out onto an open landscape — the right metaphor for this section. The long-term plan isn't an ending; it's a view forward. The illustration says what the copy says: there's something beyond this process, and it's calm.

**What was done:**

1. **Illustration integrated, two-column layout.** Step 7 was converted from a plain single-column text section to `journey-section--illustrated-left` — illustration on the left, copy on the right. This mirrors Step 3's layout and alternates with Step 5 (illustration right), maintaining the visual rhythm established across the page.

2. **Watermark number removed.** The `journey-section--watermark` class and the `<span class="watermark-num">07</span>` element were removed. Steps 1 and 7 originally had large faded background numbers for visual depth, but Step 1's watermark was already removed when its illustration was added. With Step 7 now illustrated, the watermark served no purpose — the illustration provides the visual weight the watermark was compensating for.

3. **"At NHS cost" key-fact callout removed.** The `.key-fact` box at the bottom of the section was removed. The same information ("at NHS cost") is already in the body copy. The callout was a Phase 10 addition designed to give scanners something to land on in text-heavy sections — but with the illustration now providing the visual anchor, the callout was redundant and cluttered the bottom of the section.

4. **Opening paragraph restyled, then moved.** The opening line ("This is something people often wonder about but rarely ask...") was initially given the `.step2-closing` treatment (Lora serif italic, amber left border) to match the closing beats of Steps 2, 3, and 5. On reflection, Charlie moved the highlight to the *final* paragraph instead — "Most GPs are happy to enter into shared care arrangements... Either way, you won't be left without support." The closing reassurance carries more emotional weight and earns the typographic emphasis. The opening line reverted to standard body text.

**Design reflection:**

The decision to highlight the final paragraph rather than the first is worth noting because it reveals something about how the page's emotional logic has matured. Early in the build, the instinct was to lead with the hook — grab attention, front-load the interesting line. But by Phase 18, the pattern across the page is the opposite: every section builds toward its emotional moment, and the typographic emphasis lands at the *end*, not the beginning. Steps 2, 3, 5, and now 7 all close with an italic serif beat. The consistency isn't a template — it's a reading rhythm. The reader learns, subconsciously, that each section will end by meeting them where they are. "You won't be left without support" isn't just a line — it's the last thing the page says before the CTA. That's not an accident.

The window illustration completes the visual arc of the page. Step 1 opens with a door ajar (arrival, possibility). Step 7 closes with a window looking out (continuity, calm). Both are threshold images — liminal spaces between where you are and what comes next. The page begins and ends with the same visual grammar: light, openness, an invitation rather than a conclusion.

### Phase 19: Mobile illustration placement — from decoration to narrative punctuation

Charlie spotted that on mobile, the illustrations were appearing before the section headlines — the visual arrived before the reader had any context for it. The fix seemed straightforward (swap the order), but the conversation that followed revealed something more interesting about how illustrations should function on a single-column screen.

**Three iterations in quick succession:**

**1. Illustrations after copy (first fix).** The initial mobile layout used `order: -1` on illustrations, pushing them above the copy. Removing this put illustrations after the full section — headline, body copy, then illustration at the bottom. Structurally correct but editorially inert. The illustration became a footer rather than a moment.

**2. Headline, illustration, body copy (second fix).** Charlie's instinct: the headline should come first (context), then the illustration (visual breathing space), then the body copy. This required restructuring the HTML — splitting the single `.journey-copy` div into a `.journey-header` and `.journey-body`, then using CSS grid row assignments to interleave the illustration between them on mobile while preserving the two-column desktop layout.

**3. Illustration mid-copy (final version).** Charlie pushed further: could the illustration sit *between* paragraphs, at a natural narrative break point? This is editorially precise — the illustration becomes punctuation, not decoration. Each section's copy was split into `.journey-body-before` and `.journey-body-after` at the exact point where the writing pauses or shifts register:

- **Step 1:** After "...you're in the right place." → door → "Once you sign up..." (The door lands at the moment of arrival. The practical next-steps follow.)
- **Step 3:** After "...team of ADHD specialists." → phone → "The app includes CBT tools..." (The phone appears after you learn what the app is, before you learn what it does.)
- **Step 5:** After "...what it means for you." → mirror → "For many people, a diagnosis brings..." (The mirror sits at the threshold between receiving a diagnosis and processing it.)
- **Step 7:** After "...treatment period ends?" → window → "The answer is straightforward." (The question hangs, the window offers a view forward, then the answer arrives.)

On desktop, all three content divs stack in a single grid column (header row 1, body-before row 2, body-after row 3) with the illustration spanning all rows in the adjacent column — visually identical to before. On mobile, the grid reorders to four rows: header → body-before → illustration → body-after.

A spacing fix was needed: the `h2` margin-bottom (28px) was stacking on top of the grid gap (24px), creating a visible double-break between headline and first paragraph on mobile. Zeroed out the `h2` margin inside `.journey-header` at the mobile breakpoint so the grid gap alone controls spacing.

**Design reflection:**

This sequence of iterations is worth documenting because it shows Charlie's design instinct working in real time. The first fix (swap the order) was technically correct. The second fix (headline first) was structurally better. But the third fix (mid-copy placement) is the one that reveals the design thinking.

The key insight: on a single-column mobile screen, an illustration isn't a sidebar companion to the text — it's a *moment in the reading flow*. It has a before and an after. Where you place it changes what it means. The door after "you're in the right place" feels like the door is opening *for you*. The mirror after "what it means for you" feels like the diagnosis is being handed to you. The window after "what happens when treatment ends?" feels like you're being shown the answer before it's spoken.

This is the same editorial instinct that drove the copy structure from the beginning — every section builds toward something, and the visual language should follow the same rhythm. On desktop, the illustration sits alongside the text and the reader's eye can move between them freely. On mobile, the illustration is *in* the text, and its placement is a compositional choice with narrative consequences.

The willingness to restructure the HTML three times in one session — rather than settling on the first working solution — is characteristic of the approach throughout this project. The first version that works is rarely the version that's right. Working solutions are easy; the gap between working and *good* is where the design decisions live.

---

## 5. Files

```
/CareADHD/
├── CLAUDE.md                        ← Project brief and constraints
├── CareADHD_Journey_Page_Copy.md    ← Source copy (locked)
├── Build-log.md                     ← This file
├── index.html                       ← The deliverable
├── Illustrations/
│   ├── Door-ajar-illustration.png   ← Step 1 illustration (ink/pink, transparent bg)
│   ├── phone-illustration.png       ← Step 3 illustration (hand holding smartphone, ink/pink)
│   ├── mirror-illustration.png      ← Step 5 illustration (mirror, ink/pink, CSS-flipped)
│   ├── window-illustration.png      ← Step 7 illustration (window looking out, ink/pink)
│   ├── Constellation.png            ← Unused — Step 2 concept (felt too scientific)
│   └── Illustration-prompts.md      ← Gem instructions + per-illustration prompts
├── serve.rb                         ← Local dev server helper (can delete)
└── .claude/
    └── launch.json                  ← Dev server config (can delete)
```

---

## 6. Next Steps

### Immediate
- [x] Implement key-fact callouts in text-heavy sections
- [x] Implement curved SVG section dividers
- [x] Replace hero vignette with SVG curve
- [x] Restyle bridge as section header
- [x] Integrate Step 1 illustration (door ajar)
- [x] Remove journey thread (replaced by illustrations)
- [x] Replace Step 3 phone mockup with hand-drawn illustration
- [x] Restyle Step 3 background and waiting well line
- [x] Section 4 — pink-wash background, pills removed, emotional-beat on masking paragraph
- [x] Section 5 — warm-white background, intimate column removed, step2-closing on final paragraph
- [ ] Review visual balance — do the key facts feel editorial or do any feel forced?
- [x] Step 6 — strip treatment cards, restore amber heading dots, remove key-fact callout

### Soon — illustration integration
- [x] Integrate Step 5 illustration (mirror — diagnosis/self-understanding) as right-column, CSS-flipped to face copy
- [ ] Generate Step 4 illustration (two chairs/cups of tea — conversation) and integrate as left-column (alternating with Step 5)
- [ ] Decide per-step for Step 6 whether illustration earns its place (concept: key cut to fit / ingredients being chosen)
- [x] Step 7 — window illustration integrated, illustration-left layout, closing paragraph highlighted, key-fact and watermark removed
- [x] Mobile illustration placement — illustrations now sit mid-copy at narrative break points
- [x] Step 1 watermark "01" removed — illustration carries the visual weight

### Phase 20: Hero-to-bridge transition and rhythm divider

**The question:** The hero's curved SVG transition into the bridge section didn't match the consistent wave dividers used between all other sections. Should it?

**What was tried:**

1. **Bridge → Step 1 rhythm divider added.** A new `.section-divider` between the bridge and Step 1 — same SVG wave pattern as all other section boundaries. Since both sections are warm-white, this is purely a rhythmic/spacing element rather than a colour transition. Adds consistency to the vertical rhythm without any visual disruption.

2. **Hero curve softened on mobile.** The hero's `.hero-curve svg` height was reduced from 80px to 48px (matching section dividers) at the mobile breakpoint. On the narrow viewport, the original 80px curve was disproportionately dramatic. Desktop remains at 80px.

3. **Hero curve replaced with section divider (rejected).** Attempted replacing the hero's bespoke SVG curve entirely with a standard section divider. The gradient background of the hero didn't carry through to the divider — the teal band appeared as a visible stripe rather than a seamless continuation. Reverted immediately. The hero curve earns its distinct treatment because it's transitioning from a full gradient background, not a flat colour.

**What shipped:**
- Bridge → Step 1 rhythm divider (warm-white to warm-white, wave shape only)
- Hero curve reduced to 48px on mobile
- Step 1 watermark "01" removed

**Design note:** The hero transition is intentionally different from the between-section dividers, and that's correct. The hero is a full-bleed gradient with depth — it needs a curve that's part of its own composition, not a generic section break. The consistency lives in the *language* (organic curves throughout) rather than the *implementation* (identical dividers everywhere).

- [ ] Review with fresh eyes — does the visual variety hold up, or does anything feel forced?

### Before sending
- [ ] Decide whether to host on GitHub Pages or Netlify for the outreach email
- [ ] Write the outreach email itself
- [ ] Consider whether the page needs an Open Graph image for link previews
