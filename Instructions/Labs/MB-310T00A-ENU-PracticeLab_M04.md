### Before you begin

To get the most out of this exercise and the other exercises that are included
with this module, we recommend that you have the standard sample data available
in Finance and Operations that is installed using Lifecycle services (LCS).

Exercise 1 - Create a main account category in the chart of accounts
====================================================================

Consider the following scenario:

Phyllis, the Accounting manager, wants to include the Current ratio on the
Short-term solvency KPI report. Current ratio is calculated by dividing a
company’s current assets by current liabilities. Current assets typically
consist of cash, cash equivalents, accounts receivable, inventory, and
marketable securities. Current liabilities consist of any liabilities that are
payable within one year.

To derive the current asset value, Phyllis must sum the values of the Cash,
Accounts receivable, and Inventory accounts. Fixed assets are not considered
current assets. To perform this calculation, Phyllis uses the **Main account
category** field. Main accounts that are added to the chart of accounts later
will also use the Main account category to be included in existing calculations.

Perform the following steps to create a General ledger Main account category:

1.  To access the **Main account categories** page, go to **General Ledger \>
    Chart of accounts \>-Accounts-\> Main account categories**.

2.  Click the **New** button to create a new record.

3.  Enter a unique name **Learning** for the **Main account category** and a
    **Description**.

4.  Select a **Main account type** to associate with the account category.  
    ‎The purpose of selecting a **Main account** type is to reduce the lookup of
    available **Main account categorie**s when you create a new Main account
    from the **Chart of accounts** page.

5.  To link an account category to a main account, click the **Link main
    accounts** button. Or, link a **Main account category** to an account from
    the **Main account details** page.

Exercise 2 - Create advanced rule structures
============================================

Consider the following scenario:

Phyllis, the Accounting manager, is setting up the charts of accounts for
Contoso Enterprise. For some of the accounts, the organization wants to track
additional information that is not captured in the account structures. She needs
to ensure that for the financial dimension customer group “80: Other customers"
only certain departments can be used.

Perform the following steps to create an advanced rule:

1.  Go to **General ledger \> Chart of accounts \> Structures \> Advanced rule
    structures**.

2.  Click **New** to create a new record.

3.  Enter a unique identifier for the Advanced rule structure, enter a brief
    description, and then click **OK**.

4.  Click **Add segment** to add a financial dimension to the structure.

5.  Select a financial dimension from the list and then click **Add segment**.

6.  In the Allowed value details fast tab, set the **Where** to be the segment
    you chose.

7.  For **Operator**, choose **begins with**.

8.  For **Value**, choose **8**. These define which values for the financial
    dimension are applicable for the selected rule.

9.  Optionally, select the **Blank values are allowed** check box to allow blank
    values for the segment in the advanced rule that you are defining.

10. Click **Add segment** to add another financial dimension to the structure.

11. Select the next desired financial dimension from the list and then click
    **Add segment**.

12. Filter this segment like the last one.

13. Close the page.

14. Click **Activate.**

15. Click **Activate** to save the changes and make them effective in the
    ledger.
