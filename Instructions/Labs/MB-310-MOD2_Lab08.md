---
lab:
    title: 'Exercise 8: Configure and test ledger allocation rules'
    module: 'Module 2: Set up and configure financial management'
---


## Exercise 8: Configure and test ledger allocation rules

You need to configure and test ledger allocation rules in **USMF**. Per the accountant request three new ledger accounts should be created to allocate posted transaction equally to different financial dimensions based on a rule for the current period.

### Create main accounts



1. Navigate to **General ledger &gt; Chart of accounts &gt; Accounts &gt; Main accounts**.

2. Select **+New**

3. In the **Main account** field, type '100001'

4. In the **Name** field, type 'Allocated Account 1'.

5. Select **+New**

6. In the **Main account** field, type '100002'

7. In the **Name** field, type 'Allocated Account 2'.

8. Select **+New**

9. In the **Main account** field, type '100003'

10. In the **Name** field, type 'Allocated Offset Account'.

11. Close the page


### Create date intervals for current period



1. Navigate to **General ledger &gt; Ledger setup &gt; Date intervals**.

2. Select **+New**

3. In the **Date interval code** field, type 'CurPeriod.'

4. In the **Description** field, type 'Current Period.'

5. In the **From** **date** **period** **type** field, select 'Period.'

6. In the **From** **date** **Start/End** field, select 'Start.'

7. In the **To date period type** field, select 'Period.'

8. In the **To date Start/End** field, select 'End.'

9. Close the page


### Create allocation journal name



1. Navigate to **General ledger &gt; Journal setup &gt; Journal names**.

2. Select **+New**

3. In the **Name** field, type 'AllocDemo'.

4. In the **Description** field, type 'Allocation Journals Demo'.

5. In the **Journal** **type** field, select 'Allocation'.

6. In the **Voucher** **series** field, enter or select a value.

7. Close the page


### Create allocation rule



1. Navigate to **General ledger &gt; Allocations &gt; Ledger allocation rules**.

2. Select **+New**

3. In the **Rule** field, type ‘**AdvRule’**

4. In the **Description** field, type **'Adventure Works Rent Allocation Demo**'.

5. Select the **General** tab.

6. Select **Yes** in the **Active** field.

7. In the **Allocation method** field, select **'Equally'**.

8. In the **Journal name** field, enter or select a value **AllocDemo** 

9. In the **Date interval code** field, enter or select **CurPeriod** then press tab

10. Select **Source** in the action pane.

11. Select **+New**

12. In the **Source criteria** field, enter or select 601501 

13. Select **+New**

14. In the **Field setting** field, select **'Financial dimension'**.

15. In the **Name** field, enter or select **BusinessUnit** 

16. In the **Source criteria** field, enter or select 004

17. Select **+New**

18. In the **Field setting** field, select **'Financial dimension'**.

19. In the **Name** field, enter or select **Department** 

20. In the **Source criteria** field, enter or select 024

21. Close the page

22. Select **Destination**.

23. Select **+New**

24. In the **To account** field, specify the values '100001'.

25. In the **Department** field, enter or select 023.

26. Select **+New**

27. In the **To account** field, specify the values '100002'.

28. In the **Department** field, enter or select 026.

29. Close all forms


### Create and post general journal for allocation testing



1. Navigate to **General ledger &gt; Journal entries &gt; General journals**.

2. Select **+New**

3. In the **Name** field, enter or select **GenJrn****.**

4. Select **Lines**

5. In the **Account field**, specify the values '601501-004-024--'.

6. In the **Description** field, type 'Allocation Demo'.

7. Set **Debit** to '72700.'

8. In the **Offset account** field, specify the values '605160-004-024--'.

9. Select **Post**

10. Close all forms


### Process allocation request to test the allocation rule

1. Navigate to **General ledger &gt; Allocations &gt; Process allocation request**.

2. In the **Rule** field, enter or select ‘**AdvRule’**.

3. In the **Proposal options** field, select 'Proposal only'.

4. Select **OK**

### Verify the allocation journals created by process allocation requests



1. Navigate to **General ledger &gt; Allocations &gt; Allocation journals**.

2. Find and select the proposed journal with description of 'Allocation Journals Demo'

3. Select **Lines**

4. Review and analyze data to see if the original transaction has been allocated equally.

5. Select **Validate &gt; Simulate posting** 

6. Select **Post**

7. Close all forms


 
