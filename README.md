**Main steps**
1.Geocoding the City Name:

The get_location function uses the Google Geocoding API to convert the city name into geographic coordinates (latitude and longitude).
This information is essential for querying nearby restaurants with the Places API.

2.Fetching Top Restaurants:

The get_top_restaurants function uses the latitude and longitude to retrieve a list of nearby restaurants.
We use Google Places API with filters for type=restaurant and rankby=prominence to get the top-rated restaurants within a 5 km radius.
Saving Data to JSON:

3.The save_to_json function structures and stores restaurant data in a JSON file, using the restaurant name as a key for easy lookup.

4.Downloading the JSON File in Colab:


**Challenges and Issues Encountered:**
1.API Key Retrieval:
There are 2 types of   Places API  . one is Places API (New) and the other is Places API in the google cloud console .First i tried the code with Places API (New) but got an error ,"This API project is not authorized to use this API." 
Then tried the same with Places API and it started taking the input and reading the API

2.Debugging API Responses:
Checking responses by printing raw API data (data dictionary) helps troubleshoot problems like missing fields or incorrect status messages, which can often reveal why the request failed.

3.Handling Errors and Edge Cases:
Some cities may not be found by the Geocoding API, which could result in a None response. This is because the selected Places API can give access to only 100 Million places which can be probably the major cities globally , hence not all cities can be found .
