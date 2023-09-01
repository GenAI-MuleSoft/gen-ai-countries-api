10:15 - started work

Description:  
It is an API that returns information about countries. There are different data about them, such as name , population, area, currency etc.. Data can be filtered by country name and poulation.Also it can be sorted and paginated. API has only one endpoint, named /countries. Also it has 5 optional query parameters(countryName, population, sort, offset, limit). With query parameter countryName you can search for countries names that contains string from attributes (e.g., providing `st` as attribute you could find `Estonia`, providing `Sp` you could find `Spain`). With population query parameter you search for countries where the population is less than provided number from attributes in the millions of people (e.g., by providing value `10`, you should find countries with a population less than 10 million). Sort query parameter can take two values: "asc" and "desc". It sorts countries in descending or ascending order by their names.With offset and limit you can have pagination.   
To run application locally you have to open Anypoint Studio and run it from there. Application would be run on port 8081. You also have
to be sure that this port is free or otherwise set some other value for http.port.Than it will be possible to make a request to an app.
Link for request would be http://localhost:8081/countries.   
Here are some exaples of request and responses:  
1.http://localhost:8081/api/countries:  
[  
    {  
        "name": {  
            "common": "Mauritania",  
            "official": "Islamic Republic of Mauritania",  
    ...  
]  
2.http://localhost:8081/api/countries?countryName=Ukraine:  
[  
    {  
        "name": {  
            "common": "Ukraine",  
            "official": "Ukraine",  
            "nativeName": {  
                "ukr": {  
                    "official": "Україна",  
                    "common": "Україна"  
                }  
  ...  
]  
3.http://localhost:8081/api/countries?population=1  
[  
    {  
        "name": {  
            "common": "Antigua and Barbuda",  
            "official": "Antigua and Barbuda",  
            "nativeName": {  
                "eng": {  
                    "official": "Antigua and Barbuda",  
                    "common": "Antigua and Barbuda"  
    ...  
]  
4.http://localhost:8081/api/countries?sort=asc  
[  
    {  
        "name": {  
            "common": "Afghanistan",  
            "official": "Islamic Republic of Afghanistan",  
            "nativeName": {  
                "prs": {  
                    "official": "جمهوری اسلامی افغانستان",  
                    "common": "افغانستان"  
                },  
  ...  
]  
5.http://localhost:8081/api/countries?sort=desc:  
[  
    {  
        "name": {  
            "common": "Åland Islands",  
            "official": "Åland Islands",  
            "nativeName": {  
                "swe": {  
                    "official": "Landskapet Åland",  
                    "common": "Åland"  
                }  
  ...  
]  
6.http://localhost:8081/api/countries?limit=1:  
[  
    {  
        "name": {  
            "common": "Mauritania",  
            "official": "Islamic Republic of Mauritania",  
    ...  
]  
7.http://localhost:8081/api/countries?offset=250:  
[  
    {  
        "name": {  
            "common": "Palestine",  
            "official": "State of Palestine",  
            "nativeName": {  
  ...  
]  
8.http://localhost:8081/api/countries?offset=10&limit=1  
[  
    {  
        "name": {  
            "common": "Gibraltar",  
            "official": "Gibraltar",  
            "nativeName": {  
                "eng": {  
                    "official": "Gibraltar",  
  ...  
]  
9.http://localhost:8081/api/countries?sort=asc&countryName=uNited&population=400&offset=1&limit=5:  
[  
    {  
        "name": {  
            "common": "United Arab Emirates",  
            "official": "United Arab Emirates",  
            "nativeName": {  
                "ara": {  
                    "official": "الإمارات العربية المتحدة",  
   ...  
]  
10.http://localhost:8081/api/countries?sort=desc&countryName=uNited&population=400&offset=1&limit=5  
[  
    {  
        "name": {  
            "common": "United States",  
            "official": "United States of America",  
            "nativeName": {  
                "eng": {  
                    "official": "United States of America",  
    ...  
]  
