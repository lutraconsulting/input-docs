---
layout: page
permalink: /howto/settingup_background_map_vectortile
---

# Vector tiles

Vector tiles are a better alternative for cartography maps as background data. It is lighter in size, flexible styling and your maps are not pixelated.

## Online services

There are several online services. For example you can add ESRI Basemap vector tile (QGIS 3.16+):

- In QGIS, from the **Browser panel** right-click on **Vector Tiles**
- Select **New Generic Connection**
- A new window will appear:
    - For **Name** type: **ESRI Basemap**
    - For **URL** type: **https://basemaps.arcgis.com/v1/arcgis/rest/services/World_Basemap/VectorTileServer/tile/{z}/{y}/{x}.pbf**
    - Set **Min. Zoom Level** to **0**
    - Set **Max. Zoom Level** to **14**
    - For **Style URL** type: **https://basemaps.arcgis.com/b2/arcgis/rest/services/World_Basemap/VectorTileServer/resources/styles/root.json**

![new xyz connection](../images/qgis_xyz_gen_vectortile.png)

Another source of online vector tiles are Qwant maps:
- In QGIS, from the **Browser panel** right-click on **Vector Tiles**
- Select **New Generic Connection**
- A new window will appear:
    - For **Name** type: **Qwant map**
    - For **URL** type: **https://www.qwant.com/maps/tiles/ozbasemap/{z}/{x}/{y}.pbf**
    - Set **Min. Zoom Level** to **0**
    - Set **Max. Zoom Level** to **14**
    - For **Style URL** type: **https://raw.githubusercontent.com/QwantResearch/qwant-basic-gl-style/master/style.json**


## Generating vector tiles for offline use
In QGIS (3.14+), you can generate your own vector tiles. Alternatively, you can generate vector tiles using OpenMapTiles from OpenStreetMap data.
