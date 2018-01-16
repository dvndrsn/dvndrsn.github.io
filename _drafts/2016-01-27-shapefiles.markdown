---
layout: post
title:"Shapefiles"
subtile:"and stuff"
author: Dave Anderson
date: 2015-01-27
---
Yesterday, I worked through [Mike Bostock][mike]'s D3 great [*Let's Make a Map* tutorial][lets map] with [Aliza][aliza] at [Recurse Center][recurse]. In Mike's tutorial, we take Shapefile data for the UK, filter and convert the data to GeoJSON then TopoJSON. We then load the TopoJSON file in D3, covert the data back to GeoJSON and render it as SVG in the browser, with some pretty styling and labels. It was very illustrative in how to work with map data in D3 (especially if you have a solid grasp of [D3 fundamentals][d3 fund]), but there were a few pieces of knowledge and references that can be a great aid when you're starting to step outside the bounds of the sandboxed example (besides a [great D3 tutorial][scott dataviz]).

[aliza]: http://alizauf.github.io/
[mike]: http://bost.ocks.org/mike/algorithms/
[lets map]:http://bost.ocks.org/mike/map/
[recurse]: http://www.recurse.com/
[d3 fund]: http://bost.ocks.org/mike/join/
[scott dataviz]: http://chimera.labs.oreilly.com/books/1230000000345/index.html

_Mapping Basics & Shapefiles_

Mapschool.io provides a very readable overview of mapping basics (starting from the very beginning), including some great information about the structure of the Shapefile, one of the most common formats which you can find open map data in. The Shapefile format is actually a group of files which act together, but with very different contents.

* .shp
* .prj
* .shx
* .dbf
* .prj

During [the tutorial][lets map], we filter data from our shapefile using a GIS command line tool ogr2ogr by applying filters to the database associated with the shapefile. Filters use straightforward SQL-like WHERE-clause syntax, but when you are preparing your own data, you will need to review the data in the shapefile to determine how best to filter it. A useful program for this purpose is QGIS, an open source GIS tool. You can open the file in QGIS browser easily to preview the structure and data attributes. You can also open the file in QGIS desktop and open the attribute table from the desktop.

[map school]: http://mapschool.io/
[map cheatsheet]: https://github.com/tmcw/mapmakers-cheatsheet

[create maps]: https://github.com/veltman/maps-nicar14

[nyc-map]: https://github.com/dwillis/nyc-maps


[projection]: http://www.geo.hunter.cuny.edu/~jochen/gtech201/lectures/lec6concepts/map%20coordinate%20systems/how%20to%20choose%20a%20projection.htm
[transition]: https://www.jasondavies.com/maps/transition/

_GeoJSON and TopoJSON - Geometry vs. Topology_

[This site][geojson] is a great reference for understanding the GeoJSON structure. For a deeper understanding of the file format, you can play with Tools such as [GeoJSON.io][geojson play] to create and view the text contents for new GeoJSON from arbitary shapes on top of a map or [mapshaper.org][mapshaper] to load an existing Shapefile, GeoJSON or TopoJSON to get a feel for how their contents are structured visually.

It is initially counter-intuitive to consider that we are converting our map data from Shapefile format to GeoJSON then TopoJSON, only to finally covert the data back to GeoJSON on the client side to display. TopoJSON is a more space-efficient format (especially beneficial for the transferring data on web), but understanding the difference between Geometry and Topology can really help drive home what the fundamenetal differences between these formats is.

In formats such as Shapefile and GeoJSON, the edges of the object is stored using Geometry. These file formats will store all edges separately for each shape even if there are multiple overlapping edges of shapes (say for neighboring states or countries).

In TopoJSON, there are two primary tricks used to reduce the size of the file format. First, the edges of an object are stored as topology. This means that each object is stored as a reference to its edges (called arcs in TopoJSON) allowing redundant shared arcs (between ajacent states or countries) to be reused between objects. Second, the precision of the numbers used to define the arcs and points are compressed using delta encoding (represented as integers rather than floats). Also, the same data can be used to represent a border (mesh) or solid object.


[geojson]: http://www.macwright.org/2015/03/23/geojson-second-bite.html
[topo]: http://www.esri.com/news/arcuser/0401/topo.html
[topojson]: https://github.com/mbostock/topojson/wiki
[geojson play]: http://geojson.io/
[mapshaper]: http://www.mapshaper.org/

[delta short]: http://www.dspguide.com/ch27/4.htm
[delta]: http://preshing.com/20121105/arithmetic-encoding-using-fixed-point-math/
