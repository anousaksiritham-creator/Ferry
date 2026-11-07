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

## Features in `ferry_report.html`
Animated hero (waves + ferry), live crossing view linked to the trips slider, draggable payback chart (drag the marker to change contract years), sensitivity chart, build-stage timeline with clickable installments and Play, scroll reveals and count-ups, language fade. Reduced-motion and print are static. Single file, no build step.

## Open items / TBC
- Currency of the 30,000 price (LAK vs baht) and whether 4 trips/day is the right count.
- Hull vs engine split of the 500,000 baht (from the port).
- Discount percentage, passage term in years, warranty length (12 months placeholder), 30-day delay limit.
- The user's two WhatsApp voice notes (`.ogg`, 2026-11-06) could not be transcribed (no speech model available offline), so their content is not reflected. Please re-send as text.
- The sentence "The priority of the crossing is divided into…" was cut off in the user's message.
- Ferry assumed to be a vehicle ferry with ramp (not confirmed).

## Working preferences of the user
- Discuss-first workflow: no files, edits or fixes until the user types **"Sarng"** (ສ້າງ); "Sarng" + an item means do only that item.
- Consultant; prefers Lao/English/Chinese deliverables for management.

## Files
- `ferry_report.html` – the report (logo embedded)
- `assets/dansavanh-logo.png` – logo supplied by the user
- `assets/shuttle-schedule.jpg` – Dansavanh shuttle van timetable (source for the trip counts)
- `CONTEXT.md` – this file

## Not used
- `lemomo-ai/lemo-opuscar` (film-making toolbox, MP4 output) was reviewed but not used; it needs ffmpeg 7+ and is tuned for Opus 5.5.
