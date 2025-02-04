- **Id:** BR_UI_001
- **Title:** User Can Enter Special Characters in First and Last Name Fields  
- **Severity:** Minor 
- **Preconditions:** User is on the [**Web Tables page**](https://demoqa.com/webtables)
- **Steps to Reproduce:**  
  1. Click **Add** to create a new user.  
  2. Enter `@#$%^&*()` in the **First Name** and **Last Name** fields.  
  3. Fill in other required fields with valid data.  
  4. Click **Submit**.  
- **Expected Result:**  
  - A validation error message should appear, preventing the submission of special characters in name fields.  
- **Actual Result:**  
  - The form accepts special characters, and the user is added to the table.  
- **Environment:**  
  - Browser: [Chrome 120.0]  
  - OS: [Windows 10]  
