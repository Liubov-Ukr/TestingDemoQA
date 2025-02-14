
### 🐞 **Bug Report: Newly Created User Does Not Appear in the User List

- **Bug ID:** BR_002  
 - **Related Test Case:** TC_API_004
- **Title:** Newly Created User Does Not Appear in the User List  
- **Reported By:** Liubov  
- **Date Reported:** 02.02.2025  
- **Environment:** Postman, Windows 10  

---

### 🔍 **Description:**  
After creating a new user via a **POST** request, the user’s data does not appear in response to a subsequent **GET** request.  

---

### 📋 **Steps to Reproduce:**  
1. Send a **POST** request to create a new user:  
   [https://reqres.in/api/users](https://reqres.in/api/users)  
2. Example request body:  

   ```json
   {
     "name": "Camilla QA",
     "job": "QA Engineer"
   }
   ```  
3. Copy the **ID** of the created user.  
4. Send a **GET** request:  
   [https://reqres.in/api/users](https://reqres.in/api/users)  
5. Check if the newly created user appears in the list.  

---

### ✅ **Expected Result:**  
The newly created user should appear in the response to the **GET** request.  

### ❌ **Actual Result:**  
The newly created user is **missing** from the list.  

---

### 📷 **Attachments:**  
[**Postman screenshot showing the response**](https://github.com/Liubov-Ukr/TestingDemoQA/blob/main/Screenshots/%D0%A1reated-User-Not-Displayed-in-User-List.png)

### ⚙️ **Severity:** Low *(Since the API is for demo purposes)*  
### 🔗 **Status:** Open  

