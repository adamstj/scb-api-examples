# scb-api-examples
Some notebooks I created for fetching DeSO (Swedish census data) area data. Transformation of the data and insert to PostgreSQL is also included

## Introduction:
This repository holds some example notebooks which I created when fetching census data from the [SCB API](https://www.scb.se/en/services/open-data-api/api-for-the-statistical-database/). SCB is the Central Bureau of Statistics in Sweden (Nowadays '[Statistics Sweden](https://www.scb.se/en/)').
For ease of use I used the python wrapper, [pyscbwrapper](https://github.com/kirajcg/pyscbwrapper), which also holds its own example code. I made this repository primarily for myself and I dont believe it is clearer than theirs, but I leave it public if it may help someone.

As told in their repository:

To install:
```python
pip install pyscbwrapper
```
To import:
```python
from pyscbwrapper import SCB
```

## Fetch data
The DeSO areas themselves, i.e., the polygon dataset, was downloaded directly as a geopackage (gpkg) from [SCB](https://www.scb.se/en/services/open-data-api/open-geodata/deso--demographic-statistical-areas/). With geopandas the GPKG was processed, see [notebook], and then imported to PostGIS using the shp2pgsql tool.

Examples of fetching the DeSO census data from the SCB API can be found in the [api-fetch-notebooks folder](/api-fetch-notebooks).


## Transform data
Examples of transforming the DeSO census csv-files fetched from the SCB API can be found in the [csv-to-postgresql folder](/csv-to-postgresql).
