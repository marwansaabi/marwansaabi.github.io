# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Recruiters and hiring managers evaluating Marwan for data science / machine learning internships (2026-27), plus technical reviewers who click through from the site into the live Streamlit apps and GitHub repos to verify the work firsthand. Secondary: contacts open to bioinformatics, forecasting, or health-data collaborations.

## Product Purpose

A personal portfolio that gets Marwan a data science internship by proving, not just claiming, that he can build and ship working machine learning systems end to end. Success is a recruiter reading a project card, clicking through to a live app or repo, and coming away convinced the work is real and rigorous.

## Positioning

Two combined, user-confirmed differentiators:

1. He ships full working systems, not just notebooks or research writeups. Every project links to a live, deployed app and its code, not a static write-up. (Evidence: the site's own history shows a deliberate pivot away from a narrow "Bioinformatician" framing toward "builds machine learning systems end to end... and ships them as working applications.")
2. A hybrid profile: biology/bioinformatics training combined with ML engineering, applied with the same methodological rigor (backtesting, cross-validation, honest baselines) across domains a typical candidate would specialize narrowly in (retail, dermatology/CV, drug discovery, genomics).

## Operating Context

- MSc Bioinformatics Applied to Health Sciences student at the University of A Coruña (UDC), program MUBICS; BSc Biology (Biotechnology) from University of Vigo.
- Based in A Coruña, Spain. Trilingual: English, Spanish, Galician.
- Site is a single static page deployed on GitHub Pages (`marwansaabi.github.io`, push to `main` auto-deploys).
- Each project's "live app" is a Streamlit Community Cloud deployment; "code" links to its own GitHub repo.
- The downloadable CV is a separate PDF file (`Marwan_El_Saabi_CV.pdf`) kept in sync with the site, not generated from it.

## Capabilities and Constraints

- Plain static HTML/CSS/JS, one `index.html`, no framework, no build step, no package manager. Preview images are committed files referenced by relative path.
- No CMS, no backend, no forms; the "contact" surface is mailto/LinkedIn/GitHub/CV-download links only.
- Must remain deployable as-is via GitHub Pages (no build pipeline to introduce without a reason).

## Brand Commitments

- Name on the site: "Marwan El Saabi" (logo/nav); full legal name "Marwan El Saabi González" in the footer copyright line.
- The MSc degree name must match the official UDC translation exactly: "MSc in Bioinformatics Applied to Health Sciences" (official Spanish name: "Máster Universitario en Bioinformática aplicada a las Ciencias de la Salud," MUBICS UDC). Do not rephrase it for style.
- Any job title or role shown anywhere must match LinkedIn's wording exactly (already corrected once: "Delivery Driver," not an invented title like "Last Mile Logistics Specialist").
- The part-time delivery driver role stays on the CV only. It is deliberately excluded from the web portfolio, which stays scoped to the technical/data-science profile.

## Evidence on Hand

- Project metrics shown on cards are real results from Marwan's own work and must never be invented, rounded misleadingly, or replaced with placeholder numbers: e.g. Retail Demand Forecasting (wMAPE 55.8%, +4.8% vs. best baseline), Melanoma Detection (0.735 mean IoU, 90.2% accuracy, 84% sensitivity, ISIC 2018).
- Project preview images are real captures, not decoration: a live screenshot of each Streamlit app (retail, drug designer, RNA-seq dashboard) or a real methodology figure pulled from the project's own repo (the melanoma segmentation figure, from `figures/segmentation_example.png` in that repo). Treat them as evidence, not stock imagery, when replacing or regenerating them.
- No testimonials, employer references, press mentions, or third-party endorsements exist. Future work must not fabricate any.
- CV (`Marwan_El_Saabi_CV.pdf`) is the authoritative, up-to-date resume; the site's claims should stay consistent with it.

## Product Principles

1. Every claim must be independently verifiable: a live app and/or a code link sits behind each project, and preview images are real captures, never illustrations standing in for a result.
2. Shipped, working systems outrank polished narrative. Breadth across unrelated domains, held to the same rigor, is the point, not a distraction to be narrowed away.
3. The site and the CV must stay factually consistent with each other and with LinkedIn: same titles, same dates, same degree name.
4. The portfolio's scope is deliberately professional/technical; non-technical work history has its place on the CV, not here.
5. Prefer honest limitations over inflated claims (e.g. the melanoma project states its dataset size and methodology caveats rather than overselling accuracy).
