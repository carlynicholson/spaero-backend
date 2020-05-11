# Project Overview

## Project Links

- deployment link
- [frontend repo link](https://github.com/carlynicholson/spaero-frontend)
- [backend repo link](https://github.com/carlynicholson/spaero-backend)

## Project Description

For my project, I'll be building out a flight booking app. It will search flights offered by multiple carriers, and deals offered on other travel booking sites.  

[Example](https://www.skyscanner.com/)


## API

I'll be using the [Skyscanner Flight Search](https://rapidapi.com/skyscanner/api/skyscanner-flight-search) API to pull flight data, including quotes, places, carriers, and currencies.

I'll also utilize the [City Geo-Location Lookup](https://rapidapi.com/dev132/api/city-geo-location-lookup/) API for imroved UX purposes. 


## Wireframes

[Homepage](https://res.cloudinary.com/df6sigxz7/image/upload/v1588967613/spaero/planning/home.png)

[Booking page](https://res.cloudinary.com/df6sigxz7/image/upload/v1588967612/spaero/planning/booking.png)

[Booking details](https://res.cloudinary.com/df6sigxz7/image/upload/v1588967612/spaero/planning/flight_details.png)


## [Time/Priority Matrix](https://res.cloudinary.com/df6sigxz7/image/upload/v1588968378/spaero/planning/time_estimation.png)

Estimated time: 34.5 hours

### MVP/PostMVP

#### MVP 
- Nav + Header
- Booking Form
- Search Filters
- Search Results
- Details Modal
- Footer

#### PostMVP

- Route to carrier website
- Popular Destinations
- Login/Authorization

## Components

| Component | Description | 
| --- | :--- | 
| App | This will make the initial data pull and include React Router | 
| Header | This will render the header and include the nav | 
| Booking Form | This will enable users to make flight searches | 
| Search Results | This will render available flights based on user criteria | 
| Search Filters | This will allow users to filter flight results | 
| Details Modal | This will confirm the selected flight details before directing users to the carrier site to complete booking | 
| Footer | This will render the footer for the app | 

##### Time Frames

| Component | Priority | Estimated Time | Time Invetsted | Actual Time |
| --- | :---: |  :---: | :---: | :---: |
| Working with API | H | 10 hours |   |   |
| Header | H | 2 hours |   |   |
| Booking Form | H | 5 hours |   |   |
| Search Results | H | 5 hours |   |   |
| Search Filters | H | 10 hours |   |   |
| Details Modal | H | 4 hours |   |   |
| Footer | L | 1.5 hours |   |   |
| Total |   | 34.5 hours |   |   |

## Additional Libraries
- [Bootstrap](https://getbootstrap.com/)
- [Sass](https://sass-lang.com/)

## Code Snippet

The [Skyscanner Flight Search](https://rapidapi.com/skyscanner/api/skyscanner-flight-search) API returns the below data for flights from San Francisco International airport going to John F. Kennedy International airport.

```JSON
{
    "Quotes": [
       {
          "QuoteId":1,
          "MinPrice":336,
          "Direct":true,
          "OutboundLeg": {
             "CarrierIds": [
                1864
             ],
             "OriginId":81727,
             "DestinationId":60987,
             "DepartureDate":"2018-04-01T00:00:00"
          },
          "InboundLeg": {
             "CarrierIds": [
                851
             ],
             "OriginId":60987,
             "DestinationId":81727,
             "DepartureDate":"2018-05-01T00:00:00"
          },
          "QuoteDateTime":"2018-03-08T04:54:00"
       }
    ],
    "Places": [
       {
          "PlaceId":60987,
          "IataCode":"JFK",
          "Name":"New York John F. Kennedy",
          "Type":"Station",
          "SkyscannerCode":"JFK",
          "CityName":"New York",
          "CityId":"NYCA",
          "CountryName":"United States"
       },
       {
          "PlaceId":81727,
          "IataCode":"SFO",
          "Name":"San Francisco International",
          "Type":"Station",
          "SkyscannerCode":"SFO",
          "CityName":"San Francisco",
          "CityId":"SFOA",
          "CountryName":"United States"
       }
    ],
    "Carriers": [
       {
          "CarrierId":851,
          "Name":"Alaska Airlines"
       },
       {
          "CarrierId":870,
          "Name":"jetBlue"
       },
       {
          "CarrierId":1721,
          "Name":"Sun Country Airlines"
       },
       {
          "CarrierId":1864,
          "Name":"Virgin America"
       }
    ],
    "Currencies": [
       {
          "Code":"USD",
          "Symbol":"$",
          "ThousandsSeparator":",",
          "DecimalSeparator":".",
          "SymbolOnLeft":true,
          "SpaceBetweenAmountAndSymbol":false,
          "RoundingCoefficient":0,
          "DecimalDigits":2
       }
    ]
}
```