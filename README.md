## 🛠️ Technical Pipeline & Data Architecture

This project implements a full-stack spatial data pipeline—bridging cloud-based satellite data processing, cloud GIS cartography, and reactive web development.

[ 🌌 Copernicus CDSE ] ──(JupyterLab / Python)──> [ 🗺️ GeoTIFF Rasters ] ──> [ ⚡ Felt GIS ] ──> [ 🚀 Netlify Frontend ]

### 1. Data Ingestion & Processing (Copernicus JupyterLab)
* **Environment:** Leveraged the **Copernicus Data Space Ecosystem (CDSE) JupyterHub** cloud environment to write Python scripts for processing raw satellite data.
* **Geospatial Processing:** Clipped, filtered, and processed cloud-masked imagery to extract state-wide raster layers (`.tif` format) specifically bounded to the geographic borders of Telangana.

### 2. Satellite Constellations Used
* **Sentinel-2 (MSI):** Used to compute the **NDVI** (Normalized Difference Vegetation Index) and **NDWI** (Normalized Difference Water Index) to monitor canopy density and surface water availability.
* **Sentinel-3 (SLSTR):** Utilized thermal infrared bands to compute the **Land Surface Temperature (LST)** profile and map urban heat islands.
* **Sentinel-5P (TROPOMI):** Processed atmospheric gas concentrations to monitor localized **NO₂ (Nitrogen Dioxide) emissions** over industrial and metropolitan transport corridors.

### 3. Visualization & Cartography (Felt GIS)
* The processed multi-temporal raster datasets were exported as high-resolution GeoTIFFs and imported into **Felt GIS**.
* Applied custom visualization tokens, color ramps, and vector boundaries within the Felt engine to enable interactive cloud-based map panning, zooming, and spatial data inspection.

### 4. Application Hosting (Netlify)
* Engineered a responsive single-page diagnostic dashboard UI using **Tailwind CSS** and **Vanilla JavaScript** to handle drop-down conditional UI state transitions.
* Embedded the public Felt GIS frame canvas seamlessly alongside the data tracking matrix.
* Deployed the complete optimized frontend repository via **Netlify** for high-availability production delivery.