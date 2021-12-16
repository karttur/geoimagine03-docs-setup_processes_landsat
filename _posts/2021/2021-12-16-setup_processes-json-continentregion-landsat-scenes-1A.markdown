---
layout: article
title: continentregion-landsat-scenes-1A_v090.json
categories: setup_processes
excerpt: \# With the land region linked, restrict search and link continents and countries
tags:: 
    - json/continentregion-landsat-scenes-1A
date: 2021-12-16
modified: 2021-12-16
comments: true
share: true
---

# json/continentregion landsat scenes 1A (setup_processes)

### \# With the land region linked, restrict search and link continents and countries

The json command file <span class='file'>continentregion-landsat-scenes-1A_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
        "defregmask": "land",
        "regioncat": "continent",
        "dir": "A",
        "wrs": 1,
        "ogr2ogr": true,
        "cmdpath": "/usr/local/bin",
        "clipsrc": "-180,0,180,90",
        "onlytiling": false,
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
          },
          "tiles": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "tiles",
            "prefix": "tiles-wrs1-A",
            "suffix": "0"
          }
        }
      ]
    }
  ]
}
```
