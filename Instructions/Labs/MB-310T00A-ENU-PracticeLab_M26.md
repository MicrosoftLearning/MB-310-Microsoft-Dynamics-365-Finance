Exercise: Perform a Consolidation
=================================

Sara, the Chief Financial Officer has asked Ken, the Controller, to consolidate
the activity for Contoso Entertainment USA (**USMF**) from 01/01/2012 through
12/31/2018 into the Contoso Entertainment Consolidation (**GLMF**) company. Sara
also has asked Ken to specifically review the balance of account 110110, Cash in
USMF-OPER., to verify the accuracy of the consolidation.

Select the **GLMF** company
---------------------------

1.  Go to **Consolidations \> Consolidate online**.

2.  In the **Description** type **GTL-Consolidation**

3.  Enter **110110** as the main account in the **From** and **To** fields.

4.  In the **From** period field, enter 01/01/2012.

5.  In the **To** period field, enter 12/31/2018.

6.  Click the **Currency translation** tab.

7.  Click the **New** button to add a new record.

8.  In the **Source legal entity** field, use the arrow to select **USMF**.

9.  In the **To** and **From** account fields, select account **110110**, **Bank
    Account - USD**

10. The **Exchange rate type** field. Is disabled since USMF and GLMF are using
    USD as their currency.

11. Select a row for DEMF

12. You note that you can change the exchange rate type with date criteria since
    DEMF uses EUR.

13. Click OK.

14. Navigate to **Consolidations\>Consolidation transactions** form.

15. Select the row for **USMF,** then click **Transactions\>Actuals**

16. Close all forms.

Exercise: Perform year end close
================================

The fiscal year 2014 is not closed in the Demo data company **USMF**.

Phyllis, the Accounting Manager at **USMF**, must create a closing sheet and
make the following adjustments:

-   2,500 U.S. dollars (USD) from account number 110130 to account number 110110

-   800 USD from account number 403150 to account number 110110

-   1,250 USD from account number 140750 to account number 110110

-   500 USD from account number 220270 to account number 110110

When the adjustments are finished, she must post the closing sheet and create
the opening balances for the next fiscal year.

Create and post a closing adjustment entry for 2007
---------------------------------------------------

1.  Navigate to **General ledger \> Period close \> Closing period
    adjustments**.

2.  In the **Closing sheet** field, enter **2014**.

3.  In the **Name** field, enter **2014 Closing Sheet**.

4.  In the **Posting layer** field, click the arrow, and then click **Current**.

5.  In the **Type** field, click the arrow, and then click **Closing**.

6.  Click the **General** tab.

7.  In the **From** field, type **1/1/2014.**

8.  In the **To** field, type **12/31/2014**.

9.  In the **Post** field, type **12/31/2014**.

10. Click **Save**.

11. Click the **Closing accounts** button.

12. Click the **Load balances** button.

13. Set the **Delete existing accounts** to **Yes**.

14. Click **OK**

15. Click Account number **110130**.

16. Click the **Transfers** button.

17. In the **Description** field, type **2014 close**.

18. In the **Offset account** field, click the arrow, and then click Account
    number **110110**.

19. In the Amount field, type **2500.**

20. Close the form.

21. In the quick filter type **403150**.and press enter.

22. Click the **Transfers** button.

23. In the **Description** field, type **2014 close**.

24. In the **Offset account** field, click the arrow, and then click Account
    number **110110**.

25. In the **Amount** field, type **800**.

26. Close the form.

27. In the quick filter type **140100** and press enter

28. Click the **Transfers** button.

29. In the **Description** field, type **2014 close**.

30. In the **Offset account** field, click the arrow, and then click Account
    number **110110**.

31. In the Amount field, type **1250**.

32. Close the form.

33. Click the **Post** button.

34. Close all the forms.

Follow these steps to perform year end close
--------------------------------------------

1.  Navigate to **General ledger \> Period close \> Year end close**

2.  Select **US companies**.

3.  Click **Run fiscal close** button, and then select **USMF**.

4.  Click **OK**.

5.  In the **Fiscal year,** select **2014**.

6.  In the Voucher field type **GTL-2014**

7.  Click **OK**.

8.  Close all the forms.
