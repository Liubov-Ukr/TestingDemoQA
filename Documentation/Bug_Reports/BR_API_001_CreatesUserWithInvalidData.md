## 🐞 **Bug Report: API Creates User with Invalid Data**

### 📄 **Bug Information:**
- **Bug ID:** BR_001
- **Related Test Case:** TC_API_003
- **Title:** API creates a user with an empty name and an invalid email format
- **Reported By:** Liubov
- **Date Reported:** 02.02.2025
- **Environment:** Postman, Windows 10

### 🔍 **Description:**
When sending a POST request with an empty name field and an invalid email format, the API successfully creates a new user instead of returning an error.

---
### 📋 **Steps to Reproduce:**
- Open Postman.
- [Create a new POST request:]
(https://reqres.in/api/users)
- In the request body (Body), select raw → JSON and insert the following:
```json
{
  "name": "",
  "email": "invalidemail"
}
```
- Click Send.
---
### ✅ **Expected Result:**
The API should return a 400 Bad Request error with a validation error message.

### ❌ **Actual Result:**
The API returns a 201 Created status and creates a user with invalid data.

### 📷 **Attachments:**
[**Postman screenshot showing the response**](https://github.com/Liubov-Ukr/TestingDemoQA/blob/main/Screenshots/Test-Case-Verify-Error-Handling-for-Invalid-Data-POST-Request.png)
⚙️ Severity: Medium (The API does not validate data, which could lead to inconsistent information in the system)
🔗 Status: Open
