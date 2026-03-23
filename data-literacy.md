---
layout: page
title: Data Literacy
permalink: /data-literacy/
nav_order: 4
---

# Data Literacy for Urban Planners

Data literacy is the ability to **read, understand, and communicate with data**. It's the foundational language that underpins every other skill in urban data work — just as you need to read English before you can write a compelling report, you need to understand data before you can analyse it, visualise it, or make decisions with it.

This page covers the concepts and vocabulary that every planning professional should understand, with examples drawn from Australian urban data sources.

*For the complementary skill of questioning and interrogating data, see [Critical Thinking](critical-thinking).*

---

## What Data Actually Is

This sounds obvious, but many planning professionals work with data daily without a clear mental model of what they're handling.

### Data vs information vs insight

These terms are often used interchangeably, but they describe different stages of a process:

**Data** is raw, unprocessed facts. A spreadsheet of 50,000 rows showing every development application lodged in a council over 10 years is data. On its own, it tells you nothing useful — it's too much to absorb, and it has no narrative.

**Information** is data that has been organised, filtered, or summarised to answer a question. "The median DA processing time in 2024 was 42 days, up from 35 days in 2020" is information. It's extracted from the data and tells you something specific.

**Insight** is information interpreted through domain knowledge to guide action. "Processing times are increasing because the planning team hasn't grown despite a 40% increase in application volume since the code amendment — we need either more staff or a streamlined assessment pathway for low-risk applications" is insight. It connects the numbers to context and points toward a decision.

The entire learning pathway in urban data work is about developing the skills to move from raw data to actionable insight. Data literacy is the first step — understanding the raw material.

### Structured vs unstructured data

**Structured data** is organised into rows and columns with consistent fields. A CSV of Census population counts by SA2, a database table of property valuations, or a GIS attribute table of zoning polygons are all structured. Most urban data work involves structured data.

**Unstructured data** is everything else — PDF reports, policy documents, public submission text, aerial photographs, meeting minutes, community survey free-text responses. Increasingly, AI and text analysis tools are making unstructured data accessible to analysis, but it requires different tools and approaches.

**Semi-structured data** sits in between. JSON from a government API, XML from a metadata catalogue, or a spreadsheet where someone has put notes and formatting within the data cells (a common and frustrating situation) are semi-structured — they have some organisation but don't fit neatly into rows and columns.

---

## Data Types and Formats

Understanding what type of data you're working with determines what you can do with it.

### Quantitative vs qualitative

**Quantitative data** is numerical and measurable: population counts, dwelling densities, traffic volumes, processing times, land areas, price indices. It's what most people think of when they hear "data."

**Qualitative data** is descriptive and categorical: land use zoning categories, community consultation feedback themes, development application types, heritage listing classifications. Qualitative data can be coded numerically for analysis (e.g., assigning a number to each zoning category) but the numbers represent categories, not quantities — the "average" of R20, R40, and MRS doesn't mean anything.

### Scales of measurement

This matters because it determines which statistical operations are valid:

**Nominal:** Categories with no order. Zoning types (Residential, Commercial, Industrial), council names, land use classifications. You can count them and calculate mode (most common) but not mean or median.

**Ordinal:** Categories with a meaningful order but unequal intervals. Bushfire risk ratings (Low, Moderate, High, Extreme), heritage significance levels, community satisfaction ratings (1–5 stars). You can rank them and calculate median but mean is debatable.

**Interval:** Numeric with equal intervals but no true zero. Temperature in Celsius, year of construction. The difference between values is meaningful but ratios are not (20°C is not "twice as hot" as 10°C).

**Ratio:** Numeric with equal intervals and a true zero. Population, area in hectares, price in dollars, distance in metres. All mathematical operations are valid.

A common error in urban planning analysis is treating ordinal data as ratio — for example, averaging Likert scale community survey responses (1–5) and reporting that "community satisfaction is 3.7." This is technically invalid because the intervals between 1–2, 2–3, 3–4, and 4–5 aren't necessarily equal. In practice it's widely done, but a data-literate planner knows it's an approximation.

### Common file formats

| Format | What it is | When you'll encounter it |
|--------|-----------|-------------------------|
| **CSV** | Comma-separated values — plain text, universal | Open data portals, ABS downloads, data exports |
| **Excel (.xlsx)** | Microsoft spreadsheet with formatting and formulas | Council data, consultant reports, internal work |
| **GeoJSON** | Spatial data in JSON format | Web mapping, APIs, modern spatial data |
| **Shapefile (.shp)** | Legacy spatial data format (actually 3–6 files) | GIS data from government, Landgate, councils |
| **GeoPackage (.gpkg)** | Modern spatial database file | Replacing shapefiles in professional GIS work |
| **JSON** | JavaScript Object Notation — nested key-value pairs | APIs, web data, configuration files |
| **PDF** | Portable Document Format | Government reports, planning scheme documents |
| **XML** | Extensible Markup Language — tagged hierarchical data | Metadata catalogues, legacy government systems |
| **KML/KMZ** | Google Earth spatial format | Simple mapping, community engagement |

A data-literate planner doesn't need to be expert in all of these, but should recognise them and understand which tools open which formats. Knowing that a shapefile is actually a bundle of files (`.shp`, `.dbf`, `.shx`, `.prj` minimum), for example, prevents the common mistake of emailing just the `.shp` file and wondering why the recipient can't open it.

---

## Australian Geographic Data Structures

Understanding how Australia organises geographic data is essential for anyone working with urban data. This is the vocabulary of spatial data in Australian planning.

### ABS Statistical Geography (ASGS)

The ABS uses a hierarchical system called the Australian Statistical Geography Standard. Every piece of Census data is published at one or more of these levels:

| Level | Typical size | Count (approx.) | What it represents |
|-------|-------------|-----------------|-------------------|
| **Mesh Block** | ~30–60 dwellings | 358,000 | Smallest unit — single land use type |
| **SA1** | 200–800 people | 61,000 | Smallest unit for most Census data |
| **SA2** | 3,000–25,000 people | 2,500 | Roughly equivalent to suburbs |
| **SA3** | 30,000–130,000 people | 360 | Regional groupings |
| **SA4** | 100,000–500,000 people | 107 | Labour market regions |
| **GCCSA** | Variable | 16 | Greater Capital City areas |
| **State/Territory** | Variable | 8 | Self-explanatory |
| **LGA** | Variable | 562 | Local Government Areas (council boundaries) |

**Key things to understand:**

SA2s are the workhorse geography for most urban analysis — they're roughly suburb-sized and most ABS data is available at this level. But SA2 boundaries don't always align with suburb boundaries, council boundaries, or planning scheme boundaries. A planner working in "Fremantle" needs to know whether their analysis uses the SA2 called "Fremantle," the suburb boundary, or the City of Fremantle LGA boundary — these are three different areas that produce different results.

SA1s provide finer detail but have data suppression issues — the ABS suppresses (hides) small counts to protect privacy. An SA1 with only 200 people might have income data suppressed for many categories, making it less useful than the SA2 aggregate.

**Mesh Blocks** are the finest level and are useful for precise spatial analysis, but carry very limited data (just population counts and land use category).

### Non-ABS geographies

Planning data in Australia uses many geographic systems beyond the ASGS:

**Cadastral parcels (lots):** Individual land titles. This is the finest-grained spatial unit for property-related analysis. Available through state agencies (Landgate in WA, NSW Spatial Services, etc.).

**Planning scheme zones:** The spatial extent of zoning controls. These don't align with any standard statistical geography and change when planning schemes are amended.

**Transport zones:** Used in transport modelling, these are custom geographies designed around travel behaviour patterns. They don't align with SA2s or LGAs.

**Postcodes:** Widely used but actually designed for mail delivery, not analysis. Postcode boundaries can cross council boundaries and change without notice. Using postcodes for urban analysis is common but introduces geographic imprecision.

**Suburbs:** Gazetted locality boundaries. Often used informally but their boundaries are not always consistent with other systems. In some states, suburb boundaries are maintained by the land agency; in others, they're loosely defined.

### The concordance challenge

One of the most practical data literacy skills in Australian urban planning is understanding how to map between these different geographies. If you have council rates data by property lot and Census data by SA2, linking them requires spatial analysis — you can't just match on suburb name because the boundaries don't align.

The ABS publishes **correspondence files** that map between different ASGS levels and between different Census years (when boundaries change). Understanding that these exist and how to use them is fundamental data literacy for urban analysis.

---

## Reading Statistics Correctly

You don't need to be a statistician, but you need to understand the basics that appear constantly in urban data.

### Mean, median, and mode

**Mean** (average): Add all values, divide by count. Sensitive to extreme values. A suburb where most houses are worth $500,000 but one is worth $10 million has a mean house price that overstates what "typical" looks like.

**Median**: The middle value when sorted. Much more robust for skewed distributions. Median house price, median household income, and median DA processing time are generally more useful than their means because urban data is almost always skewed — a few very large or very small values pull the mean away from what's typical.

**Mode**: Most common value. Useful for categorical data (most common dwelling type, most common zoning category) but rarely reported in urban planning contexts.

**The practical rule:** For anything involving prices, incomes, processing times, or lot sizes — use median unless you have a specific reason to use mean. These distributions are always right-skewed (a long tail of high values), and the mean will overstate what's typical.

### Rates, ratios, and percentages

Rates standardise data so you can compare areas of different sizes. A suburb with 50 burglaries and a population of 5,000 has a higher burglary rate (10 per 1,000) than a suburb with 100 burglaries and a population of 20,000 (5 per 1,000), even though the raw count is lower.

**Common urban data rates:**
- Dwelling density: dwellings per hectare
- Population density: people per km²
- Crime rate: incidents per 100,000 population
- Job density: jobs per hectare of commercial land
- Approval rate: DAs approved as percentage of DAs determined

**Watch for denominator choices:** A "job creation rate" per hectare of total land gives a very different picture from jobs per hectare of commercially-zoned land. The same numerator with a different denominator tells a different story.

### Understanding distributions

When someone reports a single number (mean, median), they're compressing an entire distribution into one point. A data-literate planner asks what the distribution looks like:

**Household income example:** An SA2 with a median household income of $85,000 could be a relatively uniform middle-income area, or it could be a bimodal distribution with many low-income renters and many high-income homeowners averaging out to "middle." The planning implications are completely different — the first needs general services, the second needs targeted support for both groups.

**Processing time example:** Median DA processing time of 42 days tells you about the typical case. But if the distribution has a long tail (10% of applications take over 200 days), that tail represents real people waiting for decisions on their property. Reporting only the median hides the worst-case experience.

Histograms, box plots, and percentile ranges (e.g., reporting the 25th, 50th, and 75th percentile) give a much richer picture than a single summary statistic.

### Statistical significance vs practical significance

A finding can be statistically significant (unlikely to occur by chance) but practically meaningless. If an analysis of 100,000 property transactions finds that houses with north-facing living rooms sell for $1,200 more on average (p < 0.001), that's statistically significant — but on a $600,000 house, it's a 0.2% difference that no buyer or planner should care about.

Conversely, a finding based on a small sample might not reach statistical significance but could be practically important. If a pilot street-calming project in one suburb reduced pedestrian injuries from 8 per year to 2 per year, the sample is too small for statistical significance — but the practical difference matters.

Data-literate planners ask both: "Is this result real?" (statistical significance) and "Does this result matter?" (practical significance).

---

## Understanding Metadata

Metadata is data about data — the documentation that tells you what a dataset contains, how it was collected, what the fields mean, and what limitations apply.

### What good metadata includes

- **Data dictionary:** Definitions of every field/column — what it measures, units, valid values
- **Collection methodology:** How the data was gathered — Census, survey, administrative records, remote sensing
- **Temporal coverage:** What time period the data covers and how frequently it's updated
- **Spatial coverage and resolution:** What geography it covers and at what level of detail
- **Known limitations:** Suppression rules, imputation rates, sampling error, coverage gaps
- **Licensing and access conditions:** Whether you can use it, share it, and publish derived work
- **Update schedule:** When the next release is expected

### What usually happens in practice

Most datasets encountered in Australian urban planning have incomplete metadata. Council open data portals often publish CSV files with no data dictionary — just column headers that might or might not be self-explanatory. Is "AREA" in square metres or hectares? Is "DATE" the lodgement date or the decision date? Is "VALUE" in current or constant dollars?

**Practical skill:** Before analysing any new dataset, spend 10 minutes looking for metadata. Check the data portal's description, look for an accompanying PDF or methodology note, check whether the publishing agency has a data dictionary on their website. If metadata doesn't exist, contact the publisher or note the limitations explicitly in your analysis. This small upfront investment prevents significant downstream errors.

---

## Understanding Data Quality

Not all data is equal. Data quality has multiple dimensions, and understanding them helps you assess how much trust to place in any particular dataset.

### Dimensions of data quality

**Accuracy:** Does the data correctly represent reality? GPS coordinates that are 100m off, addresses that are miscoded, or Census responses that are guessed rather than measured all reduce accuracy.

**Completeness:** How much is missing? A dataset of development applications might be 95% complete for suburban councils but only 60% complete for rural shires. The gaps aren't random — they systematically bias the dataset toward urban areas.

**Consistency:** Is the same thing measured the same way throughout? If one council classifies a granny flat as a "secondary dwelling" and another classifies it as an "ancillary accommodation," combining their DA data without reconciling the categories produces misleading totals.

**Currency:** How old is the data? The most recent ABS Census data (2021) is already several years old. Population estimates are updated annually but at coarser geographic levels. Land use data may not reflect recent rezonings.

**Precision:** How detailed is the measurement? Population reported as "approximately 15,000" is less precise than "14,837." Both might be equally accurate, but they support different types of analysis.

**Relevance:** Does this data actually measure what you're trying to understand? Using "number of building permits" as a proxy for "housing construction" misses projects that are permitted but never built, and projects built without proper permits.

### The "garbage in, garbage out" principle

This is the most important concept in data quality. No amount of sophisticated analysis, beautiful visualisation, or AI-powered processing can fix fundamentally flawed input data. A regression model built on inaccurate data produces inaccurate predictions, regardless of how elegant the model is. A map built on incomplete spatial data shows an incomplete picture, regardless of how polished the cartography is.

Data literacy means developing the habit of assessing quality *before* starting analysis — not after you've invested hours in processing and discover the results don't make sense.

---

## FAIR, CARE, and SHARE Principles

These frameworks guide how data should be managed and governed. They appear frequently in Australian government data policy and are increasingly relevant to planning practice.

### FAIR Principles

Originally developed for research data, FAIR principles are now widely adopted across government:

**Findable:** Data should have persistent identifiers, rich metadata, and be registered in searchable catalogues. In practice, this means publishing on data portals (data.gov.au, state portals) rather than burying datasets in obscure website pages.

**Accessible:** Data should be retrievable through standard, open protocols. Publishing a dataset behind a login wall, in a proprietary format, or only on request significantly reduces accessibility.

**Interoperable:** Data should use standard vocabularies, schemas, and formats that allow it to be combined with other datasets. Using standard geographic identifiers (SA2 codes rather than suburb names), standard date formats (ISO 8601), and open file formats (CSV, GeoJSON, GeoPackage) all support interoperability.

**Reusable:** Data should have clear licensing, provenance information, and quality documentation so that others can confidently use it for new purposes.

### CARE Principles

CARE principles apply specifically to Indigenous data and are particularly relevant in Australian planning contexts:

**Collective benefit:** Data about Indigenous communities should benefit those communities. Research or analysis that extracts data from Indigenous communities without returning value is extractive.

**Authority to control:** Indigenous peoples should have governance authority over data about their communities, lands, and resources. This includes the right to determine how data is collected, stored, accessed, and used.

**Responsibility:** Those who work with Indigenous data have a responsibility to support Indigenous data sovereignty and to use data in ways that support Indigenous rights and wellbeing.

**Ethics:** Indigenous peoples' rights and wellbeing should be the primary concern in any data-related activity. Standard ethics review processes may not adequately address Indigenous data governance requirements.

For urban planners, CARE principles are most relevant when working with data about Indigenous communities — housing needs assessments, Native Title areas, cultural heritage mapping, and community consultation data. Using Census data about Indigenous populations without considering CARE principles is technically possible but professionally and ethically problematic.

### SHARE

The principle that data created with public resources should, where possible, be shared openly for public benefit. Planning data — development application registers, zoning maps, transport studies, community surveys — is largely created with public funding and has broad potential value beyond its original purpose.

---

## Practical Data Literacy Skills

### Reading a data portal

When you land on a new dataset on data.gov.au or a state portal:

1. **Read the description** before downloading — what does this dataset actually contain?
2. **Check the update frequency** — is this a one-off publication or regularly updated?
3. **Look at the format options** — CSV is usually most versatile; GeoJSON or GeoPackage for spatial data
4. **Find the metadata** — data dictionary, methodology notes, limitations
5. **Check the licence** — Creative Commons Attribution is the most common for Australian government data
6. **Note the geographic scope and resolution** — national at SA2 level is different from local at lot level
7. **Check the temporal coverage** — when was this collected and how current is it?

### Reading a spreadsheet

When you open a new CSV or Excel file:

1. **How many rows and columns?** This tells you the scale of the dataset
2. **What do the column headers mean?** If they're abbreviated or unclear, look for a data dictionary
3. **What's in the first and last few rows?** Check for header rows, summary rows, or notes embedded in the data
4. **Are there empty cells, and what do they mean?** Empty could mean zero, unknown, not applicable, or suppressed
5. **What data types are in each column?** Text, numbers, dates, codes? Are numbers stored as text (common in Excel)?
6. **Are there any obvious anomalies?** Negative values where only positives make sense, dates in the future, population counts of zero

### Communicating about data

Data literacy includes the ability to talk about data clearly:

- Say "median household income" not "the income" — specify the statistic
- Say "at SA2 level" not "by suburb" — specify the geography
- Say "as at June 2021" not "currently" — specify the time reference
- Say "based on Census self-reporting" not "the actual figure" — specify the source method
- Say "approximately 15,000" not "15,000" when precision isn't warranted — convey appropriate certainty

---

*The companion skill to data literacy is [Critical Thinking](critical-thinking) — the discipline of questioning and interrogating data before trusting it.*

*Next: [Critical Thinking →](critical-thinking)*
