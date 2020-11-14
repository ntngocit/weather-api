1. Update settings
    * Setting file: weather-api/src/main/resources/config.yaml
2. weather-api project implemented 2 APIs:

	2.1 Get weather by city
	
		* Endpoint : /api/weather/{countryName}/{cityName}
		
		* Headers :
			- Requester-ID : the ID of the requester
		* URI params:
			- countryName : name of country (E.g : Australia)
			- cityName: name of city in countryName (E.g: Melbourne)
		* Method: GET
		* Example:
			- Request: /api/weather/Australia/Melbourne
			- Response: 
			{ "NewDataSet": { "Location": "Melbourne", "Time": "11 AM", "Wind": "15 km per hour", "Visibility": "10 km", "SkyConditions": "sunny", "Temperature": "18", "DewPoint": "2 C", "RelativeHumidity": "35", "Status": "Normal" } }
	2.2 Get cities of country 
	
		* Endpoint : /api/cities/{countryName} 
		* Headers : 
			- Requester-ID : the ID of the requester 
		* URI params: 
			- countryName : name of country (E.g : Australia) 
		* Method: GET 
		* Example: 
			- Request: /api/cities/Australia 
			- Response: [ { "city": "Archerfield Aerodrome" }, { "city": "Amberley Aerodrome" }, { "city": "Alice Springs Aerodrome" } ]
