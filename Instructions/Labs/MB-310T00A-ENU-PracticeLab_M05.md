Before you begin

To get the most out of this exercise, we recommend that you have the standard
sample data available in Finance and Operations that is installed using
Lifecycle services (LCS).

Exercise - Configure ledger and journal setup
=============================================

As a financial business user, this a daily procedure that you must perform. You
will create and validate journals to post transactions into the general ledger.
Then you will use built-in inquiries to find posted transactions, associated
vouchers, and drill down to find the original document. To save time you also
need to create a template so it can be reused in similar data entries.

Here are the tasks that you will perform:

-   Create and validate journals.

-   View journal entries or transactions.

-   Create a journal entry using a template.

Create and validate journals
----------------------------

1.  Go to **General ledger \> Journal entries \> General journals**.

2.  Click **New**.

3.  In the **Name** field, click the drop-down button to open the lookup.

4.  In the list, find and select the desired journal name **GenJrn**.

5.  Click **Lines**.

6.  In the **Account** field, enter an appropriate account based on the
    **Account type**. Use the drop down for assistance.

7.  In the **Description** field, type a value.

8.  Enter an amount for the **Account** in either **Debit** or **Credit**. For
    this lesson, use a debit amount.

9.  In the **Offset account** field, enter an appropriate account based on the
    **Offset account type**.

10. Click **Validate**.

11. Click **Validate**.

12. Click **Post**.

13. Click **Voucher**.

View journal entries or transactions
------------------------------------

To use the voucher transactions to search for journal entries or transactions,
follow these steps:

1.  Go to **General ledger \> Inquiries and reports \> Voucher transactions**.

2.  Select the field for which you want to define a filter criterion.

3.  Enter your filter criteria for the selected field.

4.  Click the **Joins** tab to add additional tables from which to filter.

5.  In the tree, select **'Tables\\General journal entry'**.

6.  Click **Add table join**.

7.  For the following step, make sure not to close the dialog box.

8.  Under the **Joins** tab, click **Cancel** if you decide not to add an
    additional table.

9.  Click the **Range** tab.

10. Click **OK** to run the query.

11. Click **Transaction origin**.

12. Close the page.

13. Click **Original document**.

14. Close the page.

Create a journal entry using a template
---------------------------------------

1.  Go to **General ledger\>Journal entries\>General journals**.

2.  Click **New**.

3.  In the **Name** field, click the drop-down button to open the lookup.

4.  In the list, find and select the desired daily journal name.

5.  Click **Lines**.

6.  Enter an account for the **Account type**.

7.  In the **Description** field, type a value.

8.  Enter an amount in the **Debit** field.

9.  Click **New**.

10. Enter a different account for the Account type.

11. In the **Description** field, type a value.

12. Enter an amount in the **Debit** field.

13. Click **New**.

14. In the **Account** field, specify the desired values.

15. In the **Description** field, type a value.

16. Enter an amount in the **Credit** field to balance the voucher.

17. Click **Post**.

18. Click **Functions**.

19. Click **Save voucher template**.

20. This procedure assumes a **Percent** template type.

21. Click **OK**.

22. Click **General journals**.

23. Click **New**.

24. In the **Name** field, click the drop-down button to open the lookup.

25. Click **Lines**.

26. Click **Functions**.

27. Click **Select voucher template**.

28. Find the template that you created earlier.

29. Click **OK**.

30. In the **Amount** field, enter the amount to be applied to the voucher. The
    amount field is only displayed if the voucher template is of type
    **Percent**.

31. Click **OK**.
