
# Remote Sensing Toolkit (RST) — QGIS Plugin
## 🖼️ Plugin Interface

![RST Interface](img/icon.png)

The **Remote Sensing Toolkit (RST)** is an open-source QGIS plugin designed to streamline the computation and analysis of biophysical indices, particularly for time series studies. It features an intuitive interface, support for multiple satellite platforms, and built-in time series analysis tools. RST is ideal for both novice and expert users in remote sensing.

## 🔍 Quick Overview
- Compute vegetation, water, soil, burn, and other indices from AVHRR, MODIS, Landsat-8, Sentinel-2, and ASTER.
- Easily apply cloud masking, clip rasters, and export statistical summaries.
- Perform time series forecasting directly within QGIS.

---

## 🚀 Installation

### 1. Install QGIS
Download and install QGIS 3.0 from the [official QGIS website](https://qgis.org).

### 2. Install Required Python Packages
The plugin depends on `numpy`, `pandas`, and `openpyxl`.  
Use the provided `requirements.txt` file and install via command line:

```bash
pip install -r requirements.txt
```

**Note:** Ensure you use the version of Python that QGIS uses, or the plugin will not function properly.

### 3. Install the Plugin

**Option A:** From QGIS Plugin Manager  
- Open QGIS → *Plugins* → *Manage and Install Plugins*
- Search for **RST**
- Click **Install**

**Option B:** Manual Installation  
- Download the plugin from the [GitHub repository](https://github.com/RST-Plugin/RST)
- In QGIS: *Plugins* → *Install from ZIP* → Select the downloaded file

---

## ⚙️ Features & Workflow

RST includes a dock widget and dialog widgets for file/manual input. The plugin interface allows:

1. Selecting a satellite and associated index
2. Automatically displaying the formula for each index
3. Manually inputting required bands or selecting folders
4. Applying optional raster clipping (masking)
5. Setting output folder and computing results
6. Exporting statistics: mean, min, max, std dev, variance (in `.txt`, `.csv`, and Excel with charts)

### 🌍 Supported Masking Options
- **File selection**: Requires a folder with rasters + a vector layer in `.gpkg` format
- **Manual selection**: Allows a different mask per raster

---

## 📁 Output
- Computed index rasters
- Statistical summaries (if enabled)
- All saved to your selected output folder

---

## 🧠 Tips for Best Experience

- ✔️ Add RST icon to toolbar (right-click toolbar → enable RST)
- 🗂️ Organize raster folders carefully to prevent mismatched bands
- ✂️ Clip rasters before computing indices (especially for high-res data)
- 📂 Choose an empty folder as output to avoid conflicts or errors

---

## 🛠️ Troubleshooting

| Issue | Solution |
|-------|----------|
| Plugin not detecting installed packages | Make sure they're installed for **QGIS's Python version** |
| Errors with raster input | Ensure proper file structure and naming for each satellite |
| Output missing | Double-check the output folder and whether the "Save to Run" button was clicked |

---

## 📚 More Info

- Full documentation available in the compiled help file included in the plugin ZIP
- [GitHub Repository](https://github.com/RST-Plugin/RST)
