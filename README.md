## PostGIS batch export to (zipped) shapefile
With this script you can export to zipped shapefiles all spatial tables (or views) from a given schema.

You can use two engines (ENGINE parameter in config file):
- ogr2ogr
- pgsql2shp

Each engine can be better than the other depending on the context (you can try both!).

You must specify tables or views (QUERYTYPE parameter in config file).

### Config file
Before execute this script you need a CONFIGFILE properly formed (See CONFIGFILE_example) in your current/working directory.

```
CRS_EPSG=4326
DATABASE=mydatabase
HOST=myhost
USER=myuser
PORT=5432
DBSCHEMA=mydbschema
EXPORTFOLDER=/tmp/shp_exp
ENGINE=pgsql2shp
QUERYTYPE=views
```

## Requirements
- GDAL.
- pgsql2shp.
- psycopg2.

## About author
Developed by Cayetano Benavent.
GIS Analyst at Geographica.

http://www.geographica.gs


## License
This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 2 of the License, or
(at your option) any later version.
