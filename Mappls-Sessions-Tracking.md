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

1. **User Data:**
   - `User ID`: unique identifier for each user
   - `User Name`: name of the user
   - `Email`: email address of the user
   - `Date of Registration`: date and time when the user registered
2. **Session Data:**
   - `Session ID`: unique identifier for each session
   - `User ID`: foreign key referencing the User ID in the User Table
   - `Start Time`: date and time when the session started
   - `End Time`: date and time when the session ended
   - `Duration`: total duration of the session
3. **Map Data:**
   - `Map ID`: unique identifier for each map
   - `Session ID`: foreign key referencing the Session ID in the Session Table
   - `Map Type`: type of map being used (e.g. street map, satellite map, terrain map)
   - `Zoom Level`: current zoom level of the map
   - `Center Latitude`: latitude of the center point of the map
   - `Center Longitude`: longitude of the center point of the map
4. **Interaction Data:**
   - `Interaction ID`: unique identifier for each interaction
   - `Map ID`: foreign key referencing the Map ID in the Map Table
   - `Interaction Type`: type of interaction (e.g. pan, zoom, tap)
   - `Latitude`: latitude of the location where the interaction took place
   - `Longitude`: longitude of the location where the interaction took place
   - `Timestamp`: date and time when the interaction took place
5. **Search Query Data:**
   - `Search Query ID`: unique identifier for each search query
   - `Session ID`: foreign key referencing the Session ID in the Session Table
   - `Query`: the search query entered by the user
   - `Results Returned`: the number of results returned for the search query
   - `Timestamp`: date and time when the search query was entered
6. **Route Data:**
   - `Route ID`: unique identifier for each route
   - `Session ID`: foreign key referencing the Session ID in the Session Table
   - `Start Latitude`: latitude of the start point of the route
   - `Start Longitude`: longitude of the start point of the route
   - `End Latitude`: latitude of the end point of the route
   - `End Longitude`: longitude of the end point of the route
   - `Mode of Transportation`: mode of transportation used for the route (e.g. driving, walking, biking)
   - `Estimated Travel Time`: estimated travel time for the route
   - `Timestamp`: date and time when the route was selected
7. **Feedback Data:**
   - `Feedback ID`: unique identifier for each feedback
   - `User ID`: foreign key referencing the User ID in the User Table
   - `Feedback Type`: type of feedback (e.g. rating, comment, suggestion)
   - `Feedback Text`: text of the feedback provided by the user
   - `Timestamp`: date and time when the feedback was provided3


This database schema can be used as a starting point for storing the data points related to activity tracking sessions in a mapping app. It can be modified or expanded based on specific requirements and constraints.

## Mappls Sesions Tracking SDK Documentation

1. **Introduction**: The Mappls Sessions Tracking SDK is a powerful tool that enables developers to track user activities in their web applications. It provides a simple and convenient way to collect and analyze user behavior data, allowing businesses to gain valuable insights into how their users interact with their products. The SDK is designed to be easy to integrate into your web application, with a flexible API that can be customized to meet your specific needs. With Mappls Sessions Tracking, you can gain a deeper understanding of your users and improve the overall user experience of your web application.

2. **Installation**: Below are the steps mentioned for installing the SDK:

   - Sign up on Mappls API Console.
   - Include the SDK in your HTML file.
   - Initialize the SDK by passing your account API key to the SDK's initialization function.
   - Verify that the SDK is installed and configured correctly by checking the SDK's log output.
   - Start tracking user sessions by calling the SDK's `startSession` function.

3. **API Reference**: 
   - `Initialization API`: This API is used to initialize the SDK and set the API key for the Mappls account.

        Sample JS Code:
        ```js
            // Initialize the SDK with API key and configuration options
            var mappls = Mappls.init({
                access_token: '<YOUR_ACCESS_TOKEN>',
                options: { ... }
            });
        ```

   - `Start Session API`: This API is used to start a new session for tracking user activity.

        Sample JS Code:
        ```js
            // Start a new session
            mappls.startSession({
                name: 'Session 1',
                // Additional session data, such as user id, timestamp, etc.
                data: { ... }
            });
        ```

   - `End Session API`: This API is used to end a session and save the session data to the Mappls server.

        Sample JS Code:
        ```js
            // Start a new session
            mappls.endSession({
                sessionId: 'ssid00112234'
            });
        ```

   - `Session Data API`: This API is used to retrieve session data, including session duration, number of pages visited, and user information.

   - `Event Tracking API`: This API is used to track specific events that occur within the session, such as button clicks or page transitions.

   - `User Data API`: This API is used to retrieve user data, including user attributes and demographic information.

   - `Error Tracking API`: This API is used to track errors that occur within the session, such as JavaScript errors or network errors.

