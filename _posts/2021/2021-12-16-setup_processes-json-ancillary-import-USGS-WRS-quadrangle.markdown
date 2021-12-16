---
layout: article
title: ancillary-import-USGS-WRS-quadrangle_v090.json
categories: setup_processes
excerpt: \# Import Landsat WRS scene positions as quadrangles
tags:: 
    - json/ancillary-import-USGS-WRS-quadrangle
date: 2021-12-16
modified: 2021-12-16
comments: true
share: true
---

# json/ancillary import USGS WRS quadrangle (setup_processes)

### \# Import Landsat WRS scene positions as quadrangles

The json command file <span class='file'>ancillary-import-USGS-WRS-quadrangle_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

```
{
  "userproject": {
    "userid": "karttur",
    "projectid": "karttur",
    "tractid": "karttur",
    "siteid": "*",
    "plotid": "*",
    "system": "ancillary"
  },
  "process": [
    {
      "processid": "OrganizeAncillary",
      "overwrite": false,
      "parameters": {
        "importcode": "shp",
        "epsg": "4326",
        "orgid": "USGS",
        "dsname": "USGSWRS",
        "dsversion": "1.0",
        "accessdate": "20050320",
        "regionid": "globe",
        "regioncat": "globe",
        "dataurl": "",
        "metaurl": "",
        "title": "USGS Landsat WRS",
        "label": "USGS Landsat WRS scene positions",
        "tolerance": 0.1,
        "angletolerance": 0,
        "quadrangle": true
      },
      "srcpath": {
        "volume": ".",
        "hdr": "shp",
        "dat": ""
      },
      "dstpath": {
        "volume": "GeoImg2021",
        "hdr": "shp",
        "dat": ""
      },
      "srcraw": [
        {
          "wrs1ascdesc": {
            "datadir": "data/USGS/wrs1_asc_desc",
            "datafile": "wrs1ascdesc_wrs_global_0_quad",
            "datalayer": "wrs1ascdesc_wrs_global_0_quad",
            "title": "Landsat WRS1 ascending and descending scene positions",
            "label": "Landsat WRS1 ascending and descending scene positions"
          }
        },
        {
          "wrs2ascdesc": {
            "datadir": "data/USGS/wrs2_asc_desc",
            "datafile": "wrs2ascdesc_wrs_global_0_quad",
            "datalayer": "wrs2ascdesc_wrs_global_0_quad",
            "title": "Landsat WRS2 ascending and descending scene positions",
            "label": "Landsat WRS2 ascending and descending scene positions"
          }
        },
        {
          "wrs1desc": {
            "datadir": "data/USGS/wrs1_descending",
            "datafile": "wrs1desc_wrs_global_0_quad",
            "datalayer": "wrs1desc_wrs_global_0_quad",
            "title": "Landsat WRS1 descending scene positions",
            "label": "Landsat WRS1 descending scene positions"
          }
        },
        {
          "wrs2desc": {
            "datadir": "data/USGS/wrs2_descending",
            "datafile": "wrs2desc_wrs_global_0_quad",
            "datalayer": "wrs2desc_wrs_global_0_quad",
            "title": "Landsat WRS2 descending scene positions",
            "label": "Landsat WRS2 descending scene positions"
          }
        }
      ],
      "dstcomp": [
        {
          "wrs1ascdesc": {
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
        },
        {
          "wrs2ascdesc": {
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
        },
        {
          "wrs1desc": {
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
        },
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
