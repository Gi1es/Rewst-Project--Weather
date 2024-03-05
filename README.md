Weather-0.1
This is a simple powershell command to pull the weather condition and temp for a city that allows you to retrieve weather information for a specified city with the OpenWeatherMap API

Use the API key - 2115601e0089670bb976cd90e6eba717

  - Paste the code into a powershell terminal
  - Type the 'Get-Weather' function
      - Get-Weather -apikey '2115601e0089670bb976cd90e6eba717' -city 'london'

"function Get-Weather {...}' declares a funtion named 'Get-Weather' in powershell
The paramaters 
  $city - the city you want the weather for
  $apiKey - the apikey for openweathermap
URL is the address for API requests
The 'try' block has code that will attempt to retrieve the information from the API
  If there is an error the 'catch' block will handle it
  $response = Invoke-RestMethod -Uri $url -Method Get - This makes an HTTP GET request from the URL. This retrieves the weather info from the API and stores it in '$response'
  $weatherDescription = $response.weather[0].description - This pulls the weather description from the response
  $temp = $response.main.temp - This pulls the temperature from the response
  Write-Output "$weatherDescription, $temp - This will output the info from the description and the temp into the format "weatherDescription, temperature"
  Write-Output "Failed to retrieve weather information." - This is the message displayed in case of errors

  ![image](https://github.com/Gi1es/Rewst-Project--Weather/assets/162375031/eac911a5-e329-478c-bc5a-0fb18422fa7f)
