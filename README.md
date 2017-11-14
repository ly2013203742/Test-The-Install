# Test-The-Install
Installing the ArcGIS API for JavaScript library on Windows
est your install. You can use the following test code to validate your JSAPI library install.

#<!DOCTYPE html>
#<html>
#  <head>
#    <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
#    <meta name="viewport" content="initial-scale=1, maximum-scale=1,user-scalable=no" />
#    <title>Test Map</title>
#   <link rel="stylesheet" href="https://www.example.com/arcgis_js_api/library/4.5/dijit/themes/claro/claro.css" />
#    <link rel="stylesheet" href="https://www.example.com/arcgis_js_api/library/4.5/esri/css/main.css" />
#    <style>
#      html,
#      body,
#      #viewDiv {
#        margin: 0;
#        padding: 0;
#        width: 100%;
#        height: 100%;
#      }
#    </style>
#    <script src="https://www.example.com/arcgis_js_api/library/4.5/dojo/dojo.js"></script>
#   <!-- 注意这里是https://www.example.com/arcgis_js_api/library/4.5/dojo/dojo.js而不是init.js -->
#   <script>
#     var myMap, view;
#     require([
#       "esri/Basemap",
#       "esri/layers/TileLayer",
#       "esri/Map",
#       "esri/views/MapView",
#       "dojo/domReady!"
#     ], function (Basemap, TileLayer, Map, MapView){
#       // --------------------------------------------------------------------
#       // If you do not have public Internet access then use the Basemap class
#        // and point this URL to your own locally accessible cached service.
#        //
#        // Otherwise you can just use one of the named hosted ArcGIS services.
#        // --------------------------------------------------------------------
#        var layer = new TileLayer({
#          url: "https://www.example.com/arcgis/rest/services/Folder/Custom_Base_Map/MapServer"
#        });
#        var customBasemap = new Basemap({
#          baseLayers: [layer],
#          title: "Custom Basemap",
#          id: "myBasemap"
#        });
#        myMap = new Map({
#          basemap: customBasemap
#        });
#        view = new MapView({
#          center: [-111.87, 40.57], // long, lat
#          container: "viewDiv",
#          map: myMap,
#          zoom: 6
#        });
#      });
#    </script>
#  </head>
#  <body class="claro">
#    <div id="viewDiv"></div>
#  </body>
#</html>
