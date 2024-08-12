# Device-tracker

1. Check if the browser supports geolocation.

2. Set options for high accuracy, a 5-second timeout, and no caching. Use watch Position to track the user's location continuously. Emit the
   latitude and longitude via a socket with "send-location". Log any errors to the console

3. Initialize a map centered at coordinates (0, 0) with a zoom level of 15 using Leaflet. Add OpenStreetMap tiles to the map

4. Create an empty object markers.

5. When receiving location data via the socket, extract id, latitude, and longitude, and center the map on the new coordinates.

6. If a marker for the id exists, update its position, otherwise, create a new marker at the given coordinates and add it to the map. When
   a user disconnects, remove their marker from the map and delete it from markers.
