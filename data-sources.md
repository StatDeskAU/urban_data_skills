---
layout: page
title: Data Sources
permalink: /data-sources/
nav_order: 9
---

# Australian Urban Data Sources

A curated guide to key data sources for urban planning professionals in Australia. This is not exhaustive — it focuses on the most useful and accessible sources for common urban data tasks.

---

## Federal / National Sources

### Australian Bureau of Statistics (ABS)
The primary source for demographic, economic, and social data in Australia.

- **[ABS Data Explorer](https://www.abs.gov.au/statistics/microdata-tablebuilder/dataexplorer)** — interactive access to census and survey data
- **[ABS.Stat](https://stat.data.abs.gov.au/)** — API-accessible statistical datasets
- **Census data** — population, housing, employment, commuting patterns (2021 latest; 2026 upcoming)
- **Regional statistics** — SA1 through SA4, LGA, and custom geographies
- **Building approvals** — monthly data on residential and non-residential construction
- **National Accounts** — GDP, household income, industry output

**Key geographies:** Statistical Areas (SA1–SA4), Local Government Areas (LGA), Greater Capital City Statistical Areas (GCCSA), Remoteness Areas

### Geoscape Australia (formerly PSMA)
National spatial data infrastructure.

- **G-NAF** — Geocoded National Address File (every physical address in Australia)
- **Administrative Boundaries** — LGA, state, postcode, suburb boundaries
- **Land Parcels** — cadastral data
- **Transport & Topography** — road network and terrain data

*Note: Geoscape data requires licensing for most commercial use, but is available free for some research and government applications.*

### Australian Government Open Data
- **[data.gov.au](https://data.gov.au/)** — federal government open data portal
- **[National Map](https://nationalmap.gov.au/)** — interactive spatial data viewer for government datasets
- **[Australian Urban Observatory](https://auo.org.au/)** — liveability indicators for urban areas

### Other Federal Sources
- **[AURIN](https://aurin.org.au/)** — Australian Urban Research Infrastructure Network (research access)
- **[Bureau of Meteorology](http://www.bom.gov.au/)** — climate, weather, and water data
- **[Geoscience Australia](https://www.ga.gov.au/)** — elevation, geology, hazards
- **[Department of Infrastructure](https://www.infrastructure.gov.au/)** — transport and cities data
- **[Jobs and Skills Australia](https://www.jobsandskills.gov.au/)** — labour market data and projections
- **[ARDC](https://ardc.edu.au/)** — Australian Research Data Commons

---

## State & Territory Sources

### Western Australia
- **[data.wa.gov.au](https://data.wa.gov.au/)** — WA Government open data portal
- **[Landgate SLIP](https://www.landgate.wa.gov.au/)** — spatial data platform (cadastre, imagery, addressing)
- **[WA Planning Commission](https://www.wa.gov.au/organisation/western-australian-planning-commission)** — planning scheme data, development applications
- **[Main Roads WA](https://www.mainroads.wa.gov.au/)** — traffic counts, road network data
- **[Department of Communities](https://www.communities.wa.gov.au/)** — housing and homelessness data
- **[PlanWA](https://www.wa.gov.au/service/planning/planning-tools/planwa)** — WA's online planning tool

### New South Wales
- **[data.nsw.gov.au](https://data.nsw.gov.au/)** — NSW Government open data
- **[NSW Spatial Collaboration Portal](https://portal.spatial.nsw.gov.au/)** — spatial datasets
- **[NSW Planning Portal](https://www.planningportal.nsw.gov.au/)** — development application data
- **[Transport for NSW Open Data](https://opendata.transport.nsw.gov.au/)** — public transport GTFS feeds, traffic data

### Victoria
- **[data.vic.gov.au](https://data.vic.gov.au/)** — Victorian Government open data
- **[VicPlan](https://mapshare.vic.gov.au/vicplan/)** — planning scheme mapping
- **[DataVic](https://data.gov.au/data/organization/victorian-government)** — Victorian datasets on data.gov.au
- **[PTV/DoT](https://data.ptv.vic.gov.au/)** — public transport data

### Queensland
- **[QSpatial](https://qldspatial.information.qld.gov.au/)** — Queensland spatial data catalogue
- **[data.qld.gov.au](https://data.qld.gov.au/)** — Queensland open data
- **[Brisbane City Council Open Data](https://www.data.brisbane.qld.gov.au/)** — local datasets

### South Australia
- **[data.sa.gov.au](https://data.sa.gov.au/)** — SA Government open data
- **[SA Planning Portal](https://plan.sa.gov.au/)** — development applications, zoning

### Other States & Territories
- **[data.act.gov.au](https://www.data.act.gov.au/)** — ACT open data
- **[data.nt.gov.au](https://data.nt.gov.au/)** — NT open data
- **[data.tas.gov.au](https://data.tas.gov.au/)** — Tasmania open data

---

## Local Government Data

Many councils publish open data through their own portals. Coverage, quality, and currency vary enormously. Large metro councils tend to have the best datasets.

Common council datasets useful for urban planning:
- Development application registers
- Footpath and cycling network layers
- Tree canopy and vegetation surveys
- Community facilities and infrastructure
- Property and rates data
- Local planning scheme zoning layers

**Tip:** Search "[council name] open data" or check if the council publishes through a platform like data.gov.au or their own ArcGIS Hub.

---

## Spatial & Geospatial Data

### OpenStreetMap (OSM)
Free, crowdsourced geographic data. Quality varies by location — generally good in Australian CBDs and inner suburbs, patchy in outer suburbs and regional areas.

- **[Overpass Turbo](https://overpass-turbo.eu/)** — query and extract OSM data interactively
- **[OSMnx](https://osmnx.readthedocs.io/)** — Python library for downloading and analysing OSM street networks
- **[Geofabrik Downloads](https://download.geofabrik.de/australia-oceania.html)** — pre-packaged OSM data extracts for Australia

### Elevation & Terrain
- **[Elvis (Elevation Information System)](https://elevation.fsdf.org.au/)** — LiDAR and elevation data for Australia
- **Geoscience Australia DEM** — digital elevation models at various resolutions

### Satellite & Imagery
- **[Digital Earth Australia](https://www.dea.ga.gov.au/)** — analysis-ready Landsat and Sentinel-2 satellite data
- **[Google Earth Engine](https://earthengine.google.com/)** — cloud-based geospatial analysis platform

---

## Transport & Infrastructure Data

- **[GTFS feeds](https://transitfeeds.com/)** — standardised public transport timetable data (available from most Australian transport agencies)
- **State transport APIs** — real-time and historical public transport data
- **Main Roads / RMS traffic count data** — vehicle counts at specific locations
- **[OpenRouteService](https://openrouteservice.org/)** — open-source routing, isochrone, and accessibility analysis

---

## Data Principles

When working with data, keep these principles in mind:

### FAIR Principles
- **Findable** — data should be easy to discover
- **Accessible** — data should be retrievable through standard protocols
- **Interoperable** — data should work with other datasets and tools
- **Reusable** — data should be well-documented and properly licensed

### CARE Principles (for Indigenous data)
- **Collective benefit** — data should benefit Indigenous peoples
- **Authority to control** — Indigenous peoples should govern their data
- **Responsibility** — those working with data have a responsibility to support Indigenous rights
- **Ethics** — Indigenous peoples' rights and wellbeing should be the primary concern

### SHARE
Open data benefits the whole community. Where possible, share your work, methodologies, and derived datasets back to the community.

---

*Next: [Resources & Tools →](../resources)*
