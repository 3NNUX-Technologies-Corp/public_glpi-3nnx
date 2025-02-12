# **GLPI - Frequently Asked Questions (FAQ)**

## **1. What is GLPI?**
GLPI (**Gestionnaire Libre de Parc Informatique**) is an open-source IT asset management and service desk software. It helps organizations manage their IT inventory, track incidents, and improve IT service management.

---

# **User Management**

## **2. How do I add a user in GLPI?**
1. Log in as an **Administrator**.  
2. Navigate to **Administration → Users**.  
3. Click **+ (Add User)** and fill in the required details:
   - **Username**
   - **Full Name**
   - **Email**
   - **Profile** (e.g., Normal User, Technician, Admin)
   - **Password** (if using local authentication)  
4. Click **Save** to add the user.  

For LDAP/AD integration, enable **LDAP synchronization** under **Setup → Authentication → LDAP Directories**.

---

## **3. How do I reset a user’s password in GLPI?**
1. Go to **Administration → Users**.  
2. Select the user and click **Edit**.  
3. Under the **Password** field, enter a new password.  
4. Click **Save**.  

If using LDAP authentication, reset the password in **Active Directory**.

---

## **4. How do I assign profiles and permissions to users?**
1. Navigate to **Administration → Users**.  
2. Select a user and go to the **Profiles** tab.  
3. Click **+ (Add Profile)** and choose a role:
   - **Administrator:** Full access.
   - **Technician:** Manage tickets and assets.
   - **Normal User:** Limited access.
4. Click **Save**.

You can also configure **entity restrictions** for multi-department organizations.

---

# **Ticketing System**

## **5. How do I create a ticket in GLPI?**
1. Go to **Assistance → Tickets**.  
2. Click **+ (Add Ticket)**.  
3. Fill in the details:
   - **Title**
   - **Requester**
   - **Category**
   - **Description**
   - **Priority**
4. Click **Save** to submit the ticket.  

---

## **6. How do I assign a ticket to a technician?**
1. Open an existing ticket.  
2. Click on the **Technician** field.  
3. Choose a **technician** from the list.  
4. Click **Save**.  

The assigned technician will be notified via email if notifications are enabled.

---

## **7. How do I track and update tickets in GLPI?**
- Go to **Assistance → Tickets**.  
- Click on any **ticket ID** to view details.  
- Update ticket status (**In Progress, Pending, Solved, Closed**).  
- Add follow-ups or solutions in the **Follow-ups** tab.  
- Click **Save**.

---

## **8. How do I enable automatic ticket assignment?**
1. Go to **Setup → Automatic Actions**.  
2. Look for **Ticket Assignment**.  
3. Set rules based on **category, urgency, and groups**.  
4. Enable the automation process.  

This ensures tickets are assigned to the correct department automatically.

---

## **9. How do I set up SLA (Service Level Agreements) in GLPI?**
1. Go to **Setup → Dropdowns → SLAs**.  
2. Click **+ (Add SLA)** and define:
   - Response Time
   - Resolution Time
   - Escalation Rules  
3. Assign the SLA to specific **categories or users**.  
4. Enable email notifications for SLA breaches.

---

## **10. How do I enable email notifications for tickets?**
1. Go to **Setup → Notifications**.  
2. Enable **Mail Notifications**.  
3. Configure SMTP settings under **Setup → Emails → Mail Receivers**.  
4. Test the settings by sending a test email.

---

# **General GLPI Questions**

## **11. How do I install GLPI?**
To install GLPI:  
1. Download the latest version from [GLPI’s official website](https://glpi-project.org/).  
2. Install a web server with **PHP, MySQL/MariaDB, and Apache/Nginx**.  
3. Extract and upload GLPI files to your web server.  
4. Run the **installation wizard** by visiting your server URL in a browser.  
5. Configure the database and finalize the installation.  

---

## **12. How do I integrate GLPI with Active Directory (LDAP)?**
1. Go to **Setup → Authentication → LDAP Directories**.  
2. Click **+ (Add LDAP Server)** and enter:
   - **Server Address (IP/Hostname)**
   - **Base DN (e.g., DC=example,DC=com)**
   - **Bind User & Password**  
3. Click **Test Connection** to verify.  
4. Enable **LDAP user import** in **Administration → Users**.

---

## **13. How do I update GLPI?**
1. **Backup** your database and files.  
2. Download the latest version from [GLPI’s website](https://glpi-project.org/).  
3. Replace the old GLPI files with the new ones.  
4. Run the **update script** by accessing GLPI in a browser.  
5. Follow the upgrade steps.

---

## **14. How do I add plugins in GLPI?**
1. Download plugins from the [GLPI marketplace](https://plugins.glpi-project.org/).  
2. Extract them to the **/plugins/** folder in your GLPI installation.  
3. Go to **Setup → Plugins** in GLPI.  
4. Click **Install** and then **Activate** the plugin.  

---

## **15. How do I back up GLPI?**
To back up GLPI:  
1. **Database Backup:**  
   ```bash
   mysqldump -u root -p glpi > backup_glpi.sql
