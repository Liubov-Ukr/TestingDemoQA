1
### Test Case: Verify GET Request for User List
- **ID:** TC_API_001
- **Title:** Verify GET request returns a list of users
- **Preconditions:** Postman is configured with the correct API endpoint
- **Test Steps:**
  1. Open Postman
  2. Send a GET request to `https://reqres.in/api/users`
- **Expected Result:** Response status is 200 OK, and the response body contains a list of users
- **Actual Result:** Status: 200 OK. The user list returned successfully with 6 users on the first page.
- **Status:** [Pass]

2.
  ### Test Case: Verify POST Request to Create New User
- **ID:** TC_API_002
- **Title:** Verify POST request successfully creates a new user
- **Preconditions:** Postman is configured with the correct API endpoint
- **Test Steps:**
  1. Open Postman
  2. Send a POST request to `https://reqres.in/api/users` with valid data
- **Expected Result:** Status: 201 Created. User data is returned with an ID and timestamp.
- **Actual Result:** A new resource was created successfully. Status: 201 Created. The response contains user data with ID and timestamp:
{
  "name": "Camilla QA",
  "job": "QA Engineer",
  "id": "123",
  "createdAt": "2025-02-01T12:34:56.789Z"
}
- **Status:** [Pass]

3.
### Test Case: Verify Error Handling for Invalid Data (POST Request)
- **ID:** TC_API_003
- **Title:** Verify API returns an error for invalid data
- **Preconditions:** Postman is configured with the correct API endpoint
- **Test Steps:**
  1. Open Postman
  2. Send a POST request with invalid data
- **Expected Result:** Status: 400 Bad Request. The response contains an error message.
- **Actual Result:** The API returned status 201 Created, and created a resource with invalid data:
  ```json
  {
    "name": "",
    "email": "invalidemail",
    "id": "509",
    "createdAt": "2025-02-02T20:54:13.532Z"
  }

4. ### Test Case: Verify Data Consistency After User Creation (GET Request)
- **ID:** TC_API_004
- **Title:** Verify newly created user appears in the user list
- **Preconditions:** A user has been created via a POST request
- **Test Steps:**
  1. Send a GET request to `https://reqres.in/api/users`
  2. Check if the created user is present in the response
- **Expected Result:** The created user's data matches the data from the POST request.
- **Actual Result:** The created user does **NOT** appear in the user list. The API returns predefined demo data.
- **Status:** **Fail** (Expected behavior for demo API without persistent storage)
