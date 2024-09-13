
# Real-time MongoDB 

A collection of resources for the `Real-time MongoDB CDC with Confluent and Tinybird` workshop.  (Learn about other workshops [HERE](https://www.tinybird.co/docs/live)



## Notes:

### JSON details

#### Flat weather report object:

```json
{
	"timestamp": "2023-05-04 18:07:08",
	"site_name": "New York City",
	"temp_f": 52.12,
	"precip": 0.0,
	"humidity": 79,
	"pressure": 1017,
	"wind_speed": 10.36,
	"wind_dir": 190,
	"clouds": 100,
	"description": "overcast clouds"
}

```

#### Nested weather report object:

```json
{
    "event_type": "report",
    "timestamp": "2024-09-01 00:00:02",
    "site_name": "Louisville",
    "message": {
        "temp_f": 75.47,
        "precip": 0,
        "humidity": 80,
        "pressure": 1014,
        "wind": {
            "speed": 8.05,
            "direction": 20
        },
        "clouds": 100,
        "description": "thunderstorm"
    }
}
```

#### Nested alert report object:

```json
{
    "event_type": "alert",
    "timestamp": "2024-09-13T03:27:42Z",
    "site_name": "Orange",
    "message": {
        "expire_time": "2024-09-14T02:27:42Z",
        "message": "Weather Alert for Orange. High Wind Watch/Warning. Expires at 2024-09-14T02:27:42Z."
    }
}
```




## Learn more: 
https://www.tinybird.co/docs/guides/querying-data/lambda-example-cdc
