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
- Once the SDK URL is open in a web view or browser within your app, users can use our solution to search and book a flight.
- The app will have to handle the redirection URLs to capture success or failure responses:
  - For success: `https://example.sastotickets.com/success?data=<data>` as set in the JSON.
  - For failure: `https://example.sastotickets.com/failure?message=<error_message>` as set in the JSON.
