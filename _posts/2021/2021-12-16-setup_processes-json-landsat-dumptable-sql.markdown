---
layout: article
title: landsat-dumptable-sql_v090.json
categories: setup_processes
excerpt: \# Dump linked landregion as sql
tags:: 
    - json/landsat-dumptable-sql
date: 2021-12-16
modified: 2021-12-16
comments: true
share: true
---

# json/landsat dumptable sql (setup_processes)

### \# Dump linked landregion as sql

The json command file <span class='file'>landsat-dumptable-sql_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

```
{
  "userproject": {
    "userid": "karttur",
    "projectid": "karttur",
    "tractid": "karttur",
    "siteid": "*",
    "plotid": "*",
    "system": "system"
  },
  "period": {
    "timestep": "static"
  },
  "process": [
    {
      "processid": "DumpTableSQL",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "schema": "landsat",
        "table": "scenecoords",
        "format": "p",
        "cmdpath": "/usr/local/bin",
        "dataonly": true,
        "definitiononly": false
      },
      "dstpath": {
        "volume": ".",
        "hdr": "shp",
        "dat": "shp"
      }
    },
    {
      "processid": "DumpTableSQL",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "schema": "landsat",
        "table": "regions",
        "format": "p",
        "cmdpath": "/usr/local/bin",
        "dataonly": true,
        "definitiononly": false
      },
      "dstpath": {
        "volume": ".",
        "hdr": "shp",
        "dat": "shp"
      }
    }
  ]
}
```
