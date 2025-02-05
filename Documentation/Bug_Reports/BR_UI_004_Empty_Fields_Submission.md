### 🐞 **Bug Report: Form Submission with All Fields Left Empty

- **ID:** BR_UI_004
- **Related Test Case:** TC_UI_008 
- **Title:** User Can Submit Form with All Fields Left Empty
- **Severity:** Medium

---

### 📋 **Preconditions:**
- User is on the [**Text Box page**](https://demoqa.com/text-box)
  
---

### 🚶‍♂️ **Test Steps:**  
1. Navigate to the **Text Box** page.  
2. Leave all fields empty.  
3. Click the **Submit** button.  
4. Repeat the test, entering data only in the **Current Address** field, leaving others empty.  
5. Click the **Submit** button again.

---

### ✅ **Expected Result:**
  - The system should prevent the submission of the form.
  - Required fields should be highlighted in red to indicate missing data.
  - A validation message should be displayed (e.g., "This field is required").
  - The Submit button should not trigger data submission if the required fields are empty.

    ---
    
### **❌ Actual Result:**
  - The form was successfully submitted even when all fields were left empty, and the entered data appeared below the form as if the submission was valid.
  - No validation error messages or highlighting appeared to indicate missing required fields.

---

### 🌍 **Environment:**  
- **Browser:** Chrome 120.0  
- **OS:** Windows 10

  ---
  
### 📷 **Attachments:**
1. **Form Submission with All Fields Left Empty:**  
   ![Form Submission with All Fields Left Empty](https://github.com/Liubov-Ukr/TestingDemoQA/blob/main/Screenshots/BR_UI_004_%20Form_Submission_with_All_Fields_Left_Empty.png)  
   _The form was submitted without validation errors or highlighting, despite empty required fields._

---

2. **Form Submission with Only Current Address Filled:**  
   ![Form Submission with Only Current Address Filled](https://github.com/Liubov-Ukr/TestingDemoQA/blob/main/Screenshots/BR_UI_004_Form_Submission_with_Only_Current_Address_Filled.png)  
   _The form was submitted successfully, although Full Name, Email, and Permanent Address fields were left empty._

---

### ⚙️ **Status:** Open

