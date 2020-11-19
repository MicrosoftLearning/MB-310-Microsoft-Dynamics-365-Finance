---
lab:
    title: 'Exercise 3: Create an Audit Policy'
    module: 'Module 5: Implement and manage expense management'
---

## Exercise 3: Create an Audit Policy

Cassie, the internal auditor at Contoso determines that a new audit policy must be created for duplicate expense report lines in the USSI company. Duplicate expenses are defined as expenses within a 90-day window where the amount, the category, and the employee are identical.

You will create a policy rule type that will allow you to select the document that you want to audit and the query type you want to apply to that document. After you create the policy rule type, you will create an audit policy in which you will define the criteria for your query and the legal entities that the policy applies. You will then assign the policy to a batch and run it. 

As the policy runs, if any violations are found, audit cases will automatically be created and the document(s) that contain the violation will be attached to the audit cases.

### Create a new audit policy rule type called, Duplicate expenses.

1. Navigate to **Audit workbench &gt; Setup &gt; Policy rule type**.

2. Select **New**.

3. In the **Rule name** field, type “**My Duplicate expenses policy**”.

4. In the **Description** field, type “Audit of duplicate expense lines”.

5. Select **Expense report line** in the **Query name** field.

6. Select **Duplicate** in the **Query type** field.

7. Select **Legal entity** in the **Legal entity** field.

8. Select **Modified date and time** in the **Document date** **reference** field.

9. Close the Policy rule type form.

### Create an audit policy

1. Navigate to **Audit workbench &gt; Setup &gt; Audit policies**.

2. Select **New**.

3. Enter “Expense reports USSI” in the **Name** field.

4. Type “Audit expense reports in USSI” in the **Description** field.

5. Expand the **Policy organizations** fast tab.

6. Select Contoso Consulting USA (USSI) in the **Available organization nodes** list.

7. Select **Add** &#8594; to place Contoso Consulting USA (USSI) in the Selected organization nodes list.

8. Expand the **Policy rules** fast tab.

9. Select the **Duplicate expenses(0)** rule and select **Create policy rule**.

10. In the Audit policy rule form select the **Filter** button.

11. In the Expense report line form select the **Group by** tab.

12. Select **Add** and in the **Field** drop-down select the **Transaction amount**.

13. Select **Add** and in the **Field** drop-down select **Date approved**.

14. Select **Add** and in the **Field** drop-down select **Expense category**.

15. Select **Add** and in the **Field** drop-down select **Employee**.

16. Select **OK**.

17. On the Audit policy rule form enter **90** in the **Additional days to evaluate for duplicates** field.

18. Select **OK**.

19. Close the form.

 
