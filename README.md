# LCSP Reporting Companion

An interactive learning tool for radiologists reporting on the NHS Lung Cancer Screening Programme. Built from the 2025 Standard Protocol and QA Standards.

Five working parts:
- **Nodules** — step-by-step decision tree for Table 4 management (baseline + incident rounds)
- **Incidental findings** — every finding from Annex 2 Table 1, searchable and filterable, with Annex 3 pathways
- **Flashcards** — 77 cards across 6 decks. Tap to flip, shuffle, mark-as-known (persists in browser), keyboard nav on desktop
- **Quiz** — 25 clinical scenarios with immediate feedback
- **Reference** — quick-lookup for size thresholds, VDT bands, scan windows, Brock/Herder, CT minimums

## Flashcard decks

- **Baseline nodules** (11 cards) — every solid-nodule size band, volumetric and diameter
- **Incident round** (8) — known stable, growth, new nodule thresholds
- **Sub-solid** (7) — GGN and PSN pathways, stability definitions, change triggers
- **VDT & risk** (7) — VDT bands, Brock, Herder, calculation rules
- **Incidentals** (25) — every finding from Table 1 plus the core reporting principles
- **Key numbers** (19) — timing windows, dose, slice thickness, scanner spec, exclusions, urgent-symptom triggers

The "✓ Known" filter shows only the cards you've marked as learned. Reset anytime.

## Run locally

Open `index.html` in any browser. No build step, no dependencies beyond Google Fonts (loaded from CDN).

## Host on GitHub Pages

1. Create a new GitHub repo (public or private — Pages works on both).
2. Upload `index.html` to the root of the repo.
3. In the repo: **Settings → Pages**.
4. Under **Source**, choose **Deploy from a branch**.
5. Select your branch (usually `main`) and folder `/ (root)`. Save.
6. Wait ~1 minute. Your site will be at `https://<your-username>.github.io/<repo-name>/`.

That URL works on any phone or laptop browser. Bookmark it.

## Keyboard shortcuts (Flashcards tab)

- **Space** — flip the current card
- **←** — previous card
- **→** — next card

## Data persistence

Flashcard "known" marks are stored in your browser's localStorage. This means:
- Marks persist across sessions on the same device/browser
- Clearing browser data will reset them
- Marks don't sync between devices (each device tracks separately)

## Updating content

Everything is in the single `index.html` file. The data arrays are clearly commented:
- `NODULE_NODES` and `OUTCOMES` — the decision tree
- `FINDINGS` — the incidental-findings table
- `FLASHCARDS` — the flashcard deck (each card has `id`, `deck`, `q`, `a`, `source`)
- `QUIZ` — the scenarios

Edit the HTML, push to GitHub, Pages redeploys in under a minute.

## Caveats

This is a learning aid, not a clinical decision system. Use it alongside — not instead of — the source NHS England documents, your Screening Review Meeting, and your Responsible Radiologist. If you find anything that doesn't match the source documents, fix it in the data arrays.

## Sources

- *Targeted Screening for Lung Cancer with Low Radiation Dose Computed Tomography: Standard Protocol* (NHS England B1646, February 2025)
- *Quality Assurance Standards prepared for the Lung Cancer Screening Programme* (NHS England B1647, February 2025)# LCSLearningApp
