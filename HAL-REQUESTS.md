# Examples of Hal Requests
## Request 1 - Insert a car
`POST` request body on `http:localhost:8080/cars/`:
```
{
  "modelName": "Opel Astra",
  "serialNumber": 42232,
  "currentPrice": "25000.99"
}
```
Response: `201 - Created`
## Request 2 - Insert a car
`POST` request body on `http:localhost:8080/cars/`:
```
{
  "modelName": "Suzuki Expensive",
  "serialNumber": 844484,
  "currentPrice": "43949.51"
}
```
Response: `201 - Created`
## Request 3 - Get all the cars
`GET` request on `http:localhost:8080/cars/`

Response:
```
{
  "_embedded": {
    "cars": [
      {
        "modelName": "Opel Astra",
        "serialNumber": 42232,
        "currentPrice": 25000.99,
        "_links": {
          "self": {
            "href": "http://localhost:8080/cars/1"
          },
          "car": {
            "href": "http://localhost:8080/cars/1"
          }
        }
      },
      {
        "modelName": "Suzuki Expensive",
        "serialNumber": 844484,
        "currentPrice": 43949.51,
        "_links": {
          "self": {
            "href": "http://localhost:8080/cars/2"
          },
          "car": {
            "href": "http://localhost:8080/cars/2"
          }
        }
      }
    ]
  },
  "_links": {
    "self": {
      "href": "http://localhost:8080/cars/"
    },
    "profile": {
      "href": "http://localhost:8080/profile/cars"
    }
  },
  "page": {
    "size": 20,
    "totalElements": 2,
    "totalPages": 1,
    "number": 0
  }
}
```
