### Persons API

This API allows you to perform CRUD (Create, Read, Update, Delete) operations on persons in a database.

* GET List Persons
> Lists all the persons in the database.

**Example Request:**
```curl
  curl --location 'https://hngpersonapi-cw36.onrender.com/api/persons'
```

**Example Response:**
```
  Status: [200](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/200) OK
  json
  {
    "people": [
      {
        "age": 21,
        "email": "verak@yahoo.com",
        "id": 1,
        "name": "Vera Kalu"
      }
    ]
  }
```

* POST New Person
> Add a new person to the database.

**Example Request:**
```bash
  curl --location 'https://hngpersonapi-cw36.onrender.com/api/persons'
  --data-raw '{
              "name": "Ibukun",
              "email": "ibk@gmail.com",
              "age": 28
              }'
```

**Example Response:**
```bash
  Status: 201 CREATED
  json
  {
    "person": {
      "age": 28,
      "email": "ibk@gmail.com",
      "id": 7,
      "name": "Ibukun"
    }
  }
```

* GET Specific Person
> Find a person by ID.

**Example Request:**
```bash
  curl --location 'https://hngpersonapi-cw36.onrender.com/api/persons/3'
```

**Example Response:**
```bash
  Status: 200 OK
  json
  {
    "result": [
      {
        "age": 22,
        "email": "ola@gmail.com",
        "id": 3,
        "name": "Stephen Ola"
      }
    ]
  }
```

* PUT Update Person by ID
> Update a person by ID.

**Example Request:**
```bash
  curl --location --request PUT 'https://hngpersonapi-cw36.onrender.com/api/persons/4'
  --header 'Content-Type: application/json'
  --data-raw '{
            "age": 23,
            "email": "kseth@yahoo.com",
            "id": 4,
            "name": "Kiara Seth"
            }'
```

**Example Response:**
```bash
  Status: 200 OK
  json
  {
    "person": {
      "age": 23,
      "email": "kseth@yahoo.com",
      "id": 4,
      "name": "Kiara Seth"
    }
  }
```

* DELETE Person by ID
> Delete a person by ID.

**Example Request:**
```bash
  curl --location --request DELETE 'https://hngpersonapi-cw36.onrender.com/api/persons/4'
```

Response:
**Example Response:**
```bash
``Status: 204 NO CONTENT
```
