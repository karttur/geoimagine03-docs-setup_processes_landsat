---
layout: article
title: landregion-landsat-scenes-2D_v090.json
categories: setup_processes
excerpt: json/landregion-landsat-scenes-1D_v090.json
tags:: 
    - json/landregion-landsat-scenes-2D
date: 2021-12-16
modified: 2021-12-16
comments: true
share: true
---

# json/landregion landsat scenes 2D (setup_processes)

### json/landregion-landsat-scenes-1D_v090.json

The json command file <span class='file'>landregion-landsat-scenes-2D_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
    "startyear": 2014,
    "endyear": 2014,
    "timestep": "singleyear"
  },
  "process": [
    {
      "processid": "LinkDefaultRegionScenes",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "defregmask": "None",
        "regioncat": "global",
        "dir": "D",
        "wrs": 2,
        "regionid": "land",
        "ogr2ogr": true,
        "cmdpath": "/usr/local/bin",
        "clipsrc": "-180,0,180,90",
        "onlytiling": true,
        "minarea": 0.0
      },
      "srcpath": {
        "volume": "GeoImg2021",
        "hdr": "shp",
        "dat": "shp"
      },
      "dstpath": {
        "volume": "GeoImg2021",
        "hdr": "shp",
        "dat": "shp"
      },
      "srccomp": [
        {
          "regions": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "tol@1km"
          }
        }
      ],
      "dstcomp": [
        {
          "region": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "tol@1km"
          }
        }
      ]
    }
  ]
}
```
