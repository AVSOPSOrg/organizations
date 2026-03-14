# AVSOPS Organizations — Open Data

Public dataset of **12,000+ veteran service organizations** across all 50 U.S. states and 3,144+ counties, maintained by [AVSOPS](https://avsops.com) — a 501(c)(3) nonprofit open data initiative.

## What's in this repo

| File | Records | Description |
|------|---------|-------------|
| `headquarters.csv` | 210 | National headquarters for all tracked VSOs and patriotic societies |
| `vfw/local-posts.csv` | 1,384 | Veterans of Foreign Wars local posts |
| `vfw/state-departments.csv` | 50 | VFW state departments |
| `legion/local-posts.csv` | 9,199 | American Legion local posts |
| `legion/state-departments.csv` | 51 | American Legion state departments |
| `dav/local-chapters.csv` | 1,136 | Disabled American Veterans chapters |
| `fra/local-branches.csv` | 336 | Fleet Reserve Association branches |
| `other/state-departments.csv` | 51 | State departments for other organizations (NSDAR, etc.) |
| `war-periods.csv` | 11 | War era categories (American Revolution through War on Terror) |

## Data fields

Every organization record includes:

- **Identity**: title, slug, abbreviation, chapter type (hq/state/local)
- **Location**: state, county, geo_tag (FIPS code), address, city, zip, coordinates
- **Contact**: phone, email, website
- **Social**: Facebook, Instagram, Twitter, YouTube, LinkedIn
- **Classification**: war period, parent organization

Some organization types have additional fields (service programs, meeting times, etc.) — see the CSV headers for details.

## War period categorization

Each organization is categorized by the war era in which it was founded:

| War Period | Dates | Example Organizations |
|-----------|-------|----------------------|
| American Revolution | 1775-1783 | DAR, SAR |
| War of 1812 | 1812-1815 | — |
| Mexican-American War | 1846-1848 | — |
| Civil War | 1861-1865 | SUV, MOLLUS |
| Spanish-American War | 1898 | VFW |
| World War I | 1914-1918 | American Legion, DAV, FRA |
| World War II | 1939-1945 | AMVETS, JWV |
| Korean War | 1950-1953 | KWVA |
| Vietnam War | 1955-1975 | VVA |
| Gulf War | 1990-1991 | — |
| War on Terror | 2001-Present | IAVA, WWP |

## How to use this data

**Download**: Click any CSV file and use the "Download raw file" button, or clone the repo.

**API**: GitHub serves raw files at:
```
https://raw.githubusercontent.com/avsops/organizations/main/headquarters.csv
```

**In code** (Python example):
```python
import pandas as pd
vfw = pd.read_csv("https://raw.githubusercontent.com/avsops/organizations/main/vfw/local-posts.csv")
indiana_vfw = vfw[vfw["state"] == "IN"]
```

## How to contribute

See [CONTRIBUTING.md](CONTRIBUTING.md) for details. Three ways to help:

1. **Report an error or update** — [Open an issue](../../issues/new/choose) (no technical skills needed)
2. **Edit a CSV directly** — Click the pencil icon on any CSV file in GitHub
3. **Bulk updates** — Fork, edit, submit a pull request

## License

This data is released under the [Creative Commons Attribution 4.0 International License](LICENSE) (CC BY 4.0). You are free to share and adapt the data for any purpose, with attribution to AVSOPS.

## About AVSOPS

AVSOPS is a 501(c)(3) nonprofit that collects, organizes, and publishes veteran service data so no veteran has to search 50 websites to find help.

- Website: [avsops.com](https://avsops.com)
- State data (CVSOs): [avsops/state-data](https://github.com/avsops/state-data)
- Contact: ed@avsops.com
