# Molina DSNP Stars Partnership Dashboard

## What this is
A single-page HTML dashboard built for the Pyx Health account team managing the Molina DSNP Stars partnership. It lives at **rswan-code.github.io/molina-stars-partnership** and is deployed via GitHub Pages from the `main` branch of `rswan-code/molina-stars-partnership`.

The dashboard is **client-facing and internal** — used in QBRs, account reviews, and internal tracking. It does not require a backend or build step. Everything is one file: `index.html`.

---

## File structure
```
index.html    — the entire dashboard (HTML + CSS + JS, all inline)
CLAUDE.md     — this file
```

---

## How the dashboard is organized

### Tabs
The nav bar has two tabs:
1. **Partnership Overview** — the client-facing value story (engagement metrics, Stars baselines, value model, Molina goals)
2. **Account Operations** — internal team view (timeline, tasks, contacts, document links)

### Data section (bottom of index.html)
All numbers live in a JavaScript `DATA` object starting around line 1515. **This is the only section that needs regular updates.** It includes:

- `markets[]` — 4 markets (OH, TX, UT, WA) with enrollment and Stars scores
- `metrics{}` — enrollment, engagement, call minutes, activation outcomes
- `outcomes[]` — value cards (PCP connections, SDOH resolutions, AWV attestations, etc.)
- `goals[]` — Molina's 4 stated priorities with live metrics

**Update cadence:** Monthly, pulling from Pyx Tableau dashboards. Fields marked with `// pull from Tableau` or `// update from Tableau` in comments are the ones to refresh.

---

## Contract context
- **SOW:** #604123v7
- **PO:** 639366
- **Program end:** 11/6/2028
- **Markets:** OH, TX, UT, WA (DSNP)
- **Total eligible members:** 53,749 across 4 markets
- **Enrollment as of last update:** 365 members

---

## Stars baseline (2026 CMS ratings)
| Market | Overall | State Avg |
|--------|---------|-----------|
| OH     | 3.0★    | 3.6       |
| TX     | 3.5★    | 4.0       |
| UT     | 3.0★    | 3.9       |
| WA     | 3.0★    | 3.6       |

Weakest domains: Member Experience (WA: 1★, UT: 2★) and Staying Healthy / Screenings (OH: 2★, WA: 2★) — these are the two domains Pyx activates most directly.

---

## Deploying changes
Push to `main` — GitHub Pages auto-deploys. No build step needed.

```bash
git add index.html
git commit -m "Update [month] metrics"
git push
```

Pages takes ~60 seconds to reflect changes.

---

## Brand
Pyx Health brand guidelines are in `/Users/rachaelswan/CLAUDE.md` (checked into the root of the user's machine, not this repo). Key values:
- Green: `#49a601` | Slate: `#2e4456` | Teal: `#29a4a2`
- Headlines: Roboto Slab | Body: Montserrat
- Tone: action-oriented, data-driven, warm — never cold or bureaucratic

---

## Owner
Rachael Swan — rachael.swan@pyxhealth.com
