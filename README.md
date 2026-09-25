# Hong-Kong-Healthcare-Facility-Optimization-Dataset

This repository contains the processed datasets used in the optimization experiments of the study:

**Hybrid NSGA-II--PSO for Multi-Objective Healthcare Facility Location and Capacity Allocation: A Case Study of Hong Kong**

## Optimization Input Datasets

This repository provides the processed input datasets used in the optimization experiments for the following problem instances:

- SB20–EXT5
- SB50–EXT10
- SB100–EXT20

Each dataset contains the spatial and service-related information required by the optimization model, including:

- representative demand-node coordinates, which also serve as candidate healthcare facility sites;
- population demand associated with each representative demand node;
- public/government healthcare facility locations retrieved from OpenStreetMap;
- the subset selected as representative existing healthcare facilities;
- initial service-capacity values for the selected existing healthcare facilities, derived from healthcare service statistics following the formulation described in the study; and
- the corresponding spatial information required for the optimization experiments.

The datasets were generated through the data-preparation procedure described in the study and the accompanying Supplementary Information and are provided in a ready-to-use form for the optimization experiments.

## Data Sources

The processed optimization datasets were derived from the following publicly available sources.

### 1. WorldPop

- **Data:** Hong Kong gridded population data
- **Year:** 2023
- **Spatial resolution:** approximately 100 m
- **Source:** https://hub.worldpop.org/geodata/summary?id=73757

The gridded population data were converted into population points and aggregated into representative demand nodes using population-weighted K-means clustering.

### 2. OpenStreetMap

- **Data:** Healthcare facility locations
- **Retrieval tool:** OSMnx in Python
- **Selection:** Only healthcare facilities identified as public or government-operated were retained; private healthcare facilities were excluded.
- **Source:** https://www.openstreetmap.org/

The retained healthcare facilities were spatially grouped using K-means clustering. For each cluster, the actual healthcare facility nearest to the cluster centroid was selected as the representative existing healthcare facility.

### 3. Hong Kong Hospital Authority

- **Data:** Healthcare service statistics used to derive the initial service capacities of the selected existing healthcare facilities
- **Report:** Hospital Authority Statistical Report 2023–2024
- **Source:** https://www3.ha.org.hk/Data/HAStatistics/StatisticalReport

## Availability

All processed datasets used in the optimization experiments are publicly available in this repository.

The repository includes the processed datasets for the SB20–EXT5, SB50–EXT10, and SB100–EXT20 experimental instances and can be accessed directly at:

https://github.com/Praeploy1311/Healthcare-Facility-Location-Hong-Kong

## Related Publication

The data-preparation procedure, construction of the initial service capacities, optimization model, and computational experiments are described in the associated research article:

**Hybrid NSGA-II--PSO for Multi-Objective Healthcare Facility Location and Capacity Allocation: A Case Study of Hong Kong**

The full citation and DOI will be added here after publication.
