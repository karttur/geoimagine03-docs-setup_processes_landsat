---
layout: article
title: wrs-extract_tile_coords_v090.json
categories: setup_processes
excerpt: \# Extract WRS tile coordinates to database
tags:: 
    - json/wrs-extract_tile_coords
date: 2021-12-16
modified: 2021-12-16
comments: true
share: true
---

# json/wrs extract tile coords (setup_processes)

### \# Extract WRS tile coordinates to database

The json command file <span class='file'>wrs-extract_tile_coords_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

```
{
  "userproject": {
    "userid": "karttur",
    "projectid": "karttur",
    "tractid": "karttur",
    "siteid": "*",
    "plotid": "*",
    "system": "landsat"
  },
  "period": {
    "timestep": "static"
  },
  "process": [
    {
      "processid": "ExtractTileCoords",
      "dsversion": "0.9",
      "parameters": {
        "centroid": true,
        "wrs": 1,
        "wrspath": "PATH",
        "wrsrow": "ROW_",
        "wrsmode": "MODE_"
      },
      "srcpath": {
        "volume": "GeoImg2021",
        "hdr": "shp",
        "dat": "shp"
      },
      "srccomp": [
        {
          "wrs2desc": {
            "source": "USGS",
            "product": "wrs",
            "content": "wrspos",
            "layerid": "wrs1ascdesc",
            "prefix": "wrs1ascdesc",
            "suffix": "quad",
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": "-32768",
            "masked": "Y",
            "measure": "N"
          }
        }
      ]
    },
    {
      "processid": "ExtractTileCoords",
      "dsversion": "0.9",
      "parameters": {
        "centroid": true,
        "wrs": 2,
        "wrspath": "PATH",
        "wrsrow": "ROW",
        "wrsmode": "MODE"
      },
      "srcpath": {
        "volume": "GeoImg2021",
        "hdr": "shp",
        "dat": "shp"
      },
      "srccomp": [
        {
          "wrs2desc": {
            "source": "USGS",
            "product": "wrs",
            "content": "wrspos",
            "layerid": "wrs2ascdesc",
            "prefix": "wrs2ascdesc",
            "suffix": "quad",
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": "-32768",
            "masked": "Y",
            "measure": "N"
          }
        }
      ]
    },
    {
      "processid": "ExtractTileCoords",
      "dsversion": "0.9",
      "parameters": {
        "centroid": true,
        "wrs": 1,
        "wrspath": "PATH",
        "wrsrow": "ROW_",
        "wrsmode": "MODE_"
      },
      "srcpath": {
        "volume": "GeoImg2021",
        "hdr": "shp",
        "dat": "shp"
      },
      "srccomp": [
        {
          "wrs2desc": {
            "source": "USGS",
            "product": "wrs",
            "content": "wrspos",
            "layerid": "wrs1desc",
            "prefix": "wrs1desc",
            "suffix": "quad",
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": "-32768",
            "masked": "Y",
            "measure": "N"
          }
        }
      ]
    },
    {
      "processid": "ExtractTileCoords",
      "dsversion": "0.9",
      "parameters": {
        "centroid": true,
        "wrs": 2,
        "wrspath": "PATH",
        "wrsrow": "ROW",
        "wrsmode": "MODE"
      },
      "srcpath": {
        "volume": "GeoImg2021",
        "hdr": "shp",
        "dat": "shp"
      },
      "srccomp": [
        {
          "wrs2desc": {
            "source": "USGS",
            "product": "wrs",
            "content": "wrspos",
            "layerid": "wrs2desc",
            "prefix": "wrs2desc",
            "suffix": "quad",
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": "-32768",
            "masked": "Y",
            "measure": "N"
          }
        }
      ]
    }
  ]
}
```
