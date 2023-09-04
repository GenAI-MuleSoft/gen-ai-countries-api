Links to assets in Exchange:
gen-ai-countries-api https://anypoint.mulesoft.com/exchange/4af9c84b-ab45-49f9-9cc2-9764f985bec1/gen-ai-countries-api/minor/1.0/
gen-ai-geo-api https://anypoint.mulesoft.com/exchange/4af9c84b-ab45-49f9-9cc2-9764f985bec1/gen-ai-geo-api/minor/1.0/pages/home/
Anypoint Exchange Specifications
Welcome to the Anypoint Exchange specifications documentation.   
We offer two APIs: one for fetching information about countries and another for fetching details on countries and their cities. Each API has comprehensive filtering, sorting, and pagination options to provide optimal flexibility.  
  
Table of Contents:  
Gen-AI-Countries-API  
Gen-AI-Geo-API  
Common Features
    
Gen-AI-Countries-API  
Endpoint: /api/countries  
  
Usage:  
Fetch details about various countries.  
  
Parameters:  
name: Filter countries by name.  
population: Filter countries by population.
    
Gen-AI-Geo-API  
Endpoint: /api/countries-cities  
  
Usage:  
Fetch details about countries and their corresponding cities.  
  
Parameters:  
name: Filter by country or city name.
population: Filter countries/cities by population. 
   
Common Features  
Sorting:  
Both APIs offer the ability to sort results by name in either ascending or descending order:  
  
sort: asc or desc  
Pagination:  
Fetch results in a paginated manner to better handle large data sets:  
  
offset: Specifies the starting point of the results to fetch.  
limit: Specifies the maximum number of results to return.  
Example:  
To fetch information about countries starting from the 10th result and limit to 20 results:  
  
/api/countries?offset=10&limit=20  
To fetch information about countries and cities, filtered by city name "Los Angeles":  
  
/api/cities?name=Los_Angeles  
Feedback  
We are always eager to improve and expand our specifications. Please feel free to provide feedback or report any issues you may encounter.  
  
Gen-AI-Countries-API in Runtime Manager  
The Gen-AI-Countries-API hosted in the Runtime Manager is a robust service providing detailed information about various countries. For enhanced   security, the API is protected using Basic Authentication. Additionally, to ensure fair usage and system stability, rate limiting policies   have been applied. Please ensure you authenticate properly and respect the rate limits when making requests.  
Link to app deployed in Runtime Manager: http://gen-ai-countries-api-ddanylo.us-e2.cloudhub.io/api/countries