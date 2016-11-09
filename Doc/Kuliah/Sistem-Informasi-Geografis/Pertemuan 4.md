Geographic Information Systems (GIS): Meeting 4
Geospatial data retrive




1. Background

     Data is a value that represents a real object. For example; geographical environment, maps and others. This time I will explain about how to retrive geospatial data. For more details will be discussed below.

2. Identification of Problems
How the student / i be able to know and understand about the geospatial data retrive?
How do ordinary people know retrive geospatial data?

3. Exposure

     Meretrive Geospatial Data is data mining of existing databases in the geospatial, one of which consists of the vector. As previously penjelasal about geospatial data, such data have shp file format called regular or shapefile. To apply, I took a sample of the work in linux terminal with consolnya;
Read the number of geometry data:
>> Import shapefile
>> Sf = shapefile.Reader ( "nama_file.Shp")
>> Sf.shapes ()
>> Len (a)
or;
>> Import shapefile
>> Sf.records ()
>> Sf.records (n)

4. Solution of the Other Resources

        Retrive Geospatial Data is one way to retrieve the geometry data and database geospatial data, where the data is the data vector which is one type of geospatial data, because the data vector is the data in the form of shape, so that data can be used to retrieve in python, shapefile or SHP itself is the data that stores geometric data in it, namely:
Bbox: view the boundary coordinates on the map, usually rectangular in the map, BBOX merupak boundary box are the coordinates of point 4.
Shape Type
Point: the coordinates of points (1 point / coordinates) standards numbered 1 from ESRI
Polyline: coordinates of the points that make up the line but does not establish a standard numbered area 3 of ESRI.
Polygon: coordinate establish a standard numbered area 5 of ESRI.

5. Conclusions and Recommendations

     So, meretrive geospatial data is a step took the form of vector geometry data / more in geospatial databases.

6. Github Writer



7. Personal Data

     Name: I. Syarif Awaludin (Arif)

     NPM: 1144095
     Class: 3D
     Prodi: DIV (Diploma IV) Technical Information
     Campus: Politeknik Pos Indonesia (Bandung)
     Course: Geographic Information Systems (GIS)

8. Bibliography

http://nadiaaayulestari.blogspot.co.id/2016/11/retrive-geospasial-data-pengmabilan.html

9. Plagiarism
