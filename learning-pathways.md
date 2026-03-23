---
layout: page
title: Learning Pathways
permalink: /learning-pathways/
nav_order: 3
---

# Empowering Urban Data Analysts: Learning Pathways

Building urban data skills is not about mastering everything at once. It's an iterative process that blends technical, analytical, and domain-specific knowledge. The key is to **find a project** that connects to your work and interests, then build skills around it.

---

## Guiding Principles

1. **Find a project** — something that has value to your work or interests now
2. **Foundations matter** — but don't use them as a reason not to start
3. **Build a skill set** — balance theory and practice; learn to read code, even if you don't intend to write it
4. **Build a toolkit** — include knowledge management tools, online tools, and a good text editor
5. **Use AI wisely** — a great learning and research tool, but agents are not always reliable

If in doubt about which programming language to learn, **choose Python**. It has the broadest ecosystem for data analysis, spatial work, and automation.

---

## Foundational Skills: The Bedrock

### Data Literacy & Critical Thinking

Before tools and techniques, the most important skills are the ability to understand data and to question it. These are covered in depth on their own pages:

- **[Data Literacy](../data-literacy)** — Understanding data types, formats, Australian geographic structures (ASGS, SA1/SA2/LGA), reading statistics correctly, metadata, data quality, and FAIR/CARE/SHARE principles
- **[Critical Thinking](../critical-thinking)** — The six questions every planner should ask before trusting any dataset: Who collected this and why? What's missing? Do the boundaries hold up? What happened during processing? Does this pass the common-sense test? Who is affected?

These two pages provide the detailed treatment. The summary below highlights the key points for the learning pathway context.

### Spreadsheet Proficiency (Advanced)

Spreadsheets remain the most widely used data tool in planning. Moving beyond basic formulas into advanced functionality significantly increases productivity.

**What to learn:**
- Pivot tables and dynamic aggregation
- VLOOKUP, INDEX/MATCH, and XLOOKUP
- Data validation and conditional formatting
- Power Query for data transformation
- Python integration in Excel (new feature)

**How to learn it:**
- Advanced Excel or Google Sheets courses (LinkedIn Learning, Coursera)
- Practice with real urban datasets (ABS data, council open data)
- Microsoft's own learning paths for Power Query

---

## Technical Skills: Tools of the Trade

### Geographic Information Systems (GIS)

Spatial data is central to urban planning. GIS skills allow you to map, analyse, and visualise geographic information.

**What to learn:**
- Spatial data types, projections, and coordinate systems
- Geocoding and address matching
- Spatial joins, buffering, and overlay analysis
- Network analysis (transport, pedestrian accessibility)
- Working with raster and vector data

**Recommended tools:**
- **QGIS** — free, open-source, excellent for beginners and professionals
- **ArcGIS Pro** — industry standard, available through many organisations
- **Google Earth Engine** — for large-scale environmental/remote sensing analysis

**How to learn it:**
- ESRI Academy (free and paid courses)
- QGIS documentation and tutorials
- University GIS courses (many available online)
- YouTube channels focused on spatial analysis

###

**Markdown - introductory point for people new to programming**
- Markup language that is read and written by AI agents
- Versatile and leverages into other uses

**Regular expressions (regex)**
- 

### Programming for Data Analysis

Programming opens up capabilities far beyond what spreadsheets can offer: automation, web scraping, API interaction, statistical modelling, and reproducible analysis.

**Python — versatile and powerful:**
- Learn the fundamentals plus the following packages:
  - **Pandas** — data manipulation and analysis
  - **GeoPandas** — spatial data in Python
  - **Matplotlib / Seaborn** — data visualisation
  - **Scikit-learn** — machine learning basics
  - **Requests / BeautifulSoup** — web scraping and API access
  - **OSMnx** — OpenStreetMap network analysis
  - **Folium** — interactive web maps

**R — strong alternative for statistical work:**
- **Tidyverse** — data wrangling (dplyr, tidyr, ggplot2)
- **sf** — spatial data handling
- **Leaflet** — interactive mapping
- **R Markdown** — reproducible reports

**How to learn it:**
- MOOCs, Codecademy, DataCamp, or Coursera (e.g. *Python for Everybody*)
- The Carpentries workshops (Data Carpentry, Software Carpentry)
- Project-based learning — pick a real problem and solve it
- University introductory courses (many available free online)

### Data Visualisation

Good visualisation transforms data into understanding. It's about telling a story with data, not just making charts. And don't forget about spreadsheet charts for visualisation - in many/most cases, that will be all you need.

**Tools to explore:**
- **Dashboards** - useful in the right environment, but many users just want to download a csv/spreadsheet file to do their own analysis. 
  - **Tableau Public** — free, powerful interactive dashboards
  - **Power BI** — Microsoft's analytics and visualisation platform
- **Python libraries**
  - **Streamlit / Dash** — Python libraries for building data apps
  - **Matplotlib, Seaborn, ggplot2** — code-based static and interactive graphics
- **Inkscape / Adobe Illustrator** — for refining publication-quality graphics

**How to learn it:**
- Online courses in data storytelling and visual communication
- Practice building visualisations with different tools
- Study examples of effective data visualisation in planning and journalism

---

## Advanced Concepts & Specialisations

### Database Management (SQL)

When data grows beyond spreadsheet size, databases become essential. SQL (Structured Query Language) is the standard for querying relational databases.

**What to learn:**
- Querying relational databases (SELECT, JOIN, GROUP BY)
- PostGIS for spatial database queries
- Data warehousing fundamentals
- Database design basics

**How to learn it:**
- Khan Academy SQL course (free)
- Codecademy SQL course
- PostGIS documentation and tutorials
- Practice with Australian open data loaded into PostgreSQL

### Web Mapping & APIs

Modern urban data increasingly comes through APIs (Application Programming Interfaces), and web mapping allows you to share spatial analysis interactively.

**What to learn:**
- Consuming public APIs (transport, planning, weather, census)
- Working with OpenStreetMap data
- Building interactive web maps (Leaflet.js, Folium, Mapbox)
- Basic web development (HTML, CSS, JavaScript)

**How to learn it:**
- API documentation for specific services
- Leaflet.js and Folium tutorials
- Web development basics (freeCodeCamp, MDN Web Docs)
- OSMnx tutorials for Python-based OSM work

### Statistical Modelling & Machine Learning

Advanced analytical techniques can reveal patterns and make predictions that inform planning decisions.

**What to learn:**
- Regression analysis (linear, logistic, spatial)
- Clustering and classification (k-means, DBSCAN, random forests)
- Time series analysis and forecasting
- Spatial autocorrelation and geostatistics

**How to learn it:**
- University statistics courses (available online)
- Andrew Ng's Machine Learning course (Coursera/Stanford)
- Scikit-learn documentation and tutorials
- Practice with real planning datasets

---

## The Data Pipeline

Understanding where your skills fit in the broader data workflow helps you identify gaps and plan your learning:

| Stage | Activities | Tools |
|-------|-----------|-------|
| **Source** | ABS, state agencies, council data, field surveys, APIs | Web browsers, data portals, API clients |
| **Process** | Cleaning, transformation, integration, analysis | Python, R, SQL, Excel, QGIS, ArcGIS |
| **Output** | Visualisation, dashboards, reports, raw data/APIs | Tableau, Power BI, Streamlit, Matplotlib |

Most urban data professionals need skills across all three stages, but it's fine to specialise. The important thing is understanding the full pipeline.

---

## Connecting Skills to Planning Values

Learning data skills in isolation from planning's professional values is a missed opportunity. Every technical capability should connect back to the purpose it serves.

**Equity:** When building a dashboard, ask — who benefits from this data system? Who is excluded? Skills in demographic disaggregation and accessibility auditing connect directly to equitable planning outcomes.

**Sustainability:** Climate data integration, scenario modelling, and lifecycle analysis connect data skills to long-term environmental stewardship.

**Public Interest:** Data storytelling, open data publication, and transparent documentation of methodology ensure that data-driven planning remains accountable to communities.

**Professional Judgment:** AI literacy, vendor claim assessment, and knowing when technology is not the right solution protect the essential role of human judgment in planning decisions. As the PIA Digital Planning Core Competencies framework emphasises, digital tools should support planning judgment, not replace it.

For a deeper exploration of how the PIA competency framework maps to these values and to different career stages, see the [Competency Framework](../competency-framework) page.

---

## Practical Strategies

### Start with Australian Urban Data
- Use the [ABS Data Explorer](https://dataexplorer.abs.gov.au/) to practice with census and survey data
- Explore state open data portals (see [Data Sources](../data-sources))
- Download local council datasets to practice cleaning and analysis

### Join Communities
- [PIA Urban Data Network](https://www.linkedin.com/groups/14617445/) on LinkedIn
- Local PyData, R-Ladies, and GIS user groups
- Stack Overflow, Reddit r/GIS and r/datascience
- Meetup.com for local data and tech events

### Work on Real Projects
- Identify a local urban problem and try to solve it with data
- Contribute to open data initiatives or community mapping projects
- Build a portfolio of work as you learn

### Embrace Continuous Learning
The urban data field evolves constantly. New tools, data sources, and techniques emerge regularly. Build habits of curiosity, experimentation, and sharing what you learn with others.

---

*Next: [Australian Data Sources →](../data-sources)*
