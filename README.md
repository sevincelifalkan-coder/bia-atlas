# BIA Atlas -- Global Budget Impact Analysis Observatory

**Explore, compare, and benchmark budget impact parameters across HTA agencies worldwide.**

**Live site:** https://sevincelifalkan-coder.github.io/bia-atlas

---

## What is BIA Atlas?

BIA Atlas is an open-data platform for structured, searchable budget impact analyses (BIAs) from health technology assessment (HTA) agencies globally. Every entry is verified from published source documents -- no estimated or fabricated data.

Budget impact analyses are submitted by pharmaceutical companies to HTA agencies as part of reimbursement dossiers. They estimate how much a new drug will cost the health system over a defined time horizon. BIA Atlas extracts, standardises, and makes these parameters searchable across countries and therapeutic areas.

## What problem does it solve?

BIAs are critical for HTA reimbursement decisions, but they are scattered across:
- Agency websites (NICE, CADTH, PBAC, IQWiG, ZIN, TLV, NCPE)
- Journal articles behind paywalls
- Grey literature and HTA dossiers
- Conference presentations (ISPOR, HTAi)

No single resource structures and standardises BIA parameters for cross-country comparison. BIA Atlas fills this gap.

## Who is it for?

- **Health economists** benchmarking budget impact models
- **HTA analysts** comparing cost structures across jurisdictions
- **Pharmaceutical companies** preparing BIA dossiers for multi-country submissions
- **Policy makers** assessing affordability of new technologies
- **Researchers** studying HTA decision-making and pricing patterns
- **Students** learning about budget impact methodology

## What can you do with it?

- **Search** BIAs by drug name, disease area, country, or HTA agency
- **Filter** by therapeutic area (Neurology, Oncology, Ophthalmology) and country
- **Compare** budget impact parameters side-by-side across jurisdictions
- **View details** including per-patient costs, eligible populations, uptake assumptions, methodology, and sensitivity parameters
- **Verify** every data point against the cited source document (DOI link provided)
- **Contribute** your own verified BIA data via GitHub pull requests

## Current Data

| # | Drug | Country | Agency | Therapeutic Area | Verification | Source |
|---|------|---------|--------|-----------------|-------------|--------|
| 1 | Lecanemab (Leqembi) | Ireland | NCPE | Neurology | Verified | Sen SE. PharmacoEconomics (2026) |
| 2 | Lecanemab (Leqembi) | United States | CMS/Medicare | Neurology | Verified | Arbanas et al. JAMA Intern Med 2023 |
| 3 | Ranibizumab Biosimilar | Jordan | GPD | Ophthalmology | Partial | Frontiers in Public Health 2026 |
| 4 | CAR T-cell (axi-cel/tisa-cel) | Germany | GKV | Oncology | Verified | Skalt et al. HemaSphere 2022 |

### Verification status

- **Verified**: All parameters confirmed from the published source document. Every number is traceable.
- **Partial**: Key figures confirmed from the source abstract, but some detailed parameters are not available in the publication.

## Data parameters captured

For each BIA entry, the Atlas captures (where available):

**Population**: Eligible population size, estimation method, uptake rates (Year 1, 3, 5)

**Costs**: Drug cost per patient per year, diagnostic costs, monitoring costs (Year 1 and Year 2+), total per-patient cost

**Budget impact**: Annual budget impact (Year 1 and Year 5), cumulative budget impact, budget as percentage of total health expenditure, drug cost share

**Methodology**: Time horizon, perspective, model type, methodology framework, top sensitivity parameter, HTA decision status

**Source**: Full citation with DOI, journal/agency, and direct link to source document

## How to contribute

Have a published or submitted BIA? Add it to the Atlas:

1. **Fork this repository** on GitHub
2. **Open `index.html`** and find the `const DB=[...]` array
3. **Add your BIA entry** following the existing data structure (copy an existing entry as template)
4. **Include source citation** with DOI or URL -- this is mandatory
5. **Mark verification status** as "verified" (all parameters from source) or "partial" (key figures only)
6. **Submit a pull request** with a description of what you added

### Data quality rules

- Only include parameters you can verify directly from the source document
- Use `null` for any parameter not reported in the source
- Convert all costs to the currency used in the original publication
- Include the DOI or URL for every entry
- Do not estimate or interpolate missing parameters

## Data sources

All data is extracted from:
- Published peer-reviewed articles (with DOI)
- HTA agency public assessment reports
- Preprints on medRxiv/SSRN (marked as preprint status)

Every entry includes a source citation and URL. Parameters marked as "Not available" when not reported in the source document.


## Tech stack

- Pure HTML, CSS, JavaScript (no build step, no framework dependencies)
- Hosted on GitHub Pages (free, no server required)
- All data embedded in `index.html` for maximum portability
- Open source -- anyone can inspect, verify, and contribute

## License

- **Data**: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/)
- **Code**: MIT License

## Author

**Sevinc Elif Sen**
Independent Health Economist | HEOR, Decision-Analytic Modelling, HTA, Budget Impact Analysis

Cross-country experience: NICE, HIQA, NCPE, ZIN, IQWiG, TLV, CADTH, PBAC, SFDA

Technical Officer, HTAi Disinvestment and Early Awareness Interest Group (DEA-IG)

## Citation

If you use BIA Atlas data in your research, please cite:

> Sen SE. BIA Atlas: Global Budget Impact Analysis Observatory. 2026. Available from: https://sevincelifalkan-coder.github.io/bia-atlas

## Roadmap

- [ ] Expand to 10+ verified BIA entries across therapeutic areas
- [ ] Add NICE, CADTH, PBAC, and TLV agency data
- [ ] Enable CSV/JSON export for research use
- [ ] Add cross-country comparison visualisation
- [ ] Develop contributor guidelines and data extraction template
- [ ] Integrate with published BIA systematic reviews
