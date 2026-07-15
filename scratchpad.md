# KONTAKT International — Redesign Working Notes

## Source
- `uploads/Presentation KI.pdf` — 22 pages. Verbatim text dump: `extracted/text.txt` (proofread against this).
- All raster assets extracted to `assets/pNN-MM.png` (NN = source page).

## Asset map (extracted, max available resolution)
- p01-01 — Kontakt "K" ribbon mark, transparent, 632×474 (also used as corner mark on every slide)
- p02-03 — mission icon, red mountain+flag, 249×249
- p03-02 Russia flag 226×143 · p03-03 Tajikistan flag 226×144 · p03-04 Saudi Arabia flag 388×260
- p04-02 Gazprom Neft 835×387 · p04-03 Rosneft 1270×888
- p05-02 — original donut raster 376×168 → REBUILT as live SVG (brief §3 `.donut`), values 63/37 preserved
- p06-02..07 — red generic icons (truck, check, bulldozer, NEW, ID card, excavator) → replaceable w/ custom SVG per brief §1
- p07-02 welder · p07-03 gas processing site · p07-04 truck fleet in snow · p07-05 high-voltage towers
- p08-02 — regional map w/ K pins, 423×398 ⚠ LOW RES (largest usable ~500px wide)
- p08-03/04/05 — original pipe-arrow graphics → superseded by `.pill-arrow` per brief §5.8 (not reused)
- p09-02..11, p10-02, p14-02..05, p16-02, p17-02, p18-02, p19-02, p20-02, p21-02 — red calendar-clock icons → replaced by custom SVG per brief §1
- p10-03 Kharampur aerial 1280×960
- p11-02..07 — six CBCS construction photos (800×600 … 1341×789)
- p13-02 HVPL photo 1457×1080
- p15-02..06 — arena / canteen / dining / dorm / bathroom
- p16-03/04 residential renders · p17-03/04 mall (797×371, 812×456 — medium) · p18-03/04 base renders
- p19-03/04 school · p20-03/04 kindergarten · p21-03/04 mosque
- p22-02/03/04 red contact icons → replaced w/ cyan SVG per brief §5.22 · p22-05 QR code 400×400

## Title sequence (verbatim from source — slide titles ARE the source headers)
01 KONTAKT International (cover) · 02 ABOUT COMPANY · 03 COMPANY`S ACTIVITIES · 04 COMPANY`S ACTIVITIES IN RUSSIA · 05 COMPANY RESOURCES · 06 TECHNICAL EQUIPMENT · 07 AREAS OF ACTIVITIES · 08 PIPELINE CONSTRUCTION · 09–11 CONSTRUCTION OF TECHNICAL FACILITIES · 12 CONSTRUCTION OF SITE FACILITIES · 13 CONSTRUCTION OF HVPL · 14–15 CONSTRUCTION OF INFRASTRUCTURAL FACILITIES · 16–18 CIVIL CONSTRUCTION · 19–21 SOCIAL INITIATIVE · 22 CONTACT INFORMATION

## System (checked against §2 avoid-list)
- Tokens: graphite #101519 / paper #F1F3F5 / cyan #00A0DF (lines only) / signal #EE1D23 (≤3%) / slate #6B7885 / white
- Rhythm: graphite = cover, ch.10, 11, 15, 22 · paper = data/text slides
- Type: Oswald 600/700 display · Archivo wght 800 wdth 125 numerals (tabular) · Inter body · IBM Plex Mono utility
- Scale @1920×1080: 96/64/40/28/20/16/12 · 96px margins · 24px gutter · 48px hairline grid sheet at 7–8%
- Signature 1: dimension callouts (ticks + hairline + mono label) on measured figures only
- Signature 2: shard wipe (skewX -12°, red then cyan +90ms) on slide transitions; cover mark assembles from 3 diagonal slices
- Radius 0 everywhere; 2px on photo frames. No outlined rectangles. Red = key numerals + status labels only.
- Anti-generic check: no gradients, no glass, no dark+neon, no decorative numbering (slide 2's 01–04 is the company's own ordering → kept as mono indices on a hairline). Engineering-sheet vocabulary throughout.

## Motion
Default DOM = final state (print/thumbnails/reduced-motion safe). JS applies enter animations per `data-a`
(+`data-ad` delay ms) on `slidechange`; counters via `data-count`; wipe overlay on nav; all gated by
`prefers-reduced-motion` and the `animations` tweak. FIG indices: s7:01–04 · s8 map:05 · s10:06 · s11:07–12 ·
s13:13 · s15:14–18 · s16:19–20 · s17:21–22 · s18:23–24 · s19:25–26 · s20:27–28 · s21:29–30.

## Status
- [x] Extraction + report
- [x] Vertical slice: slides 1, 5, 9, 11
- [x] Remaining 18 slides — all 22 in source order
- [x] Icons: slide 2/6 reuse extracted originals (bulldozer+NEW composited); slide 9 durations in mono (no icon needed); slide 22 custom cyan stroke SVGs (pin/phone/mail)
- [ ] Self-critique + verbatim proofread pass + print QA (verifier round)
