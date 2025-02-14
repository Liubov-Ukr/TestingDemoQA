## 📝 **Functional Testing**
---
### **Test Case 1: Verify Text Box Functionality**
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
- **Actual Result:** Entered data is displayed correctly below the form without any errors. 
- ✅ **Status:** Pass 
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
-✅ **Status:** Pass
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
-✅ **Status:** [Pass]  
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
-✅ **Status:** [Pass]  
--- 
### ✔️ **Test Case 10: Ensure Only One Radio Button Can Be Selected**
- **ID:** TC_UI_010  
- **Title:** Ensure Only One Radio Button Can Be Selected  
- **Preconditions:**  
  - User is on the [**Radio Button** page](https://demoqa.com/radio-button)  
### 🚶‍♂️ **Test Steps:**  
1. Click the **"Yes"** radio button.  
2. Observe the behavior of the radio button selection.  
3. Click the **"Impressive"** radio button.  
4. Observe the behavior of the radio button selection.  
5. Click the **"No"** radio button.  
6. Observe whether the selection changes.  
### ✅ **Expected Result:**  
- Users should be able to switch easily between radio button options.  
- When clicking a selected radio button again, the selection should remain (radio buttons cannot be deselected manually).  
- The user should be able to select any of the three options: **"Yes," "Impressive," and "No."**  
- Only **one** radio button should be selected at a time.  
### ❌ **Actual Result:**  
- ✅ The user **can** switch between "Yes" and "Impressive" radio buttons correctly.  
- ❌ The user **cannot select "No"**—clicking it does nothing.  
- ✅ The user **cannot select multiple options at once**, which is expected behavior.  
- ❌ Clicking a selected radio button **does not remove the selection**, which may not be intuitive.  
### 🌍 **Environment:**  
- **Browser:** Chrome 120.0  
- **OS:** Windows 10  
  [View detailed bug report with screenshot ➜ BR_UI_006](https://github.com/Liubov-Ukr/TestingDemoQA/blob/main/Documentation/Bug_Reports/BR_UI_006_Ensure_Only_One_Radio_Button_Can_Be_Selected.md)
### ⚙️ **Status:** ❌ **Fail**  
---
  ### 📋 **Test Case 12: Verify Data on the Table is Displayed Correctly in all Columns**  
- **ID:** TC_UI_012  
- **Title:** Verify data on the table is displayed correctly in all columns
- **Preconditions:** User is on the  ([**Web Tables page**](https://demoqa.com/webtables)) 
### 🚶‍♂️ **Test Steps:**    
1. Navigate to the [**Web Tables** page](https://demoqa.com/webtables).  
2. Observe the data displayed in all columns (First Name, Last Name, Age, Email, Salary, Department, Action).  
3. Check if all information is fully visible without any truncation.  
4. Try resizing the columns to check if truncated data becomes visible.  
#### **Expected Result:**  
- All data should be fully visible in each column without truncation.  
- If truncation occurs due to column width, users should be able to resize the column to reveal the full content.  
- The email column should display complete text or provide a tooltip when hovered over.  
#### **Actual Result:**  
- ✅ All columns display data correctly, except for the **Email** column, which appears truncated.  
- ❌ The email field is **not fully visible by default**, but **it becomes visible after resizing the column**.  
- ❌ There is **no tooltip on hover** to display the full email when the column is not expanded.  
📌 **Status:** ⚠️ **Not a bug but a UI improvement suggestion**  
✔ **Enhancement Suggestion:** Add a tooltip to show the full email when hovered over.
--- 
  ### 📋 **Test Case 13: Test editing an existing record.**    
- **ID:** TC_UI_013  
- **Title:** Test editing an existing record.   
- **Preconditions:** User is on ([**Web Tables page**](https://demoqa.com/webtables))
- **Test Steps:**  
  1. Click on the **Edit (✏️)** icon in any row of the table.  
  2. Modify the data in one or more fields (e.g., First Name, Age, Email).  
  3. Click the **Submit** button to save changes.  
  4. Verify if the updated data is displayed correctly in the table.  
  - **Expected Result:**  
  - The user can successfully modify the content of the table’s fields, and the updated data 
    is saved correctly.  
  - **Actual Result:**  
  - The user can successfully modify the content of the table’s fields, and the updated data 
    is saved correctly.  
-✅ **Status:** [Pass]    
---
  ### 📋 **Test Case 14: Ensure sorting functionality works correctly for all columns**    
- **ID:** TC_UI_014  
- **Title** Ensure sorting functionality works correctly for all columns   
- **Preconditions:** User is on ([**Web Tables page**](https://demoqa.com/webtables))
### **Test Steps:**
1. Navigate to the **Web Tables** page.  
2. To sort the data, click on each column's header (**First Name, Last Name, Age, Email, Salary, Department**).  
3. Observe the order of the column values after each sort operation.  
4. Click the same column header again to check if it toggles between ascending and descending order.  
5. Repeat the sorting test for all columns.  
  ### **Expected Result:**  
- When clicked, each column should **sort correctly** in ascending and descending order.  
- The data in the table should be rearranged accordingly without errors.  
- Sorting should remain consistent even after multiple toggles.  
  ### **Actual Result:**  
 ✅ Sorting functionality works correctly for all columns. The table updates as expected, and the sorting order toggles properly.  
**Status:** ✅ **Pass** 

---
### ✔️ **Test Case 15: Verify Button Click Functionality**
- **ID:** TC_UI_015  
- **Title:** Verify Button Click Triggers Correct Message  
- **Preconditions:**  
  - User is on the [**Buttons** page](https://demoqa.com/buttons).  
### 🚶‍♂️ **Test Steps:**  
1. Click the **"Click Me"** button.  
2. Observe the displayed message.  
### ✅ **Expected Result:**  
- After clicking the button, the message **"You have done a dynamic click"** should appear below the button.  
### ✅ **Actual Result:**  
- After clicking the button, the message **"You have done a dynamic click"** appears correctly.  
### 🌍 **Environment:**  
- **Browser:** Chrome 120.0  
- **OS:** Windows 10  
### 📌 **Status:** ✅ **Pass**  
---
### ✔️ **Test Case 16: Test double-click functionality.**
- **ID:** TC_UI_016  
- **Title:** Test double-click functionality.
- **Preconditions:**  
  - User is on the [**Buttons** page](https://demoqa.com/buttons).  
### 🚶‍♂️ **Test Steps:**  
1. Double-click the **"Double click Me"** button.  
2. Observe the displayed message.  
### ✅ **Expected Result:**  
- After clicking the button, the message **"You have done a double click"** should appear below the button.  
### ✅ **Actual Result:**  
- After clicking the button, the message **"You have done a double click"** appears correctly.  
### 🌍 **Environment:**  
- **Browser:** Chrome 120.0  
- **OS:** Windows 10  
### 📌 **Status:** ✅ **Pass**  
---
### ✔️ **Test Case 17: Test right-click functionality.**
- **ID:** TC_UI_017  
- **Title:** Test right-click functionality
- **Preconditions:**  
  - User is on the [**Buttons** page](https://demoqa.com/buttons).  
### 🚶‍♂️ **Test Steps:**  
1. Right-click on the button **"Right click Me"** button.  
2. Observe the displayed message.  
### ✅ **Expected Result:**  
- After clicking the button, the message **"You have done a right click"** should appear below the button.  
### ✅ **Actual Result:**  
- After clicking the button, the message **"You have done a right click"** appears correctly.  
### 🌍 **Environment:**  
- **Browser:** Chrome 120.0  
- **OS:** Windows 10  
### 📌 **Status:** ✅ **Pass**
---
### ✔️ **Test Case 18: Check hover effects and UI responsiveness.**
- **ID:** TC_UI_018  
- **Title:** Check hover effects and UI responsiveness.
- **Preconditions:**  
  - User is on the [**Buttons** page](https://demoqa.com/buttons).  
### 🚶‍♂️ **Test Steps:**  
1. Hover your mouse over the **"Сlick Me"** button.  
2. Observe the behavior of the button.  
### ✅ **Expected Result:**  
- When hovering over the button, the following UI changes should occur:
  -The button’s color should change.
  -The cursor should change to indicate a clickable element.
### ✅ **Actual Result:**  
- The button changed color and the cursor indicated it was clickable, confirming the hover effect works correctly.
### 🌍 **Environment:**  
- **Browser:** Chrome 120.0  
- **OS:** Windows 10  
### 📌 **Status:** ✅ **Pass**
---
## 📝 **Boundary Value Testing**
---
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
  - [View detailed bug report with screenshot ➜ BR_UI_002](https://github.com/Liubov-Ukr/TestingDemoQA/blob/main/Documentation/Bug_Reports/BR_UI_002_Age_Field_Validation_Issue)
- **Status:** ❌ **Fail**
---
  ### 📋 Test Case 9: Verify Minimum and Maximum Character Limits in Input Fields   
- **ID:** TC_UI_009  
- **Title:** Test maximum and minimum character limits.   
- **Preconditions:**  
  - User is on the [**Text Box** page](https://demoqa.com/text-box)  
  - The form is loaded correctly without any issues
 - **Test Steps:**  
  1. Enter 1 character (a) in each field:
    - Full Name
    - Email
    - Current Address
    - Permanent Address.
  2. Click Submit.
  3. Observe field behavior. 
  4. Enter a long text (~255 characters a) in each field.
  5. Click Submit.
  6. Observe field behavior.  
- **Expected Result:**  
  - Fields should have minimum and maximum character input limits.
  - Email should validate and reject incorrect input.
  - Full Name, Current Address, and Permanent Address should have character limits.
  - If the maximum limit is exceeded, one of the following should happen:
  - Input restriction (users cannot enter more characters).
  - Validation error displayed after form submission.  
- **Actual Result:**  
   - Email correctly displays an error for invalid input.
   - Full Name, Current Address, and Permanent Address do not have character limits, and the form is submitted without validation errors.
- **Status:** ❌ **Fail**
   - [View detailed bug report with screenshot ➜ BR_UI_009](https://github.com/Liubov-Ukr/TestingDemoQA/blob/main/Documentation/Bug_Reports/BR_UI_005_Fields_Do_Not_Have_Character_Limit_Validation.md) 
---
## 📝 **Negative Testing**
---
### 🔤 **Test Case 6: Verify Form Submission with Special Characters in Name Field**  
- **ID:** TC_UI_006  
- **Title:** Verify Error When Special Characters Are Entered in the Full Name Field  
- **Preconditions:**  
  - User is on the **webtables** page ([https://demoqa.com/webtables](https://demoqa.com/webtables))  
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
---
### 🔤 **Test Case 7: Check Validation Messages for Incorrect Input**  
- **ID:** TC_UI_007  
- **Title:** Verify Validation Messages for Incorrect Input  
- **Preconditions:**  
  - User is on the [**Text Box** page](https://demoqa.com/text-box)  
  - The form is loaded correctly without any issues  
- **Test Steps:**  
  1. Enter **"558798#)-@"** in all fields (Full Name, Email, Current Address, and Permanent Address).  
  2. Click the **Submit** button.  
- **Expected Result:**  
  - The system should **prevent submission** and display a **validation error message** or **highlight the invalid field** in red to indicate incorrect input.  
  - Alternatively, the system should **sanitize the input** by automatically removing special characters.  
- **Actual Result:**  
  - ❌ The fields **Full Name, Current Address, and Permanent Address** were **accepted without any validation error** or **highlighting**, meaning the system allows special characters in these fields.  
  - ✅ The **Email** field correctly **highlighted the invalid input**, indicating an incorrect email format.  
- **Bug Report Reference:**  
  - [View detailed bug report with screenshot ➜ BR_UI_003](https://github.com/Liubov-Ukr/TestingDemoQA/blob/main/Documentation/Bug_Reports/BR_UI_003_fields_accepted_without_validation_error_or_highlighting.md)  
- **Status:** ❌ **Fail**  
---
### 🔤 **Test Case 8: Check Required Fields Cannot Be Left Empty**  
- **ID:** TC_UI_008  
- **Title:** Ensure Required Fields Cannot Be Left Empty  
- **Preconditions:**  
  - User is on the [**Text Box** page](https://demoqa.com/text-box)  
  - The form is loaded correctly without any issues
### 🚶‍♂️ **Test Steps:**  
1. Navigate to the **Text Box** page.  
2. Leave all fields empty.  
3. Click the **Submit** button.  
4. Repeat the test, entering data only in the **Current Address** field, leaving others empty.  
5. Click the **Submit** button again.
### ✅ **Expected Result:**  
- The system should **prevent submission** of the form.  
- Required fields should be **highlighted in red** to indicate missing data.  
- A **validation message** should be displayed (e.g., "This field is required").  
- The **Submit** button should not trigger data submission if required fields are empty.
### ❌ **Actual Result:**  
- The form was **successfully submitted** even when all fields were left empty.  
- **No validation error messages** or **highlighting** appeared to indicate missing required fields.  
- [View detailed bug report with screenshots ➜ BR_UI_004](https://github.com/Liubov-Ukr/TestingDemoQA/blob/main/Documentation/Bug_Reports/BR_UI_004_Empty_Fields_Submission.md)  
### ⚙️ **Status:** ❌ **Fail**
---
## 📝 **Cross-Browser Testing**
---
### 🖥️ Test Case 11: Verify UI Consistency Across Browsers
- **ID:** TC_UI_011  
- **Title:** Verify the Form Layout is Consistent in Chrome, Firefox, and Edge  
- **Preconditions:** The form is accessible in different browsers  
- **Test Steps:**  
  1. Open the form in Google Chrome.  
  2. Repeat in Firefox and Microsoft Edge.  
- **Expected Result:**  
  - The form layout, fonts, buttons, and fields look consistent across all browsers.  
- **Actual Result:** [The form layout, fonts, buttons, and fields look consistent across all browsers.]  
- **Status:** [Pass]  

