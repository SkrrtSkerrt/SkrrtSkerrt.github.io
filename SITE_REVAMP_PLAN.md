# Site Revamp Plan

STATUS: planning only

## Goal
Make the site feel like it is assembled from scrap metal: welded plates, bolted frames, exposed brackets, rivets, scuffed panels, and improvised structure.

Keep these intact:
- current color theme
- hero treatment
- 4 featured projects on the homepage
- separate full project archive page
- the scrappy-metal image re-theme already shipped

Do not bring back clutter. Do not add decorative noise before the layout reads clean.

## Current context
- Repo: `/home/linuxbox/SkrrtSkerrt.github.io`
- Phase 1 is done: homepage decluttered, full inventory moved to `projects.html`
- Phase 2 is done: project media already uses the scrappy-metal re-theme
- Next visual work is structural: make the whole site feel fabricated from scrap
- Raccoon stays last and optional

## Visual direction
Use a layered industrial language, not a full redesign.

Required look:
- steel plates with uneven edges
- bolted corners and rivet runs
- bracketed frames around key blocks
- seam lines between sections
- scratched / scorched surfaces
- dark steel accents against the existing warm palette
- repair-weld detail, not polished chrome
- improvised, assembled, tinker-built feeling

Avoid:
- heavy grunge that hurts readability
- too many competing textures
- game UI clutter
- bright cyberpunk glow everywhere
- anything that fights the existing hero or typography

## Proposed approach
Build the scrap-metal look in layers:
1. page shell accents
2. section framing
3. card/frame treatment
4. micro-details and motion
5. optional mascot last

Keep each layer subtle enough that the page still reads fast.

## Phase 1 — page shell accents
Goal: make the site frame feel fabricated.

Add visual structure around the whole page:
- top nav as a metal strip or control rail
- section separators that look like bolted seams
- subtle corner brackets on major panels
- background texture that suggests brushed steel, not dirt
- occasional panel cutlines behind hero and content blocks

Checklist:
- [x] Define the shell accents in CSS only first
- [x] Add one reusable seam/bracket style for both pages
- [x] Keep the nav readable and low-clutter
- [x] Test the shell against the existing warm palette
- [x] Verify the page still feels fast and open on mobile

Likely touch points:
- `index.html` CSS
- `projects.html` CSS

Implementation shape:
- use pseudo-elements first, not new images
- prefer simple CSS gradients, borders, and corner cuts
- keep the existing palette and typography

## Phase 2 — hero framing
Goal: make the hero feel like a central machine bay, not just a card on a page.

Possible additions:
- metal frame around the portrait block
- small bracket or plate tabs at portrait corners
- subtle seam/bolt detail near the title
- industrial base plate under the hero copy
- light wear/scrape treatment at the edges only

Constraints:
- hero itself stays intact
- no extra text
- no motion that hurts the clean title treatment

Checklist:
- [x] Frame the portrait with a metal edge or bracket treatment
- [x] Add one subtle industrial base element under the hero copy
- [x] Keep the title readable at all viewport sizes
- [x] Avoid adding any new copy or badges
- [x] Verify the hero still feels balanced, not heavy

Likely touch points:
- `index.html` hero markup/CSS only if the frame needs a new wrapper

## Phase 3 — project cards as scrap-built modules
Goal: make each project card feel like a mounted metal module.

Add consistent card detailing:
- steel plate border with uneven highlights
- rivets or bolt heads at corners
- small label-strip / serial-tag treatment
- side bracket or riveted tab edge
- stronger distinction between featured cards and archive cards

Keep the current image treatment, but let the card shell do more of the work.

Checklist:
- [x] Add a stronger metal frame around each card
- [x] Give featured and archive cards a consistent shell language
- [x] Use small tag or serial details instead of extra decoration
- [x] Keep image treatment secondary to the card structure
- [x] Check that fallback cards still match the themed cards

Likely touch points:
- `index.html` project card CSS
- `projects.html` project card CSS

## Phase 4 — section-specific industrial accents
Goal: give each major section a distinct fabricated character without adding clutter.

Section ideas:
- `Current projects` as a bolted maintenance bay
- `Operating posture` as a control panel / loadout slab
- `Contact` as a terminal panel or service hatch
- archive page as a warehouse rack / parts wall

Use these as style cues only, not literal illustrations.

Checklist:
- [x] Assign one structural identity to each major section
- [x] Keep section accents subtle and readable
- [x] Reuse the same industrial vocabulary across both pages
- [x] Avoid adding separate artwork for every section
- [x] Confirm the archive page still feels like a warehouse, not a collage

Likely touch points:
- `index.html` section CSS
- `projects.html` header and container CSS

## Phase 5 — micro-details and motion
Goal: add life without turning the site into a noisy animation demo.

Safe accents:
- tiny idle glows on bolts or indicators
- slow shimmer on metal edges
- brief hover lift on cards
- subtle “weld heat” or “power-on” flicker on a few elements
- optional light parallax only if it stays cheap and motion-safe

Rules:
- motion must be subtle
- reduced-motion must stay clean
- no constant motion on every surface

Checklist:
- [x] Add only a few motion points, not everywhere
- [x] Keep hover effects light and short
- [x] Make sure reduced-motion disables the flourish cleanly
- [x] Test that motion does not harm readability or scanning speed
- [x] Stop if the site starts to feel busy instead of built

## Phase 6 — mascot last, optional
Goal: decide whether the raccoon deserves a place after the structure is solved.

If used, keep it:
- tiny
- sparse
- motion-safe
- decorative only
- separate from primary navigation and content

Good placement candidates:
- near a corner bracket
- on a small shelf / pipe / beam
- as a one-off wandering accent, not a recurring UI element

Do not add this until the site already looks right without it.

Checklist:
- [x] Confirm the page works without the mascot first
- [x] If added, keep it tiny and non-essential
- [x] Place it where it feels mounted into the structure
- [x] Avoid turning it into a repeated motif
- [x] Drop it entirely if it starts competing with the layout

## Files likely to change
Primary:
- `/home/linuxbox/SkrrtSkerrt.github.io/index.html`
- `/home/linuxbox/SkrrtSkerrt.github.io/projects.html`

Possible support files if the visual system needs reusable assets:
- `/home/linuxbox/SkrrtSkerrt.github.io/assets/`

Prefer CSS-first changes. Only add new assets if a texture or bracket detail cannot be done cleanly in CSS.

## Verification
Local:
- open `index.html` in preview
- open `projects.html` in preview
- check the pages still read fast on mobile width
- confirm the scrap-metal accents support the layout instead of hiding it
- confirm reduced-motion still looks clean

Published:
- verify GitHub Pages with cache-busted URLs
- confirm the homepage still shows only 4 featured projects
- confirm the archive page still shows the full inventory
- confirm there are no broken image states or layout jumps

## Risks
- Too much texture will make the page look busy
- Decorative metal can easily fight the warm palette
- Extra visual elements can reduce scanning speed on mobile
- Mascot art can become a distraction if added too early

## Open questions
- Should the scrap-metal look stay CSS-only, or should one reusable SVG/PNG motif be introduced?
- Should the industrial accents be mostly structural edges, or should sections get more explicit “panel” framing?
- If the raccoon happens, should it be static, hover-based, or lightly animated?

## Suggested order
1. Frame the page shell with metal accents.
2. Add hero framing.
3. Strengthen the project card shells.
4. Add section-specific industrial details.
5. Verify mobile and reduced-motion.
6. Decide on the raccoon last.

## Rocket-raccoon welding motif plan
Goal: add a tiny animated rocket-raccoon that feels like it is welding the site together as you scroll, without turning the pages into mascot wallpaper.

Rules:
- keep the motif small and sparse
- reuse one asset across both pages
- keep it decorative only
- keep motion subtle and reduced-motion safe
- stop if it competes with titles, cards, or CTAs

## Phase 7 — define the rocket-raccoon asset
Goal: create one reusable visual that can be placed in multiple spots.

Checklist:
- [x] Decide SVG vs inline CSS shape vs PNG fallback
- [x] Draw the raccoon as a tiny welded rocket shell with ember accents
- [x] Keep the silhouette readable at small size
- [x] Make sure the art can be flipped or rotated for variation
- [x] Confirm the asset stays legible in grayscale/low contrast

Likely touch points:
- `index.html` if embedded inline
- `projects.html` if embedded inline
- `assets/` if a reusable image is added

Status:
- Phase 7 asset created at `assets/rocket-raccoon-seq/frame-1.png` through `frame-5.png`.

## Phase 8 — place the motif through the page
Goal: make the raccoon appear in a few deliberate spots instead of everywhere.

Checklist:
- [x] Add one hero-adjacent cameo on the homepage
- [x] Add one section-seam appearance on the homepage
- [x] Add one archive-page cameo near a lower section or footer
- [x] Keep the total appearances low enough to avoid clutter
- [x] Reuse the same asset with small transform differences only

Likely touch points:
- `index.html` hero, section, or footer markup/CSS
- `projects.html` section or footer markup/CSS

Status:
- Phase 8 placement is live in `index.html` and `projects.html`.

## Phase 9 — add the welding animation
Goal: make the motif feel alive without constant motion.

Checklist:
- [x] Add a slow idle bob for the rocket-raccoon
- [x] Add a brief weld-spark or torch flicker loop
- [x] Add tiny exhaust shimmer only if it stays subtle
- [x] Keep animation cheap and low-frequency
- [x] Avoid motion on every instance at once

Likely touch points:
- `index.html` CSS and possibly small JS reveal hooks
- `projects.html` CSS and possibly small JS reveal hooks

Status:
- Phase 9 motion is live and stays small.

## Phase 10 — make it reveal cleanly on scroll
Goal: let the motif appear as the user moves through the page.

Checklist:
- [x] Trigger the appearance by section visibility or a simple reveal class
- [x] Stagger the entrances so it feels intentional
- [x] Prevent overlap with text or CTA buttons at all viewport sizes
- [x] Keep the archive page quieter than the homepage if needed
- [x] Ensure reduced-motion shows the motif statically

Likely touch points:
- `index.html` scroll handling if needed
- `projects.html` scroll handling if needed

Status:
- Phase 10 reveal hooks are live with reduced-motion fallback.

## Phase 11 — final polish and verification
Goal: prove the motif is decorative, readable, and safe.

Checklist:
- [x] Check desktop placement for subtlety
- [x] Check mobile stacking and spacing
- [x] Verify reduced-motion disables all animation cleanly
- [x] Verify the homepage still reads fast and clean
- [x] Verify the archive page still feels quieter than the homepage
- [x] Publish only after local preview and cache-busted GitHub Pages verification