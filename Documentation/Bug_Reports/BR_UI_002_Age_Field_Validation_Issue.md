
### 🐞 **Bug Report: Age Field Validation Issue**

- **ID:** BR_UI_002
- **Related Test Case:**  TC_UI_005
- **Title:** The Age field accepts values below 18 without validation errors  
- **Reported By:** Liubov  
- **Date:** 03.02.2025  
- **Severity:** Medium  
- **Priority:** High  

### **Description:**  
The system allows users to enter and save age values below 18 (e.g., 1 and 17) without displaying any validation errors, even though the expected minimum age is 18. This behavior contradicts the business rules for age validation.

### **Preconditions:**  
- User is on the **Web Tables** page (`https://demoqa.com/webtables`)

### **Steps to Reproduce:**  
1. Click the **Add** button to open the form.  
2. Enter the following details:  
   - **First Name:** Liubov  
   - **Last Name:** Opryshchenko  
   - **Age:** 1 (or 17)  
   - **Email:** liubov@gmail.com  
   - **Salary:** 4000  
   - **Department:** QA  
3. Click the **Submit** button.  

### **Expected Result:**  
- The system should display a validation error when younger than 18, preventing form submission.

### **Actual Result:**  
- The system allows the form to be submitted successfully, and the user is added to the table with an invalid age.  
- **No validation message** is displayed.

### **Attachments:**  
- 📷 **Screenshot:** [screenshot showing the age field validation issue](https://github.com/Liubov-Ukr/TestingDemoQA/blob/main/Screenshots/BR_UI_002_Age_Field_Validation_Issue.png)  
  

### **Environment:**  
- **Browser:** Chrome 120  
- **OS:**  Windows 10 
- **Device:** Desktop  

### **Status:** Open  

