BiGCZ GeoJSON files
====================================

See http://geojson.org for GeoJSON specification. http://geojson.io enables an interactive creation and examination of GeoJSON data. Onehandy reason for converting to GeoJSON as an intermediate format is that github provides native map rendering of geojson files, so you get a simple map visualization w/o doing any extra work (and the markers are clickable, so you can explore the attributes). These files can also be downloaded and easily opened in desktop GIS clients like QGIS.

* [IGSN samples GeoJSON:](https://github.com/emiliom/mapdata/blob/master/igsn_czoshalehills_validresp_fc.geojson) I've examined the web service responses (requested by IGSN number) for the Shale Hills CZO IGSN's that Megan sent me in November. A little less than half of the ~1,700 IGSN's generated XML parsing errors with the standard Python XML parser I used, and my limited testing suggests that these are due to invalid (or not properly escaped) "<" and ">" characters in the XML responses; I ignored those. Of the remaining ~950 IGSN's, ~400 had no latitude and longitude entries ("Not Provided"). In order to examine the remaining IGSN sample responses, I first converted them into a standard GeoJSON structure, before converting and subsetting to what we'll use in the initial visualization portal test/pilot. The GeoJSON file available here has all ~550 IGSN's with lat & lon entries.

* [MG-RAST metagenomic GeoJSON:](https://github.com/emiliom/mapdata/blob/master/mgrast_usa1_fc.geojson)
