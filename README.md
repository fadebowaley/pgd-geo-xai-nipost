# pgd-geo-xai-nipost

**Leveraging Explainable AI for Transparent Geolocation Services: A Case Study on Nigeria's Digital Postal Infrastructure**

## Short description

This repository contains materials, code, datasets and documentation for a PGD research project that (1) surveys global and national practice for AI in postal geolocation, (2) proposes an explainability-by-design framework for NIPOST geolocation services, and (3) implements a lightweight GeoXAI prototype (address-matching/geocoding) and evaluation.

## Project goals

* Produce a comparative literature & case-study report on postal AI and GeoXAI.
* Design a practical XAI governance + technical framework for postal geolocation.
* Implement a reproducible GeoXAI prototype with maps, SHAP-based explanations, and a mixed-method user evaluation.

## Specific objectives

1. **Landscape & comparative lessons** — systematic lit review and case studies; deliver a 20–30 page comparative report.
2. **Explainability-by-design framework** — decision matrices, model guidance, data governance, and UI wireframes for explanations.
3. **Prototype & evaluation** — code, interactive demo, user study report, and adoption thresholds.

## Repo structure (suggested)

```
/data                 # raw and processed datasets (do NOT store private PII here)
/notebooks            # exploratory notebooks and reproducible analyses
/src                  # production-ready scripts and modules
/results              # figures, maps, evaluation tables
/docs                 # reports, framework documents, wireframes
/tests                # test suites
/.github              # issue templates, workflows
README.md
LICENSE
requirements.txt
```

## Getting started (developer)

1. Clone repo

```bash
git clone https://github.com/fadebowaley/pgd-geo-xai-nipost.git
cd pgd-geo-xai-nipost
```

2. Create Python env and install

```bash
python -m venv .venv
source .venv/bin/activate    # or .venv\Scripts\activate on Windows
pip install -r requirements.txt
```

3. Jupyter notebooks

```bash
pip install jupyterlab
jupyter lab
```

## Data sources (starter)

* OpenStreetMap / Nominatim (Nigeria extracts via Geofabrik)
* NIPOST public postcode/address pages (where available)
* Sample crowdsourced address lists (anonymize before committing)

## Prototype stack (suggested)

* Python 3.10+, pandas, geopandas, geopy (Nominatim), scikit-learn/xgboost, shap, folium/kepler, matplotlib

## Ethics & data handling

* Do **not** commit raw personally-identifiable addresses to this public repo. Store any PII-only datasets privately and add processing scripts in `/data` that transform/anonymize before analysis.
* Include an `ethics.md` in `/docs` describing consent, anonymization and approval status.

## Contribution & issues

Please open issues for: `literature-review`, `data-ingest`, `prototype-geocode`, `explainability-visuals`, `user-study`, `writeup-intro`, `writeup-methods`.

## Next steps (short-term)

1. Add `requirements.txt` with minimal packages.
2. Add `LICENSE` (MIT suggested) and `CODE_OF_CONDUCT.md`.
3. Create an initial Google Sheet for literature and add 20 entries.
4. Push a small `sample_addresses.csv` (anonymized) in `/data/sample/`.

## Contact

Project owner: 
Ademola Adebowale 
https://fadebowaley.xyz

---

*Generated as part of an interactive PGD research workshop — use the files and the issue checklist to drive the chapter-by-chapter work.*
