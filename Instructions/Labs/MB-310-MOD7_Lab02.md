---
lab:
    title: 'Exercise 2: Configure Budget control components'
    module: 'Module 7: Configure and manage budgeting'
---

## Exercise 2: Configure Budget control components

You need to configure the budget control for your company. Select **USMF** to practice and learn how. 

**Note:** You need to complete Exercise 1

### Instructions

1. Open **Budgeting &gt; Setup &gt; Budget control &gt; Budget cycles**.

2. Select **+New** and enter a name for the budget cycle time span.

3. Select a fiscal calendar to associate with the budget cycle time span.

4. In the **Length of budget cycle** field, select **Specify number of periods** or **Map to fiscal year**.

5. If you select **Specify number of periods**, enter the number of accounting periods for the budget cycle.

6. If you select **Map to fiscal year**, the budget cycle time span uses the fiscal year that is defined by the starting and ending periods for the budget cycle.

7. Select **+Add**. Enter the name of the first period in the budget cycle time span and enter the date when that period starts. The ending date for the budget cycle is determined automatically based on the number of fiscal periods in the budget cycle time span.

8. Open **Budgeting &gt; Setup &gt; Budget control &gt; Budget control configuration**.

9. Select an **Account structure.** If you have multiple active account structures in the chart of accounts, select the account structure that will be used for profit and loss or expense accounts. This account structure includes the main account range for expense accounts.   
‎**Note:** You may need to **Create draft** of the budget control if you are working with one of the companies provided as part of the demo data to make changes in this form. 

10. After you select an account structure, all the financial dimensions in that account structure and advanced rules that are defined for budgeting are displayed in the Budget dimensions list.

11. Select a financial dimension and move it to the **Budget control dimensions** list.

12. Select a **Budget control interval**, such as **Fiscal year** or **Fiscal year to date**. The budget control interval works with the budget cycle to determine how amounts are aggregated for budget checking. 

13. For example, if you select Fiscal year, all the funds for the fiscal year are aggregated for budget checking. If you select Fiscal year to date or Budget to date, the ending date is determined from the fiscal period and the accounting date of the source document or accounting journal that is being checked.

14. Select the **Budget cycle time span**, which defines the length of the budget cycle. 

15. Select a **Budget manager**, which is a user who can approve budget workflows. Another budget manager can be defined by using a budget control rule.

16. In the **Budget threshold** field, enter the percentage of the budget that can be spent. The threshold can be used to provide warning messages or to define budget permissions to prevent specific user groups from exceeding the budget threshold. This threshold can exceed 100 percent.

17. Select the **Display a message when exceeding budget threshold** check box to display messages when the budget threshold is exceeded.

18. Select the **Over budget permissions** tab.

19. Select **+Add** to create a new rule.

20. Select the desired **User group**.

21. Select the **Over budget** option.

22. Select **Budget funds available** tab and select desired check boxes to formulate how the available funds gets calculated.

23. Select **Documents and journals**.

24. Select the **Purchase requisitions** check box. The **Purchase orders** and **Vendor invoices** check boxes are automatically selected.

25. If you do not select the **Purchase requisitions** check box and you instead select the **Purchase orders** check box, the **Vendor invoices** check box is automatically selected.

26. You can select **Vendor invoices**, **Travel requisitions**, and **Expense reports** independently of the other source documents.

27. For each source document, you can select the **Enable budget control** for line item on entry check box to enable budget checking for each line as the line is entered and saved.

28. Select the **Assign budget models** tab.

29. Select **+Add** and then select a **budget cycle time span**.

30. Select a **Budget cycle**.

31. Select a **Budget model**. Only budget models that do not contain submodels are available for budget control.

32. Select **Define budget control rules**. Define rules as desired.

33. Select **Select main accounts**.

34. Select the check boxes to select the main accounts or select **Select all** to select all the main accounts.

35. Select **Activate budget control**.

36. Select **Activate** to make the draft version of the budget control configuration active. The Date when last activated field displays the current date, and the Activated by field displays your user ID. Select **OK** and **Activate**.

37. You have started budget control by using the active configuration. The budget control status changes to Turned on, and the Turn on button is replaced with Turn off.

 

 
