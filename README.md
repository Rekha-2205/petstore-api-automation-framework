# Petstore API Testing using Postman

## Overview

This project contains basic API testing done on the Swagger Petstore APIs using Postman.
The purpose of this work is to understand how APIs work and how to test them manually before moving to automation.

I have covered different scenarios like sending requests, validating responses, checking status codes, and using environment variables.

Base URL used:
https://petstore.swagger.io/v2

---

## Tools Used

* Postman (for API testing)
* GitHub (for storing and sharing the project)

---

## Project Structure

petstore-api-testing/

* postman/

  * petstore_collection.json
  * petstore_environment.json

* screenshots/
  (contains screenshots of all assignments)

* README.md

---

## Assignments Covered

### 1. GET Request with Query Parameters

* Endpoint: /pet/findByStatus
* Added query parameter: status = available
* Verified that the response returns status code 200

This helped me understand how query parameters work in APIs.

---

### 2. POST Request with Request Body

* Endpoint: /pet
* Method: POST
* Sent JSON data with id, name, and status

Example:
{
"id": 12345,
"name": "Doggy",
"status": "available"
}

* Verified that the response contains the same pet name

This helped me understand how to send data in request body.

---

### 3. Understanding Status Codes

Tested different scenarios:

* Valid request → 200 OK
* Invalid pet ID → 404 Not Found
* Empty body request → 400 / 405 error

This helped me understand how APIs respond in different situations.

---

### 4. Environment Variables

* Created a variable called {{url}}
* Stored base URL in it
* Used it in requests like:
  {{url}}/pet/123

This makes the requests reusable and easy to manage.

---

## Assertions Used

In Postman, I added basic test scripts like:

* Checking status code is 200
* Verifying response contains expected data

These validations ensure that API is working as expected.

---

## Screenshots

Screenshots are added in the screenshots folder for:

* Request setup
* Response output
* Test scripts
* Status code validation
* Environment variables

These are included to make it easier to understand the work.

---

## How to Run

1. Open Postman
2. Import the collection file
3. Import the environment file
4. Select the environment
5. Run the requests

---

## What I Learned

* Basics of API testing
* How to send GET and POST requests
* How to validate responses
* Understanding status codes
* Using environment variables in Postman

---

## Author

Rekha
