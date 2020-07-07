Exercise: Perform Write-Offs
============================

Write off a customer balance from the aged balances page
--------------------------------------------------------

As a collection agent in **USMF**, you need to create a write off journal, since
the Birch company is not going to pay the balance due to defect on the products
that were shipped to them.

1.  Go to **Credit and collections \> Collections \> Aged balances**.

2.  Mark the row for the customer that you want to write off. For example, mark
    the line with **Birch Company** on it.

3.  On the Action Pane, click **Collect**.

4.  Click **Write off**.

5.  Click **OK**.

6.  Close the page.

7.  Go to **General ledger \> Journal entries \> General journals**.

8.  Select the journal batch number for the journal that contains your
    write-off. One line is created to reverse the customer balance. One or more
    lines are created to post the write-off to the write-off account.

9.  Close all forms.

Write off transactions from the collections form.
-------------------------------------------------

1.  Go to **Credit and collections \> Collections \> Aged balances**.

2.  Select the name of the customer that has the transactions that you want to
    write off. For example, select Cave Wholesales (**US-004**).

3.  Mark the row for the first transaction.

4.  Mark the row for the second transaction.

5.  Click **Write off**.

6.  In the **Reason comment** field, type **'Bad debts'**.

7.  Click **OK**.

8.  Close all pages.

9.  Go to **General ledger \> Journal entries \> General journals**.

10. Select the journal batch number for the journal that contains your
    write-off. One line is created to reverse the customer balance. One or more
    lines are created to post the write-off to the write-off account.

11. Close all pages.

Write off an invoice from the Open customers invoices page
----------------------------------------------------------

1.  Go to **Accounts receivable \> Invoices \> Open customer invoices**.

2.  Mark the line for an invoice. For example, mark the line for **CIV-000715**.

3.  On the Action Pane, click **Invoice**.

4.  Click **Write off.**

5.  Click **OK**.

6.  Close the page.

Write off a customer balance from the customer page
---------------------------------------------------

1.  Go to **Accounts receivable \> Customers \> All customers.**

2.  Select a customer account. For example, select **US-001** (Contoso Retail
    San Diego).

3.  On the Action Pane, click **Collect**.

4.  Click **Write off**.

5.  Click **OK**.

6.  Close the page.

Exercise: Process the credit and collection
===========================================

Age customer balance
--------------------

As a collection agent in **USMF**, you need to identify delinquent customers’
balances, and send collection letters to them.

1.  Go to **Credit and collections \> Periodic tasks \> Age customer balances**.

2.  In the **Aging period definition** field select **30_60_90_180**.

3.  Leave the **Pool Id** field blank to create an aging snapshot for all
    customers. If a customer pool is selected, the aging snapshot process is
    applied only to the customer accounts that are part of the customer pool.
    The selected customer pool must be of the Aging snapshot type.

4.  In the **Criteria** field select **Due date**. Other choices are;
    **Transaction date** – Age each transaction based on its transaction date.,
    and **Document date** – Age each transaction based on its document date.

5.  In the **Aging as of** field select **Today's date.** You can choose
    **Selected date** to enter an aging date.

6.  Click **OK**.

View aged customer balances
---------------------------

1.  Go to **Credit and collections \> Collections \> Aged balances**.

2.  Select the customer **US-003 Forest Wholesales**

3.  Expand the **Contact** FactBox.

4.  View the collection contact for the customer, and default sales person for
    the customer.

5.  Expand the **Credit limit** FactBox.

6.  Use the **Credit information** FactBox to view the credit limit and current
    balance information for the customer.

View customer collections details
---------------------------------

1.  In the list, click the link **Forest Wholesales** in the selected row.

2.  Expand the **Address** FactBox. View the customer’s address.

3.  Expand the **Contact** FactBox. View the customer’s contact.

4.  Expand the Aging FactBox. View the customer’s aged balances.

5.  Expand the **Credit limit** FactBox. view the credit limit and current
    balance information for the customer.

6.  On the Action Pane, click **Collect**.

7.  Click **Update aging** button to update the snapshot for the customer

8.  Under the **View** group, select **Statement** to open a dialog box. This
    allows you to view the customer’s statement in Microsoft Excel format.

9.  Click **OK**.

10. Open excel to view customer’s statement.

11. Close excel and return to **Finance and Operations**.

12. On the Action Pane, click **Communicate**.

13. Click the **Statements** button.

14. in the **Show credit limit** field select **Yes**.

15. Click **OK**.

16. View the report; Optionally you can export the report into different formats
    such as pdf, excel, and word.

17. Close all pages.

Create collection letters
-------------------------

1.  Go to **Credit and collections \> Collection letter \> Create collection
    letters**.

2.  In the **Collection letter** field, select **All**.

3.  In the **Collection letter date** field enter today’s date.

4.  Expand the **Records to include** section.

5.  Click **Filter**.

6.  In the **Criteria** field, enter a Customer ID. For example, enter 'US-003'.

7.  Click **OK**.

8.  Click **OK**.

Print collection letters
------------------------

1.  Go to **Credit and collections \> Collection letter \> Review and process
    collection letters**.

2.  In the **Status** field, select **Created**.

3.  In the **Printed** field, select **Not printed**.

4.  Click **Print**.

5.  Click **Collection letter note**.

6.  in the **Postings were considered until** field, enter today’s date.

7.  Click **OK** to print the collection letter.

8.  View the collection letter, then close the form.

Post the collection letter.
---------------------------

1.  Click **Post**.

2.  Click **OK**.

3.  In the **Status** field, select **Posted**.

4.  In the **Printed** field, select printed.

5.  View the results

6.  Close all pages.

Calculate interest
------------------

1.  Go to **Credit and collections \> Interest \> Create interest notes**.

2.  Select **Interest** field to be **Yes**.

3.  Expand or collapse the Records to include section.

4.  Click Filter.

5.  In the Criteria field, enter a Customer ID. For example, enter 'US-003'.

6.  Click **OK**.

7.  Click **OK**.

Print interest notes
--------------------

1.  Go to **Credit and collections \> Interest \> Review and process interest
    notes**.

2.  In the **Status** field, select **'Created'**.

3.  In the **Printed** field, select **'Not printed'**.

4.  Click **Print**.

5.  **Click OK.**

6.  View the report. Optionally you can export the report into different formats
    such as pdf, excel, and word.

7.  Close the page.

Post the interest note
----------------------

1.  In the **Status** field, select **'Created'**.

2.  In the **Printed** field, select **'Printed'**.

3.  Click **Post**.

4.  In the **Posting date** field enter today’s date.

5.  Click **OK**.

6.  In the **Status** field, select **'Posted'**.

7.  View the results.

8.  Close all pages

Process Collection Letters
--------------------------

Connie, the Credit and Collections Manager at Contoso, must process and post the
first collection letter for customer Shrike Retail (US-023).

-   Run a collection letter job for the first collection letter.

-   Use 8/28/2017 as the date.

-   Print the letter.

-   Post the collection letter.

Create a collection letter
--------------------------

1.  Click **Credit and collections**, click **Collection letter,** click
    **Create Collection letters**,

2.  Set the **Invoice** field to **Yes**.

3.  Click the **Collection letter** arrow, and then click **Collection letter
    1**.

4.  In the **Collection letter date** field, enter **8/28/2017**.

5.  Click the **Use posting profile from** arrow, and then click **Select**.

6.  Click the **Posting profile** arrow, and then click GEN.

7.  Click **Select**.

8.  Open the **Records to include** form.

9.  Click on the **Filter** icon.

10. Enter **US-023** into the Criteria column on the **Customer account** row,
    and then click **OK**.

11. Click **OK** to process the **Creation of collection letter** job.

12. Follow these steps to review, print, and post the collection letter.

13. Click **Credit and collections**, click **Collection letter**, and then
    click **Review and process collection letters**.

14. Click the collection letter previously created for customer US-023, click
    the **Print** button, and then click **Collection letter note**.

15. Click **OK**.

16. Review the collection letter.

17. **Close** the collection letter.

18. Note that the **Printed** field is **Yes**.

19. Click the collection letter previously created for customer **US-023**, and
    then click the **Post** button.

20. Enter **9/29/2017** in the **Posting date** field.

21. Click **OK**.

22. **Close** the Infolog telling you that the Collection letter posting process
    is complete. It also tells you Collection letter number as well as the
    collection letter code and customer that was processed.

23. Close the **Review and Process Collection Letters** form.

Exercise: Review collections information
========================================

Review collections information
------------------------------

In this walkthrough you’ll learn how the system supports you in initiating
collections and tracking progress on collecting the outstanding funds from your
customers.

Go to Credit and collections \> Workspaces \> Customer credit and collections.

At the heart of the credit and collections solution is the credit and
collections workspace which provides visibility into key metrics such as open
cases, activities, and customers over their credit limit. Charts provide
visibility into aged balances and amounts such as promise to pay and disputed
amounts. Information can be filtered to a specific company, customer pool, or
customer.

1.  Go to **Credit and collections \> Collections \> Aged balances**.

2.  Use this list page to view customer balances and aged amounts by aging
    periods.

3.  In the list click on customer name ‘Contoso Retail San Diego’ to navigate to
    **Collections** details form.

4.  Expand the **Contact** FactBox.

5.  Use the **Contact** FactBox to view collections contact information for the
    customer. You can click the email icon next to the E-mail or Salesperson
    fields to create an email message for the contact or the salesperson.

6.  Expand the **Aging** FactBox.

7.  In **Aged balances** Fact box you can see aged balances based on aging
    period definition selected.

8.  Expand the **Credit limit** FactBox.

9.  In **Credit information** FactBox you can see current balance and credit
    information for the customer.

10. Easily link marked cases, transactions and activities.

11. View and perform actions on cases for the customer.

12. View and perform actions on transactions for the customer.

13. View and perform actions on collections activities for the customer.

14. Click **Change** status.

15. In the **Collections status** field, select 'Promised to pay'.

16. In the **Reason code** field, enter or select a value.

17. Click **Change** status.

Exercise: Generate accounts receivable aging information
========================================================

You need to set up an aging period definition, age customer balances, and view
balances in the Aged balance list and the Collections page. in USMF demo
company.

Create an aging period definition
---------------------------------

1.  Go to **Credit and collections \> Setup \> Aging period definitions**.

2.  Click **New**.

3.  In the **Aging period definition** field, type a value.

4.  In the **Description** field, type a value.

5.  Click **Add below** to insert a new aging period.

6.  In the **Period** field, enter the description to show on aging reports.

7.  In the **Unit** field, enter a number.

8.  In the **Interval** field, select an option. Ledger period matches the
    period to your ledger calendar. Day, week, month, quarter and years define
    the size of the interval by date type. Unlimited selects all transactions
    before or after the previous period, depending on whether it is the first or
    last period.

9.  In the **Aging indicator** field, select an option.

10. Select the period at the top of the grid. Update the description to describe
    the oldest period in the aging period definition

11. In the **Period** field, enter the new description of the aging period.

12. Close the page.

Age the balances
----------------

1.  Go to **Credit and collections \> Periodic tasks \> Age customer balances**.

2.  In the **Aging period definition** field, select the aging period definition
    that you created. You can have one active snapshot for each aging period
    definition. All customers are processed by default. You can use this
    selection to calculate a single collections pool of customers.

‎Select the date from the transaction that you will use for the aging. Select an
"as of" date for aging. The default is today but, if you change this field to
Selected date, you will be able to pick the date that you want. For batch
processing, use Today's date.

1.  Expand the **Company range**. You can select the companies that will be
    included in the snapshot. The current company is selected by default.

2.  Click **Ok** to process the snapshot. It will take some time so wait for the
    slider to disappear and check the message center for a message.

View the balances on the Aged balances list and on the Collection page
----------------------------------------------------------------------

1.  Go to **Credit and collections \> Collections \> Aged balances**.

2.  The list page shows the balances for the customer. The aging icon shows the
    aging period for the oldest transaction.

3.  Select a customer with a balance.

4.  Expand the **Aging** fact box area to view the aged balances.

5.  The aging period definition for the fact box is taken from the default aging
    period definition specified in the parameters. You can change it using the
    Collect menu.

Run customer aging report
-------------------------

1.  Go to **Credit and collections \> Inquiries and reports \> Customers \>
    Customer aging report**.

2.  In the **Aging as of** field, Select Today's date

3.  In the **Balance as of** field, Select Today's date

4.  In the **Print aging period description** field, select 'Yes'.

5.  In the **Interval** field, enter '1'.

6.  In the **Day/Mth** field, select 'Month'.

7.  In the **Printing direction** field, select 'Backward'.

8.  Select Yes in the **Details** field.

9.  Select Yes in the **Include amounts in transaction currency** field.

10. Select Yes in the **Negative balance** field.

11. Select Yes in the **Payment positioning** field.

12. Click **OK**.

13. Close all pages.
