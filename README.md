# Hong-Kong-Healthcare-Facility-Optimization-Dataset

This repository contains the processed datasets used in the optimization experiments of the study:

**Hybrid NSGA-II--PSO for Multi-Objective Healthcare Facility Location and Capacity Allocation: A Case Study of Hong Kong**

## Optimization Input Datasets

This repository provides the processed input datasets used in the optimization experiments for the following problem instances:

- SB20–EXT5
- SB50–EXT10
- SB100–EXT20

Each dataset contains the spatial and service-related information required by the optimization model, including:

- representative demand-node coordinates, which also serve as candidate facility locations,
- population demand associated with each demand node,
- all retrieved public/government healthcare facility locations and the subset selected as representative existing healthcare facilities,
- derived service-capacity indices for the selected existing healthcare facilities, calculated in Python from healthcare service statistics following the formulation described in the study, and
- corresponding distance information used in the optimization model.

The datasets were generated through the data-preparation procedure described in the study and are ready for direct use in the optimization process. Detailed information on the data-preparation procedure and the formulation used to derive the service-capacity indices will be provided in the associated publication. The DOI of the published article will be added to this repository after publication.

## Data Sources

The processed optimization datasets were derived from the following publicly available sources.

### 1. WorldPop

- **Data:** Hong Kong gridded population data
- **Year:** 2023
- **Spatial resolution:** approximately 100 m
- **Source:** https://hub.worldpop.org/geodata/summary?id=73757

### 2. OpenStreetMap

- **Data:** Public/government healthcare facility locations
- **Retrieval tool:** OSMnx in Python
- **Selection:** Only healthcare facilities identified as public or government-operated were retained for this study; private healthcare facilities were excluded.
- **Temporal reference:** OSM records available at the time of data collection for this study
- **Source:** https://www.openstreetmap.org/

The retained healthcare facilities were spatially grouped, and a subset was selected to represent the existing healthcare facilities used in each experimental instance.

### 3. Hong Kong Hospital Authority

- **Data:** Healthcare service statistics used to derive the service-capacity indices
- **Report:** Hospital Authority Statistical Report 2023–2024
- **Source:** https://www3.ha.org.hk/Data/HAStatistics/StatisticalReport

## Availability

The processed, ready-to-use experimental datasets used in the study are available from the first author upon reasonable request.

**Contact:**  
Praeploy Poonprapan  
Email: praeploy.po@kkumail.com

No formal application or data use agreement is required to request the processed datasets.

This repository is currently maintained for the associated research study and will be made publicly available following publication of the article.

## Related Publication

The detailed methodology for data preparation, service-capacity index construction, optimization modeling, and computational experiments is described in the associated research article:

**Hybrid NSGA-II--PSO for Multi-Objective Healthcare Facility Location and Capacity Allocation: A Case Study of Hong Kong**

The full citation and DOI will be added here after publication.
