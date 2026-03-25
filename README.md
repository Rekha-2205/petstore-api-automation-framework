# 🐾 Petstore API Testing – Postman

## 📌 Project Overview

This project demonstrates API testing using Postman on the Swagger Petstore APIs.
The focus is on building API requests, validating responses using assertions, handling different status codes, and improving reusability with environment variables.

**Base URL:**
https://petstore.swagger.io/v2

---

## 🛠 Tools and Technologies

* Postman (API Testing)
* GitHub (Version Control)

---

## 📁 Project Structure

```
petstore-api-testing/
│
├── postman/
│   ├── petstore_collection.json
│   └── petstore_environment.json
│
├── screenshots/
│
└── README.md
```

---

## 📚 Assignment Implementation

### ✅ Assignment 1: Simple Request Building

**Endpoint:**
https://petstore.swagger.io/v2/pet/findByStatus

**Query Parameter:**
status = available

**Objective:**
Retrieve pets based on availability status

**Assertions:**

* Verified response status code is **200**

---

### ✅ Assignment 2: Working with Request Body

**Endpoint:**
https://petstore.swagger.io/v2/pet

**Objective:**
Create a new pet using JSON request body

**Sample Request Body:**

```json
{
  "id": 101,
  "name": "ruby",
  "status": "available"
}
```

**Assertions:**

* Verified response status code is **200**
* Validated that response contains correct **pet name ("ruby")**

---

### ✅ Assignment 3: Understanding Status Codes

Tested multiple scenarios to validate API behavior:

* **Valid Request**
  https://petstore.swagger.io/v2/pet/findByStatus
  ✔ Expected: 200 OK

* **Not Found**
  https://petstore.swagger.io/v2/pet/889900
  ✔ Expected: 404 Not Found

* **Invalid Input**
  https://petstore.swagger.io/v2/pet (POST with empty body)
  ✔ Expected: 400 Bad Request / 405 Method Not Allowed

---

### ✅ Assignment 4: Using Environment Variables

**Environment Variable:**

```
{{url}} = https://petstore.swagger.io/v2
```

**Usage Example:**

```
{{url}}/pet/{petId}
```

**Objective:**

* Avoid hardcoding URLs
* Improve maintainability and reusability

---

## Assertions (Test Scripts)

Assertions are implemented in the **Tests tab** in Postman to validate API responses.

* Status code validation (200, 404, 400/405)
* Response body validation (e.g., pet name)
* Ensures API behaves as expected

---

## Execution Steps

1. Import the Postman collection into Postman
2. Import the environment file
3. Select the environment
4. Run requests individually or using **Collection Runner**

---

## Key Learnings

* Understanding API request and response lifecycle
* Hands-on experience with HTTP methods (GET, POST)
* Validating responses using assertions
* Handling different status codes
* Using environment variables for reusability

---

## Challenges Faced

* Handling invalid input scenarios
* Understanding response structure for validations

---

## Conclusion

This project helped build a strong foundation in API testing using Postman.
It provided practical experience in request creation, response validation, and writing test scripts for real-world APIs.

---

##  Author

**Rekha**
