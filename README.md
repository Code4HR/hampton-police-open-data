# hampton-police-open-data  

#####Background  
The City of Hampton Police Department recently created an [open data page](http://www.hampton.gov/police/opendata) as part of the [White House Police Data Initiative](https://www.whitehouse.gov/blog/2015/05/18/launching-police-data-initiative). The released data includes a quarterly selection ofcrimes within the City. Seeing the data as a table is great, but within the context of location, it's much easier to visualize crime across the city.  

#####How We Made It  
There are a few options to access the information via the `Socrata Data Player`. Ideally, the data would include the lat/long coordinates for block locations of crimes, so we could use the API option and stream the data from Hamptons' site. In our case, it didnt, so we downloaded a `.json` file of the data. To get the data on a map, we use a process called geocoding which assigns a lat/long point by matching the address to address data from a provider like OpenStreetMap, MapQuest, or Google. To geocode this data, we used QGIS (an open-source desktop mapping software), which can perform the geocode for us. The data was then loaded into CartoDB (web-based mapping software) to create several map based views of the data. Finally, we used `CartoDB.js` and `jquery.js` to make the website and `GitHub` to host the code and the site.  

It's important to note that the data only provides the address block for which the crime was reported. For instance if the crime was listed as `400 Block Armistead Avenue`, it was geocoded as `400 Armistead Avenue`, meaning the dot on the map is an approximation.

made with &#9829; by [Code for Hampton Roads](http://www.code4hr.org">Code for Hampton Roads) and [Maptime HRVA](https://twitter.com/maptimehrva)  

Get in contact with us at [code4hr-team@codeforamerica.org](code4hr-team@codeforamerica.org)  


