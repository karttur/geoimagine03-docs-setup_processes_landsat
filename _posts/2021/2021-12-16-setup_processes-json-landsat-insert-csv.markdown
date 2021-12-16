---
layout: article
title: landsat-insert-csv_v090.json
categories: setup_processes
excerpt: \# Insert region to Landsat WRS links from csv
tags:: 
    - json/landsat-insert-csv
date: 2021-12-16
modified: 2021-12-16
comments: true
share: true
---

# json/landsat insert csv (setup_processes)

### \# Insert region to Landsat WRS links from csv

The json command file <span class='file'>landsat-insert-csv_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
      "processid": "InsertTableCsv",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "schema": "landsat",
        "table": "scenecoords"
      },
      "srcpath": {
        "volume": ".",
        "hdr": "csv"
      }
    },
    {
      "processid": "InsertTableCsv",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "schema": "landsat",
        "table": "regions"
      },
      "srcpath": {
        "volume": ".",
        "hdr": "csv"
      }
    }
  ]
}
```
