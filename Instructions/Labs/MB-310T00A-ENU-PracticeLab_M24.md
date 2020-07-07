### Before you begin

To get the most out of this exercise and the other exercises that are included
with this module, we recommend that you have the standard sample data available
in Finance and Operations that is installed using Lifecycle services (LCS).

Exercise - Acquire an asset using the Fixed assets Journal
==========================================================

April is the Accounts payable coordinator at the USMF Company. The company has
just purchased a new gas boiler for 10,000 United States dollars (USD). April's
task is to register the acquisition by using the **Fixed assets** journal.

To create the new fixed asset, follow these steps:
--------------------------------------------------

1.  Go to **Fixed assets**\>**Fixed assets**\> **Fixed assets**.

2.  Click the **Fixed asset** button to create a new asset.

3.  In the **Fixed asset group** field, select ‘MACH’.

4.  In the **Fixed asset number** field, the system defaults this number.

5.  Note this number for the journal entry.

6.  In the **Name** field, enter ‘Gas boiler \#2’.

7.  In the **Search name** field, enter ‘Boiler 2’.

8.  Click the **Books** button. Note all the Books associated with the asset and
    the **Status** is **Not yet acquired**.

9.  Close all pages.

To record the acquisition, follow these steps:
----------------------------------------------

1.  Go to **Fixed assets**\> **Journal entries\>Fixed assets journal.**

2.  Click the **New** button to create a journal

3.  In the **Name** field, select ‘FACur’ (Fixed Asset Entries - Current).

4.  Click the **Lines** button.

5.  In the **Transaction type** field, select ‘Acquisition’.

6.  In the **Account** field, select the asset previously created which is ‘Gas
    boiler \#2’.

7.  The **Book** will default based on the set up of the asset selected in the
    **Account** field. In this case it would be ‘CONSUM’.

8.  In the **Description** field, select ‘acquisition’.

9.  In the **Debit** field, enter ‘10,000.00’. The **Offset account type** and
    **Offset account** will default based on the Posting profile for the Book.

10. Click the **Post** button, and then click **Post**.

11. Close all the pages.

12. Go to **Fixed assets\>Fixed assets\> Fixed assets**.

13. Select ‘Gas boiler \#2’.

14. Click the **Books** button. Note that the **Status** is now set to **Open**.

15. Click **Transactions** and verify the amount of voucher.

16. Close all pages.

Exercise - Depreciate and dispose of a fixed asset
==================================================

Cassie is the Accountant at the Contoso company. It is the end of the month, and
Cassie must create a proposal to depreciate all the assets in the Fixed asset
group MACH. After she creates the proposal, Cassie's manager reviews it, and
then Cassie posts the proposal.

To record the depreciation, follow these steps.
-----------------------------------------------

1.  Go to **Fixed assets**\> **Journal entries\>Fixed assets journal.**

2.  Click the **New** button to create a journal

3.  In the **Name** field, select ‘FACur’ (Fixed Asset Entries - Current).

4.  Click the **Lines** button.

5.  In the **Transaction type** field, select ‘Depreciation’.

6.  In the **Account** field, select the asset **Gas boiler \#2**.

7.  The **Book** will default based on the set up of the asset selected in the
    **Account** field. In this case it would be ‘CONSUM’.

8.  In the **Description** field, select ‘Depreciation’.

9.  In the **Credit** field, enter ‘600.00’. The **Offset account type** and
    **Offset account** will default based on the Posting profile for the Book.

10. Click the **General** tab.

11. In the **Consumption units** field enter ‘2’.

12. Click the **Post** button, and then click **Post**.

13. Close all the pages.

14. Go to **Fixed assets\>Fixed assets\> Fixed assets**.

15. Select ‘Gas boiler \#2’.

16. Click **Transactions** and verify the amount of voucher for the
    depreciation.

17. Close all pages.

To dispose of an asset, follow these steps.
-------------------------------------------

1.  Go to **Fixed assets**\> **Journal entries\>Fixed assets journal.**

2.  Click the **New** button to create a journal

3.  In the **Name** field, select ‘FACur’ (Fixed Asset Entries - Current).

4.  Click the **Lines** button.

5.  In the **Date** field, enter a date 1 day from the date of your last
    acquisition date.

6.  In the **Transaction type** field, select ‘Disposal – sale’.

7.  In the **Account** field, select the asset ‘Gas boiler \#2’.

8.  The **Book** field will default based on the set up of the asset selected in
    the **Account** field. In this case it would be ‘CONSUM’.

9.  In the **Description** field, type ‘Disposal’.

10. In the **Debit** field, enter ‘9000.00’. The **Offset account type** and
    **Offset account** will default based on the Posting profile for the book.

11. Click the **Post** button, and then click **Post**.

12. Close all the pages.

13. Go to **Fixed assets\>Fixed assets\> Fixed assets**.

14. Select ‘Gas boiler \#2’.

15. Click the **Books** button. Note that the **Status** is now set to **Sold**.

16. Click **Transactions** and review the amounts of each voucher.

17. Close all pages.
