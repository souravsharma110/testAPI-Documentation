# Mappls Sessions Tracking

The following data points could be relevant for tracking user activity sessions:

- `User Location`: This could include the GPS coordinates of the user, the accuracy of the GPS reading, and the altitude.

- `Map Information`: This could include information about the map being used, such as the type of map (e.g. street map, satellite map, terrain map), the zoom level, and the center point of the map.

- `Map Interactions`: This could include information about the actions taken by the user while interacting with the map, such as panning, zooming, and tapping on specific map features.

- `Search Queries`: This could include information about the search queries entered by the user, such as the search terms and the results returned.

- `Route Information`: This could include information about the routes selected by the user, such as the start and end points, the mode of transportation, and the estimated travel time.

- `User Feedback`: This could include information about any feedback provided by the user, such as ratings, comments, and suggestions.

- `Device Information`: This could include information about the device used to access the app, such as the type of device, the operating system, and the version.

- `Session Information`: This could include the start and end times of the session, the duration of the session, and any other relevant information about the session.

These data points can help provide insights into how users are interacting with the mapping app and can be used to improve the user experience and provide more personalized recommendations.

### Data Points for Activity Tracking Session in a Mappls App

Here is a basic database schema that we can store related to activity tracking sessions in a mapping app:

1. **User Table:**
   - `User ID`: unique identifier for each user
   - `User Name`: name of the user
   - `Email`: email address of the user
   - `Date of Registration`: date and time when the user registered
2. **Session Table:**
   - `Session ID`: unique identifier for each session
   - `User ID`: foreign key referencing the User ID in the User Table
   - `Start Time`: date and time when the session started
   - `End Time`: date and time when the session ended
   - `Duration`: total duration of the session
3. **Map Table:**
   - `Map ID`: unique identifier for each map
   - `Session ID`: foreign key referencing the Session ID in the Session Table
   - `Map Type`: type of map being used (e.g. street map, satellite map, terrain map)
   - `Zoom Level`: current zoom level of the map
   - `Center Latitude`: latitude of the center point of the map
   - `Center Longitude`: longitude of the center point of the map
4. **Interaction Table:**
   - `Interaction ID`: unique identifier for each interaction
   - `Map ID`: foreign key referencing the Map ID in the Map Table
   - `Interaction Type`: type of interaction (e.g. pan, zoom, tap)
   - `Latitude`: latitude of the location where the interaction took place
   - `Longitude`: longitude of the location where the interaction took place
   - `Timestamp`: date and time when the interaction took place
5. **Search Query Table:**
   - `Search Query ID`: unique identifier for each search query
   - `Session ID`: foreign key referencing the Session ID in the Session Table
   - `Query`: the search query entered by the user
   - `Results Returned`: the number of results returned for the search query
   - `Timestamp`: date and time when the search query was entered
6. **Route Table:**
   - `Route ID`: unique identifier for each route
   - `Session ID`: foreign key referencing the Session ID in the Session Table
   - `Start Latitude`: latitude of the start point of the route
   - `Start Longitude`: longitude of the start point of the route
   - `End Latitude`: latitude of the end point of the route
   - `End Longitude`: longitude of the end point of the route
   - `Mode of Transportation`: mode of transportation used for the route (e.g. driving, walking, biking)
   - `Estimated Travel Time`: estimated travel time for the route
   - `Timestamp`: date and time when the route was selected
7. **Feedback Table:**
   - `Feedback ID`: unique identifier for each feedback
   - `User ID`: foreign key referencing the User ID in the User Table
   - `Feedback Type`: type of feedback (e.g. rating, comment, suggestion)
   - `Feedback Text`: text of the feedback provided by the user
   - `Timestamp`: date and time when the feedback was provided3


This database schema can be used as a starting point for storing the data points related to activity tracking sessions in a mapping app. It can be modified or expanded based on specific requirements and constraints.