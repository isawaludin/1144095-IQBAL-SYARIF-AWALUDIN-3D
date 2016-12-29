MapServer




1. Background
Map is one of the media to locate somewhere on the earth's surface. MapServer is freeware and open source application that allows to display spatial data on the web. For more details will be discussed below.

2. Identification of Problems
· How the student / i know about MapServer?
· How does the general public know MapServer?

3. Exposure
          That is, a program MapServer CGI (Common Gateway Interface). The program will be executed on the web server, and based on certain parameters (especially in the form of a configuration file * .map) will generate data that will then be sent to a web browser, either in the form of map images and other images.

When MapServer works;
Map Server works side by side with the web application server. Web server receives a request through MapServer map. MapServer generates a request to the map and send it to the web server as shown below.


The main function of MapServer is doing the reading of data from many sources and place them into layers simultaneously into a graphic file. One of the layer may be satellite images. Each layer overlay each other with each other and displayed into the web browser.

From these images we can see a satellite photograph (obtained from a remote server), the lines of roads, urban locations, and labels the city in the show are generic by MapServer. Pengambaran process map (rendering) appears each time a request to the new map made by Mapserver including when a user does a zoom level of the map view.

Main components

Mapserver produce the output of graphic file based on the input provided by the user. The key component is composed of MapServer executable CGI program, file maps, data sources and output image. As the picture below all the components work together, after user request / perminataan then CGI will access the map file, describing the information obtained from the data source and re-display it on a map.
MapServer Executable

In a simple MapServer running executable CGI applications on Web servers that are technically stateless process based on HTTP. Stateless is a demanding process that is followed by a stop running. CGI application receives requests from a web server, then the process is done and returns the response or data to the web server. CGI worked very simple not require programming to be able to use it. We just do edit based on text base, the runtime configuration file, create web pages, and put them to work on a web server. MapServer CGI executable works as an intermediary between the map file to the Web server programs that ask for a map. Demand is passed in the form of a web server CGI parameters to the MapServer. Images are created by MapServer further provides fed back to the web server and then to the user via a web browser.

MapServer Map File

MapServer as a machine that needs fuel to work and need a delivery system (delivery system) fuel to reach the engine. MapServer program needs to know the map layer that will be drawn, how to describe it, and where the location of the data source. Data is the fuel and a map file or .map.file a delivery system (delivery system). The map is a text configuration file that consists of a list of settings to be used to draw and interact with the map. The information contained therein is what data layer to be drawn, where the geographic focus of the map, the projection system used, what format will be used to display images, and how to define the legend and scale on the map.

Examples of basic mapping script with one layer.

FOLDER

SIZE 600 300

EXTENT -180 -90 180 90

LAYER

NAME countries

TYPE POLYGON

DEFAULT STATUS

DATA countries.shp
CLASS

OUTLINECOLOR 100 100 100

END

END

END

When a request or a request dating from the MapServer application must mention sepesifikasi reguest the desired map file. Then MapServer create maps based on the settings on a given map file earlier.

4. Solution from other sources
     
What Is a Map Server?

MapServer program in the form of a CGI (Common Gateway Interface). The program will be executed on the web server, and based on certain parameters (especially in the form of a configuration file * .map) will generate data that will then be sent to a web browser, either in the form of map images or other forms.

MapServer has fitur¬fitur following:
 Displaying spatial data in a vector format such as: Shapefile (ESRI), ArcSDE (ESRI), PostGIS and various other vector data formats using OGR library
· Displaying spatial data in raster format such as TIFF / GeoTIFF, EPPL7 and various other raster data formats using GDAL library
· Using the quadtree indexing spatial data, so that the spatial operasi¬operasi can be done quickly
· Can be developed (customizable), with an output that can be set using a template file¬file
· Can perform value-based object selection, based on the point, area, or on a specific spatial objects
· Supports TrueType font rendering of characters
· Supports raster and vector data usage which di¬tiled (dibagi¬bagi into smaller sub-sections so that the process to retrieve and display images can be accelerated)
· Be able to describe the elements of the map automatically: graphic scale, the index map and the map legend
· Use the scale in the depiction of spatial objects
· Can describe the thematic maps are constructed using logical expressions mapun regular expressions
· Can display the label of spatial objects, the label may be arranged so that no overlap
· Configuration can be adjusted on the fly through the parameters specified in the URL
· Can handle a variety of projection systems on the fly

Currently, in addition to access MapServer as a CGI program, we can access the MapServer as Mapscript module, through a variety of scripting languages: PHP, Perl, Python or Java. MapServer fungsi¬fungsi access via scripts will further facilitate the development of applications. Developers can choose the language most familiar.

Websites that support Web Mapping

There are several websites that mapping can be used and in eksporer are:
· Wikimap http://wikimapia.org
· Mesonet http://mesonet.tamu.edu/
· SpasialGuru http://spatialguru.com/maps/
· MapitOut http://www.mapitout.com/
5. Conclusions and suggestions
                So, MapServer is a freeware and open source application that allows us to show the spatial data (maps) on the web. This application was first developed at the University Minesotta, United States to project Fornet (a project for the management of natural resources) sponsored by NASA (National Aeronautics and Space Administration). Support NASA proceed with the project developed TerraSIP for data management field. At present, because it is open (open source), MapServer development is done by developers from various countries.

6. Github Writer
 github


 7. Personal Data:
    
     Name: I. Syarif Awaludin (Arif)

     NPM: 1144095
     Class: 3D
     Prodi: DIV (Diploma IV) Technical Information
     Campus: Politeknik Pos Indonesia (Bandung)
     Course: Geographic Information Systems (GIS)


8. Bibliography

http://inigis.com/mengenal-mapserver/
http://www.mapserverfoundation.org/
http://mapserver.gis.umn.edu/
http://www.dmsolutions.ca/
http://www.autodesk.com/dwftoolkit/
http://usa.autodesk.com/adsk/servlet/item?siteID=123112&id=6153839
http://www.spatialgis.com/
https://dennycharter.wordpress.com/2008/05/09/cara-kerja-mapserver/

9. Plagiarism

https://drive.google.com/open?id=0BynaTCCzaRSeRXBsX21ZdFJLLTQ
