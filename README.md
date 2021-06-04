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
   - Collect the following data from the JSON file and add it to a DataFrame:
      - City, country, and date
      - Latitude and longitude
      - Maximum temperature
      - Humidity
      - Cloudiness
      - Wind speed
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

## Results
### Scatter Plots

![Fig1](https://user-images.githubusercontent.com/67847583/120711149-a4877500-c484-11eb-9f7e-b02f19457f55.png)
![Fig2](https://user-images.githubusercontent.com/67847583/120711182-afdaa080-c484-11eb-9723-f482afebe766.png)
![Fig3](https://user-images.githubusercontent.com/67847583/120711194-b2d59100-c484-11eb-8f21-ed15bc67f692.png)
![Fig4](https://user-images.githubusercontent.com/67847583/120711201-b537eb00-c484-11eb-8f0c-7b8f86961a58.png)

### Correlations

![Linear Regression on the Northern Hemisphere(%Cloudiness)](https://user-images.githubusercontent.com/67847583/120711290-d0a2f600-c484-11eb-8713-143461422e42.png)
![Linear Regression on the Northern Hemisphere(%Humidity)](https://user-images.githubusercontent.com/67847583/120711313-d698d700-c484-11eb-97d1-d4eabe021cdf.png)
![Linear Regression on the Northern Hemisphere(Max Temp)](https://user-images.githubusercontent.com/67847583/120711318-d8fb3100-c484-11eb-840c-b0c4bf63f399.png)
![Linear Regression on the Northern Hemisphere(Wind Speed)](https://user-images.githubusercontent.com/67847583/120711326-dbf62180-c484-11eb-83f6-62bdaec44955.png)
![Linear Regression on the Southern Hemisphere(%Cloudiness)](https://user-images.githubusercontent.com/67847583/120711345-e1536c00-c484-11eb-9e32-a0c7805adaf9.png)
![Linear Regression on the Southern Hemisphere(%Humidity)](https://user-images.githubusercontent.com/67847583/120711356-e3b5c600-c484-11eb-9b08-94084829702b.png)
![Linear Regression on the Southern Hemisphere(Max Temp)](https://user-images.githubusercontent.com/67847583/120711362-e57f8980-c484-11eb-80ed-35c22589a91e.png)
![Linear Regression on the Southern Hemisphere(Wind Speed)](https://user-images.githubusercontent.com/67847583/120711364-e7494d00-c484-11eb-9e8a-b920e1132e1f.png)


### Travel Preferences: Heatmap with pop-up markers

![heatmap_vacation_spots_with_pop-up_markers](https://user-images.githubusercontent.com/67847583/120734235-28a22280-c4ae-11eb-8e13-7f1db00139fe.png)


### Findings

The correlation between the latitude and the maximum temperature is strong to very strong because the r^2-value is less than 0.55292 and a p-value of 0.00 and a slope of -0.644; for the Northern Hemisphere; r^2-value: 0.583 and a p-value of 0.00 and a slope of 0.736; and greater than 0.7 for the Southern Hemisphere, as shown by the plots here. This means that as we approach the equator, 0° latitude, the temperatures become warmer. And when we are further from the equator the temperatures become cooler.

The correlation between the latitude and percent humidity is very low (r^2-value: 0.008 and a p-value of 0.078 and a slope of 0.1) because the r-value is less than 0.04 for the Northern and Southern Hemispheres (r^2-value: 0.001 and a p-value of 0.632 and a slope of 0.049) for the plots shown here. This means that percent humidity is unpredictable due to changing weather patterns that can increase or decrease percent humidity.

The correlation between the latitude and percent cloudiness is very low because the r-value is less than –0.09 for the Northern Hemisphere and less than –0.02 for the Southern Hemisphere for the plots shown here. This means that cloudiness is unpredictable due to changing weather patterns that can increase or decrease percent cloudiness.

The correlation between the latitude and wind speed is very low because the r-value is less  than –0.07 for the Northern Hemisphere and less than –0.3 for the Southern Hemisphere for the plots shown here. This means that wind speed is unpredictable due to changing weather patterns that can increase or decrease wind speed. 


### PlanMyTrip Analysis: Control Flow
1. Create a Weather Database
   - In a Jupyter Notebook, Create a new set of 2,000 random latitudes and longitudes.
   - Get the nearest city using the citipy module.
   - Perform an API call with the OpenWeatherMap.
   - Retrieve the following information from the API call
      - Latitude and longitude
      - Maximum temperature
      - Percent humidity
      - Percent cloudiness
      - Wind speed
      - Weather description
   - Add the data to a new DataFrame.
   - Export the DataFrame as a CSV file
2. Create a Customer Travel Destinations Map
   - using the Weather Database as DataFrame, write two input statements that will search for the DataFrame for cities that fall in the range of the minimum and maximum temperature range provided.
   - using the loc method filter the DataFrame for temperature criteria collected in the above step, then create a new DataFrame of the preferred cities.
   - determine if there are any empty rows, then drop them if necessary and create a new DataFrame that will hold the hotel names from the hotel search
   - using the google place API search for hotel names for the records in the DataFrame.
   - iterate through the hotel DataFrame and retrieve the latitude and longitude of each city to find the nearest hotel based on the search parameters, then add the hotel name to the new DataFrame. If a hotel isn't found, skip to the next city.
   - drop any rows in the hotel DataFrame where a hotel name is not found and create an output file to store the hotel DataFrame as CSV
   - add the city name, the country code, the weather description, and the maximum temperature for each city to a map marker box template
   - using list comprehension retrieve the city data from each row, which will then be added to the formatting template and saved in the hotel_info list
   - create a marker layer map.
3. Create a Travel Itinerary Map
   - Use the Google Directions API to create a travel itinerary that shows the route between four cities chosen from the customer’s possible travel destinations. Then, create a marker layer map with a pop-up marker for each city on the itinerary.
   - using the vacation search csv as DataFrame, Use the Google Directions API to create a travel itinerary that shows the route between four cities chosen from the customer’s possible travel destinations. Then, create a marker layer map with a pop-up marker for each city on the itinerary.
   - From the vacation search map, choose four cities that a customer might want to visit
   - using the loc method, create separate DataFrames for each city on the travel route
   - using the to_numpy() function and list indexing, write code to retrieve the latitude-longitude pairs as tuples from each city DataFrame.
   - create a directions layer map where the starting and ending city are the same city, the waypoints are the three other cities, and the travel_mode is either "DRIVING", "BICYCLING", or "WALKING"
   - Combine the four cities into a DataFrame and create a map marker layer map 
