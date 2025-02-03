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
- **Status:** Passed

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
```json
{
  "name": "Camilla QA",
  "job": "QA Engineer",
  "id": "123",
  "createdAt": "2025-02-01T12:34:56.789Z"
}
- **Status:** Passed

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

  ### 5. **Test Case: Verify Status Code for GET Request**
- **ID:** TC_API_005
- **Title:** Verify status code for successful GET request
- **Preconditions:** The API endpoint is available and functional
- **Test Steps:**
  1. Open Postman
  2. Send a GET request to `https://reqres.in/api/users`
  3. Add the following test script in the **Post-response** 
```json
  pm.test("Status code is 200", function ()
    {
         pm.response.to.have.status(200);
     });
     ```
- **Expected Result:** The response status code should be **200 OK**
- **Actual Result:** Status code is 200
- **Status:** Passed

### 6. **Test Case: Verify Response Structure for User Data**
- **ID:** TC_API_006
- **Title:** Verify that the response contains user data in the correct structure
- **Preconditions:** The API returns data for the GET request
- **Test Steps:**
  1. Open Postman
  2. Send a GET request to `https://reqres.in/api/users`
  3. Add the following test script in the **Post-response**
     ```json
     pm.test("Response contains user data", function () {
         var jsonData = pm.response.json();
         pm.expect(jsonData.data).to.be.an("array");
         pm.expect(jsonData.data.length).to.be.above(0);
     });
     ```
- **Expected Result:** 
  - The response should contain a `data` field.
  - The `data` field should be an **array** with at least one user object.
- **Actual Result:** Response contains user data
- **Status:** Passed

  ### 7. Test Case: Verify User Creation (POST Request)
- **ID:** TC_API_003
- **Title:** Verify User Creation via POST Request
- **Preconditions:** Postman is configured with the correct API endpoint (`https://reqres.in/api/users`)
  
**Test Steps:**
1. Open Postman.
2. Set the request method to **POST**.
3. Enter the URL: `https://reqres.in/api/users`.
4. Go to the **Body** tab → Select **raw** → Choose **JSON**.
5. Add the following JSON:
```json
  {
     "name": "Camilla QA",
     "job": "QA Engineer"
   }
 6. Go to the Tests tab and add this script:
    ```json
    pm.test("Status code is 201 (User Created)", function () {
        pm.response.to.have.status(201);
    });
    
    pm.test("Response contains user details", function () {
        var jsonData = pm.response.json();
        pm.expect(jsonData).to.have.property("name", "Camilla QA");
        pm.expect(jsonData).to.have.property("job", "QA Engineer");
        pm.expect(jsonData).to.have.property("id");
        pm.expect(jsonData).to.have.property("createdAt");
    });

  7. Click Send.
 **Expected Result:** 
  - Status code: 201 Created
  - The response body contains:
  - "name": "Camilla QA"
  - "job": "QA Engineer"
  - An auto-generated "id"
  - A timestamp "createdAt"
 
 **Actual Result:** Status code is 201 (User Created)
                    The response contains user details
- **Status:** Passed
