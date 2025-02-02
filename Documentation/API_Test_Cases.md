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

2. Test Case: Verify POST Request to Create New User
  -ID: TC_API_002
  -Title: Verify POST request successfully creates a new user
  -Preconditions: Postman is configured with the correct API endpoint

Test Steps:
  1)Open Postman
  2)Send a POST request to https://demoqa.com/api/users with the following JSON body:

    {
      "name": "Camilla QA",
      "email": "camilla@example.com"
    }

  -Expected Result: Response status is 201 Created, and the response body contains the new user's details
  -Actual Result: [To be filled after execution]
  -Status: [Pass/Fail]

3. Test Case: Verify Error Handling for Invalid Data (POST Request)
  -ID: TC_API_003
  -Title: Verify API returns an error for invalid data
  -Preconditions: Postman is configured with the correct API endpoint

Test Steps:
  1)Open Postman
  2)Send a POST request to https://demoqa.com/api/users with invalid JSON:
    
    {
      "name": "",
      "email": "invalidemail"
    }

  -Expected Result: Response status is 400 Bad Request, and the response body contains an error message
  -Actual Result: [To be filled after execution]
  -Status: [Pass/Fail]

4. Test Case: Verify Data Consistency After User Creation (GET Request)
  -ID: TC_API_004
  -Title: Verify newly created user appears in the user list
  -Preconditions: A user has been created via POST request

Test Steps:
  1)Send a GET request to https://demoqa.com/api/users
  2)Verify the new user exists in the response data
  
  -Expected Result: The created user's data matches the data sent in the POST request
  -Actual Result: [To be filled after execution]
  -Status: [Pass/Fail]

