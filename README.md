# Module 8. Interactive Mapping
In this assignment, you will customize the Lab 8 interactive map template found here to feature a college or institution outside of Philadelphia. You will update the map, sidebar, and popups to match your chosen location, then publish your finished map as a live webpage using GitHub Pages.

1. Choose a Non Philadelphia College or Institution
Pick any campus not located in Philadelphia. Examples:
•	Penn State
•	Rutgers
•	University of Maryland
•	Harvard
•	UCLA
•	Ohio State
•	A community college or technical institute
You’ll be customizing the map to this new location.
2. Update the Map Center and Zoom

Open js/setup.js.
Find:
center: [39.983219999796114, -75.15356557830536],
zoom: 16,
Replace the coordinates with the latitude and longitude of your chosen campus. Set the zoom to something you like.

3. Draw a Polygon Around a Building
In the HTML file, you’ll see a polygon example:
var polygon = L.polygon([
    [ ... ],
    [ ... ],
]).addTo(map);
Replace the coordinates with a polygon that outlines one building on your chosen campus.
You can get coordinates from:
•	Google Maps (right click → “What’s here?”)
•	geojson.io
•	OpenStreetMap

Add a popup to the building name:
polygon.bindPopup("Your Building Name");
Advanced path: Draw a geojson in geojson.io and add a “name” field. Examine the tyler.js file and see how you can modify it to match your new building.

5. Add a Marker or Circle for Your Favorite Coffee Shop
Find a coffee shop near your chosen campus.
Add either a marker or a circle:
L.marker([lat, lng]).addTo(map).bindPopup("My favorite coffee shop!");

L.circle([lat, lng], {
  radius: 20,
  color: "brown"
}).addTo(map)
  .bindPopup("Coffee!");

6. Add the School Logo to the Sidebar
Replace the Temple Logo in the sidebar:
<img src="images/temple.png" ...>

with your chosen school’s logo, saved in the images/ folder. Example:
<img src="images/ucla.png" style="width:60%">
Make sure the file name matches exactly.
7. Update the Sidebar Text
Change the headings and description to match your new location. For example:
<h3> Mapping UCLA Campus </h3>
<p> This map highlights Royce Hall and my favorite coffee shop near campus. </p>

7. Publish your Map Using GitHUB Pages
1.	Create a GitHub repository
2.	Upload your project files
3.	Go to Settings → Pages
4.	Under “Source,” choose main branch
5.	GitHub will give you a live URL like:
https://yourusername.github.io/GeoTag/
Submit this link as your assignment in the Discussion board.


