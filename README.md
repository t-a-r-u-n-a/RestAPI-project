# RESTful API Automation with ReadyAPI

This project contains automated tests for RESTful API endpoints using ReadyAPI. The test suite is named **RESTful API Automation** and automates the following endpoints from https://restful-api.dev/.

---------

## Prerequisites

- ReadyAPI installed
- Microsoft Excel for storing test data

---------

## Endpoints Overview

| Method | Endpoint                                      | Description                                    |
|--------|----------------------------------------------|------------------------------------------------|
| GET    | https://api.restful-api.dev/objects          | Retrieve all existing objects                 |
| GET    | https://api.restful-api.dev/objects?id={ID}  | Retrieve multiple objects by multiple IDs     |
| GET    | https://api.restful-api.dev/objects/{ID}     | Retrieve a single object by ID                |
| POST   | https://api.restful-api.dev/objects          | Add a new object                              |
| PUT    | https://api.restful-api.dev/objects/{ID}     | Update or partially update an object by ID    |
| DELETE | https://api.restful-api.dev/objects/{ID}     | Remove an existing object by ID               |

---------

## Test Suite Overview

### **Test Case 1: Add a New Object**

**Endpoint:** `POST /objects`

**Steps:**
1. Use the POST endpoint to add a new object with the sample payload schema.
2. Assert the following response data:
   - Response code
   - Value of `id` field (not empty)
   - Value of `name`, `year`, `price`, `CPU model`, and `Hard disk size` fields

---------

### **Test Case 2: Retrieve the Newly Added Object**

**Endpoint:** `GET /objects/{ID}`

**Steps:**
1. Use the GET endpoint to retrieve the newly added object by its ID.
2. Assert the following response data:
   - Response code
   - Values of `id`, `name`, `year`, `price`, `CPU model`, and `Hard disk size` fields

---------

### **Test Case 3: Update the Object**

**Endpoint:** `PUT /objects/{ID}`

**Steps:**
1. Use the PUT endpoint to update all fields of the newly added object with the updated payload schema.
2. Assert the following response data:
   - Response code
   - Updated values of `name`, `year`, `price`, `CPU model`, `Hard disk size`, and `color` fields
   - Value of `updatedAt` field (not empty)

---------

### **Test Case 4: Retrieve the Updated Object**

**Endpoint:** `GET /objects/{ID}`

**Steps:**
1. Use the GET endpoint to retrieve the updated object by its ID.
2. Assert the following response data:
   - Response code
   - Values of `id`, `name`, `year`, `price`, `CPU model`, `Hard disk size`, and `color` fields

---------

### **Test Case 5: Remove the Updated Object**

**Endpoint:** `DELETE /objects/{ID}`

**Steps:**
1. Use the DELETE endpoint to remove the updated object by its ID.
2. Assert the following response data:
   - Response code
   - Value of the message stating the object is deleted

---------

## Data Source

- TestData.xlsx

---------

## Screen recording of test run

- Recording.mp4
  
---------

## Setup

1. Import the ReadyAPI project file 'Rest-API-readyapi-project.xml' into ReadyAPI.
2. Ensure the Excel data source 'TestData.xlsx' is configured and mapped correctly to the test cases.
3. Run the test suite:
   - Open ReadyAPI.
   - Navigate to the "RESTful API Automation" test suite.
   - Execute the tests.

---------
