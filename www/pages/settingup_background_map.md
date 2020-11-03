---
layout: page
permalink: /howto/settingup_background_map
---

When surveying in the field, it is essential to have appropriate background maps. There are several sources of online and offline background maps you can use in your QGIS project. Note that you need to comply with the terms of use of the background maps and their data sources. This page simply explains how to add the data to your QGIS maps and use it in Input. It will be the sole responsibility of the end user to comply with such terms and conditions.

# Raster tiles

## Online services

[QGIS comes by default with the OpenStreetMap online services for XYZ tiles](https://docs.qgis.org/3.10/en/docs/user_manual/managing_data_source/opening_data.html?highlight=xyz#using-xyz-tile-services). When adding cartographic basemap, ensure you set the tile size correctly, so that the texts and labels are readable on mobile devices with high resolution display.

You can also add [other sources](https://gis.stackexchange.com/questions/20191/adding-basemaps-from-google-or-bing-in-qgis/217670#217670) of XYZ tiles to your QGIS.

## Generating raster tiles
QGIS also offers a [processing algorithm](https://docs.qgis.org/3.10/en/docs/user_manual/processing_algs/qgis/rastertools.html) to generate [your own XYZ tiles](https://ocw.un-ihe.org/mod/book/tool/print/index.php?id=5497&chapterid=491) for offline use.

# Vector tiles

Vector tiles are a better alternative for cartography maps as background data. It is lighter in size, flexible styling and your maps are not pixelated.

## Online services

There are several online services. For example you can add ESRI Basemap vector tile (QGIS 3.16+):

- In QGIS, from the **Browser panel** right-click on **Vector Tiles**
- Select **New ArcGIS Server Vector Tile Service Connection**
- A new window will appear:
    - For **Name** type: **ESRI Basemap**
    - For **URL** type: **https://basemaps.arcgis.com/v1/arcgis/rest/services/World_Basemap/VectorTileServer/tile/{z}/{y}/{x}.pbf**
    - Set **Min. Zoom Level** to **0**
    - Set **Max. Zoom Level** to **14**
    - For **Style URL** type: **https://basemaps.arcgis.com/b2/arcgis/rest/services/World_Basemap/VectorTileServer/resources/styles/root.json**
    
Another source of online vector tiles are Qwant maps:
- In QGIS, from the **Browser panel** right-click on **Vector Tiles**
- Select **New Generic Connection**
- A new window will appear:
    - For **Name** type: **Qwant map**
    - For **URL** type: **https://www.qwant.com/maps/tiles/ozbasemap/{z}/{x}/{y}.pbf**
    - Set **Min. Zoom Level** to **0**
    - Set **Max. Zoom Level** to **14**
    - For **Style URL** type: **https://raw.githubusercontent.com/QwantResearch/qwant-basic-gl-style/master/style.json**


## Generating vector tiles
In QGIS (3.14+), you can generate your own vector tiles. Alternatively, you can generate vector tiles using OpenMapTiles from OpenStreetMap data.
