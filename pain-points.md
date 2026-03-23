---
layout: page
title: Pain Points
permalink: /pain-points/
nav_order: 2
---

# The Urban Data Landscape: Pain Points & Pitfalls

Urban data work is full of promise — better evidence for planning decisions, deeper insight into how cities function, more transparent engagement with communities. But the reality for most planning professionals involves a daily struggle with data that is hard to find, harder to use, and often incomplete.

---

## A Day in the Life

Research consistently shows that data professionals spend the majority of their time on data preparation rather than analysis:

| Activity | Time spent | Sources |
|----------|-----------|---------|
| **Finding data** | ~2.4 hours/day | Nakash & Bouhnik 2024; Atlassian 2025 |
| **Cleaning & organising data** | ~3.6 hours/day | CrowdFlower 2020; Kaggle 2019–; Anaconda 2020– |
| **Actual analysis** | ~2 hours/day | Derived from above |

That means roughly **75% of a data analyst's day** is spent on finding, cleaning, and organising data — not on the analysis that creates value.

For urban planners, this problem is compounded by the particular characteristics of urban data in Australia.

---

## Pain Points in Finding Urban Data

### Fragmented Sources & Data Silos

Urban data in Australia is spread across multiple levels of government (federal, state, local), private organisations, and academic institutions. There is no single, comprehensive portal or API for urban data. Trying to link transport data from state departments with demographic data from the ABS and land use data from local councils requires navigating multiple systems with different access methods.

### Inconsistent Formats & Metadata

Data is published in diverse formats — PDFs, Excel spreadsheets, CSV files, GeoJSON, shapefiles, APIs — each requiring different pre-processing approaches. Metadata quality varies enormously: some datasets come with thorough documentation of definitions, units, and collection methods, while others offer almost nothing.

**Example:** One council provides building approvals as PDF reports while another offers downloadable CSVs, making aggregation across jurisdictions a manual and error-prone process.

### Accessibility & Usability Challenges

Government websites and data portals can be difficult to navigate. Some datasets are restricted due to licensing, privacy concerns, or simply not being published in machine-readable formats. Many portals lack user-friendly search, filtering, or API access for non-technical users.

### Temporal & Spatial Inconsistencies

Urban data is collected at different time intervals (annual, quarterly, decadal census) and at varying spatial scales (LGA, SA1, SA2, street level, custom polygons). Boundary changes over time — such as council amalgamations or ABS geography revisions — make longitudinal analysis particularly challenging.

---

## Pain Points in Analysing Urban Data

### Data Quality & Reliability

Source data often contains errors, omissions, and inconsistencies. Sampling methodologies, imputation techniques, and collection standards vary between agencies and over time. The principle of "garbage in, garbage out" makes critical assessment of data trustworthiness an essential but often overlooked skill.

### Lack of Interoperability & Linkage

Combining disparate datasets to gain holistic insights — for example, linking transport usage with health outcomes and urban green space — is one of the most valuable but also most difficult tasks in urban data analysis. The lack of common identifiers, consistent geographic references, and standardised schemas across datasets creates significant integration challenges.

### Technological Barriers

Many planning professionals have limited skills in programming languages (Python, R) or advanced GIS software. Access to computational resources for working with large datasets can be limited, particularly in smaller organisations. There is often an over-reliance on basic spreadsheet software for tasks that would benefit from more powerful tools.

### Skills Gap in Analytical Techniques

There is a widespread gap in understanding of statistical methods, spatial analysis techniques, and predictive modelling approaches relevant to urban challenges. Translating raw data into actionable insights and compelling narratives — data storytelling — is a skill that is rarely taught in planning education.

---

## What Can Be Done?

The pain points outlined above are real and significant, but they are not insurmountable. The [Learning Pathways](../learning-pathways) section of this site provides structured guidance for building the skills needed to work effectively with urban data, from foundational data literacy through to advanced specialisations.

Beyond individual skill-building, there are systemic barriers that the profession and organisations need to address. These are explored in detail in the [Competency Framework](../competency-framework) page, but in summary:

**Organisational barriers** include legacy systems and budget constraints, key-person dependency for technical skills, and limited digital maturity in smaller councils. Managers need to build team capability rather than concentrating all technical skills in one person.

**Individual barriers** include unclear expectations about what skills are needed at different career stages, ambiguous thresholds between "core" and "specialist" competencies, and limited access to training and mentoring.

**Community barriers** include digital literacy gaps in communities being consulted, managing misinformation in digital engagement, and the critical question of when digital tools are not appropriate — particularly in Indigenous community engagement contexts where the CARE principles for data governance apply.

Key principles:

- **Start with a project** that matters to your work — motivation drives learning
- **Build skills iteratively** — you don't need to master everything before you begin
- **Learn to read code** even if you don't intend to write it — understanding what's possible opens new doors
- **Use AI wisely** — it's a powerful learning and research tool, but agents are not always reliable
- **Join a community** — the PIA Urban Data Network and local meetup groups provide support and shared learning

---

## References

- Nakash, M. & Bouhnik, D. (2024). *How Much Time does the Workforce Spend Searching for Information in the "new normal"?* [doi:10.13140/RG.2.2.28311.59043](https://doi.org/10.13140/RG.2.2.28311.59043)
- Atlassian (2025). *The State of Teams 2025.* [Report](https://atlassianblog.wpengine.com/wp-content/uploads/2025/03/the-state-of-teams-2025.pdf)
- CrowdFlower (2020). *Data Science Report.*
- Kaggle (2019–). *Annual Machine Learning and Data Science Surveys.*
- Anaconda (2020–). *State of Data Science Reports.*

---

*Next: [Learning Pathways →](../learning-pathways)*
