---
lab:
    title: 'Exercise 8: Configure vendor collaboration'
    module: 'Module 4: Implement and manage accounts payable'
---

## Exercise 8: Configure vendor collaboration

Verify External Roles


1. In **USMF**, navigate to **System administration &gt; Security &gt; External roles**

2. Verify that **Vendor (external)** and **Vendor admin (external)** roles are listed.  
‎Navigate to **Procurement and sourcing &gt; Vendors &gt; All vendors**

3. Select the vendor 1001 link to open the details page.

4. In the **Collaboration activation** field in the **General** section, select **Active (PO is not auto-confirmed)**

5. Select **Add contacts** from the action pane under Vendor, Set up, Contacts

6. In the **First name** field select **Alex Darrow**

7. Select **Save**.

8. Select **Provision vendor user** under Contact, Requests

9. Setup an email alias.

10. Enter **Demo vendor collaboration** in the **Business justification** field.

11. Select **Vendor collaboration access allowed** check box in the **Legal entities the person is a contact for** section.

12. In the **Assign user roles** section, check the box for **Assign** next to Maintains vendor documents and responds to vendor inquiries in the vendor collaboration interface.

13. Select **Submit.**


**Note**: a workflow step Azure B2B can be used to communicate to the Azure portal to create a user account, and add this as a guest user, so that the user later can be authenticated and log into Dynamics 365 – or if the email is already recognized as an existing Azure user add this user as guest user.


 

