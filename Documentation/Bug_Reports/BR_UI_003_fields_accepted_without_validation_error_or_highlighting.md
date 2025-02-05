### 🐞 **Bug Report: Incorrect Input Handling in Full Name, Current Address, and Permanent Address Fields**

- **ID:** BR_UI_003
- **Related Test Case:** TC_UI_007  
- **Title:** User Can Enter Special Characters in Full Name, Current Address, and Permanent Address fields.
- **Severity:** Minor

---

### 📋 **Preconditions:**
- User is on the [**Text Box page**](https://demoqa.com/text-box)
  
---

### 🚶‍♂️ **Steps to Reproduce:**  
1. Enter `@#$%^&*()` in the **Full Name**, **Current Address** and **Permanent Address** fields.  
2. Click **Submit**.  

---

### ✅ **Expected Result:**  
   - The system should **prevent submission** and display a **validation error message** or **highlight the invalid field** in red to indicate incorrect input.   
   - Alternatively, the system should automatically **process the input** by removing special characters.

---

### ❌ **Actual Result:**  
  - The fields **Full Name, Current Address, and Permanent Address** were **accepted without any validation error or highlighting**.   
  - The system did not restrict the use of special characters in these fields.

### 🌍 **Environment:**  
- **Browser:** Chrome 120.0  
- **OS:** Windows 10  

### 📷 **Attachments:**
![Screenshot fields **accepted without any validation error or highlighting**](https://github.com/Liubov-Ukr/TestingDemoQA/blob/main/Screenshots/BR_UI_003_the_fields_accepted_without_validation_error_or_highlighting.png).

### ⚙️ **Status:** Open

