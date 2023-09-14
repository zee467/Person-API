###Persons api
This API allows you perform CRUD(create, read, update, delete) operations on persons in a database.

##GET
List Persons
https://hngpersonapi-cw36.onrender.com/api/persons
Lists all the persons in the database.

Example Request
List Persons
curl
curl --location 'https://hngpersonapi-cw36.onrender.com/api/persons'
200 OK
Example Response
Body
Headers (11)
View More
json
{
  "people": [
    {
      "age": 21,
      "email": "verak@yahoo.com",
      "id": 1,
      "name": "Vera Kalu"
    },
}

##POST
New Request
http://127.0.0.1:5000/api/personhttps://hngpersonapi-cw36.onrender.com/api/persons
Add a new person to the database.

Body
raw (json)
json
{"name": "Ibukun", "email": "ibk@gmail.com", "age": 28}
Example Request
Add a new person
curl
curl --location 'https://hngpersonapi-cw36.onrender.com/api/persons' \
--data-raw '{"name": "Ibukun", "email": "ibk@gmail.com", "age": 28}'
201 CREATED
Example Response
Body
Headers (5)
json
{
  "person": {
    "age": 28,
    "email": "ibk@gmail.com",
    "id": 7,
    "name": "Ibukun"
  }
}

##GET
Specific person
https://hngpersonapi-cw36.onrender.com/api/persons/<id>
Find a person by id.

Example Request
Specific person
curl
curl --location 'https://hngpersonapi-cw36.onrender.com/api/persons/3'
200 OK
Example Response
Body
Headers (5)
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

##PUT
Update person by id
https://hngpersonapi-cw36.onrender.com/api/persons/<id>
Update a person by id.

Body
raw (json)
json
{"name": "Kiara Seth", "email": "kseth@yahoo.com", "age": 23}
Example Request
Update person by id
View More
curl
curl --location --request PUT 'https://hngpersonapi-cw36.onrender.com/api/persons/4' \
--header 'Content-Type: application/json' \
--data-raw '  {
            "age": 23,
            "email": "kseth@yahoo.com",
            "id": 4,
            "name": "Kiara Seth"
        }'
200 OK
Example Response
Body
Headers (5)
json
{
  "person": {
    "age": 23,
    "email": "kseth@yahoo.com",
    "id": 4,
    "name": "Kiara Seth"
  }
}

##DELETE
Delete person by id
http://hngpersonapi-cw36.onrender.com/api/persons/<id>
Delete a person by id.

Example Request
Delete person by id
View More
curl
curl --location --request DELETE 'https://hngpersonapi-cw36.onrender.com/api/persons/4'
204 NO CONTENT
Example Response
Body
Headers (4)
No response body
This request doesn't return any response body
