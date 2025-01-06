### JSON Configuration for Booking
To initiate the booking process, the following JSON configuration must be generated:
```json
{
    "access_token": "<accessToken from previous step>",
    "phone_number": 9800000000,
    "wallet_balance": 30000,
    "success_url": "https://example.sastotickets.com/success",
    "failure_url": "https://example.sastotickets.com/failure"
}
```
!!! note

    *wallet_balance* can be set to null if restriction related to amount is NOT required when booking.

### Base64 Encoding and URL Construction
1. Convert the JSON configuration to a Base64-encoded string.
2. Append the encoded string to the base URL provided by the Sasto Tickets Team as follows:
   ```
   https://<b2c_url>/?data=<encoded base64 value>
   ```

### Open the URL in the App
Once the URL is constructed, open it in a web view or browser within your app to initiate the booking process.

### Flights Search & Booking
The SDK facilitates the flight search functionality and the availability of selected flights and provides detailed options. The SDK handles flight reservation, returning booking details to the vendor.

### Capturing Response
- Once the SDK URL is open in a web view or browser within your app, users can use our solution to search and book a flight
- The app will have to handle the redirection URLs to capture success or failure responses:

#### Success
For success: `https://example.sastotickets.com/success?data=<data>` as set in the JSON.
Example:

    https://example.sastotickets.com/success?data=eyJ0b3RhbENvc3QiOjQ0MDcsImJlYXJlclRva2VuIjoiZXlKMGVYQWlPaUpLVjFRaUxDSmhiR2NpT2lKSVV6STFOaUo5LmV5SnBjM01pT2lKb2RIUndPbHd2WEM5aGNHa3VjMkZ6ZEc5MGFXTnJaWFJ6TG1OdmJWd3ZZWEJwWEM5aU1tSmNMM1l4WEM5blpYUXRkRzlyWlc0aUxDSnBZWFFpT2pFMk9EVTROamN6Tmpnc0ltNWlaaUk2TVRZNE5UZzJOek0yT0N3aWFuUnBJam9pVVc4MmExWkZNVGxMY1ZCcVZrSkNaeUlzSW5OMVlpSTZOeXdpY0hKMklqb2laakkzWkdKbU16YzVNR1UzWWpGbVkyRTRaR1ppTm1NNE9HVm1PVFZoWmprd05EWmhPRGhtWXlKOS4wREhFMzNIUWpJeUZGTzZPQ00zSlB5a3FMeGNBVDFpSXBuYzExUTBYVU1NIiwiZmxpZ2h0U3VtbWFyeSI6eyJkZXBhcnR1cmVGbGlnaHQiOnsiY2FycmllckNvZGUiOiJTMSIsImNhcnJpZXJMb2dvIjoiaHR0cHM6Ly9zYXN0b3RpY2tldHMtdWF0LWZsaWdodHMuczMuYXAtc291dGhlYXN0LTEuYW1hem9uYXdzLmNvbS9haXJsaW5lcy8xNTYyNTc4NTQ4LTUzMzk4Mi5wbmciLCJjYXJyaWVyTmFtZSI6IlNhdXJ5YSBBaXJsaW5lcyIsImRlcHREYXRlIjoiMjAyNS0wMy0xNSIsImRlcHRUaW1lIjoiMDg6MDAgQU0iLCJhcnJpdmFsRGF0ZSI6IjIwMjUtMDMtMTUiLCJhcnJpdmFsVGltZSI6IjA4OjMwIEFNIiwiZGVwYXJ0dXJlQWlycG9ydENvZGUiOiJLVE0iLCJkZXBhcnR1cmVBaXJwb3J0IjoiVHJpYmh1dmFuIEludOKAmWwgQWlycG9ydCIsImRlcGFydHVyZUNpdHkiOiJLYXRobWFuZHUiLCJkZXBhcnR1cmVDb3VudHJ5IjoiTmVwYWwiLCJhcnJpdmFsQWlycG9ydENvZGUiOiJQS1IiLCJhcnJpdmFsQWlycG9ydCI6IlBva2hhcmEgQWlycG9ydCIsImFycml2YWxDaXR5IjoiUG9raGFyYSIsImFycml2YWxDb3VudHJ5IjoiTmVwYWwifSwicmV0dXJuRmxpZ2h0IjpudWxsfSwiZW1lcmdlbmN5Q29udGFjdCI6eyJjb250YWN0IjoiOTg0MDAxMDE5MSIsImVtYWlsIjoic29uYWFtLmhpdGFuZ0BnbWFpbC5jb20iLCJuYW1lIjoiQW5pbCBSYXlhbWFqaGkifSwiYm9va2luZ1N1bW1hcnkiOnsiUE5SIjoiSVVTUDFDIiwiYm9va2luZ1JlZmVyZW5jZUlEIjoiZDU2ODBlZDctYTI3ZC00ZDc2LTg5MjEtMmE2MGI0YWFlODY2IiwiY3VycmVuY3kiOiJOUFIiLCJwYXNzZW5nZXJzIjpbeyJwYXNzZW5nZXJfaWQiOiJTVDI0NjY4IiwicGFzc2VuZ2VyX3R5cGUiOiJBRFQiLCJwYXNzZW5nZXJfbmFtZSI6IlJheWFtYWpoaSBBbmlsIn1dLCJ0cmlwVHlwZSI6Im9uZXdheSJ9fQ==
    
    
!!! note

    You will have to decode the data captured from base64 to get the json response, The data from this step will be used in the Ticketing API


=== "One Way"

    ``` c++
    {
        "totalCost": 4407,
        "bearerToken": "-",
        "flightSummary": {
            "departureFlight": {
            "carrierCode": "S1",
            "carrierLogo": "https://sastotickets-uat-flights.s3.ap-southeast-1.amazonaws.com/airlines/1562578548-533982.png",
            "carrierName": "Saurya Airlines",
            "deptDate": "2025-01-14",
            "deptTime": "08:00 AM",
            "arrivalDate": "2025-01-14",
            "arrivalTime": "08:30 AM",
            "departureAirportCode": "KTM",
            "departureAirport": "Tribhuvan Int’l Airport",
            "departureCity": "Kathmandu",
            "departureCountry": "Nepal",
            "arrivalAirportCode": "PKR",
            "arrivalAirport": "Pokhara Airport",
            "arrivalCity": "Pokhara",
            "arrivalCountry": "Nepal"
            },
            "returnFlight": null
        },
        "emergencyContact": {
            "contact": "9800000001",
            "email": "sonam@sastotickets.com",
            "name": "-"
        },
        "bookingSummary": {
            "PNR": "JUSP1C",
            "bookingReferenceID": "52c8a810-089a-428f-b12d-4040592a9116",
            "currency": "NPR",
            "passengers": [
            {
                "passenger_id": "ST24669",
                "passenger_type": "ADT",
                "passenger_name": "-"
            }
            ],
            "tripType": "oneway"
        }
    }
    ```

=== "Round Trip"

    ``` c++
    {
        "totalCost": 67342,
        "bearerToken": "-",
        "flightSummary": {
            "departureFlight": {
            "carrierCode": "AI",
            "carrierLogo": "https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/1703064315-1249041617.png",
            "carrierName": "Air India",
            "deptDate": "2025-09-23",
            "deptTime": "14:55 PM",
            "arrivalDate": "2025-09-23",
            "arrivalTime": "21:10 PM",
            "departureAirportCode": "KTM",
            "departureAirport": "Tribhuvan Int’l Airport",
            "departureCity": "Kathmandu",
            "departureCountry": "Nepal",
            "arrivalAirportCode": "DOH",
            "arrivalAirport": "Hamad Int’l Airport",
            "arrivalCity": "Doha",
            "arrivalCountry": "Qatar"
            },
            "returnFlight": {
            "carrierCode": "AI",
            "carrierLogo": "https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/1703064315-1249041617.png",
            "carrierName": "Air India",
            "deptDate": "2025-09-30",
            "deptTime": "22:10 PM",
            "arrivalDate": "2025-10-01",
            "arrivalTime": "13:55 PM",
            "departureAirportCode": "DOH",
            "departureAirport": "Hamad Int’l Airport",
            "departureCity": "Doha",
            "departureCountry": "Qatar",
            "arrivalAirportCode": "KTM",
            "arrivalAirport": "Tribhuvan Int’l Airport",
            "arrivalCity": "Kathmandu",
            "arrivalCountry": "Nepal"
            }
        },
        "emergencyContact": {
            "contact": "9840000000",
            "email": "sonam@sastotickets.com",
            "name": "Anil Rayamajhi"
        },
        "bookingSummary": {
            "PNR": "RABPWV",
            "bookingReferenceID": "aceba74f-a152-4626-b3b2-8173845adae5",
            "currency": "NPR",
            "passengers": [
            {
                "passenger_id": "ST608028",
                "passenger_type": "ADT",
                "passenger_name": "Rayamajhi Anil"
            }
            ],
            "tripType": "round"
        }
        }
    ```
=== "Multi City"

    ``` c++
    //TBA
    {
       
    }
    ```



#### Failure
  - Failure: `https://example.sastotickets.com/failure?message=<error_message>` as set in the JSON.
  - Example:

    ```https://example.sastotickets.com/failure?message=access_token%20and%20phone_number%20is%20required```
    ```https://example.sastotickets.com/failure?message=Booking%20Failed.%20Flight%20has%20been%20booked%20or%20not%20available.%20Please%20try%20with%20another%20flight```
