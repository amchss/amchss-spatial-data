# AMCHSS Spatial Data Resources

**Comprehensive geospatial datasets designed for researchers, GIS professionals, and data scientists.**

🌐 **Website:** [https://amchss.github.io/amchss-spatial-data](https://amchss.github.io/amchss-spatial-data)

## 📋 Overview

This repository contains high-quality spatial datasets from AMCHSS (Achutha Menon Centre for Health Science Studies) research initiatives. Currently featuring **Tuberculosis Units in Kerala, India** - a comprehensive dataset of 77 tuberculosis administrative units across various districts in the state.

### Key Features

- **Multiple Formats**: Available in Shapefile, GeoJSON, R Data, and KML formats
- **Open Access**: Available under MIT License for research and education
- **High-Quality Data**: 77 spatial features with complete attribute information
- **Ready-to-Use**: Includes documentation, examples, and citation guidelines

## 📊 Dataset Details

### Tuberculosis Units - Kerala

- **Total Records:** 77 spatial features
- **Geometry Type:** MULTIPOLYGON
- **Coordinate System:** WGS 84 / UTM zone 43N (EPSG:32643)
- **Coverage:** All districts in Kerala state
- **Last Updated:** August 2025
- **Version:** 1.0.0

### Data Dictionary

| Field Name | Type    | Description                           |
|------------|---------|---------------------------------------|
| `fid`      | Integer | Feature identifier (1-77)             |
| `District` | String  | District name where the TU is located |
| `TU_Name`  | String  | Tuberculosis Unit name                |

### Sample Districts Included

- Kasaragod (Kasaragod_TU, Panathady_TU, Kanhangad_TU)
- Kannur (Payannur_TU, Taliparamba_TU, DTC_Kannur_TU, Iritty_TU, etc.)
- Wayanad (DTC_TU_Wayanad)
- And more across Kerala

## 📥 Downloads

| Format | Description | File Size | Best For | Download |
|--------|-------------|-----------|----------|----------|
| **Shapefile** | Traditional GIS format (includes .shp, .shx, .dbf, .prj files) | ~4.5 MB | Desktop GIS (ArcGIS, QGIS) | [Download](https://amchss.github.io/amchss-spatial-data/data/tuberculosis_units_kerala.zip) |
| **R Data** | Native R format using sf package | ~5.7 MB | R users, statistical analysis | [Download](https://amchss.github.io/amchss-spatial-data/data/tuberculosis_units_kerala.rds) |
| **GeoJSON** | Modern web-friendly spatial format | ~18.7 MB | Web applications, modern GIS | [Download](https://amchss.github.io/amchss-spatial-data/data/tuberculosis_units_kerala.geojson) |
| **KML** | Google Earth and GPS compatible | ~11.5 MB | Google Earth, web maps, GPS | [Download](https://amchss.github.io/amchss-spatial-data/data/tuberculosis_units_kerala.kml) |

## 💻 Usage Examples

### R (using sf package)

```r
# Load required libraries
library(sf)
library(tidyverse)

# Method 1: Load from RDS file (recommended)
tu_sf <- read_rds("tuberculosis_units_kerala.rds")

# Method 2: Load from shapefile
tu_sf <- st_read("tuberculosis_units_kerala.shp")

# Method 3: Load from GeoJSON
tu_sf <- st_read("tuberculosis_units_kerala.geojson")

# Basic plotting
tu_sf |> 
  ggplot() +
  geom_sf() +
  theme_minimal() +
  labs(title = "Tuberculosis Units in Kerala")

# Plot by District
tu_sf |> 
  ggplot() +
  geom_sf(aes(fill = District)) +
  theme_minimal() +
  labs(title = "TB Units by District",
       fill = "District") +
  theme(legend.position = "bottom")

# Summary statistics
tu_sf |> 
  st_drop_geometry() |> 
  count(District, sort = TRUE)
```


## 🚀 Getting Started

### Clone the Repository

```bash
git clone https://github.com/amchss/amchss-spatial-data.git
cd amchss-spatial-data
```

### Project Structure

```
amchss-spatial-data/
├── README.md                    # This file
├── _quarto.yml                  # Website configuration
├── index.qmd                    # Main website page
├── data/                        # Spatial datasets
│   ├── tuberculosis_units_kerala.zip
│   ├── tuberculosis_units_kerala.rds
│   ├── tuberculosis_units_kerala.geojson
│   └── tuberculosis_units_kerala.kml
├── docs/                        # Generated website (GitHub Pages)
└── styles/                      # Website styling
```

