# Steps to Calculate NDVI with QGIS 🌿

This document includes the steps to calculate NDVI (Normalized Difference Vegetation Index) in QGIS using Sentinel-2 satellite images.

---

## 🛰️ 1. Download Satellite Imagery
- Download Sentinel-2 L2A data from [Copernicus Open Access Hub](https://scihub.copernicus.eu/).
- Required bands:
- **Band 4 (Red)**
- **Band 8 (NIR - Near Infrared)**

---

## 📥 2. Load Bands into QGIS
- Open QGIS.
- From the menu: `Layer > Add Layer > Add Raster Layer`
- Load the downloaded `.jp2` or `.tif` format Band 4 and Band 8 files.

---

## 🧮 3. NDVI Calculation (Raster Calculator)
- From the menu: `Raster > Raster Calculator`
- Write the following in the formula field:

- Note: Use the band names as they appear on the map (for example, `"T34SFC_20240601T081601_B08"`).

- Save the output as `.tif` and add it to your project.

---

## 🎨 4. Color Scale and Rendering
- Right click on the NDVI raster layer > **Properties**
- From the `Symbology` tab:
- Render type: `Singleband pseudocolor`
- Color scale: Green (high NDVI) → Red (low NDVI)
- Set the range to be between `-1` and `+1`.

---

## 🗺️ 5. Print the Map
- From the menu: `Project > New Print Layout`
- Lay out your map, add title, description, legend and north arrow.
- Print with `Layout > Export as PNG/PDF`.

---

## 📝 Notes
- NDVI may be unreliable in cloudy images.
- NDVI value varies between -1 and +1.
- Below 0.2 = poor vegetation
- 0.3-0.6 = healthy
- Above 0.6 = dense and vibrant vegetation
