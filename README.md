# Security Tests for API Authentication and Authorization

## Overview

This repository contains tests for API security focusing on authentication and authorization. The API under test requires authentication using JWT tokens, and specific authorization checks based on user roles.

## Prerequisites

- [Postman](https://www.postman.com/) - The tests are written in Postman, a popular API testing tool.

## Authentication Tests

### Test 1: Authentication Check without Token

- **Description:** Ensures that the API returns a 401 status code when no JWT token is provided.
  ![image](https://github.com/LocNgoVnK2/JWT-Authentication-Authorization-In-NET6-API/assets/77975567/5f192dbd-bd91-4cf9-8293-459c518d8b03)

- **Steps:**
  1. Make a request to the API without providing a JWT token.
  2. Verify that the response status code is 401.

### Test 2: Authentication Check with Invalid Token

- **Description:** Verifies that the API returns a 401 status code when an invalid JWT token is provided.
  ![image](https://github.com/LocNgoVnK2/JWT-Authentication-Authorization-In-NET6-API/assets/77975567/7f31cf94-de4b-44d9-8bfe-58db56428de3)

- **Steps:**
  1. Make a request to the API with an invalid JWT token.
  2. Verify that the response status code is 401.

### Test 3: Authentication Check with Valid Token

- **Description:** Tests successful access to the API after a successful login.
  ![image](https://github.com/LocNgoVnK2/JWT-Authentication-Authorization-In-NET6-API/assets/77975567/141fd436-67b3-4525-88e8-121281dd2cad)
  ![image](https://github.com/LocNgoVnK2/JWT-Authentication-Authorization-In-NET6-API/assets/77975567/1350e58b-5cf5-4219-add4-9c2b947d16fd)

- **Steps:**
  1. Login to the API to obtain a valid JWT token.
  2. Make a request to the API with the obtained JWT token.
  3. Verify that the response status code is 200.

## Authorization Tests

### Test 4: Authorization Check without Token

- **Description:** Ensures that the API returns a 401 status code when no JWT token is provided.
 ![image](https://github.com/LocNgoVnK2/JWT-Authentication-Authorization-In-NET6-API/assets/77975567/8c07f0da-7895-4d20-8179-e45c586b23bd)

- **Steps:**
  1. Make a request to the API without providing a JWT token.
  2. Verify that the response status code is 401.

### Test 5: Authorization Check with User Token (Non-Admin)

- **Description:** Verifies that a user without admin role receives a 403 status code.
  ![image](https://github.com/LocNgoVnK2/JWT-Authentication-Authorization-In-NET6-API/assets/77975567/f464b104-2deb-4d93-97c6-9f10de2dce1d)
  ![image](https://github.com/LocNgoVnK2/JWT-Authentication-Authorization-In-NET6-API/assets/77975567/402bceea-b43d-4a45-8e01-1748a433db95)

- **Steps:**
  1. Obtain a JWT token for a user without admin role.
  2. Make a request to the API with the obtained JWT token.
  3. Verify that the response status code is 403.

### Test 6: Authorization Check with Admin Token

- **Description:** Tests successful access to the API with an admin role.
  ![image](https://github.com/LocNgoVnK2/JWT-Authentication-Authorization-In-NET6-API/assets/77975567/f679110d-9509-410e-be17-36b44d7034e2)
  ![image](https://github.com/LocNgoVnK2/JWT-Authentication-Authorization-In-NET6-API/assets/77975567/79910a51-aba3-45e4-a00f-732c7645cb9b)

- **Steps:**
  1. Obtain a JWT token for a user with admin role.
  2. Make a request to the API with the obtained JWT token.
  3. Verify that the response status code is 200.

## How to Run Tests

1. Clone this repository to your local machine.
2. Import the Postman collection (`security-tests.postman_collection.json`) into Postman.
3. Update the collection variables with your API credentials and endpoints.
4. Run the collection in Postman.


