# Hex Nursing: Honeycomb Geometry Applied to Hospital Nursing Station Design

**Article title:**  
*Applying Honeycomb Geometry to Nursing Station Design in Mexican Hospitals: A Quantitative Biomimetic Analysis with Adjusted Wall-Sharing Accounting*

**Authors:** Juan Ramón Lara Mora · Diana Paola Ayala Roldán · Luis Mallo Álvarez  
**Target journal:** HERD: Health Environments Research & Design Journal  
**Fallback:** Journal of Healthcare Engineering / Frontiers in Built Environment

---

## Repository structure

```
HexNursing/
├── latex_article/
│   ├── main.tex             ← Full LaTeX manuscript
│   ├── references.bib       ← BibTeX bibliography (25 entries)
│   └── figures/             ← Auto-populated by the notebook
├── analysis/
│   ├── hex_nursing_analysis.ipynb   ← All analyses and figures
│   └── figures/             ← Figure outputs (PDF + PNG)
├── README.md
├── SUBMISSION_NOTES.md
└── .gitignore
```

---

## Key results

| Metric | Square | Hexagonal |
|--------|--------|-----------|
| Side length (m) | 3.339 | 2.071 |
| Perimeter / module (m) | 13.356 | 12.429 |
| **Unadjusted total perimeter, 20 modules (m)** | **267.1** | **248.6** |
| **Unadjusted saving** | — | **6.94 %** |
| Walls removed (floor plan) | 39 | 46 |
| **Adjusted total perimeter (m)** | **136.9** | **153.3** |
| **Adjusted difference** | — | **+12.0 % (hex needs MORE)** |
| Unadjusted cost (MXN) | 494 172 | 459 873 |
| Adjusted cost (MXN) | 253 265 | 283 605 |
| Crossing points / route | 2–3 | 4–6 |

> **Key insight:** The theoretical 6.94 % perimeter advantage is a geometric identity
> (honeycomb conjecture), but it reverses after floor-plan-specific wall-sharing
> and circulation-passage accounting. The practical case for hexagonal nursing
> stations rests on circulation topology (more route options), not material savings.

---

## Mockup data flags

| Notebook section | MOCKUP flag | What to replace |
|------------------|-------------|-----------------|
| §8 Expert survey | `MOCKUP = True` | 5 real participant ratings (Q1–Q3, 1–5 Likert) |

---

## How to run the notebook

```bash
cd analysis
pip install numpy matplotlib pandas jupyter
jupyter notebook hex_nursing_analysis.ipynb
```

Figures are saved to `analysis/figures/` and `latex_article/figures/` automatically.

---

## How to compile the article

Upload the entire `latex_article/` folder to Overleaf, or compile locally:

```bash
cd latex_article
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

Requires: `lmodern`, `siunitx`, `booktabs`, `tabularx`, `natbib`, `authblk`, `mdframed`.

---

## License

Code: MIT.  Manuscript: All rights reserved (pre-publication).
