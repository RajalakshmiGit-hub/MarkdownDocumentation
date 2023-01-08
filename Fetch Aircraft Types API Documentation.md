# **API to Fetch Different Types of Aircraft** -- ***API Documentation***

Data about various aircraft types may be obtained using the aircraft type endpoint of the Aviationstack api. (Aviationstack API)
### **URL**
#### GET https://api.aviationstack.com/v1/aircraft\_types?access\_key=YOUR\_ACCESS\_KEY
### **Query Parameters**

|Parameter|Description|Type|Required/Optional|
| :- | :- | :- | :- |
|access\_key|Your API access key, which may be located on your account dashboard|String|Required|
|callback|This argument is used to specify the name of a JSONP callback function to wrap the API response in.|String|Optional|
|limit|Sets the maximum number of results to return in your API response. The maximum allowable value is 100 for Professional Plans below and 1000 for Professional Plans and higher. 100 is the default value.|Number|Optional|
|offset|Specifies an offset for pagination. Example: Specifying an offset of 10 in combination with a limit of 10 will show results 10-20. Default offset value is 0, starting with the first available result.|Number|Optional|
|search|Use this parameter to get autocomplete suggestions for aircraft types by specifying any search term as a string. |String|Optional|
###
### **Response**
The response will be sent back in the form of a JSON object. 





|**Element**|**Description**|**Type**|
| :- | :- | :- |
|<p>pagination.limit </p><p></p><p></p>|Returns the specified or default limit of results per pagination page.|Number|
|<p>pagination.offset </p><p></p><p></p>|Returns the specified or default pagination offset.|Number|
|pagination.count |Returns the number of results found on the current pagination page.|Number|
|pagination.total |Returns the total number of results found for your API request.|Number|
|data|Returns an array of aircrafts|Array of objects|
|data. aircraft\_name|Returns the aircraft name associated with the aircraft type.|String|
|data. iata\_code|Returns the IATA code associated with the aircraft type.|Number|
### **Sample Response**
{

`   `"pagination": {

`       `"limit": 100,

`       `"offset": 0,

`       `"count": 100,

`       `"total": 310

`   `},

`   `"data": [

`      `{

`         `"aircraft\_name": "Fokker 100",

`         `"iata\_code": "100"

`      `},

`      `[...]

`   `]
### **Status Codes and Errors**
The following table lists the returned HTTP status codes.

|**Code**|**Description**|
| :- | :- |
|200 |Success|
|400|Bad Request – Your request is invalid.|
|401|Unauthorized – Your API key is invalid.|
### **References**
*Aviationstack API*. (n.d.). Retrieved from Aviationstack: https://aviationstack.com/documentation



***Disclaimer:*** This has been created as part of the IIM Skills - Technical Writing Master Course's assignment. The Aviationstack’s aircraft\_types API has been documented. This has been created solely for educational purposes and not for commercial purposes.
