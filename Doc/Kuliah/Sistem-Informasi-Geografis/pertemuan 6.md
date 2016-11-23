Edit Geospatial Data




1. Background
     Data is a value that represents a real object. For example; geographical environment, maps and others. This time I will explain about how to edit geospatial data (edit shapefile). For more details will be discussed below.

2. Identification of Problems
How the student / i know about how to edit the shapefile?
How do ordinary people know how to edit geospatial data?
3. Exposure
     Shapefile is a common geospatial data format for geographic information systems software. Shapefile was developed and organized by ESRI's open specification for interoperability of data between ESRI and other soft data card products.

writer () is a method in shapefile to create a new shp file (dbf & shp).
example ;

>> Import shapefile
>> Sf = shapefile.writter (shapeType = 1)
>> Sf.field ( 'name', 'c', '40')
>> Sf.field (the 'owner', 'c', '40')
>> Sf.record ( 'the rice shop,' 'Asep Dinamo')
>> Sf.point (10,10,0,0)
>> Sf.save ( 'warteg.shp')

editor () is as editing the shapefile for example, delete records.
example ;

>> Import shapefile
>> Sf = shapefile.editor ( 'warteg.shp')
>> Sf.point (16,10,0,0)
>> Sf.record ( 'field')
>> Sf.save ( 'warteg.shp')

4. Solution from other sources
     
ESRI shapefile or so-called shapefile is a common geospatial data format for geographic information system software. Developed and managed by the ESRI as a specification (almost) open for the interoperability of data between ESRI and other software products.
[1] A "shapefile" usually consists of a set of files with extension ".shp", ".shx", ".dbf", and other extensions on a same name (e.g., "the street."). When use, shapefile actually refer to is the extension ".shp", but this file is incomplete and requires other files.
Shapefile spatial geometry is described by: points, lines, and extents. The geometry, for example, can represent, river, stream, and lake. Each section has an attribute that describes the attributes, such as the name of the river or the temperature.

5. Conclusions and suggestions
   So, as a shapefile format geospatial data created and managed by ESRI for relations with other software products. When the editing is done manually delete the data and then insert because the system is still primitive.

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
https://id.wikipedia.org/wiki/Shapefile

9. Plagiarism

 https://drive.google.com/open?id=0BynaTCCzaRSeY1gxY0NsR3dZSWs
