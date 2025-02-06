
### 🐞 **Bug Report: Input Fields Do Not Have Character Limit Validation**  
- **ID:** BR_UI_005  
- **Related Test Case:** TC_UI_009  
- **Title:** Input Fields Do Not Have Character Limit Validation  
- **Severity:** Medium  

---

### 📋 **Preconditions:**  
- The user is on the [**Text Box** page](https://demoqa.com/text-box)  

---

### 🚶‍♂️ **Steps to Reproduce:**  
1. Enter **1 character** in **Full Name, Email, Current Address, and Permanent Address**.  
2. Click **Submit**.  
3. Verify whether the system accepts minimal values.  
4. Enter **255+ characters** in each field.  
5. Click **Submit**.  
6. Check if validation errors appear.  

---

### ✅ **Expected Result:**  
- **Character input limits should be enforced** for all fields.  
- **Email** should validate incorrect inputs and reject them.  
- If the maximum limit is exceeded, a validation error should be displayed.  

---

### ❌ **Actual Result:**  
- **Email** correctly rejects invalid input.  
- **Full Name, Current Address, and Permanent Address** **accept unlimited characters**, and the form is submitted without validation errors.  

📷 **Attachments:**  
1. ![Min Character Input](https://github.com/Liubov-Ukr/TestingDemoQA/blob/main/Screenshots/BR_UI_005_Min_Character_Input.png)  
2. ![Max Character Input](https://github.com/Liubov-Ukr/TestingDemoQA/blob/main/Screenshots/BR_UI_005_Max_Character_Input.png)  

---

### 🌍 **Environment:**  
- **Browser:** Chrome 120.0  
- **OS:** Windows 10  

---

### ⚙️ **Status:** Open
