# Weather API Reflection

## Part 1: Sending a Request to the Weather API

### Accessing the Weather API

- **API Endpoint:** `https://api.weatherapi.com/v1/current.json`
- **Authentication:** API key (required)

### Query Parameters Used

| Parameter      | Description                        | Example Value |
|----------------|------------------------------------|---------------|
| `key`          | Your API key                      | `YOUR_API_KEY`|
| `q`            | Location query (city or coords)   | `London`      |
| `aqi`          | Air quality information (optional)| `yes`         |

### Example Request URL

```
https://api.weatherapi.com/v1/current.json?key=YOUR_API_KEY&q=London&aqi=yes
```

## Part 2: Analyzing and Documenting the Response

### Example JSON Response:
-see json file

### Observations

- **Location Details:** City name, region, country, coordinates, and local time.
- **Current Weather:** Temperature, weather conditions, wind data, humidity, and cloud coverage.
- **Air Quality:** (if `aqi` is set to `yes`) Additional details on air quality metrics.

### Status Codes

| Status Code | Description                    |
|-------------|--------------------------------|
| `200`       | Success - Request successful   |
| `401`       | Unauthorized - Invalid API key |
| `400`       | Bad Request - Invalid query    |

## Part 3: Documentation and Reflection

### Postman Request Setup

- **Method:** `GET`
- **Headers:** None required.
- **Query Parameters:**
  - `key`: Your API key.
  - `q`: Location (e.g., `London`).
  - `aqi`: Optional (`yes` for air quality data).

### Reflection on Query Parameters

Query parameters are critical in defining the scope and granularity of the data returned by an API.Query parameters help get the right data. Correct usage ensures accurate responses and minimizes API calls.

 For example

- The `q` parameter specifies the location, ensuring the API returns weather details for the intended area.
- The optional `aqi` parameter enriches the response with air quality data, demonstrating the API's flexibility.

Incorrect or missing query parameters can result in incomplete or erroneous data, emphasizing the need for careful parameter configuration
