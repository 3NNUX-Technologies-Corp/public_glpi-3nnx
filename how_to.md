# How to Add a User in GLPI

## **Via the GLPI Web Interface**
1. **Log in to GLPI**  
   - Open your web browser and go to your GLPI URL.  
   - Log in with an administrator account.

2. **Navigate to User Management**  
   - Click on **Administration** → **Users**.

3. **Add a New User**  
   - Click the **+ (Add User)** button.  
   - Fill in the required details:
     - **Username**
     - **Full name**
     - **Email**
     - **Profile** (e.g., Normal User, Technician, Administrator)
     - **Password** (if using local authentication)

4. **Set Additional Details (Optional)**  
   - Define groups, entities, and permissions.  
   - Assign associated assets (computers, software, etc.).

5. **Save the User**  
   - Click **Add** or **Save**.

---

## **Via LDAP/Active Directory (If Integrated)**
If your GLPI is connected to an LDAP/Active Directory:  
1. Go to **Administration** → **Users**.  
2. Click **LDAP Directory Synchronization**.  
3. Search for users and import them into GLPI.

---

## **Via API (For Advanced Users)**
If you're using GLPI’s API, you can add users via API requests.

Would you like help setting up LDAP or API integration? 🚀
