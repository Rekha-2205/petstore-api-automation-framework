# Petstore API Testing – Postman

## Project Overview

This project demonstrates API testing using Postman on the Swagger Petstore APIs. The focus is on building requests, validating responses, handling different status codes, and improving reusability using environment variables.

Base URL:
https://petstore.swagger.io/v2

---

## Tools and Technologies

* Postman (API Testing)
* GitHub (Version Control)

---

## Project Structure

petstore-api-testing/

* postman/

  * petstore_collection.json
  * petstore_environment.json

* screenshots/

* README.md

---

## Assignment Implementation

### Assignment 1: Simple Request Building

**Endpoint:**
GET https://petstore.swagger.io/v2/pet/findByStatus

**Query Parameter:**
status = available

**Objective:**
Retrieve pets based on their availability status

**Validation:**

* Verified that the response returns status code 200

---

### Assignment 2: Working with Request Body

**Endpoint:**
POST https://petstore.swagger.io/v2/pet

**Objective:**
Create a new pet using a JSON request body

**Validation:**

* Verified that the response contains the created pet name

---

### Assignment 3: Understanding Status Codes

Tested multiple scenarios to validate API behavior:

**Valid Request:**
GET https://petstore.swagger.io/v2/pet/findByStatus
Expected: 200 OK

**Not Found:**
GET https://petstore.swagger.io/v2/pet/999999
Expected: 404 Not Found

**Invalid Input:**
POST https://petstore.swagger.io/v2/pet (empty body)
Expected: 400 Bad Request or 405 Method Not Allowed

---

### Assignment 4: Using Environment Variables

**Environment Variable:**
{{url}} = https://petstore.swagger.io/v2

**Usage Example:**
{{url}}/pet/{petId}

**Objective:**
Improve maintainability and avoid hardcoding URLs

---

## Assertions (Test Scripts)

Test scripts are implemented using the Postman **Tests** tab to validate API responses.

* Validates status code 200 for successful requests
* Validates status code 404 for non-existing resources
* Validates error handling for invalid input (400/405)
* Validates response content (e.g., pet name in response)

---

## Execution Steps

1. Import the Postman collection into Postman
2. Import the environment file
3. Select the environment
4. Run the requests individually or using Collection Runner

---

## Key Learnings

* Understanding API request and response lifecycle
* Hands-on experience with HTTP methods (GET, POST)
* Working with different status codes and validations
* Using environment variables for better reusability
* Writing basic test scripts for response validation

---

## Challenges Faced

* Handling invalid input scenarios and error responses
* Understanding API response structures and validations

---

## Conclusion

This project helped build a strong foundation in API testing using Postman. It provided practical experience in request creation, response validation, and writing test scripts for real-time APIs.

---

## Author

Rekha
