# World_Weather_Analysis
## Overiew

The World Weather Analysis project is about applying analysis, visualizations, statistical skills, while  API data retrival from a website. We would use Jupyter Notebook, Pandas Library, CitiPy, Python Requests, APIs, JSON Traversals to collect weather from a website from over 500 cities around the world. We would then analyze the data using Pandas and plot the data using the MatplotLib Library and Google API. We would then perform perform statistical analysis using the SciPy Libarary. In the end, we would produce a series of plots that visually and statistically (using linear regression) show the relationship between Latitidue and Longitude and a variety of weather parameters. Export the data and use the weather to determine the best cities for vacation based on search criteria based on certain weather criteria. We would then map these cities using gmaps and google places API

In the second phase of our analysis, we would be assisting PlanMyTrip, a top travel technology company in the hotel and lodging industry. We collect and present data for customers via the search page, users will then filter based on their preferred criteria to find their ideal hotel any where in the world. We would use a Jupyter Notebook and the CitiPy module to get the cities from more than 600 random Latitude and Longitudes. We would then perform requests from the open weather API to retrive wether information for the cities. Finally, we would produce a  weather database, a vacation search results, and a travel itineary based on users search parameters

### Control Flow
1. Collect the Data
   - Use the NumPy module to generate more than 1,500 random latitudes and longitudes.
   - Use the citipy module to list the nearest city to the latitudes and longitudes.
   - Use the OpenWeatherMap API to request the current weather data from each unique city in your list.
   - Parse the JSON data from the API request.
   - Collect the following data from the JSON file and add it to a DataFrame
2. Exploratory Analysis with Visualization
   - Create scatter plots, correlations, and heat maps using the Google Maps and Places API of the weather data for the following comparisons
     - Latitude versus temperature
     - Latitude versus humidity
     - Latitude versus cloudiness
     - Latitude versus wind speed
3. Visualize the data
    - Create a heatmap with pop-up markers that can display information on specific cities based on a customer's travel preferences
      - Filter the Pandas DataFrame based on user inputs for a minimum and maximum temperature.
      - Create a heatmap for the new DataFrame.
      - Find a hotel from the cities' coordinates using Google's Maps and Places API, and Search Nearby feature.
      - Store the name of the first hotel in the DataFrame.
      - Add pop-up markers to the heatmap that display information about the city, current maximum temperature, and a hotel in the city. 
