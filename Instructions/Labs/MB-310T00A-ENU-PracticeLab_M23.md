**Before you begin**

To get the most out of this exercise and the other exercises that are included
with this module, we recommend that you have the standard sample data available
in Finance and Operations that is installed using Lifecycle services (LCS).

Exercise - Configure fixed assets components
============================================

This exercise will set up fixed asset posting profiles and multiple transaction
types. It uses the Accountant role and demo data for the **USMF** company.
Examples given in the exercise are for a basic posting profile, though posting
profiles must be created for your specific chart of accounts and financial
reporting requirements.

Set up fixed asset posting profiles
-----------------------------------

1.  Go to **Fixed assets \> Setup \> Fixed asset posting profiles**.

2.  Click **New**.

3.  In the **Posting profile** field, type **FAPP**

4.  In the **Description** field, type Fixed asset posting profile. You will
    need to create a posting profile for each fixed asset transaction type you
    will be using when working with fixed assets. Let’s start with the
    **Acquisition** transaction type.

5.  Click **Add**.

6.  In the **Book** field, enter **SLLR**.

The **Groupings** field allows you to define the posting profile down to the
Table (one account set up for each fixed asset) or Group (one account set up for
each fixed asset group). For this exercise, I will leave the value set to “All”
to apply to all fixed assets with the specified Book.

1.  In the **Main account** field, specify **180100**.

2.  In the **Offset account** field, specify **300160**.

For Acquisitions, you can enter an offset account or leave it blank to be filled
in for the specific transaction.

1.  In the **Transaction type** field, select **'Acquisition adjustment'**.

For Acquisition adjustment transactions, we will use the same accounts as used
for Acquisition transactions.

1.  Click **Add**.

2.  In the **Book** field, enter **SLLR**.

3.  In the **Main account** field, specify **180100**.

4.  In the **Offset account** field, specify **300160**.

For Acquisition adjustments, you can enter an offset account or leave it blank
to be filled in for the specific transaction.

1.  In the **Transaction type** field, select 'Depreciation'.

2.  Click **Add**.

3.  In the **Book** field, enter **SLLR**.

4.  In the **Main account** field, specify **180200**.

5.  In the **Offset account** field, specify **607200**.

6.  In the **Transaction type** field, select 'Depreciation adjustment'.

For Depreciation adjustment transactions, we will use the same accounts as used
for Depreciation transactions.

1.  Click **Add**.

2.  In the **Book** field, enter **SLLR**.

3.  In the **Main account** field, specify **180200**.

4.  In the **Offset account** field, specify **607200**.

5.  In the **Transaction type** field, select 'Disposal - sale'.

6.  Click **Add**.

7.  In the **Book** field, enter or select **SLLR**.

8.  In the **Main account** field, specify **801100**.

9.  In the **Offset account** field, specify **801100**.

For Disposals, you can enter an offset account or leave it blank to be filled in
for the specific transaction.

1.  In the **Transaction type** field, select 'Disposal - scrap', you will use
    the same accounts for Disposal sale and Disposal scrap.

2.  Click **Add**.

3.  In the **Book** field, enter or select **SLLR**.

4.  In the **Main account** field, specify **801100**.

5.  In the **Offset account** field, specify **801100**.

For Disposals, you can enter an offset account or leave it blank to be filled in
for the specific transaction.

1.  Expand the **Disposal** section. You must set up disposal posting profiles
    for both sale and scrap.

2.  We will start with disposal sale transactions. Click **Add**.

3.  In the **Book** field, enter or select **SLLR**.

4.  In the **Post value** field, select 'Acquisition value'.

Acquisition value will address Acquisition and Acquisition adjustment values for
all years. You can also define accounts for these transaction types separately.

You can set the disposal process to use different accounts depending upon if the
disposal results in a gain or loss. I will set the Sales value type to “All” to
use the same accounts for all types of disposals.

1.  In the **Main account** field, specify **180100**

2.  In the **Offset account** field, specify **180200**

3.  Click **Add**.  
    ‎

4.  In the **Book** field, enter or select **SLLR**.

5.  In the **Post value** field, select 'Depreciation (prior years)'.

6.  In the **Main account** field, specify **180100**.

7.  In the **Offset account** field, specify **180200**

8.  Click **Add**.

9.  In the **Book** field, enter or select a value.

10. In the **Post value** field, select 'Depreciation (this year)'.

11. In the **Main account** field, specify the desired values.

12. In the **Offset account** field, specify the desired values.

13. Click **Add**.

14. In the **Book field**, enter or select **SLLR**.

15. In the **Post value** field, select 'Depreciation adjustments (prior
    years)'.

16. In the **Main account** field, specify **180100**.

17. In the **Offset account** field, specify **180200**.

18. Click **Add**.

19. In the **Book** field, enter or select **SLLR**.

20. In the **Post value** field, select 'Depreciation adjustments (this year)'.

21. In the **Main account** field, specify **180100**...

22. In the **Offset account** field, specify **180200**.

23. Click **Add**.  
    ‎

24. In the **Book** field, enter or select a value.

25. In the **Post value** field, select 'Net book value'.

26. In the **Main account** field, specify **180100**.

27. In the **Offset account** field, specify **180200**.

28. In the **Sale** or **scrap** field, select 'Scrap'.

29. Click **Add**.  
    ‎

30. In the **Book** field, enter or **SLLR**.

31. In the **Post value** field, select 'Acquisition value'.

32. In the **Main account** field, specify **180100**...

33. In the **Offset account** field, specify **180200**.

34. Click **Add**.

35. In the **Book** field, enter or select **SLLR**.

36. In the **Post value** field, select 'Depreciation (prior years)'.

37. In the **Main account** field, specify **180100**...

38. In the **Offset account** field, specify **180200**.

39. Click **Add**.

40. In the **Book** field, enter or select **SLLR**.

41. In the **Post value** field, select 'Depreciation (this year)'.

42. In the **Main account** field, specify **180100**...

43. In the **Offset account** field, specify **180200**

44. Click **Add**.

45. In the **Book** field, enter or select **SLLR**.

46. In the **Post value** field, select 'Depreciation adjustments (prior
    years)'.

47. In the **Main account** field, specify **180100**...

48. In the **Offset account** field, specify **180200**.

49. Click **Add**.

50. In the **Book** field, enter or select **SLLR**.

51. In the **Post value** field, select 'Depreciation adjustments (this year)'.

52. In the **Main account** field, specify **180100**...

53. In the **Offset account** field, specify **180200**.

54. Click **Add**.

55. In the **Book** field, enter or select a **SLLR**.

56. In the **Post value** field, select 'Net book value'.

57. In the **Main account** field, specify **180100**...

58. In the **Offset account** field, specify **180200**.

Exercise - Create and acquire assets from Accounts payable
==========================================================

In this exercise you will set up fixed assets parameters and then create a new
vendor invoice

Set up fixed assets parameters
------------------------------

1.  Go to **Fixed assets \> Setup \> Fixed assets parameters**.

2.  Expand or collapse the **Purchase orders** section.

3.  Enable the **Allow asset acquisition from Purchasing** option.

4.  Enable the **Create asset during product receipt or invoice posting**
    option.

Create a new vendor invoice
---------------------------

1.  Go to **Accounts payable \> Workspaces \> Vendor invoice entry**.

2.  Click **New vendor invoice**.

3.  In the **Invoice account** field, click the drop-down button to open the
    lookup.

4.  In the list, click the link in the selected row.

5.  In the **Number** field, type a value.

6.  In the **Posting date** field, enter a date.

7.  Click **Add line**.

8.  In the **Item number** field, click the drop-down button to open the lookup.
    Either non-stocked items or procurement categories can be used for fixed
    asset acquisition.

9.  In the list, click the link in the selected row.

10. In the **Quantity** field, enter a number.

One invoice line will only create one fixed asset, regardless of quantity. The
invoice quantity field value will be transferred to the fixed asset quantity.

1.  In the **Unit price** field, enter a number.

2.  Expand or collapse the **Line details** section.

3.  Click the **Fixed assets** tab.

4.  Enable the **Create a new fixed asset** option.

5.  In the **Fixed asset group** field, click the drop-down button to open the
    lookup.

6.  In the list, select the fixed asset group to be used when creating the new
    fixed asset.

7.  In the list, click the link in the selected row.

8.  Click **Post**. The fixed asset will be created and acquired when the
    invoice is posted.

Exercise - Set up and create a depreciation profile
===================================================

Depreciation profiles determine the type and the frequency of depreciation for
an asset.

Acting as an accountant, perform the following tasks.

Create a depreciation profile
-----------------------------

1.  Go to **Fixed assets \> Setup \> Depreciation profiles**.

2.  Click **New**.

3.  In the **Depreciation** profile field, type a value.

4.  In the **Name** field, type a value.

5.  In the **Method** field, select an option. If selecting reducing balance,
    you will need to enter a percentage in the Percentage field.

6.  In the **Depreciation year** field, select an option.

7.  In the **Period frequency** field, select an option.

8.  Close the form.

Create a book
-------------

1.  Go to **Fixed assets \> Setup \> Books**.

2.  Click **New**.

3.  In the **Book** field, type a value.

4.  In the **Description** field, type a value.

If **Calculate depreciation** is selected, the associated asset book will be
included in depreciation proposals. If it is not selected, the asset book will
not be automatically depreciated.

1.  Select **Yes** in the **Calculate depreciation** field.

2.  In the **Depreciation** profile field, enter or select a value.

3.  Select **Yes** in the Create depreciation adjustments with basis adjustments
    field.

4.  By default, fixed asset book transactions will post to the general ledger.
    You can disable posting to the general ledger for the book by setting the
    Post to general ledger field to **No**.

5.  Books that do not post to the general ledger are typically used for tax
    reporting purposes. This gives you additional flexibility to delete
    historical transactions for the asset book because they have not been
    committed to the general ledger.

6.  The Posting layer defaults to the Current layer if the book posts to general
    ledger, and None if it does not post to general ledger. Update Posting layer
    if you need transactions for this book to be posted to a different layer.

7.  In the **Calendar** field, enter or select a value.

8.  Derived books will post transactions to different books at the same time.
    You create the transactions with the primary book and during posting, an
    exact copy of the transaction is posted to the derived book. There is no
    recalculation with derived book transactions, so it should not be used for
    depreciation transactions.

Associate the book with a fixed asset group
-------------------------------------------

1.  Click **Fixed asset groups**.

2.  In the **Fixed asset group** field, enter or select a value.

3.  In the **Service life** field, enter a number.

4.  Note that **Depreciation** periods is calculated after setting the Service
    life.

5.  You can set the depreciation convention as required for tax purposes.
