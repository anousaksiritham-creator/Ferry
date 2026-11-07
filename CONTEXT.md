# Ferry Project – Context State (saved 2026-11-07)

Handoff note so any session can resume this work. Main deliverable: `ferry_report.html`.

## Project
- Dansavanh (DSV) contributes funds to the port to build a **new ferry** (hull + engine).
- Report purpose: conclusion → analysis → plan, for management. Three languages: **Lao (ລາວ) / English / 中文**, switchable in one HTML file.
- Branded to Dansavanh: logo, deep green `#006a3c`, lime `#6aa72b`, sky blue `#00a0e3`, Montserrat + Noto Sans Lao/SC.

## The 3 conditions (structure of the report)
1. **Budget** proposed by the port, accepted by DSV: **500,000 baht** for hull + engine (breakdown hull/engine = TBC from the port).
2. **Right of passage for DSV** (maximum benefit): priority boarding, free/discounted fare, long fixed term, schedule, recognition, safety/maintenance/insurance, breach & refund, ownership/lien. Marked MUST / SHOULD / NICE.
3. **Disbursement in 3 installments**, each released only after the previous stage is checked and approved:
   - 30% = 150,000 – contract, steel delivered, keel laid
   - 40% = 200,000 – hull complete and inspected (independent surveyor)
   - 30% = 150,000 – engine installed, sea trial, handover
   - Optional ~10% retention of installment 3 until a 12-month warranty ends.

## Passage-value calculator (defaults set by the user)
- Shuttle trips per day: **4** (to confirm; the full timetable has 14) + **2** executive cars
- Price: **30,000 LAK per car per trip** (currency to confirm), rate **683 LAK per 1 baht**, 365 days/year
- Contract period: **5 years**; DSV contribution: 500,000 baht
- Result: 96,193 baht/year → 480,966 over 5 years = **96%** of the contribution → payback **5.2 years** → suggest a contract of at least 6 years.
- Sensitivity: at 14 trips/day payback is about 2 years.

## Features in `ferry_report.html` (current design, 2026-11-07)
Formal report layout (A4-width paper, numbered clauses 1.3, 2.1.1, 3.2.1…), Dansavanh logo, three languages.
- **Cover, 2 steps:** opens on a dark screen (dot → ring → Dansavanh mark). Scroll once → logo + report title. Scroll again → the document. Arrow/Space keys and swipe also work; scrolling up inside the document does not return to the cover. Printed PDF starts with a cover page.
- **Executive summary** table with key figures (blur-in on reveal).
- **Section dividers** 01–04 as full-width colour bands (green, blue, lime, black) with large numerals.
- **Section 2.2** editable calculator (inputs a–h, formula, results, verdict) and payback chart with a draggable contract-years marker.
- **Section 2.3** "race" figure: dots run to 100% recovery for 4/8/14 trips/day, speed proportional to years; plus the sensitivity table.
- **Section 3.1** gates figure: one dot passes 3 inspection gates (150k → 350k → 500k), plus the expandable installment table.
- Sections 4 (risks, next steps), 5 (approval signature blocks), Annexes A (shuttle timetable + image), B (assumptions), C (items to agree with the port).
- Motion style: short, one-time, Ant Motion timings (150/300/450/600 ms); kinetic typography inspired by a reference motion reel. Static in print and for reduced-motion users.
- **Phone layout:** page fits the screen (wide tables scroll inside their own box with an edge shadow; the installment Progress column is hidden on phones), cover sized with 100dvh and safe areas, "SWIPE UP ↑" hint on touch screens, figures 1–3 redrawn for narrow screens (redrawn on rotate), shorter motion and no blur on phones, 40 px tap targets, and a "≡ Sections" drop-down menu.
- Fonts from Google Fonts: Noto Sans/Lao/SC, Archivo Black, Instrument Serif (italic), IBM Plex Mono.

## Deployment
- GitHub Pages via `.github/workflows/static.yml` (deploys the whole repo on every push to `main`).
- `index.html` is a copy of `ferry_report.html` so the site root opens the report. Keep both in sync.

## Open items / TBC
- Trip data confirmed by the user: 4 trips/day + 2 executive cars, 30,000 LAK per car per trip, 683 LAK per baht, 5-year contract.
- Hull vs engine split of the 500,000 baht (from the port).
- Discount percentage, passage term in years, warranty length (12 months placeholder), 30-day delay limit.
- The user's two WhatsApp voice notes (`.ogg`, 2026-11-06) could not be transcribed (no speech model available offline), so their content is not reflected. Please re-send as text.
- The sentence "The priority of the crossing is divided into…" was cut off in the user's message.
- Ferry assumed to be a vehicle ferry with ramp (not confirmed).

## Working preferences of the user
- Discuss-first workflow: no files, edits or fixes until the user types **"Sarng"** (ສ້າງ); "Sarng" + an item means do only that item.
- Consultant; prefers Lao/English/Chinese deliverables for management.

## Files
- `ferry_report.html` – the report (logo, mark and timetable embedded)
- `index.html` – same file, site root for GitHub Pages
- `assets/dansavanh-logo.png` – logo supplied by the user
- `assets/shuttle-schedule.jpg` – Dansavanh shuttle van timetable (source for the trip counts)
- `CONTEXT.md` – this file

## Not used
- `lemomo-ai/lemo-opuscar` (film-making toolbox, MP4 output) was reviewed but not used.
- `ant-design/ant-motion`: only its timing/easing spec was applied, no library code.
