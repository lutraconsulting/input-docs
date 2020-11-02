---
layout: page
permalink: /howto/package_qgis_project
---


To work with Input, you need to create a self contained folder with all your files. If you work with several data sources spread across multiple folders/drives, there are various tools and plugins in QGIS to copy your data to a self contained folder, ready to be transfered to Input.

# QGIS processing algorithm: Package layers

In QGIS, from **Processing Toolbox > Database > Package layers**, you can consolidate all your vector layers to a single GeoPackage. You can use this GeoPackage to generate a new project to use in Input.

# QConsolidate3

With [this plugin](https://github.com/danzig666/qconsolidate3/), you can copy all your vector layers to GeoPackage and save the project under a new folder. Note that the plugin, you will need to manually copy and move your raster data.


**Notes**:
- Each layer will be translated to a seprate GeoPackage file.
- Symbology, layer styling and Map Themes will be preserved
- Reference to SVGs will be lost
- Reference to external services will be maintained (e.g. XYZ tiles, WM(T)S)
- Raster layers need to be handled manually

