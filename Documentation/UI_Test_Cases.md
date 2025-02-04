## 📝 **Functional Testing**

### ✅ **Test Case 1: Verify Text Box Functionality**
- **ID:** TC_UI_001  
- **Title:** Verify Text Box Accepts Valid Input  
- **Preconditions:** User is on the **Text Box** page (`https://demoqa.com/text-box`)  
- **Test Steps:**  
  1. Navigate to the **Text Box** section.  
  2. Enter valid data in all fields:  
     - Full Name: "Liubov Opryshchenko"  
     - Email: "liubov@gmail.com"  
     - Current Address: "Shelley Street, 2897"  
     - Permanent Address: "First Street, 98"  
  3. Click the **Submit** button.  
- **Expected Result:**  
  - Entered data is displayed correctly below the form without any errors.  
- **Actual Result:** [Entered data is displayed correctly below the form without any errors.]  
- **Status:** [Pass]  
---
### ✔️ **Test Case 2: Verify Check Box Selection and Deselection**
- **ID:** TC_UI_002  
- **Title:** Ensure User Can Select and Deselect Checkboxes  
- **Preconditions:** User is on the **Check Box** page (`https://demoqa.com/checkbox`)  
- **Test Steps:**  
  1. Expand the checkbox tree.  
  2. Select multiple checkboxes (e.g., "Home," "Documents," "Downloads").  
  3. Deselect some checkboxes (e.g., "Documents").  
- **Expected Result:**  
  - Selected checkboxes are marked with a check icon.  
  - Deselected boxes are unmarked.  
  - The result section updates correctly.  
- **Actual Result:**
  - Selected checkboxes are marked with a check icon.  
  - Deselected boxes are unmarked.  
  - The result section updates correctly.  
- **Status:** [Pass]  
---
### 🗑️ **Test Case 3: Verify Data Reset After Page Refresh**
- **ID:** TC_UI_003  
- **Title:** Ensure Entered Data Clears After Refresh  
- **Preconditions:** User is on the **Text Box** page  
- **Test Steps:**  
  1. Enter valid data into all fields.  
  2. Refresh the page.  
- **Expected Result:**  
  - All previously entered data is cleared.  
- **Actual Result:** [All previously entered data is cleared]  
- **Status:** [Pass]  
---
### 📋 **Test Case 4: Verify Edit and Delete Functionality in the Table**  
- **ID:** TC_UI_004  
- **Title:** Verify User Can Edit and Delete Data in the Table  
- **Preconditions:** User is on the **Web Tables** page on DemoQA  
- **Test Steps:**  
  1. Click on the **Edit (✏️)** icon in any row of the table.  
  2. Modify the data in one or more fields (e.g., First Name, Age, Email).  
  3. Click the **Submit** button to save changes.  
  4. Verify if the updated data is displayed correctly in the table.  
  5. Click on the **Delete (🗑️)** icon for any record.  
  6. Confirm the deletion (if applicable) and verify the record is removed from the table.  
- **Expected Result:**  
  - The user can successfully modify the content of the table’s fields, and the updated data is saved correctly.  
  - The user can delete records, which are no longer visible in the table after deletion.  
- **Actual Result:**  
  - The user can successfully modify the content of the table’s fields, and the updated data is saved correctly.  
  - The user can delete records, which are no longer visible in the table after deletion.  
- **Status:** [Pass]  

## 📝 **Boundary Value Testing**

### 📋 **Test Case 5: Verify Age Field with Minimum and Maximum Values**  
- **ID:** TC_UI_005  
- **Title:** Verify that the Age field accepts values between 18 and 99  
- **Preconditions:** User is on ([**Web Tables page**](https://demoqa.com/webtables))
 
- **Test Steps:**  
  1. Enter **18** in the Age field and submit.  
  2. Enter **99** in the Age field and submit.  
  3. Enter **17** and submit to check for validation errors.  
  4. Attempt to enter **100** to verify if validation restricts three-digit numbers.  
  5. Enter **1** to check for validation behavior with extremely low values.  
  6. Enter **-1** to check for validation behavior with negative values.  
- **Expected Result:**  
  - The system should accept ages **18–99**.  
  - Validation errors should be displayed for values outside this range (**less than 18** or **greater than 99**).  
  - The system should allow entering three-digit numbers but display an error if the value exceeds 99.  
  - **Negative values** should not be accepted, and an appropriate validation error should be displayed.  
- **Actual Result:**  
  - ✅ The system accepted ages **18** and **99** without errors.  
  - ⚠️ The system **accepted** age **17** **without any validation error**, which **does not meet the expected behavior**.  
  - 🚫 It was **impossible to enter** a three-digit number like **100** — the system **restricts input to two digits** without displaying an error message.  
  - ✅ The system **accepted** age **1** **without any validation error**, which also **does not meet the expected behavior**.  
  - ❌ The system **did not allow entering** the value **-1**, which is correct, but **no validation message** was displayed.
  - - [View detailed bug report with screenshot ➜ BR_UI_002](https://github.com/Liubov-Ukr/TestingDemoQA/blob/main/Documentation/Bug_Reports/BR_UI_002_Age_Field_Validation_Issue)
- **Status:** ❌ **Fail**  

## 📝 **Negative Testing**

### 🔤 **Test Case 6: Verify Form Submission with Special Characters in Name Field**  
- **ID:** TC_UI_006  
- **Title:** Verify Error When Special Characters Are Entered in the Full Name Field  
- **Preconditions:**  
  - User is on the **Text Box** page ([https://demoqa.com/webtables](https://demoqa.com/webtables))  
  - The form is loaded correctly without any issues  
- **Test Steps:**  
  1. Navigate to the **webtables** page.  
  2. Enter `@#$%^&*()` in the **First Name** and **Second Name** fields.  
  3. Fill in other required fields with valid data (e.g., valid email and addresses).  
  4. Click the **Submit** button.  
- **Expected Result:**  
  - The system should **prevent submission** and display a **validation error message** indicating that special characters are not allowed in the fields.  
  - Alternatively, the system should **sanitize the input** automatically, removing special characters.  
- **Actual Result:**  
  - The form was submitted successfully without any validation error.
  - [View detailed bug report with screenshot ➜ BR_UI_001](https://github.com/Liubov-Ukr/TestingDemoQA/blob/main/Documentation/Bug_Reports/BR_UI_001_User_Can_Enter_Special_Characters.md)
- **Status:** ❌ **Fail**  

## 📝 **Cross-Browser Testing**

### 🖥️ **Test Case 7: Verify UI Consistency Across Browsers**  
- **ID:** TC_UI_007  
- **Title:** Verify the Form Layout is Consistent in Chrome, Firefox, and Edge  
- **Preconditions:** The form is accessible in different browsers  
- **Test Steps:**  
  1. Open the form in Google Chrome.  
  2. Repeat in Firefox and Microsoft Edge.  
- **Expected Result:**  
  - The form layout, fonts, buttons, and fields look consistent across all browsers.  
- **Actual Result:** [The form layout, fonts, buttons, and fields look consistent across all browsers.]  
- **Status:** [Pass]  

