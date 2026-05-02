# AZ-Corridor-Monitor: Automated Vegetation Monitoring

**Author:** [Your Name]
**Role:** Environmental Data Analyst

## Project Objective
Automate hazard-tree mitigation reporting for proposed transmission line corridors in the US Southwest. This tool programmatically generates biological survey corridors and analyzes real-time satellite imagery to assess vegetation density.

## Technical Architecture
* **Data Ingestion:** Streams real-time, cloud-free Sentinel-2 Surface Reflectance (L2A) imagery via the AWS Earth Search STAC API.
* **Spatial Processing:** Utilizes `geopandas` and `shapely` to project, buffer (2-mile), and map proposed transmission routes (EPSG:26912/4326).
* **Zonal Statistics:** Deploys `rasterio` to dynamically mask multi-band GeoTIFFs and calculate the Normalized Difference Vegetation Index (NDVI) strictly within the corridor footprint.

## Core Deliverable
The primary analytical engine and automated mitigation report are documented in the interactive Jupyter Notebook:
[`notebooks/01_stac_discovery.ipynb`](notebooks/01_stac_discovery.ipynb)