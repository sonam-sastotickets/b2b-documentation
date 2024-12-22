```
Endpoint: ~/issue-ticket
Method: Post
Header Params: Content-Type  : application/json
Authorization : Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOlwvXC9nZHMtYWRtaW4udGVzdFwvYXBpXC9pbnRsXC9hbmRyb2lkXC9pbml0aWFsaXplIiwiaWF0IjoxNjEzMzg1ODY3LCJleHAiOjE2MTMzODk0NjcsIm5iZiI6MTYxMzM4NTg2NywianRpIjoiY3o2eFZLdEVkd05jTTRVcCIsInN1YiI6MTMsInBydiI6IjQyZWRlMzMzNGEwNGNkNjVjYjJiZTNmNWFkZmViMmMxZWRkMzA3NzQifQ.UzEWszpOW92jOqSkdciWoGV4456CdS1nuPx7Tql-_Xk
```


| **Attribute**          | **Datatype**        | **Required** | **Description**                                               | **Values**                   |
|-------------------------|---------------------|--------------|---------------------------------------------------------------|------------------------------|
| `user_type`            | `string`           | Optional     | Agent user type                                               | `agent`, `customer`          |
| `bookingReferenceID`   | `bookingReferenceID` | Required     | Booking Reference ID from booking response                    |                              |
| `tripType`             | `string`           | Required     | Trip Type                                                     |                              |
| `currency`             | `string`           | Required     | Currency Type                                                 | `NPR`, `USD`                 |
| `PNR`                  | `string`           | Optional     | Passenger Name Record (PNR)                                   |                              |
| `amount`               | `integer`          | Optional     | Total fare amount                                             |                              |
| `referenceCode`        | `string`           | Optional     | Agent Reference code or transaction identifier                |                              |

### Sample Request

=== "One Way"

    ``` c++
    {
        "user_type": "agent",
        "bookingReferenceID": "e1caec16-f675-48ea-a40c-5e1d05741300",
        "tripType": "oneway",
        "referenceCode": "KFIKDHKSKDH",
        "PNR": "PQMJ8E",
        "amount": 42149,
        "currency": "NPR"
    }
    ```

=== "Round Trip"

    ``` c++
    {
        "user_type": "agent",
        "bookingReferenceID": "2368c81d-d420-453f-a0ae-9fb5530ba34b",
        "tripType": "round",
        "referenceCode": "KFIKDHKSKDH",
        "PNR": "PQVBOE",
        "amount": 74514,
        "currency": "NPR"
    }
    ```
=== "Multi City"

    ``` c++
    {
        "user_type": "agent",
        "bookingReferenceID": "d2c3b2fc-9bcd-4718-b0ee-7ed147b083e7",
        "tripType": "multicity",
        "referenceCode": "KFIKDHKSKDH",
        "PNR": "PQXM2B",
        "amount": 106959,
        "currency": "NPR"
    }
    ```
### Sample Response
=== "One Way"

    ``` c++
    {
        "success": true,
        "data": {
            "ticketSummary": {
                "ticketReferenceID": "29f27b24-3f33-4190-9835-9859c790fc47",
                "PNR": "PQMJ8E",
                "tripType": "oneway",
                "currency": "NPR",
                "issued_date": "Tue, Feb 14, 2023"
            },
            "flightSummary": {
                "airline_confirmation_code": "PQMJ8E",
                "departure_date": "2023-07-22",
                "departure_time": "10:10 AM",
                "arrival_date": "2023-07-22",
                "arrival_time": "12:25 PM",
                "total_flying_hours": "05 Hr 00 Min",
                "depart_city_airport_code": "KTM",
                "depart_city_airport_name": "Tribhuvan Intl Airport",
                "depart_city_name": "Kathmandu City",
                "depart_city_country": "Nepal",
                "carrierCode": "QR",
                "carrierLogo": "https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/1633428326-1898803185.png",
                "carrierName": "Qatar Airways",
                "dest_city_airport_code": "DOH",
                "dest_city_airport_name": "Hamad Int’l Airport",
                "dest_city_name": "Doha",
                "dest_city_country": "Qatar",
                "flight_segments": [
                    {
                        "carrierCode": "QR",
                        "carrierName": "Qatar Airways",
                        "carrierLogo": "https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/1633428326-1898803185.png",
                        "flight_number": "653",
                        "flight_equipment": "Airbus A330-300",
                        "cabin_class": "M",
                        "seg_departure_date": "2023-07-22",
                        "seg_departure_time": "10:10 AM",
                        "seg_arrival_date": "2023-07-22",
                        "seg_arrival_time": "12:25 PM",
                        "seg_total_flying_hours": "05:00:00",
                        "seg_departure_airport_code": "KTM",
                        "seg_departure_airport": "Tribhuvan Intl Airport",
                        "seg_departure_city": "Kathmandu City",
                        "seg_departure_country": "Nepal",
                        "seg_departure_terminal": "I",
                        "seg_arrival_airport_code": "DOH",
                        "seg_arrival_airport": "Hamad Int’l Airport",
                        "seg_arrival_city": "Doha",
                        "seg_arrival_country": "Qatar",
                        "seg_arrival_terminal": "",
                        "seg_connection_time": false
                    }
                ]
            },
            "fareInformation": {
                "total_adt": 41893,
                "total_chd": 0,
                "total_inf": 0,
                "total_cost": 41893,
                "cashBack": 300
            },
            "baggageDetails": {
                "cabin": "7 Kg",
                "baggage": "30 Kg"
            },
            "passengers": [
                {
                    "passenger_type": "ADT",
                    "passenger_name": "Maharjan Rabi",
                    "eticket_number": "157-6752209683",
                    "PNR": "PQMJ8E",
                    "airlines_confirmation": "PQMJ8E"
                }
            ],
            "contactDetails": {
                "email": "maharjanrabi1@gmail.com",
                "phone": "9849932310"
            },
            "eticketLink": "https://sastotickets-flights-private.s3.ap-southeast-1.amazonaws.com/tickets/PQMJ8E-1676354461.pdf?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIA4CEOEY6AUXGMCTXF%2F20230214%2Fap-southeast-1%2Fs3%2Faws4_request&X-Amz-Date=20230214T060104Z&X-Amz-SignedHeaders=host&X-Amz-Expires=900&X-Amz-Signature=a834632054848ad610561f9a7588a1ff789ae2a35c7991f091d97a043ed7d043"
        }
    }
    ```

=== "Round Trip"

    ``` c++
    {
        "success": true,
        "data": {
            "ticketSummary": {
                "ticketReferenceID": "f767edef-1334-4ac9-ae02-2f328db9fd8c",
                "PNR": "PQVBOE",
                "tripType": "round",
                "currency": "NPR",
                "issued_date": "Tue, Feb 14, 2023"
            },
            "flightSummary": {
                "airline_confirmation_code": "PQVBOE",
                "departure_date": "2023-07-22",
                "departure_time": "10:10 AM",
                "depart_city_airport_code": "KTM",
                "depart_city_airport_name": "Tribhuvan Intl Airport",
                "depart_city_name": "Kathmandu City",
                "depart_city_country": "Nepal",
                "arrival_date": "2023-07-22",
                "arrival_time": "12:25 PM",
                "total_flying_hours": "05 Hr 00 Min",
                "dest_city_airport_code": "DOH",
                "dest_city_airport_name": "Hamad Int’l Airport",
                "dest_city_name": "Doha",
                "dest_city_country": "Qatar",
                "carrierCode": "QR",
                "carrierLogo": "https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/1633428326-1898803185.png",
                "carrierName": "Qatar Airways",
                "return_departure_date": "2023-07-30",
                "return_departure_time": "00:35 AM",
                "return_depart_city_airport_code": "DOH",
                "return_depart_city_airport_name": "Hamad Int’l Airport",
                "return_depart_city_name": "Doha",
                "return_depart_city_country": "Qatar",
                "return_arrival_date": "2023-07-30",
                "return_arrival_time": "08:05 AM",
                "return_total_flying_hours": "04 Hr 45 Min",
                "return_dest_city_airport_code": "KTM",
                "return_dest_city_airport_name": "Tribhuvan Intl Airport",
                "return_dest_city_name": "Kathmandu City",
                "return_dest_city_country": "Nepal",
                "carrierCodeReturn": "QR",
                "carrierLogoReturn": "https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/1633428326-1898803185.png",
                "carrierNameReturn": "Qatar Airways",
                "flight_segments_outbound": [
                    {
                        "carrierCode": "QR",
                        "carrierName": "Qatar Airways",
                        "carrierLogo": "https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/1633428326-1898803185.png",
                        "flight_number": "653",
                        "flight_equipment": "Airbus A330-300",
                        "cabin_class": "M",
                        "seg_departure_date": "2023-07-22",
                        "seg_departure_time": "10:10 AM",
                        "seg_arrival_date": "2023-07-22",
                        "seg_arrival_time": "12:25 PM",
                        "seg_total_flying_hours": "05:00:00",
                        "seg_departure_airport_code": "KTM",
                        "seg_departure_airport": "Tribhuvan Intl Airport",
                        "seg_departure_city": "Kathmandu City",
                        "seg_departure_country": "Nepal",
                        "seg_departure_terminal": "I",
                        "seg_arrival_airport_code": "DOH",
                        "seg_arrival_airport": "Hamad Int’l Airport",
                        "seg_arrival_city": "Doha",
                        "seg_arrival_country": "Qatar",
                        "seg_arrival_terminal": "",
                        "seg_connection_time": false
                    }
                ],
                "flight_segments_return": [
                    {
                        "carrierCode": "QR",
                        "carrierName": "Qatar Airways",
                        "carrierLogo": "https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/1633428326-1898803185.png",
                        "flight_number": "652",
                        "flight_equipment": "Airbus A330-300",
                        "cabin_class": "M",
                        "seg_departure_date": "2023-07-30",
                        "seg_departure_time": "00:35 AM",
                        "seg_arrival_date": "2023-07-30",
                        "seg_arrival_time": "08:05 AM",
                        "seg_total_flying_hours": "04:45:00",
                        "seg_departure_airport_code": "DOH",
                        "seg_departure_airport": "Hamad Int’l Airport",
                        "seg_departure_city": "Doha",
                        "seg_departure_country": "Qatar",
                        "seg_departure_terminal": "",
                        "seg_arrival_airport_code": "KTM",
                        "seg_arrival_airport": "Tribhuvan Intl Airport",
                        "seg_arrival_city": "Kathmandu City",
                        "seg_arrival_country": "Nepal",
                        "seg_arrival_terminal": "I",
                        "seg_connection_time": false
                    }
                ]
            },
            "fareInformation": {
                "total_adt": 41893,
                "total_chd": 0,
                "total_inf": 0,
                "total_cost": 41893,
                "cashBack": 300
            },
            "baggageDetails": {
                "outbound": {
                    "cabin": "7 Kg",
                    "baggage": "30 Kg"
                },
                "return": {
                    "cabin": "7 Kg",
                    "baggage": "25 Kg"
                }
            },
            "passengers": [
                {
                    "passenger_type": "ADT",
                    "passenger_name": "Maharjan Rabi",
                    "eticket_number": "157-6752209684",
                    "PNR": "PQVBOE",
                    "airlines_confirmation": "PQVBOE"
                }
            ],
            "contactDetails": {
                "email": "maharjanrabi1@gmail.com",
                "phone": "9849932310"
            },
            "eticketLink": "https://sastotickets-flights-private.s3.ap-southeast-1.amazonaws.com/tickets/PQMJ8E-1676354461.pdf?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIA4CEOEY6AUXGMCTXF%2F20230214%2Fap-southeast-1%2Fs3%2Faws4_request&X-Amz-Date=20230214T060104Z&X-Amz-SignedHeaders=host&X-Amz-Expires=900&X-Amz-Signature=a834632054848ad610561f9a7588a1ff789ae2a35c7991f091d97a043ed7d043"
        }
    }
    ```
=== "Multi City"

    ``` c++
    {
        "success": true,
        "data": {
            "ticketSummary": {
                "ticketReferenceID": "c6493116-25b8-4105-a26a-1c79937c5421",
                "PNR": "PQXM2B",
                "tripType": "multicity",
                "currency": "NPR",
                "issued_date": "Tue, Feb 14, 2023"
            },
            "flightSummary": {
                "flight_segments": [
                    {
                        "airline_confirmation_code": "197IJB",
                        "seg_departure_date": "2023-08-01",
                        "seg_departure_time": "15:45 PM",
                        "seg_arrival_date": "2023-08-02",
                        "seg_arrival_time": "03:20 AM",
                        "seg_total_flying_hours": "01 Hr 45 Min",
                        "seg_departure_airport_code": "KTM",
                        "seg_departure_airport": "Tribhuvan Intl Airport",
                        "seg_departure_city": "Kathmandu City",
                        "seg_departure_country": "Nepal",
                        "seg_arrival_airport_code": "DEL",
                        "seg_arrival_airport": "Indira Gandhi Int’l Airport",
                        "seg_arrival_city": "New Delhi",
                        "seg_arrival_country": "India",
                        "carrierCode": "FZ",
                        "carrierLogo": "https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/FZ_flydubai.png",
                        "carrierName": "Fly Dubai",
                        "connecting_segments": [
                            {
                                "carrierCode": "FZ",
                                "carrierName": "Fly Dubai",
                                "carrierLogo": "https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/FZ_flydubai.png",
                                "flight_number": "540",
                                "flight_equipment": "Boeing 737",
                                "cabin_class": "M",
                                "seg_departure_date": "2023-08-01",
                                "seg_departure_time": "15:45 PM",
                                "seg_arrival_date": "2023-08-01",
                                "seg_arrival_time": "18:50 PM",
                                "seg_total_flying_hours": "04:50:00",
                                "seg_departure_airport_code": "KTM",
                                "seg_departure_airport": "Tribhuvan Intl Airport",
                                "seg_departure_city": "Kathmandu City",
                                "seg_departure_country": "Nepal",
                                "seg_departure_terminal": "I",
                                "seg_arrival_airport_code": "DXB",
                                "seg_arrival_airport": "Dubai Int’l Airport",
                                "seg_arrival_city": "Dubai",
                                "seg_arrival_country": "United Arab Emirates",
                                "seg_arrival_terminal": "2",
                                "seg_connection_time": false
                            },
                            {
                                "carrierCode": "FZ",
                                "carrierName": "Fly Dubai",
                                "carrierLogo": "https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/FZ_flydubai.png",
                                "flight_number": "431",
                                "flight_equipment": "Boeing 737",
                                "cabin_class": "M",
                                "seg_departure_date": "2023-08-01",
                                "seg_departure_time": "22:10 PM",
                                "seg_arrival_date": "2023-08-02",
                                "seg_arrival_time": "03:20 AM",
                                "seg_total_flying_hours": "03:40:00",
                                "seg_departure_airport_code": "DXB",
                                "seg_departure_airport": "Dubai Int’l Airport",
                                "seg_departure_city": "Dubai",
                                "seg_departure_country": "United Arab Emirates",
                                "seg_departure_terminal": "2",
                                "seg_arrival_airport_code": "DEL",
                                "seg_arrival_airport": "Indira Gandhi Int’l Airport",
                                "seg_arrival_city": "New Delhi",
                                "seg_arrival_country": "India",
                                "seg_arrival_terminal": "3",
                                "seg_connection_time": "05 hr 10 min"
                            }
                        ]
                    },
                    {
                        "airline_confirmation_code": "197IJB",
                        "seg_departure_date": "2023-08-10",
                        "seg_departure_time": "04:20 AM",
                        "seg_arrival_date": "2023-08-10",
                        "seg_arrival_time": "07:00 AM",
                        "seg_total_flying_hours": "01 Hr 45 Min",
                        "seg_departure_airport_code": "DEL",
                        "seg_departure_airport": "Indira Gandhi Int’l Airport",
                        "seg_departure_city": "New Delhi",
                        "seg_departure_country": "India",
                        "seg_arrival_airport_code": "DXB",
                        "seg_arrival_airport": "Dubai Int’l Airport",
                        "seg_arrival_city": "Dubai",
                        "seg_arrival_country": "United Arab Emirates",
                        "carrierCode": "FZ",
                        "carrierLogo": "https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/FZ_flydubai.png",
                        "carrierName": "Fly Dubai",
                        "connecting_segments": [
                            {
                                "carrierCode": "FZ",
                                "carrierName": "Fly Dubai",
                                "carrierLogo": "https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/FZ_flydubai.png",
                                "flight_number": "432",
                                "flight_equipment": "Boeing 737",
                                "cabin_class": "M",
                                "seg_departure_date": "2023-08-10",
                                "seg_departure_time": "04:20 AM",
                                "seg_arrival_date": "2023-08-10",
                                "seg_arrival_time": "07:00 AM",
                                "seg_total_flying_hours": "04:10:00",
                                "seg_departure_airport_code": "DEL",
                                "seg_departure_airport": "Indira Gandhi Int’l Airport",
                                "seg_departure_city": "New Delhi",
                                "seg_departure_country": "India",
                                "seg_departure_terminal": "3",
                                "seg_arrival_airport_code": "DXB",
                                "seg_arrival_airport": "Dubai Int’l Airport",
                                "seg_arrival_city": "Dubai",
                                "seg_arrival_country": "United Arab Emirates",
                                "seg_arrival_terminal": "2",
                                "seg_connection_time": false
                            }
                        ]
                    },
                    {
                        "airline_confirmation_code": "197IJB",
                        "seg_departure_date": "2023-08-15",
                        "seg_departure_time": "13:50 PM",
                        "seg_arrival_date": "2023-08-15",
                        "seg_arrival_time": "20:00 PM",
                        "seg_total_flying_hours": "01 Hr 45 Min",
                        "seg_departure_airport_code": "DXB",
                        "seg_departure_airport": "Dubai Int’l Airport",
                        "seg_departure_city": "Dubai",
                        "seg_departure_country": "United Arab Emirates",
                        "seg_arrival_airport_code": "KTM",
                        "seg_arrival_airport": "Tribhuvan Intl Airport",
                        "seg_arrival_city": "Kathmandu City",
                        "seg_arrival_country": "Nepal",
                        "carrierCode": "FZ",
                        "carrierLogo": "https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/FZ_flydubai.png",
                        "carrierName": "Fly Dubai",
                        "connecting_segments": [
                            {
                                "carrierCode": "FZ",
                                "carrierName": "Fly Dubai",
                                "carrierLogo": "https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/FZ_flydubai.png",
                                "flight_number": "573",
                                "flight_equipment": "Boeing 737",
                                "cabin_class": "M",
                                "seg_departure_date": "2023-08-15",
                                "seg_departure_time": "13:50 PM",
                                "seg_arrival_date": "2023-08-15",
                                "seg_arrival_time": "20:00 PM",
                                "seg_total_flying_hours": "04:25:00",
                                "seg_departure_airport_code": "DXB",
                                "seg_departure_airport": "Dubai Int’l Airport",
                                "seg_departure_city": "Dubai",
                                "seg_departure_country": "United Arab Emirates",
                                "seg_departure_terminal": "2",
                                "seg_arrival_airport_code": "KTM",
                                "seg_arrival_airport": "Tribhuvan Intl Airport",
                                "seg_arrival_city": "Kathmandu City",
                                "seg_arrival_country": "Nepal",
                                "seg_arrival_terminal": "I",
                                "seg_connection_time": false
                            }
                        ]
                    }
                ]
            },
            "fareInformation": {
                "total_adt": 41893,
                "total_chd": 0,
                "total_inf": 0,
                "total_cost": 41893,
                "cashBack": 300
            },
            "baggageDetails": {
                "cabin": "7 Kg",
                "baggage": "20 Kg"
            },
            "passengers": [
                {
                    "passenger_type": "ADT",
                    "passenger_name": "Maharjan Rabi",
                    "eticket_number": "141-6752209685",
                    "PNR": "PQXM2B",
                    "airlines_confirmation": "197IJB"
                }
            ],
            "contactDetails": {
                "email": "maharjanrabi1@gmail.com",
                "phone": "9849932310"
            },
            "eticketLink": "https://sastotickets-flights-private.s3.ap-southeast-1.amazonaws.com/tickets/PQMJ8E-1676354461.pdf?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIA4CEOEY6AUXGMCTXF%2F20230214%2Fap-southeast-1%2Fs3%2Faws4_request&X-Amz-Date=20230214T060104Z&X-Amz-SignedHeaders=host&X-Amz-Expires=900&X-Amz-Signature=a834632054848ad610561f9a7588a1ff789ae2a35c7991f091d97a043ed7d043"
        }
    }
    ```

### Sample Error Response

    Case: Validation Error
    {
        "success": false,
        "data": {
            "error": "Invalid Ticket Parameters."
        }
    }

    {
        "success": false,
        "data": {
            "error": "Ticket already issued."
        }
    }

    {
        "success": false,
        "data": {
            "error": "Invalid PNR record"
        }
    }


    Case: Booking transaction not found
    {
        "success": false,
        "data": {
            "error": "Booking Records Not Found."
        }
    }


    Case: Insufficient Agent Balance
    {
        "success": false,
        "data": {
            "error": "Insufficient balance amount. Please top up and continue."
        }
    }

    Case: Ticketing Failed
    {
        "success": false,
        "data": {
            "error": "Sorry! Flight has been booked or not available. Please try with another flight."
        }
    }