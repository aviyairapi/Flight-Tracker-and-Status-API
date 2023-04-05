# Flight-Tracker-and-Status-API
*Real-time flight position and status data.*

<div id="header" align="center">
  <img src="https://media.giphy.com/media/LRZc4dV2kf787nbOB3/giphy.gif" width="100"/>
</div>

[Aviyair’s Flight Tracker and Status API]( https://aviyair.com/flight-tracker-and-status-api/) focuses on the real-time coordinates and speed of live flights as well as their updated status. It has REST structure and output is provided in JSON format via GET requests. Updates for the data are in real-time and it is possible to get all flights at once or narrow down the data to cover flights of a certain airline, departure/arrival airport, flight number and more.

--------

## Main Endpoint and Filters with Description

**GET** `https://data.aviyair.com/data/v1/tracker?key=APIKEY&limit=30`

The limit can be anything, either be 5 or 14000 to set a limit to the total number of flights in the output. You can add the below filters to narrow down all live flights.

| Request Parameter  | Description |
| ------------- | ------------- |
| departure_iata  | Filter the flights based on the three-letter IATA code of the departure airport   |
| departure_icao  | Filter the flights based on the four-letter ICAO code of the departure airport   |
| arrival_iata  | Filter the flights based on the three-letter IATA code of the arrival airport  |
| arrival_icao  | Filter the flights based on the four-letter ICAO code of the arrival airport  |
| aircraft_icao | The ICAO code of the aircraft  |
| registration_number | The registration number of the aircraft to the relevant authority  |
| aircraft_icao24  | ICAO24 code of the aircraft  |
| airline_iata  | Airline IATA code  |
| airline_icao | Airline ICAO code  |
| flight_iata  | Flight number in IATA format, as in AB1234 |
| flight_icao  | Flight number in ICAO format, as in ABC1234  |
| flight_number  | Fllight number without the airline code at the front |
| status | The current status of the flight (started, en-route, unknown, landed  |
| limit | Limit the number of flights displayed in the output  |
| &lat=&lng=&distance= | Flights falling in a specified circle based on the coordinates (distance is measured in radius in km) |

------

## 200 OK Response Example

```
{
    "status": {
        "message": "Success"
    },
    "results": [
{
"aircraft":
{
"iataCode":""B77W"",
"icao24":4BA94E,
"icaoCode":"B77W",
"regNumber":"TC-JJN"
},
"airline":
{
"iataCode":"TK",
"icaoCode":"THY"
},
"arrival":
{
"iataCode":"IST",
"icaoCode":"LTBA"
},
"departure":
{"iataCode":"IAD",
"icaoCode":"KIAD"
},
"flight":
{
"iataNumber":"TK8",
"icaoNumber":"THY8",
"number":"8"
},
"geography":
{
"altitude":10668,
"direction":79,
"latitude":58.67,
"longitude":-44.16},
"speed":
{"horizontal":	937.112,
"isGround":0.0,
"vspeed":0.0
},
"status":"en-route",
"system":
{
"squawk":null,
"updated":1669878102
}

```

-------


## Full Documentation

Please visit our [website]( https://aviyair.com/documentation/).

-------

## Most Popular Use Cases

These are the most common use cases for the Flight Tracker and Status API but there are no limitations regarding how the API can be useful for you. If you have any concerns about the Terms and Conditions for the API, you may visit the hyperlink or contact us to ask about it.

-	Real-time interactive maps where people can track the current position of live flights and see flight details
-	Flight status tracking for travel agencies and airport greeting services
-	Air traffic analysis in real-time and also historically by saving the real-time data on your end
-	Measuring the airplane traffic density in an airport for airlines and airport ground operations
-	Gate assessment
-	Fuel consumption calculation (we do not provide fuel data but the API can be used to measure the total km a flight takes with speed and other determinants to calculate this)
-	Building flight simulations with actual routes

---------

## License

[Terms and Conditions of Use](https://aviyair.com/terms-and-conditions/) apply. If you have any questions or concerns about your use case of the Flight Tracker and Status API, please [contact us](https://aviyair.com/contact-aviyair/). 

--------

## How to Access

The API key to access the Flight Tracker and Status API is possible by creating an API subscription. The subscriptions do not require any commitments. It is possible to cancel anytime or make changes to your subscription level.

[View the prices and get an API key here.](https://aviyair.com/pricing-subscription-plans/)

