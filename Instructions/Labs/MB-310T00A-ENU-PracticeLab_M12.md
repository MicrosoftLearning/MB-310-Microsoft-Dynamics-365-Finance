**Before you begin**

To get the most benefit from this and other exercises in this module, we
recommend that you have the standard sample data available in Finance and
Operations that is installed via Lifecycle Services.

Exercise 1 - Set up ledger posting groups for sales tax
=======================================================

In this exercise, you will set up ledger posting groups for sales tax.

Use the company DEMF for all exercises in this module.

1.  Go to **Tax \> Setup \> Sales tax \> Ledger posting groups**.

2.  Select **New**.

3.  In the **Ledger posting group** field, type a value.

4.  In the **Description** field, type a value.

5.  In the **Sales tax payable** field, select the main account for outgoing
    sales taxes that are payable to the tax authority.

6.  In the **Sales tax receivable** field, select the main account for incoming
    taxes that are received from the tax authority.

7.  In the **Use tax expense** field, select the main account for posting
    deductible use taxes that are not claimed or reported to the tax authority
    by vendors as part of EU reverse charge VAT.

8.  In the **Use tax payable** field, select the main account for posting
    incoming use taxes that are payable to tax authorities.

9.  In the **Settlement account** field, select the main account that the net
    balance of the ledger accounts specified in the **Use tax payable** and
    **Sales tax receivable** fields will be posted.

10. In the **Vendor cash discount** field, select the main account to post cash
    discounts for sales tax codes associated with this ledger posting group.

11. In the **Customer cash discount** field, select the main account to post
    cash discounts for sales tax codes associated with this ledger posting
    group.

12. Select **Save**.

Exercise 2 - Set up sales tax authorities
=========================================

In this exercise, you will set up sales tax authorities.

1.  Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax authorities**.

2.  Select **New**.

3.  In the **Authority** field, type a value.

4.  In the **Name** field, type a value.

5.  In the **Vendor account** field, click the drop-down button to open the
    lookup.

6.  In the list, find and select the desired record.

7.  Select the report layout for your country or region, if one is available. If
    the report layouts do not correspond to the requirements of the sales tax
    authority, use **Default layout**.

8.  Enter values in the **Rounding** page and the **Round-off** fields to
    specify how the tax total amount to be paid should be rounded. Any rounding
    differences will be posted to **Accounts for automatic transactions** that
    is set up in **General ledger**.

9.  In the **Round-off** field, enter a number.

10. Select **Save**.

Exercise 3 - Set up sales tax settlement periods
================================================

In this exercise, you will set up sales tax settlement periods.

1.  Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax settlement
    periods**.

2.  Select **New**.

3.  In the **Settlement period** field, type a value.

4.  In the **Description** field, type a value.

5.  In the **Authority** field, select the sales tax authority that receives the
    reports and the payments that are created for the settlement period.

6.  In the list, find and select the desired record.

7.  In the **Terms of payment** field, click the drop-down button to open the
    lookup. In the list, find and select the desired record.

8.  In the list, click the link in the selected row.

9.  Select a type for the settlement period intervals.

10. Enter the number of Period interval units per period. For example, a quarter
    has 3 months.

11. Select or clear the **Use batch processing for sales tax settlement** check
    box.

    -   The settlement process for the settlement period can be processed as a
        batch job in the background. This is recommended for many tax
        transactions within a period interval.

12. Enable or disable the **Prevent generating offset tax transactions** check
    box.

    -   By default, the system generates offset tax transactions during the
        settlement process, which can cause performance issues if many tax
        transactions exist within a period interval. Select this check box to
        prevent generating offset tax transactions.

13. Expand the **Period intervals** tab.

14. Select **Add**.

15. In the **From date** field, enter a date.

16. In the **To date** field, enter a date.

17. Select **New period interval**. When the first period interval has been
    entered, new periods can be created automatically. You can return later and
    add new period intervals, as required.

18. Close the page.

Exercise 4 - Set up sales tax codes and sales tax groups
========================================================

In this exercise, you will set up sales tax codes and sales tax groups.

Set up sales tax codes
----------------------

Sales tax codes are created for every indirect tax or duty that the legal entity
is obligated to calculate, collect, and pay to sales tax authorities.

1.  Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.

2.  Select **New**.

3.  In the **Sales tax code** field, type a value.

4.  In the **Name** field, type a value.

5.  Select a **Settlement period** to specify which **Sales tax authority** and
    in which intervals this sales tax needs to be reported and paid.

6.  Select a **Ledger posting group** to specify the main accounts to post sales
    tax to the general ledger.

7.  In the list, find and select the desired record.

8.  Expand the **Calculation** FastTab. Verify the fields that control how sales
    tax amounts will be calculated.

9.  On the Action Pane, select **Sales tax code**.

10. Select **Values**.

11. Enter the value for this tax code.

12. Select **Save**.

13. Close the page.

14. Select **Save**.

Set up sales tax groups and item sales tax groups
-------------------------------------------------

1.  Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax groups**.

2.  Select **New**.

3.  In the **Sales tax group** field, type a value.

4.  In the **Description** field, type a value.

5.  Toggle the expansion of the **Setup** section.

6.  Select **Add**.

7.  In the **Sales tax code** field, click the drop-down button to open the
    lookup.

8.  Select **Save**.

9.  Close the page.

10. Go to **Tax \> Indirect taxes \> Sales tax \> Item sales tax groups**.

11. Select **New**.

12. In the **Item sales tax group** field, type a value.

13. In the **Description** field, type a value.

14. Select **Add**.

15. In the **Sales tax code** field, click the drop-down button to open the
    lookup.

16. Select **Save**.

Exercise 5 – Set up sales tax reporting codes and withholding tax
=================================================================

In this exercise, you will set up sales tax reporting codes and withholding tax.

Set up sales tax reporting codes
--------------------------------

1.  Go to **Tax \> Setup \> Sales tax \> Sales tax reporting codes**.

2.  Select **New**.

3.  Select the report layout that the reporting code belongs to.

4.  Enter a number that refers to a field on a sales tax report.

5.  In the **Report text** field, enter a description to display on reports.

6.  In the **Brief description** field, enter a description for internal
    purposes.

7.  Select **Save**.

Set up withholding tax
----------------------

1.  Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax codes**.

2.  Select **New**.

3.  In the **Withholding tax code** field, type a value.

4.  In the **Withholding tax name** field, enter the name of the withholding tax
    code.

5.  In the **Main account** field, select the main account for posting the
    withholding tax liability.

6.  Select **Save**.

7.  Select **Values**.

8.  In the **Values** field, enter a percentage used for the calculation of the
    withholding tax.

9.  Select **Save**.

10. Close the page.

11. Select **Save**.

12. Close the page.

13. Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax
    groups**.

14. Select **New**.

15. In the **Withholding tax group** field, enter the identifier of the
    withholding tax group.

16. In the **Description** field, enter the name of the withholding tax group.

17. In the **Withholding tax code** field, select the withholding tax code.

18. Select **Save**.

Exercise 6 - View posted sales tax transactions
===============================================

You can view posted sales tax transactions from various pages depending on what
you need to view.

The following exercise is an example for how to accomplish this task.

1.  Go to **Tax \> Inquiries and reports \> Sales tax inquiries \> Posted sales
    tax**.

2.  Select **Show filters**.

3.  Close the page.

4.  Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax settlement
    periods**.

5.  Expand the **Period intervals** section.

6.  Select the interval you are interested in.

7.  Display posted sales tax transactions for the selected settlement period
    interval.

8.  You can further filter the list of posted sales tax transactions.

9.  Close the page.

10. Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.

11. On the Action Pane, select **Sales tax codes**.

12. Select **Posted sales tax**.

‎
