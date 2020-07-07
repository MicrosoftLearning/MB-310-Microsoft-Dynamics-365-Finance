Exercise 1 - Record an invoice
==============================

The following steps show you how to use the invoice register to record invoices
and then use the approval journal to update the expense accounts.

Create and post and invoice
---------------------------

1.  In **USMF**, go to **Accounts payable \> Invoices \> Invoice register**.

2.  Click **New**.

3.  Select the name of the invoice register that you want to use.

4.  Click on **Lines** to open the register and enter expense lines.

5.  Select a vendor. For example, enter or select **US-104**.

6.  In the **Invoice** field, type a value.

7.  In the **Description** field, type a value.

8.  In the **Credit** field, enter a number.

9.  In the **Approved by** field, click the drop-down button to open the lookup.

10. Highlight an approver and click **Select** to select that approver.

11. Click **Post**.

12. Close all pages.

Approve an invoice
------------------

1.  Go to **Accounts payable \> Invoices \> Invoice approval**.

2.  Click **New**.

3.  Select the name of the invoice approval journal that you want to use.

4.  Click **Lines** to display a page where you will be able to select the
    invoices that you want to approve.

5.  Select **Find Vouchers** to display all the invoices that are ready for
    approval.

6.  Select the invoice that you created.

7.  Click **Select**. The vouchers that you selected above are moved to this
    list after you select them.

8.  Click **OK**.

9.  Click on the **Account number** field to add an expense account to the
    invoice.

10. Enter an account number and tab off the field. For example, enter 600120.

11. Click **Post**.

12. Click **Voucher** to view the entries that were posted. The Invoice pending
    approval account is reversed and replaced with the actual expense account.

Exercise 2 - Record a vendor invoice that is not associated with a purchase order
=================================================================================

This exercise explores recording vendor invoices that are not associated with
purchase orders. Examples of this type of invoice include expenses for supplies
or services.

This exercise uses the USMF demo company.

1.  Go to **Accounts payable \> Workspaces \> Vendor invoice entry**.

2.  Click **New invoice journal**.

3.  Click **New**.

4.  In the **Name** field, enter the journal name or click the drop-down button
    to open the lookup.

5.  In the **Description** field, type a value.

6.  Click **Lines**.

7.  In the **Date** field, enter the posting date that will update General
    ledger.

8.  In the **Account** field, specify the **Vendor account.**

9.  In the **Invoice** field, enter the invoice number.

10. In the **Description** field, type a value.

11. In the **Credit** field, enter a number.

12. In the **Offset account** field, select an expense account number. The Sales
    tax group will default from the vendor account, and the Item sales tax group
    will default from the main account specified in the **Offset account**
    field. Additionally, the due date will be calculated based on the terms of
    payment, and the cash discount will default from the vendor account.

13. Click **Post**.

14. Close the page.

Exercise 3 - Process a vendor payment by using a payment journal
================================================================

This exercise will walk you through various methods used to create vendor
payments, including how to use a payment proposal or manually entering a one-off
payment.

This exercise uses the USMF demo company.

1.  Go to **Accounts payable \> Payments \> Payment journal**.

2.  Click **New**.

3.  Select the payment journal in which to save the vendor payments.

4.  Select the journal or manually enter it.

5.  Click **Lines**.

6.  Click **Payment proposal**.

7.  Click **Create payment proposal**.

8.  Select invoices for payment by due date, cash discount, or both.

9.  Enter the date for comparing to the due date or cash discount.

10. Optional: Enter a payment date used for all payments. (The date entered here
    will be the payment date for all payments created, regardless of the due
    date or cash discount date.)

11. Optional: Enter a **minimum payment date** which can be used as the payment
    date. (The **minimum payment date** will be the earliest date used when
    creating payments. For example, if an invoice has a due date after the
    minimum payment date, the due date will become the payment date instead of
    the minimum payment date to pay the invoice on the latest possible date.)

12. Enter additional query restrictions under **Records to include**. (The
    filter is often used to restrict the invoices selected for payment by vendor
    group or method of payment. For example, you can add a filter to only pay
    invoices by check in this pay run.)

13. Enter additional query restriction or payment defaults. (The additional
    parameters can be used to define the payment currency or to enable
    centralized payments for this pay run.)

14. Click **OK**. (After clicking **OK**, the results of the query will appear.
    If you don't want to preview the list of invoices selected to pay, you can
    go back to the **Parameters** tab and change **Create payments without
    invoice preview** to **Yes**.

15. Choose the **Show payment overview** button to view the payments that will
    be created for the vendor on the invoice selected.

16. Choose the **Hide payment overview** button to hide the payments.

17. Click **Create payments**. (Before choosing **Create payments**, you can
    right click on the grid and export the list of invoices to Excel. The
    **Create payments** button will create the vendor payments in the payment
    journal.)

18. Scan your payments and make sure the method of payment is defined for all
    payments. (If you generate the payments, such as printing a check or
    creating an electronic payment, the method of payment must be defined. The
    method of payment will also default to the bank account from where the
    payment will be made.)

19. Click **New** to create a one-off payment. (A one-off payment can be added
    to a payment journal at any time prior to posting. This is done by clicking
    the **New** button and adding the payment information manually, rather than
    using the Payment proposal.)

20. Select the vendor to whom the payment will be made.

21. If an invoice exists to pay, select **Settle transactions** to select the
    invoice for payment. (If this is a prepayment, this step is optional. You
    can create the payment without selecting an invoice.)

22. Mark any invoices that will be paid. (If you use **Settle transactions** to
    select the invoices for payment, the payment amount will automatically be
    calculated based on what invoices you mark for payment and what amount you
    enter in the **Amount to settle**.)

23. Click **OK**.

24. If you want to delete a payment, mark the row.

25. Click **Delete**. (Deleting a payment will only delete the payment. Any
    invoices marked for payment will still be available to be paid by another
    payment.)

26. Click **Yes**.

27. Choose **Generate payment** to print checks or create the electronic payment
    file.

28. Select the method of payment that you want to generate. (The payment journal
    can contain payments for both checks and electronic payments, but you can
    only generate one payment type at a time.)

29. Select the bank account from which to generate the payments.

30. Click **OK**. (Payments will only be generated for payments that match the
    method of payment and bank account you selected.)

31. If you are generating checks, select **Document** to ensure the correct
    print destination for the checks.

32. Click **OK**.

33. Click **OK** to generate the payments.

34. Click **Post** if all the payments are approved and generated.
