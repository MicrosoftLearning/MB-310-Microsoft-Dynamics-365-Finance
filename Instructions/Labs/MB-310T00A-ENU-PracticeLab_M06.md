### Before you begin

To get the most benefit from this and other exercises in this module, we
recommend that you have the standard sample data available in Finance and
Operations that is installed via Lifecycle Services.

Exercise 1 - Create bank transaction types and bank transaction groups
======================================================================

Annie, the bookkeeper at USMF, must create a bank transaction type for cash
withdrawals. USMF also wants the option to analyze the total charges paid to
each bank. Annie will create an additional bank transaction group for bank fees
and interest charges.

Follow the steps to help Annie.

1.  Create a bank transaction type for cash withdrawals.

2.  Create a bank transaction group for bank charges.

3.  Define cash and bank parameters

Create a bank transaction type for cash withdrawals
---------------------------------------------------

1.  Go to **Cash and bank management**, expand **Setup**, and then click **Bank
    transaction types**.

2.  Click the **New** button to insert a new record.

3.  In the **Bank transaction type** field, enter **20**.

4.  Enter the name **Cash Withdrawal** in the **Name** field.

5.  Type **110110** in the **Main account** field.

6.  Close the **Bank transaction type** page.

Create a bank transaction group for bank charges.
-------------------------------------------------

1.  Go to **Cash and bank management**, expand **Setup**, and then click **Bank
    transaction groups**.

2.  Click the **New** button to insert a new record.

3.  In the **Bank transaction groups** field, enter **80**.

4.  Enter **Bank Charges** in the **Description** field.

5.  From the **Bank transaction groups** page, click the **Type** FastTab.

6.  Click the **Bank transaction type** arrow and select the bank transaction
    type of **07** for **Fees**.

7.  Verify that the **Name** field is automatically populated with the **Bank
    transaction type** name.

8.  Click the **Add** button to insert a new record.

9.  Click the **Bank transaction type** arrow and select the bank transaction
    type of **08** for **Interest charges**.

10. The **Name** field is automatically populated with the **Bank transaction
    type** name.

11. Close the page.

Define cash and bank parameters
-------------------------------

1.  Go to **Cash and bank management**, expand **Setup**, and then click **Cash
    and bank management parameters**.

2.  Click the **General** link if is not automatically selected.

3.  Select the **Bank transaction type** that is used for **Non-Sufficient
    Funds** (NSF) from the **NSF** list.

4.  Select the **Allow checks for bank or ledger accounts** check box to
    indicate whether a check can be printed for a bank or ledger account.

5.  Select the **Allow check reuse** check box to indicate whether a check
    number can be reused if the check was printed incorrectly or the check stock
    was not used.

6.  To require reason codes for bank transactions, select one or more of the
    check boxes in the **Reason code requirements** for **Require reasons for
    payment reversals** and **Require reasons for deposit slip payment
    cancellations**.

Exercise 2 - Create a direct debit mandate for a customer, and define the electronic payment method
===================================================================================================

In this exercise you will:

1.  Create a direct debit mandate for a customer.

2.  Define the electronic payment method.

3.  Add a direct debit mandate to a customer.

Create a direct debit mandate for a customer
--------------------------------------------

1.  In company **USMF**, go to **Accounts receivable \> Customers \> All
    customers**.

2.  Select **US-001**.

3.  On the Action Pane, click **Customer**.

4.  Click **Bank accounts**.

5.  Click **New**.

6.  In the **Bank account** field, type a value.

7.  In the **Name** field, type a value.

8.  In the **IBAN** field, type a value.

9.  In the **Currency** field, type a value.

10. Click **Save**.

11. Close the page.

12. Go to **Cash and bank management \> Bank accounts \> Bank accounts**.

13. In the list, find and select **USMF OPER**.

14. Click **Edit**.

15. Expand the **Additional identification** section.

16. In the **Direct debit ID** field, type a value.

17. In the **IBAN** field, type a value.

18. Close the page.

Define the electronic payment method
------------------------------------

1.  Go to **Accounts receivable \> Payments setup \> Methods of payment**.

2.  Click **New**.

3.  In the **Method of payment** field, type a value.

4.  In the **Description** field, type a value.

5.  The payment type for a direct debit mandate method of payment must be
    **Electronic payment**.

6.  Select **Yes** in the **Require mandate** field.

7.  Close the page.

Add a direct debit mandate to a customer
----------------------------------------

1.  Go to **Accounts receivable \> Customers \> All customers**.

2.  Select **US-001**.

3.  Click **Edit**.

4.  Expand the **Payment defaults** section.

5.  In the **Method of payment** field, enter or select a value.

6.  the **Payment defaults** section.

7.  Expand the **Direct debit mandates** section.

8.  Click **Add**.

9.  In the **Bank account** field, select **USMF OPER**.

10. In the **Creditor bank account** field, enter or select a value.

11. Enter the number of payments that you expect to process for this mandate.

12. Click **OK**.

13. Click **Print**.

14. Click **Mandate report**.

15. Close the page.

16. Click **Edit**.

17. In the **Signature date** field, enter a date.

18. Click **Yes**.

19. Enter the location where the mandate was signed.

20. Click **OK**.

21. Close the page.
