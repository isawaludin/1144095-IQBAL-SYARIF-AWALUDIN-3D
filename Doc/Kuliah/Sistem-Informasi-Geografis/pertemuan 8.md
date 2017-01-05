Installation MAP SERVER


Background :

At last week's meeting we have discussed what are the things about Map Server. Need we recall that, MapServer is a freeware and open source application that allows us to show the spatial data (maps) on the web. At this meeting we will discuss about how to install it from the Map Server.

discussion:

MapServer program in the form of a CGI (Common Gateway Interface). The program will be executed on the web server, and based on certain parameters (especially in the form of a configuration file * .map) will generate data that will then be sent to a web browser, either in the form of map images or other forms.

How to install Map Server
To run the server folder, first run CentOS on a virtual box
Subsequently connect with the host computer network virtualbox
After that, go into the root through the terminal
Then type at the terminal #install mapserver5
Wait until the installation is complete
After performing the steps above, then perform the installation of Proxy Folders as follows:
Open a terminal type #install python-pip
Then type # python-dev
Then type #pip install mapproxy
Then type #install Vwsqi
After that, wait until the install is complete
Here is the script the way through Linux menginstallasi Map Server is as follows:

services:
  demo:
  tms:
    use_grid_names: true
    # origin for /tiles service
    origin: 'nw'
  kml:
      use_grid_names: true
  wmts:
    # use restful access to WMTS
    restful: true
    # this is the default template for MapProxy
    restful_template: '/{Layer}/{TileMatrixSet}/{TileMatrix}/{TileCol}/{TileRow}.{Format}'
    # and also allow KVP requests
    kvp: true
    md:
      # metadata used in capabilities documents for WMTS
      # if the md option is not set, the metadata of the WMS will be used
      title: Awangga GeoMap
      abstract: This is the Awangga GeoMap.
      online_resource: http://www.awangga.net/
      contact:
        person: Rolly Maulana Awangga
        position: Software Engineer
        organization: Belant Persada
        address: Jl. Ligar Nyawang No.2
        city: Bandung
        postcode: 40191
        country: Indonesia
        phone: +62(0)813-12000-300
        fax: +62(0)813-12000-300
        email: rolly@awang.ga
      # multiline strings are possible with the right indention
      access_constraints:
        This service is intended for Sekretariat Negara Only.
        The data is under development on Sekretarian Negara Republik Indonesia.
        (http://setneg.go.id/)
      fees: 'None'
  wms:
    md:
      title: MapProxy WMS Proxy
      abstract: This is a minimal MapProxy example.

layers:
  - name: agm
    title: Awangga Geo Map - www.awangga.net
    sources: [agm_cache]

caches:
  agm_cache:
    grids: [webmercator]
    sources: [agm_source]

sources:
  agm_source:
    type: mapserver
    req:
      layers: roads
      map: /var/mapdata/mapfile/agm.map
    coverage:
      bbox: [94.5011475, -11.007385, 141.01947, 6.076721]
      srs: 'EPSG:4326'
    mapserver:
      binary: /usr/libexec/mapserver
      working_dir: /var/mapdata/tmp
    supported_srs: ['EPSG:4326']

grids:
    webmercator:
        base: GLOBAL_WEBMERCATOR

globals: 

Kesimpulan :
Mapserver dapat kita gunakan dengan menginstall sendiri pada komputer kita dan mengkonfigurasinya sendiri dengan tata cara yang baik dan benar.
Saran :
Gunakanlah aplikasi Map Server karena dapat kita gunakan dan aplikasikan dengan mudah dalam komputer kita sendiri. 
Identitas Diri :
Iqbal Syarif A
D4 - Teknik Informatika - 3D
1144095
Politeknik Pos Indonesia

Plagiarisme :
https://drive.google.com/drive/folders/0Bw2KSpg8rXu5QlVhcXMwMmdydTA
Github :

Sumber :
http://arifbae17.blogspot.co.id/2016/12/mapserver-1.html
http://laptoprus4k.blogspot.co.id/2017/01/install-map-server.html
