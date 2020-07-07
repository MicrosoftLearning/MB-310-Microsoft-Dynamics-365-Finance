### Before you begin

To get the most out of this exercise and the other exercises that are included
with this module, we recommend that you have the standard sample data available
in Finance and Operations that is installed using Lifecycle Services (LCS).

Exercise 1 - Configure and use accrual schemes
==============================================

You need to assist Sabrina, the accountant in USMF, on how to configure and use
accrual schemes in Finance and Operations. She wants to lease a vehicle from a
vendor for \$81,720 US dollars (USD) and record accruals in Finance and
Operations within the terms of lease of 24 months. She wants to understand the
monthly and number of day option in the accrual schemes.

Create accrual schemes
----------------------

1.  Go to **General ledger \> Journal setup \> Accrual schemes**.

2.  Click **New**.

3.  In the **Accrual identification** field, type '24M'.

4.  In the **Description** of accrual scheme field, type '2 Year Lease'.

5.  In the **Debit** field, specify the values '420100'.

6.  In the **Credit** field, specify the values '420200'.

7.  In the **Voucher field**, select **New voucher for each transaction**.

8.  In the **Number sequence code** field, enter or select a value.

9.  In the **Period** frequency field, select **Monthly**.

10. In the **Number of occurrences by period** field, enter '24'.

11. In the **Post transactions** field, select **Month**.

12. In the **Post in week, month or quarter** field, select **Middle**.

13. Close the page.

Create general journal to use accrual schemes
---------------------------------------------

1.  Go to **General ledger \> Workspaces \> General journal processing**.

2.  Click **New journal**.

3.  In the **Name** field, enter or select **GenJrn.**

4.  In the **Description** field, type 'General Daily Journal - Accruals Demo'.

5.  Click **Lines**.

6.  In the **Account type** field, select **Vendor**.

7.  In the **Account field**, specify a vendor account of your choice.

8.  Set **Debit** to '81720'.

9.  In the **Offset account** field, specify the values '601512-025-009- '.

10. In the **Offset transaction** text field, type 'Accruals Demo'.

11. Click **Functions**.

12. Click **Ledger accruals**.

13. In the **Accrual identification** field, enter or select **24M.**

14. Click **Transactions**.

15. Review the values. The total amount is distributed evenly.

16. Close the page.

17. Click to follow the link in the **Accrual identification** field, or
    right-click and view details.

18. In the **Spread month and quarter values** field, select **Number of days**.

19. Close the page.

20. Click **Cancel**.

21. Click **Yes**.

22. Click **Functions**.

23. Click **Ledger accruals**.

24. In the **Accrual identification** field, enter or select **24M**, and then
    press the Tab key.

25. Click **Transactions**. Note that amounts have been prorated for the
    specified number of days.

26. Close the page.

27. Click **OK**.

28. Click **Validate \> Validate**.

29. Click **Post**.

30. Close all pages.

31. Go to **General ledger \> Inquiries and reports \> Audit trail**.

32. Find the journal that you just posted, which should be the last record or
    you can use the filter option.

33. Click **Voucher transactions**.

34. Review and analyze posted transactions. Note that the original transactions
    have been reversed and accruals have been posted through 24 months.

35. Close all pages.

Exercise 2 - Configure and test ledger allocation rules
=======================================================

You need to configure and test ledger allocation rules in USMF. The accountant
requests that you create three new ledger accounts to allocate posted
transactions equally to different financial dimensions, based on a rule for the
current period.

Create main accounts
--------------------

1.  Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**.

2.  Click **New**.

3.  In the **Main account** field, type '100001'

4.  In the **Name** field, type 'Allocated Account 1'.

5.  Click **New**.

6.  In the **Main account** field, type '100002'

7.  In the **Name** field, type 'Allocated Account 2'.

8.  Click **New**.

9.  In the **Main account** field, type '100003'

10. In the **Name** field, type 'Allocated Offset Account'.

11. Close the page.

Create date intervals for current period
----------------------------------------

1.  Go to **General ledger \> Ledger setup \> Date intervals**.

2.  Click **New**.

3.  In the **Date interval code** field, type 'CurPeriod'.

4.  In the **Description** field, type 'Current Period'.

5.  In the **From date period type** field, select **Period**.

6.  In the **From date Start/End** field, select **Start**.

7.  In the **To date period type** field, select **Period**.

8.  In the **To date Start/End** field, select **End**.

9.  Close the page.

Create an allocation journal name
---------------------------------

1.  Go to **General ledger \> Journal setup \> Journal names**.

2.  Click **New**.

3.  In the **Name** field, type 'AllocDemo'.

4.  In the **Description** field, type 'Allocation Journals'.

5.  In the **Journal type** field, select **Allocation**.

6.  In the **Voucher series** field, enter or select a value.

7.  Close the page.

Create an allocation rule
-------------------------

1.  Go to **General ledger \> Allocations \> Ledger allocation rules**.

2.  Click **New**.

3.  In the **Description** field, type **'Seahorse Rent Allocation Demo**'.

4.  Click the **General** tab.

5.  Select **Yes** in the **Active** field.

6.  In the **Allocation method** field, select **Equally**.

7.  In the **Journal name** field, enter or select **AllocDemo.**

8.  In the **Date interval code** field, enter or select **CurPeriod**, and then
    press the Tab key.

9.  Click **Source**.

10. Click **New**.

11. In the **Source criteria** field, enter or select **601511.**

12. Click **New**.

13. In the **Field setting** field, select **Financial dimension**.

14. In the **Name** field, enter or select **Department.**

15. In the **Source criteria** field, enter or select **024.**

16. Close the page.

17. Click **Destination**.

18. Click **New**.

19. In the **To account** field, specify the values '100001'.

20. In the **Department** field, enter or select **023.**

21. Click **New**.

22. In the **To account** field, specify the values '100002'.

23. In the **Department** field, enter or select **026.**

24. Close all pages.

Create and post general journal for allocation testing
------------------------------------------------------

1.  Go to **General ledger \> Journal entries \> General journals**.

2.  Click **New**.

3.  In the **Name** field, enter or select **AllocDemo**\*\*.\*\*

4.  Click **Lines**.

5.  In the **Account field**, specify the values '601511-024-020- '.

6.  In the **Description** field, type 'Allocation Demo'.

7.  Set **Debit** to '72700'.

8.  In the **Offset account** field, specify the values ' 605160 -024-020- '.

9.  Click **Post**.

10. Close all pages.

Process an allocation request to test the allocation rule
---------------------------------------------------------

1.  Go to **General ledger \> Allocations \> Process allocation request**.

2.  In the **Rule** field, enter or select **Seahorse Rent Allocation Demo**.

3.  In the **Proposal options** field, select **Proposal only**.

4.  Click **OK**.

Verify the allocation journals created by processing the allocation requests
----------------------------------------------------------------------------

1.  Go to **General ledger \> Allocations \> Allocation journals**.

2.  Click **Lines**.

3.  Review and analyze data to see if the original transaction has been
    allocated equally.

4.  Go to **Validate \> Simulate posting.**

5.  Click **Post**.

6.  Close all pages.
