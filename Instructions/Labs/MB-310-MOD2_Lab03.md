---
lab:
    title: 'Exercise 3: Create Advanced Rule Structures'
    module: 'Module 2: Set up and configure financial management'
---

## Exercise 3: Create Advanced Rule Structures

Consider the following scenario:

Phyllis, the Accounting Manager, is setting up the charts of accounts for Contoso Enterprise. For some of the accounts, the organization wants to track additional information that is not captured in the account structures. She needs to ensure that for the customer group (one of the financial dimensions)"80: Other customers" that only certain departments can be used. 

### Perform the following steps to create an advanced rule: 

1. Navigate to General **ledger &gt; Chart of accounts &gt; Structures &gt; Configure account structures**.

2. On the **Action pane**, select **New** to open the drop dialog.

3. In the **Account structure** field, type a name “**My Acct. Structure**” to describe the purpose of the account structure.

4. In the **Description** field, type a description “**My first Acct. Structure”** to specify the purpose of the account structure.

5. Ensure that **Add main account** is set to **Yes**.

6. Select **Create**

7. In the **Segments and allowed values** section, select **Add segment**.

8. In the dimensions list, select the **Department** dimension to add to the account structure.

9. At the end of the list, Select **Add segment**.

10. Repeat step 6 to8 to add **Cost center** as segment.

11. In the **Segments and allowed values** section, select the segment to edit the allowed values in the **Allowed value details** section. For example, Select the **Main Account** field.

12. In the **Operator** field, select an option, such as **is between and includes**.

13. In the **Value** field, type a value:600000.

14. In the **through** field, type a value: 699999.

15. In the **Allowed value details** section, select **Apply**.

16. In the **Segments and allowed values** section, select the segment to edit the allowed values in the **Allowed value details** section. For example, select the **Department** field.

17. In the **Operator** field, select an option, such as **is between and includes**.

18. In the **Value** field, type a value: 033.

19. In the **through** field, type a value: 034.

20. Select **Apply**

21. In the **Segments and allowed values** grid, select the segment to edit the allowed values in the **Allowed value details** section: **Cost Center.**

22. In the **Value** field, type a value: 007..021.

23. In the **Segments and allowed values**, select **Add**.

24. In the **MainAccount** field, type a value:700000.699999

25. In the grid, select the segment to edit the allowed values: **Department**.

26. In the **Department** field, type a value, for example, 032.

27. In the **CostCenter** field, type a value, for example, 086.

28. On the **Action pane**, select **Validate**.

29. On the **Action pane**, select **Activate**.

30. Select **Activate**



