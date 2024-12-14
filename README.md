# biomass_data

# Biomass Study Pipeline

This repository contains the workflow and scripts for conducting a biomass study, focusing on processing and analysing environmental data to predict above-ground biomass (AGB) across the Northern Territory, Australia. The pipeline integrates various datasets, including height metrics, vegetation density, climate variables, and fire history, to calculate zonal statistics and perform spatial analysis.

## Overview

The biomass study leverages geospatial and statistical methodologies to analyse and model biomass. The project involves pre-processing environmental layers, computing zonal statistics, and integrating diverse datasets for analysis.

## Key Steps in the Pipeline

### 1. Process Height

- Derive canopy height metrics, including 95th percentile, standard deviation, and median height values.
- Process satellite imagery (e.g., LiDAR or Sentinel-2) to extract relevant height features.
- **Output**: Raster datasets containing height metrics.

### 2. Process Density

- Compute vegetation density metrics from remote sensing data.
- Integrate NDVI, MSR vegetation indices, or similar proxies for density analysis.
- **Output**: Density rasters for further analysis.

### 3. Process SILO (Climate Data)

- Extract climate variables such as temperature, rainfall, and humidity from the SILO database.
- Summarise variables for wet and dry seasons.
- **Output**: Raster datasets and time series for climate variables.

### 4. Process Fire

- Analyse fire history data for the study region.
- Compute fire frequency, time since last fire, and fire severity metrics.
- **Output**: Fire metrics rasters.

## Zonal Statistics

### 5. Calculate Zonal Stats

- Aggregate spatial data for each site to calculate zonal statistics.
- Summarise height, density, climate, and fire metrics within site boundaries.
- **Output**: CSV or DataFrame summarising zonal statistics by site.

### 6. Spectral Reflectance (SR)

- Integrate spectral reflectance data from satellite imagery.
- Compute key indices such as NDVI and MSR for site-level analysis.
- **Output**: SR-derived metrics summarised by site.

## Workflow Structure

### Notebooks

- `process_height.ipynb`: Scripts for height metric processing.
- `process_density.ipynb`: Scripts for density data analysis.
- `process_silo.ipynb`: SILO climate data extraction and summarisation.
- `process_fire.ipynb`: Fire history analysis and metric derivation.
- `zonal_stats.ipynb`: Zonal statistics calculation for all datasets.
- `spectral_reflectance.ipynb`: SR computation and integration.

### Pipelines

- `height_pipeline.py`
- `density_pipeline.py`
- `silo_pipeline.py`
- `fire_pipeline.py`
- `zonal_stats_pipeline.py`
- `sr_pipeline.py`

### Outputs

- Final CSV files summarising site-level statistics.
- Raster datasets for visualisation and further analysis.

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/biomass-study.git
   cd biomass-study