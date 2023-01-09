# **API to Search Destination Countries** - ***API Documentation***

Use the countries endpoint of the Aviationstack API to search for destination countries.
### **URL**
#### GET https://api.aviationstack.com/v1/countries?access\_key=YOUR\_ACCESS\_KEY
### **Query Parameters**

|Parameter|Description|Type|Required/Optional|
| :- | :- | :- | :- |
|access\_key|Your API access key, which may be located on your account dashboard|String|Required|
|callback|This argument is used to specify the name of a JSONP callback function to wrap the API response in.|String|Optional|
|limit|Sets the maximum number of results to return in your API response. The maximum allowable value is 100 for Professional Plans below and 1000 for Professional Plans and higher. 100 is the default value.|Number|Optional|
|offset|Specifies an offset for pagination. Example: Specifying an offset of 10 in combination with a limit of 10 will show results 10-20. Default offset value is 0, starting with the first available result.|Number|Optional|
|search|Use this parameter to get autocomplete suggestions for countries by specifying any search term as a string. |String|Optional|
### **Response**
The response will be sent back in the form of a JSON object. 

|Element|Description|Type|
| :- | :- | :- |
|<p>pagination.limit </p><p></p>|Returns the specified or default limit of results per pagination page.|Number|
|<p>pagination.offset </p><p></p>|Returns the specified or default pagination offset.|Number|
|pagination.count |Returns the number of results found on the current pagination page.|Number|
|pagination.total |Returns the total number of results found for your API request.|Number|
|data|Returns an array of countries|Array of objects|
|data. country\_name|Returns the name of the country.|String|
|data. country\_iso2|Returns the 2-letter ISO code of the country.|String|
|data. country\_iso3|Returns the 3-letter ISO code of the country.|String|
|data. country\_iso\_numeric|Returns the numeric ISO code of the country.|Number|
|data. population|Returns the population of the country.|Number|
|data. capital|Returns the capital of the country.|String|
|data. continent|Returns the continent the country is located in.|String|
|data. currency\_name|Returns the name of the currency associated with the country.|String|
|data. currency\_code|Returns the code of the currency associated with the country.|String|
|data. fips\_code|Returns the FIPS code of the country.|String|
|data. phone\_prefix|Returns the phone prefix associated with the country.|Number|

 **Sample Response**
 
{

`   `"pagination": {

`       `"limit": 100,

`       `"offset": 0,

`       `"count": 100,

`       `"total": 252

`   `},

`   `"data": [

`      `{

`         `"country\_name": "Andorra",

`         `"country\_iso2": "AD",

`         `"country\_iso3": "AND",

`         `"country\_iso\_numeric": "20",

`         `"population": "84000",

`         `"capital": "Andorra la Vella",

`         `"continent": "EU",

`         `"currency\_name": "Euro",

`         `"currency\_code": "EUR",

`         `"fips\_code": "AN",

`         `"phone\_prefix": "376"

`      `},

`      `[...]

`   `]

}      

### **Status Codes and Errors**
The following table lists the returned HTTP status codes.

|Code|Description|
| :- | :- |
|200 |Success|
|400|Bad Request – Your request is invalid.|
|401|Unauthorized – Your API key is invalid.|

### **References**
*Aviationstack API*. (n.d.). Retrieved from Aviationstack: https://aviationstack.com/documentation

***Disclaimer:*** This has been created as part of the IIM Skills - Technical Writing Master Course's assignment. The countries endpoint of Aviationstack API has been documented. This has been created solely for educational purposes and not for commercial purposes.
