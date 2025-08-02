# Tuberculosis Units Kerala Shapefile

## Overview
This shapefile contains the spatial boundaries of Tuberculosis Units (TUs) in Kerala, India. The dataset represents 77 tuberculosis administrative units across various districts in the state, providing comprehensive coverage for TB surveillance and management purposes.

## Dataset Specifications

### Spatial Properties
- **Feature Count**: 77 tuberculosis units
- **Geometry Type**: MULTIPOLYGON
- **Dimension**: XY (2D)
- **Coordinate Reference System**: WGS 84 / UTM zone 43N (EPSG:32643)


### Attribute Fields
The shapefile contains 3 attribute fields:

| Field Name | Type | Description |
|------------|------|-------------|
| `fid` | Integer | Feature identifier (1-77) |
| `District` | String | District name where the TU is located |
| `TU_Name` | String | Tuberculosis Unit name |

### Sample Data
The dataset includes tuberculosis units from multiple districts such as:
- **Kasaragod**: Kasaragod_TU, Panathady_TU, Kanhangad_TU
- **Kannur**: Payannur_TU, Taliparamba_TU, DTC_Kannur_TU, Iritty_TU, Kuthuparamba_TU, Thalassery_TU
- **Wayanad**: DTC_TU_Wayanad
- And others across Kerala

## File Components
This shapefile dataset consists of multiple files with the same base name:

- `tuberculosis_units_kerala.shp` - Main shapefile containing geometry
- `tuberculosis_units_kerala.shx` - Shape index file
- `tuberculosis_units_kerala.dbf` - Attribute database file
- `tuberculosis_units_kerala.prj` - Projection information file
- Additional metadata files may be present (.xml, .cpg, etc.)

## Usage Notes

### Loading in R

```r
library(sf)
library(here)

tu_sf <- st_read(here::here("data", "formats", "shapefile", 
                      "tuberculosis_units_kerala",
                      "tuberculosis_units_kerala.shp"))
```

*NOTE*: The path to the file may change based on where you save the file

### Coordinate System
The data is projected in UTM Zone 43N, which is appropriate for Kerala's geographic location. If you need to work with other datasets, you may need to transform to a common coordinate system:

```r
# Transform to WGS84 geographic coordinates
tu_sf_wgs84 <- st_transform(tu_sf, crs = 4326)

```

## Contact/Source
This dataset appears to be part of the AMCHSS (Achutha Menon Centre for Health Science Studies) spatial data library. 
For questions about data source, methodology, or updates, contact [amchss.sctimst@gmail.com].

## Last Updated

02-08-2025

