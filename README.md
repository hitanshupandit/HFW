# Youth Detention & HFW Programs — National Dashboard

An interactive, single-file HTML dashboard combining:

- **Youth in Juvenile Detention data** (1997–2021, all 50 states) from the Annie E. Casey Foundation KIDS COUNT Data Center
- **High Fidelity Wraparound (HFW) program map** across the US with tier-based state classifications
- **North Carolina spotlight** with NCDHHS Tiered Care Coordination detail
- **NC county-level** Healthy Families / home-visiting program reference data

---

## Live Demo

Open `index.html` in any modern browser — no server or dependencies needed.

```bash
open index.html
# or
python3 -m http.server 8080   # then visit http://localhost:8080
```

---

## Dashboard Tabs

| Tab | Contents |
|-----|----------|
| **Overview** | National trend chart, State rankings, NC HFW impact |
| **National Trends** | Full US trend (count + rate), Year-over-year state change, Top 10 state trajectories |
| **HFW Map** | Interactive US map colored by HFW program tier, click any state for detail, full program directory table |
| **NC Spotlight** | NC detention trend with HFW launch marker, NC vs national rate, 3-tier TCC model diagram |
| **NC Counties** | County-level HFW/home-visiting programs, LME-MCO coverage areas |

---

## HFW Tier Classification

| Color | Tier | Criteria |
|-------|------|----------|
| 🟢 Green | **HFW Established** | Formal, documented statewide High Fidelity Wraparound program with certified teams |
| 🔵 Blue | **Similar Program** | Intensive wraparound-like care coordination with substantial state infrastructure |
| 🟠 Orange | **Emerging / Pilot** | Active pilots, planning grants, or limited county programs with state involvement |
| ⚫ Gray | **No statewide program** | No documented statewide HFW or equivalent program |

---

## Data Sources

| Dataset | Source |
|---------|--------|
| Youth detention counts & rates | [Annie E. Casey KIDS COUNT](https://datacenter.aecf.org/) — *Youth Residing in Juvenile Detention, Correctional, and/or Residential Facilities* |
| NC HFW / TCC program details | [NCDHHS Whole Child Health](https://www.ncdhhs.gov/divisions/child-and-family-well-being/whole-child-health-section/child-behavioral-health/new-service-planning-and-design) |
| Vaya Health HFW definition | Vaya Health Provider Network Operations (Rev. 03.13.2025) |
| Trillium HFW definition | Trillium Health Resources ILOS Service Description (Rev. 5/1/2025) |
| State program classifications | CHCS, SAMHSA, NWI/PDX, Sentencing Project, OJJDP research |
| NC county HFW data | Illustrative — based on publicly available NC program records |

---

## File Structure

```
hfw-dashboard/
├── index.html          # Complete self-contained dashboard (no build step)
├── README.md           # This file
├── data/
│   └── source.xlsx     # Original KIDS COUNT data (place your file here)
└── .gitignore
```

---

## Customization

All data is embedded directly in `index.html` as JavaScript constants:

- **`stateData`** — detention counts and rates by state/year
- **`nationData`** — US totals by year
- **`HFW_STATES`** — HFW program data by state (tier, summary, programs, JJ flag)
- **`ncCounties`** — NC county HFW reference data

To update program data, edit the `HFW_STATES` object in the `<script>` section.

---

## Browser Support

Chrome 90+, Firefox 88+, Safari 14+, Edge 90+

Uses: Chart.js 4.4.1 (CDN), Google Fonts (CDN). No frameworks, no build tools.

---

## License

Data: See respective source organizations.  
Dashboard code: MIT License.
