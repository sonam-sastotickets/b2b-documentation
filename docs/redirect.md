1. Generate a JSON  based on these params as

        {
        "access_token": "<accessToken from previous step>",
        "phone_number": 9800000000,
        "wallet_balance": 30000,
        "success_url": "https://example.sastotickets.com/success",
        "failure_url": "https://example.sastotickets.com/failure"
        }

2. Convert it to base64 and append to our web solution e.g.

        https://<b2c_url>/?data=<encoded base64 value>
        
    Note: **b2c_url** will be provided by Sasto Tickets Team

3. Open this URL in the App