---
layout: article
title: landsat-export-csv_v090.json
categories: setup_processes
excerpt: \# Export linked landregion as csv
tags:: 
    - json/landsat-export-csv
date: 2021-12-16
modified: 2021-12-16
comments: true
share: true
---

# json/landsat export csv (setup_processes)

### \# Export linked landregion as csv

The json command file <span class='file'>landsat-export-csv_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
      "processid": "ExportTableCsv",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "schema": "landsat",
        "table": "regions"
      },
      "dstpath": {
        "volume": "GeoImg2021",
        "hdr": "csv",
        "dat": "shp"
      }
    },
    {
      "processid": "ExportSchemaCsv",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "schema": "landsat"
      },
      "dstpath": {
        "volume": "GeoImg2021",
        "hdr": "csv",
        "dat": "shp"
      }
    }
  ]
}
```
