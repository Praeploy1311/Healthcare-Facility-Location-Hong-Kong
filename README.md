# Healthcare-Facility-Location-Hong-Kong

# Healthcare Facility Location Optimization in Hong Kong

This repository contains the processed datasets used in the optimization experiments of the study:

**A Hybrid NSGA-II–PSO Algorithm for Multi-Objective Healthcare Facility Location with TOPSIS-Based Decision Support**

## Optimization Input Datasets

This repository provides the processed input datasets used in the optimization experiments for the following problem instances:

- SB20–EXT5
- SB50–EXT10
- SB100–EXT20

Each dataset contains the spatial and service-related information required by the optimization model, including:

- representative demand-node coordinates,
- population demand associated with each demand node,
- selected existing healthcare facility locations,
- derived service-capacity indices,
- candidate facility locations, and
- corresponding distance information.

The datasets were generated through the data-preparation procedure described in the paper and are ready for direct use in the optimization process.

## Data Sources

The processed optimization datasets were derived from the following publicly available sources:

### 1. WorldPop

- **Data:** Hong Kong gridded population data
- **Year:** 2023
- **Spatial resolution:** approximately 100 m
- **Source:** https://hub.worldpop.org/geodata/summary?id=73757

### 2. OpenStreetMap

- **Data:** Healthcare facility locations
- **Retrieval tool:** OSMnx in Python
- **Temporal reference:** OSM records available at the time of data collection for this study
- **Source:** https://www.openstreetmap.org/

### 3. Hong Kong Hospital Authority

- **Data:** Healthcare service statistics
- **Report:** Hospital Authority Statistical Report 2023–2024
- **Source:** https://www3.ha.org.hk/Data/HAStatistics/StatisticalReport

## Temporal Scope of the Data

The source data represent specific time periods and may change over time. In particular, population distributions, healthcare facility information, and healthcare service statistics may differ from current conditions.

Therefore, the processed datasets provided in this repository should be interpreted as representing the data conditions used in the study rather than current real-time conditions.

## Availability

The processed datasets used in the study are available from the first author upon reasonable request.

**Contact:**  
Praeploy Poonprapan  
Email: praeploy.po@kkumail.com

The repository will be made publicly available following publication of the article.
