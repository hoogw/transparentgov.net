# transparentgov.net


https://transparentgov.net

 ESRI and Socrata constantly change their REST Service API without notice ! Without fix it can severely damage transparentgov.net availability and performance. Recently ESRI update 3D scene layer REST API on all organization's arcgis Server upgrade package. ESRI's upgrade package has unfixed bugs, this bug cause transparentgove.net outage. All search layer page failure. I had fixed this issue for now. But in future I hope you and any one can help report the issue, so I can fix the bug. 

              Map Engine used in transparentgov.net supposed to work with any organization's arcgis online portal, arcgis server.  However, different org can set up and config their arcgis server differently. As well as using different projection for their data.  This map engine is build to support all org from east coast to west coast even Europ and Asia etc by automatically re-projection from cutomized projection for example state plane to web mercator WGS84 (EPSG:4326) on google maps, bing maps,  and  pseudo-Mercator (EPSG:3857) on openlayers, esri maps. Be aware that EPSG:3857 is projected coordinate system, is not a sphere, no lat long, instead it is a plane with x,y coordinate.  EPSG:4326 is geographic coordinate system, it is a sphere, with lat, long coordinate. For example, openlayers use projected EPSG:3857,  your city data use 'state plane california 5',  Map engine will automatically re-project from state plane to 3857.  If the base map is google maps or mapbox, map engine will auto re-project your data from state plane to 4326.  If you have lat long, in order to show on openlayers, you have to re-project it from 4326 to 3857.  REST api on arcgis server can be config differently. Some org disabled CORS, but enabled JSONP, Some org disabled both. Some org enabled both. That is why 3 google map icon provided, one for CORS, one for JSONP, one for Proxy.  If arcgis server's admin disabled both CORS and JSONP, at least Proxy icon still works. Think about transparentgov.net support over 10,000 arcgis online portal and arcgis server, it must be some org's arcgis server configuration I have not cover yet. In that case, you can not browsing that org's arcgis server or portal through transparentgov.net. You will have a error on map engine. Please report that org's name and arcgis server URL to creator. I can improve the map engine to accommodate more special case.

               You can report bug issue at   create a new issue at github.com 

                 Some organization may shut down their arcgis server on week end for maintenance.  Some organization may change their arcgis server domain name to a different one without a notice. That is why you may experience broken links.  Report that organization to me, so I can update our database to fix that broken links. 

                 





Simple is beauty        

All  Data  are  Location  Based     

Map engine now support .kml file and .shp shape file along with .geojson
Map engine now support arcgis rest api, socrata SODA api and many many vendor specialized api running on Oracle, SQLserver, MySQL, MongoDB, Postgre, SQLite.
Map engine (designed for bulk load) can handle unlimit size of dataset. Now your device(pc/tablet/mobile) memory capacity is your limit. The larger RAM memory you have, the larger dataset you can see. One million parcels can cause a 2GB memory PC browser not responsive.


How can I view one million parcels on 2GB memory PC? Just use the map engine (designed for progressive loading). Capacity limit, performance, speed rely on remote server ( arcgis, socrata etc.) , not your device CPU RAM.  


Map engine (designed for bulk load)  can load .geojson file, shape file (.shp), zipped shape file (.zip), .kml file,  zipped kml file (.kmz) etc directly. eliminate the need for arcgis server and socrata server,  lower the bar of gis data distribution.  You can share your shape file,geojson, kml file to the world by simple copy past to any cloud drive ( OneDrive, DropBox, GoogleDrive, Box.com, Amazon Cloud Drive, Microsoft Azure, Google Cloud Drive etc...).  Then copy your shape file/geojson/kml URL on dropbox or box.com, use        geojson viewer,        shape file (.shp) viewer,       .kml .kmz viewer    generated a permanent url link. You can bookmark this permanent url link or share with your audience. With this permanent url link, the world can see your gis data on googleMaps, bingMaps, hereMap, openlayers, leaflet, appleMaps as of users choice.


GIS data distribution was simplified from previous expensive complex arcgis server/socrata server to a simple, zero cost, free cloud file distribution.  Complex spatial query/indexing in terms of browsing map data and keyword searching was moved from previous remote server (arcgis server/socrata server) to our bulk load map engine. Now any one can upload shape file/geojson/kml to any cloud drive vendor and generate permanent viewer url link, share with the world at zero cost!


Spatial indexing powered by RTree .  Now 1 million parcels will NOT freeze your browser.  Before this improvement, any dataset with more than 5000 records will freeze your browser, make your browser not responsive even crash.
