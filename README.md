# Hong-Kong-Healthcare-Facility-Optimization-Dataset

This repository contains the processed datasets used in the optimization experiments of the study:

**A Hybrid NSGA-II–PSO Algorithm for Multi-Objective Healthcare Facility Location with TOPSIS-Based Decision Support**

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

The WorldPop raster data were used to represent the spatial distribution of population in Hong Kong. Population grid cells were converted into spatial points and subsequently aggregated into representative demand nodes using population-weighted K-means clustering. The population associated with each representative demand node corresponds to the total population assigned to its cluster.

### 2. OpenStreetMap

- **Data:** Public/government healthcare facility locations
- **Retrieval tool:** OSMnx in Python
- **Selection:** Only healthcare facilities identified as public or government-operated were retained for this study; private healthcare facilities were excluded.
- **Temporal reference:** OSM records available at the time of data collection for this study
- **Source:** https://www.openstreetmap.org/

Healthcare facility locations were retrieved programmatically from OpenStreetMap using OSMnx. Hospitals and clinics were initially retrieved, after which the dataset was filtered to retain only public or government-operated healthcare facilities.

The retained healthcare facilities were spatially grouped, and a subset was selected to represent the existing healthcare facilities used in each experimental instance.

### 3. Hong Kong Hospital Authority

- **Data:** Healthcare service statistics used to derive the service-capacity indices
- **Report:** Hospital Authority Statistical Report 2023–2024
- **Source:** https://www3.ha.org.hk/Data/HAStatistics/StatisticalReport

Healthcare service statistics published by the Hong Kong Hospital Authority were used to derive the service-capacity indices of the selected existing healthcare facilities.

The service-capacity indices provided in the processed datasets are not direct capacity values reported by the Hospital Authority. They were calculated by the authors in Python using healthcare service statistics and the formulation described in the study.

## Data Preparation

The publicly available source data were processed to construct the optimization instances used in the study.

The main data-preparation steps include:

1. converting the WorldPop population raster into spatial population points;
2. aggregating the population points into representative demand nodes using population-weighted K-means clustering;
3. using the representative demand-node locations as candidate locations for new healthcare facilities;
4. retrieving public/government hospitals and clinics from OpenStreetMap using OSMnx;
5. filtering out private healthcare facilities;
6. selecting representative existing healthcare facilities from the retained public/government facilities;
7. deriving service-capacity indices for the selected existing healthcare facilities using healthcare service statistics from the Hong Kong Hospital Authority; and
8. calculating the corresponding distance information between demand nodes and healthcare facility locations.

The resulting processed datasets were then used directly as inputs to the optimization models.

## Experimental Instances

Three experimental problem instances are provided:

- **SB20–EXT5:** 20 representative demand nodes and 5 selected existing healthcare facilities
- **SB50–EXT10:** 50 representative demand nodes and 10 selected existing healthcare facilities
- **SB100–EXT20:** 100 representative demand nodes and 20 selected existing healthcare facilities

In each instance, the representative demand-node locations also serve as candidate locations for the establishment of new healthcare facilities.

## Temporal Scope of the Data

The source datasets represent specific time periods and should not be interpreted as real-time data.

In particular:

- the population data represent the spatial distribution of the Hong Kong population in **2023**;
- the healthcare facility information reflects the OpenStreetMap records available at the time the data were collected for this study; and
- the healthcare service statistics are based on the **Hospital Authority Statistical Report 2023–2024**.

Population distributions, healthcare facility information, and healthcare service statistics may change over time. Therefore, the processed datasets provided in this repository represent the data conditions used in the study rather than current conditions in Hong Kong.

## Availability

The processed, ready-to-use experimental datasets used in the study are available from the first author upon reasonable request.

**Contact:**  
Praeploy Poonprapan  
Email: praeploy.po@kkumail.com

No formal application or data use agreement is required to request the processed datasets.

This repository is currently maintained for the associated research study and will be made publicly available following publication of the article.

## Related Publication

The detailed methodology for data preparation, service-capacity construction, optimization modeling, and computational experiments is described in the associated research article:

**A Hybrid NSGA-II–PSO Algorithm for Multi-Objective Healthcare Facility Location with TOPSIS-Based Decision Support**

The full citation and DOI will be added here after publication.
