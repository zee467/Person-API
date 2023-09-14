### Persons API

This API allows you to perform CRUD (Create, Read, Update, Delete) operations on persons in a database.

#### GET List Persons
> Lists all the persons in the database.

**Request:**
```bash
  curl --location 'https://hngpersonapi-cw36.onrender.com/api/persons'
  Response:
  
  Status: 200 OK
  json
  Copy code
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

####POST New Person
> Add a new person to the database.

**Request:**
```bash
Copy code
curl --location 'https://hngpersonapi-cw36.onrender.com/api/persons' --data-raw '{"name": "Ibukun", "email": "ibk@gmail.com", "age": 28}'
Response:

Status: 201 CREATED
json
Copy code
{
  "person": {
    "age": 28,
    "email": "ibk@gmail.com",
    "id": 7,
    "name": "Ibukun"
  }
}
GET Specific Person
Find a person by ID.

Request:

bash
Copy code
curl --location 'https://hngpersonapi-cw36.onrender.com/api/persons/3'
Response:

Status: 200 OK
json
Copy code
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
PUT Update Person by ID
Update a person by ID.

Request:

bash
Copy code
curl --location --request PUT 'https://hngpersonapi-cw36.onrender.com/api/persons/4' --header 'Content-Type: application/json' --data-raw '{"age": 23, "email": "kseth@yahoo.com", "id": 4, "name": "Kiara Seth"}'
Response:

Status: 200 OK
json
Copy code
{
  "person": {
    "age": 23,
    "email": "kseth@yahoo.com",
    "id": 4,
    "name": "Kiara Seth"
  }
}
DELETE Person by ID
Delete a person by ID.

Request:

bash
Copy code
curl --location --request DELETE 'https://hngpersonapi-cw36.onrender.com/api/persons/4'
Response:

Status: 204 NO CONTENT
