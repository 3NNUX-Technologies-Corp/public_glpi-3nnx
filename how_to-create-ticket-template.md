# **GLPI Documentation: Assistance Templates & ITIL Categories**

## **1. Introduction**  
GLPI allows administrators to set up **Assistance Templates** and **ITIL Categories** to streamline ticket management. ITIL Categories help classify incidents and requests, while Assistance Templates ensure consistency in ticket handling.

---

## **2. Creating an Assistance Template**  

### **Step 1: Navigate to Assistance Templates**  
1. Log in to **GLPI** as an administrator.  
2. Go to **Setup → Dropdowns → Assistance Templates**.  
3. Click **Add a new template**.  

---

### **Step 2: Configure the Assistance Template**  
1. **Enter a Template Name** (e.g., "General IT Request").  
2. **Predefine Ticket Fields**:
   - **Title**: Set a default subject for the ticket.  
   - **Category**: Choose an ITIL Category (e.g., Hardware, Software, Network).  
   - **Urgency & Priority**: Define default values.  
   - **Assigned Group/Technician**: Automatically assign requests.  
   - **Request Type**: Select **Incident** or **Service Request**.  
3. **Set Default Ticket Description** – Include instructions or additional details for users.  

---

### **Step 3: Set Permissions & Apply the Template**  
1. Define which users/groups can access this template.  
2. Click **Save** to store the template.  
3. Test it by creating a new ticket and selecting the template from the dropdown.  

---

## **3. Creating & Managing ITIL Categories**  

### **Step 1: Navigate to ITIL Categories**  
1. Go to **Setup → Dropdowns → ITIL Categories**.  
2. Click **Add a new category**.  

---

### **Step 2: Define ITIL Category Settings**  
1. **Enter a Category Name** (e.g., "Network Issues").  
2. **Choose a Parent Category** (if applicable).  
3. **Set Default SLA** (if using Service Level Agreements).  
4. **Define Visibility**:  
   - Select user profiles that can view this category.  
   - Enable/disable automatic assignment to a group/technician.  

---

### **Step 3: Assign ITIL Categories to Ticket Templates**  
1. Edit an existing **Ticket Template** (`Setup → Dropdowns → Ticket Templates`).  
2. Select the **ITIL Category** to associate with the template.  
3. Save the changes and test by creating a new ticket.  

---

## **4. Automating ITIL Category Assignment**  
- Use **Business Rules** to assign categories automatically:  
  1. Go to **Setup → Rules → Business Rules for Tickets**.  
  2. Click **Add a New Rule**.  
  3. Define conditions (e.g., if the title contains "Email issue", set category to "Email Support").  
  4. Click **Save & Activate** the rule.  

---

## **5. Need More Help?**  
📖 **Official GLPI Documentation**: [GLPI Project](https://glpi-project.org/documentation)  
🐞 **Report Issues**: [GitHub Issues](https://github.com/3NNUX-Technologies-Corp/public_glpi-3nnx/issues)  
📧 **Contact Support**: your-email@example.com  
