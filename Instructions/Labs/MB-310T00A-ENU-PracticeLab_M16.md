**Before you begin**

To get the most out of this exercise and the other exercises that are included
with this module, we recommend that you have the standard sample data available
in Finance and Operations that is installed using Lifecycle services (LCS).

Exercise - Configure customer posting profiles
==============================================

Phyllis, the Accounting Manager at Contoso, has asked Arnie, the Accounts
receivable Clerk, to set up a new posting profile for a group of retail
customers.

Select the appropriate options to ensure the following:

-   Entries will be created using this profile for automatic settlement.

-   The application will calculate interest on outstanding balances for
    customers who have this profile.

-   A collection letter may be issued for customers who have this profile.

-   When transactions are settled in full, the transactions should not change to
    another posting profile.

-   Transactions for the retail customers group will post to the summary account
    130100 and settle account 110110.

Set up a customer posting profile
---------------------------------

1.  In the **USMF** company, Go to **Accounts receivable\>Setup\>Customer
    posting profiles**.

2.  Click **New**.

3.  In the **Posting Profile** field, type **Prom**.

4.  In the **Description** field, type **Promotion**.

5.  On the **Table restrictions** tab, make sure that the following options is
    set the **Allow automatic settlement** to **Yes.**

6.  Set the **Interest** and **Collection letter** options to **Yes**.

7.  Verify that the **Close** field is blank.

8.  In the **Account code** field, select **group**.

9.  In the **Account\\Group Number** field, select **30 Retail Customers**.

10. In the **Summary account** field, select **130100**.

11. In the **Settle account** field, select **110110**.

12. In the **Collection letter sequence** field, select **High**.

13. Close the page.

Establish customer payment terms
--------------------------------

1.  In **USMF**, go to **Accounts receivable \> Payments setup \> Payment
    days**.

2.  Click **New**.

3.  In the **Payment day** field, enter **17**.

4.  In the **Description** field, enter **17th of the month**.

5.  In the **Week/Month** field, select **Month**.

6.  In the **Day of month** field, enter **17**.

7.  Click **Save**.

8.  Close the page.

9.  Navigate to **Accounts receivable \> Payments setup \> Terms of payment**.

10. Click **New**. Terms of payment is used to define how the due dates will be
    calculated. The cash discount date setup is defined in a separate page.

11. In the **Terms of payment** field, enter **GTL-45**.

12. In the **Description** field, enter **Net 45 days**.

13. Select a Payment method **Current month**. The Payment method is used to
    define the start of how the due will be calculated. For example, **Net** is
    used if the due date is always a set number of months or days after the
    invoice date. **COD** can be used to when payment is required upon invoice,
    so a due date wouldn't be calculated.

14. Select a **Payment day** field value to be **17**. Depending on your terms
    of payment, you may enter a quantity in Months or Days. Or you can use the
    Payment schedule or Payment day to 'add' to the end of the Payment method.
    If the due date will always be the 17th of the next month, select a Payment
    day of the 17th.

15. Click **Save**.

16. Close the page.

17. Navigate to **Accounts receivable \> Payments setup \> Cash discounts**.

18. Click **New**.

19. In the **Cash discount** field, enter **GTL-15D5%**.

20. In the **Description** field, enter **Offer 5% if paid with 15 days**.

21. Enter the number of days used to calculate the cash discount date. Enter
    **15**. If Net principle is selected, the number of days will be added to
    the invoice date to calculate the cash discount date.

22. Enter the **percentage** of the cash discount. Enter **5**.

23. Enter the main account to which the cash discount will post for customer
    invoices. Select **403300**

24. In the **Discount offset accounts** field, select an option. If you select
    'Accounts on the invoice lines', the cash discount will post to the same
    asset/expense main account on the lines of the Customer invoice. If you
    select **'Use main account for Customer invoices'**, the cash discount will
    post to the main account you define in the **Main account for Customer
    invoices**. For this example, select **'Use main account for Customer
    invoices**.'

25. Enter the main account to which the cash discount will post for Customer
    invoices. Select **212160**

26. Click **Save**.

Create a method of payment for customer payments.
-------------------------------------------------

1.  In **USMF**, Go to **Accounts receivable \> Payments setup \> Methods of
    payment**.

2.  Click **New**.

3.  In the **Method of payment** field, enter **GTL-EP**. The Method of payment
    ID is shown on invoices and payments, so make it descriptive enough to
    understand what type of payment is being recorded, and for what bank
    account.

4.  In the **Description** field, enter **Electronic payments**.

5.  Select what payment status is required for payments to be posted. Select
    **Approved**. When creating a customer payment, it can only be posted when
    the payment status matches the payment status you define here.

6.  Select how customers payments should be created for invoices. Select
    **Total**. This option is only used when running a payment proposal. A
    payment proposal could be used for customer payments when doing direct
    debits and pulling the funds from the customers' bank accounts.

7.  Select the type of payment as **Electronic payment**. The payment type will
    help determine whether some validation will occur or not on the payment.

8.  Select what account type payments will post to. Select **Bank.**

9.  Select the bank account into which this payment will be recorded. Choose
    **USMF OPER**.

10. Enter the **Bank transaction type** to identify the type of payment used by
    your bank. Select **Deposit**. The bank transaction type is used during the
    bank reconciliation process and can make reconciliation easier.

11. Select this payment will temporarily post to a bridging account. Set the
    bridging posting to **Yes**. If you want to try the float time for a payment
    to clear the bank, use the Bridging functionality. The payment will
    temporarily post to a Ledger account until it clears the bank, at which time
    the payment will move to the bank account you defined here.

12. Enter the main account used for the bridging posting. Select **130730.**
    This is the main account to which the payment will temporarily post if using
    bridging.

13. Use the **File format** tab to define setting for electronic payments.

14. Use the **Payment control** tab to define fields that are mandatory. For
    example, if you require all payments with this method of payment to be
    deposited, you can choose that option on this tab.

15. Use the **Payment attributes** tab to define which payment attributes you
    want to use for this method of payment.

16. Click **Save**.

Create payment fees for customer payments.
------------------------------------------

1.  In **USMF**, Go to **Accounts receivable \> Payments setup \> Payment fee**.

2.  Click **New**.

3.  In the **Fee ID** field, enter **W01**. The **Fee ID** displays on payment
    journals, so make it descriptive to understand what fee is being assessed.

4.  In the **Name** field, enter **Wire**.

5.  In the **Fee description** field, enter **Bank fee for wire transfer**.

6.  Select whether the fee will be charged to the **Customer** or a **Ledger
    account**.

7.  If the customer is assessed the fee, select **Customer**. If the fee will be
    charged to your organization as an expense, select **Ledger**. For this
    task, select **Customer**.

8.  Select the type of journal that can use this payment fee. If these fees are
    used for customer payments, the journal type will likely be **Customer
    payment**.

9.  Click **Save**.

10. Click **Payment fee setup**. The Payment fee setup is used to define the
    criteria for when the payment fee will be assessed. For example, you can
    define that the fee will be calculated if the bank account is **USMF OPER**,
    and the method of payment is **check**.

11. Select either **Table**, **Group** or **All** to define which bank accounts
    will be assessed this fee. If you select **All**, all bank accounts could be
    assessed this fee. If you select **Table**, only the bank account you select
    could be assessed this fee. If you select **Group**, only the bank accounts
    in the selected bank group could be assessed this fee.

12. Select either a **bank group** or a **bank account**. If you selected
    **Table**, the lookup will display bank accounts. If you selected **Group**,
    the lookup will display **bank groups**.

13. Select the **Method of payment** for which this fee will be assessed. For
    example, you may assess a fee to your customers if they send payments as a
    check, rather than as an **electronic payment**.

14. Enter a **payment currency**. The payment currency is used as an additional
    criterion for whether the fee will be assessed. For example, your bank may
    charge an extra fee for payments received in **USD** currency, since they
    normally only transact in **EUR** currency.

15. Select whether the fee will be a **percent**, **amount** or **interval**.
    Enter either **percentage** or **amount** of the fee. If the
    **Percentage/Amount** field is **Percent**, then the value enter here will
    be a percentage. If the **Percentage/Amount** field is **Amount**, then the
    value you enter here will be an amount. If the **Percentage/Amount** field
    is **Interval**, use the **Interval** tab to define the tiers.

16. In the **Fee currency** field, select the currency of the fee. This is the
    currency in which the fee will be created.

17. Click **Save**.

‎

Exercise - Create a new customer
================================

The USMF company has started to work with a new customer, Pelican Inc. Arnie,
the Accounts Receivable Clerk, must set up this new customer.

1.  Go to **Accounts receivable\>Customers\>All customers**.

2.  Click **New**

3.  In the **Customer account** field, enter **US-069**

4.  In the **Type** field, select **Organization**.

5.  In the **Name** field, type **Pelican Inc**.

6.  In the **Customer group** field, select customer group **20**.

7.  Click **Save**.

8.  Click the **Credit and collections** FastTab.

9.  In the **Credit limit** field, enter **10000**.

10. Click the **Invoice and delivery** FastTab.

11. In the **Mode of delivery** field, select **20, Air**.

12. In the **Sales tax group** field, select **CA**.

13. Click the **Payment defaults** FastTab.

14. In the **Terms of payment** field, select **Net10**.

15. In the **Method of payment** field, select **CHECK**.

16. Close the page.
