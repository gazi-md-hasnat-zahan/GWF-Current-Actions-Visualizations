# GWF-Current-Actions-Visualizations

This was an initiative by Global Water Futures (GWF) and the Dept. of CS, University of Saskatchewan to visualize the ongoing projects that are being maintained by the GWF researchers and students all over Canada. I loved building this website as it was my first work using mapbox. It built this as a part-time Software Developer when I was a graduate student at U of S.

## How it Works:

The basic flow is like this:
-	A base map is loaded (from mapbox maps) at the start
-	3 data layers are added (from 3 GeoJSON files) overlaying the base map: basin, project, and site
    o	Basin: colored polygons
    o	Project: circles with very small radius, designed not to be visible to the users, but to be still present
    o	Site: visible colored circles, colors are based on basins they belong to
-	The left sidebar displays the projects in thumbnail view (at the start). There are-
    o	2 listing options: projects and sites
    o	2 viewing options: thumbnail and list
    o	1 search field: using project/site names
-	The top middle div shows ‘base map toggle’ options
    o	6 map options, custom one is the default 
-	The top right div shows ‘layer toggle’ options
    o	By default, both layers (project and site) are visible
-	The bottom right div ‘basin legend and color’ options
    o	7 color palette options, 7 is default 

## Interactions:

-	Clicking the ‘base map’ options changes the base map
-	Clicking the ‘layer toggle’ sliders shows/hides the layers
-	Clicking the ‘color palette’ options changes the basin colors
-	Clicking the ‘project/Research Site’ buttons expands and collapses the left sidebar
-	Clicking the ‘thumbnail/list’ buttons shows the corresponding view
-	Writing names on the search field shows the matching project/site names
-	Hovering one of the listed projects/sites from the left sidebar shows pop-up/s pointing the exact location on the map
-	Clicking one of the listed projects/sites from the left sidebar expands/collapses the corresponding details
-	Clicking any circle (site) on the base map also expands/collapses the site’s corresponding details

## Basin GeoJSON (GWFbasins_v3.json):

-	Has 8 basins listed
-	The ‘id’ field hold the ID of the basin
-	The ‘NAMRB_EN’ field keeps the name of the basin
-	The ‘coordinates’ field is a ‘polygon’ type array that constructs the polygon of the basin

## Project GeoJSON (GWFprojects.json):

-	Has 58 projects listed
-	The ‘id’ field holds the ID of the project
-	The ‘PI’ field lists the principal investigators, separated by semicolon (;)
-	The ‘CoI’ field lists the co-principal investigators, separated by semicolon (;)
-	The ‘NumberofSites’ holds the number of sites the project is running on
-	The ‘Site’ field lists the site names, separated by semicolon (;)
-	The ‘X’ and ‘Y’ fields list the coordinates of the sites, separated by semicolon (;)
-	The ‘BasinLocation’ field lists the basin names the sites belong to, separated by semicolon (;)
-	The ‘URL’ field holds a link to the project
-	The ‘coordinates’ field is a ‘multipoint’ type, holding one or many coordinates of the associated sites for the project

## Observatory/Site GeoJSON (2020-Jan6-GWFobservatoriesGeo_withID3.json):

-	Has 91 sites listed
-	The ‘id’ field holds the ID of the site
-	The ‘Site’ field holds the site name
-	The ‘X’ and ‘Y’ fields list the X and Y coordinates of the site
-	The ‘BasinLocation’ field holds the basin name that the site belongs to
-	The ‘URL’ field holds a link to the site 
-	The ‘coordinates’ field is a ‘point’ type, holding the coordinates of the site

*** The source code has sufficient documentation/comments/definitions for better understanding. 

Thanks, happy coding!
