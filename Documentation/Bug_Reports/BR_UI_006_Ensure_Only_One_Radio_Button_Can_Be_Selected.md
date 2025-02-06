
### 🐞 **Bug Report: Ensure Only One Radio Button Can Be Selected  **  
- **ID:** BR_UI_006
- **Related Test Case:** TC_UI_010
- **Title:** Ensure Only One Radio Button Can Be Selected    
- **Severity:** Medium  

---

- **Preconditions:**  
  - User is on the [**Radio Button** page](https://demoqa.com/radio-button)  

---

### 🚶‍♂️ **Test Steps:**  
1. Click the **"Yes"** radio button.  
2. Observe the behavior of the radio button selection.  
3. Click the **"Impressive"** radio button.  
4. Observe the behavior of the radio button selection.  
5. Click the **"No"** radio button.  
6. Observe whether the selection changes.  

---

### ✅ **Expected Result:**  
- Users should be able to switch easily between radio button options.  
- When clicking a selected radio button again, the selection should remain (radio buttons cannot be deselected manually).  
- The user should be able to select any of the three options: **"Yes," "Impressive," and "No."**  
- Only **one** radio button should be selected at a time.  
---
### ❌ **Actual Result:**  
- ✅ The user **can** switch between "Yes" and "Impressive" radio buttons correctly.  
- ❌ The user **cannot select "No"**—clicking it does nothing.  
- ✅ The user **cannot select multiple options at once**, which is expected behavior.  
- ❌ Clicking a selected radio button **does not remove the selection**, which may not be intuitive.  

### 📷 **Attachments:**  
1. **"Impressive" radio button selected:**  
   ![Impressive Selected](https://github.com/Liubov-Ukr/TestingDemoQA/blob/main/Screenshots/BR_UI_006_Impressive_Selected.png)  
2. **"Yes" radio button selected:**  
   ![Yes Selected](https://github.com/Liubov-Ukr/TestingDemoQA/blob/main/Screenshots/BR_UI_006_yes_Selected.png)  
3. **Attempting to select "No" (but it does not work):**  
   ![No Not Selectable](https://github.com/Liubov-Ukr/TestingDemoQA/blob/main/Screenshots/BR_UI_006_No_Not_Working.png)  
---

### 🌍 **Environment:**  
- **Browser:** Chrome 120.0  
- **OS:** Windows 10  

---

### ⚙️ **Status:** Open
