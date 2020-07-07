Exercise: Create and process free text invoices
===============================================

The goal of the lab exercise is to apply the knowledge we’ve learned regarding
the Invoice to cash processes.

1.  In **USMF**, Navigate to **Accounts receivable \> Invoices \> All free text
    invoices**.

2.  Click **New**.

3.  In the **Customer account** field, select a **US-003**. The invoice account
    will default to the same account used for the customer account.

4.  Note the value of **Accounting status** field. The accounting status starts
    with **In process** if the invoice is not posted and the invoice number will
    be assigned when the invoice is posted.

5.  In the **Description** field, type **Selling old computers**.

6.  In the **Main account** field, specify account number **130700**.

7.  The sales tax group is populated from the customer. If the customer does not
    have a sales tax group, the sales tax group from the main account is used.

8.  The items sales tax group is populated from the main account. If the main
    account does not have an item sales tax group, then the item sales tax group
    in the General ledger sales tax parameters is used.

9.  In the **Quantity** field, enter 15. The value of quantity field is
    optional.

10. In the **Unit price** field, enter **128**. The value of unit price is
    optional.

11. The amount is calculated as the quantity times the unit price. However, you
    can override that calculation and enter an amount.

12. Click on **Sales tax** to view the sales tax calculated for your invoice.

13. View the sales tax amounts in this page or you can override the amounts on
    the **Adjustment** tab.

14. Click **OK**.

15. Click **Charges** to add a charge to your invoice.

16. In the **Charges code** field, select **FREIGHT**.

17. In the **Charges value** field, enter **150**.

18. Close the page.

19. Click **Totals** to view the summary invoice details and totals.

20. Click **Close**.

21. Expand the **Line details** fasttab so you can add dimensions to your main
    account.

22. Click the **Financial dimensions line** tab.

23. In the **Cost center** field select 007. The dimension values are for the
    selected line only.

24. Click **Post** to post the invoice. You will be able to cancel before you
    post.

25. To change the timing of your invoice printing: in the **Print** field select
    **Current** to print each invoice as it is updated or select **After** to
    print after all invoices have been updated.

26. If you want to change how the customer's credit limit is checked before
    posting, change the **Credit limit type** field.

27. If you want to print the invoice, select **Yes**.

28. If the **Posting** field is enabled, the free text invoices that are
    selected will be posted when you click **OK**. To print a pro forma invoice,
    clear this option and select the Print invoice option

29. Click **OK**.

30. Click **Payment journal**.

31. Click **New**.

32. In the **Name** field, enter or select **CustPay**

33. Click **Enter customer payments**.

34. In the **Customer** field, specify the values **'US-003'**.

35. In the list, find and select the row with the value of 2,209.20 in the
    **amount available to pay** field.

36. Click **Mark selected**.

37. Set **Amount** field to '2198.85'.

38. Click **Save in journal**. Close the page.

39. Click Lines.

40. Click the **Bank** tab.

41. Select **Yes** in the **Use a deposit slip** field.

42. In the **Payment reference** field, type 'FreeText Payment'.

43. Click **Post**.

44. Close all pages.

Assign free text invoice template to a customer
-----------------------------------------------

As a user who is responsible for managing and processing Accounts receivable
invoices, you need to assign a free text invoice template to a customer in USMF
demo company

To start, navigate to **Accounts receivable \> Customers \> All customers**.

1.  In the list, find and select the desired record.

2.  On the Action Pane, click Invoice.

3.  Click **Recurring invoices**. Use this page to assign free text invoice
    templates to customers and specify how frequently invoices will be sent to
    the customer.

4.  Click **New** to assign a new template to the customer.

5.  Select the free text invoice template you want to assign to the customer.

6.  In the list, find and select the desired record.

7.  In the list, click the link in the selected row.

8.  Enter the date when the first invoice will be generated.

    -   Enter a recurring end date.

    -   Select one of the following: No end date – Invoices will be generated
        indefinitely until the template is removed from the customer account.
        Billing end date – Select this option and enter the last date that the
        invoice can be generated.

    -   Maximum cumulative amount after which invoice generation will stop.

    -   Enter the maximum cumulative amount that can be reached using the
        selected template. For example, if you enter 1,000.00 and generate
        monthly invoices for 100.00 each, invoices will stop generating after
        the tenth invoice is generated.

    -   Generate recurring invoices by using the default values from either free
        text invoice template or the customer account.

    -   Select whether to use the free text invoice template or the customer
        account to determine the default values for the language, posting
        profile, sales tax group, item sales tax group, list code,
        country/region for delivery, currency, terms of payment, method of
        payment, payment specification, payment schedule, cash discount,
        financial dimensions, and giro money transfer slip when invoices are
        created.

9.  Select the recurrence pattern.

    -   Daily – Select this option and enter the number of days in the Per
        field. For example, if you enter 15, an invoice will be generated every
        15 days for this customer. Weekly - Select this option and enter the
        number of weeks in the Per field. For example, if you enter 2, an
        invoice will be generated every two weeks for this customer. Monthly -
        Select this option and enter the number of months in the Per field. For
        example, if you enter 6, an invoice will be generated every six months
        for this customer. Yearly – Select this option and enter the number of
        years in the Per field. For example, if you enter 2, an invoice will be
        generated every two years for this customer.

10. In the Per field, enter a number.

Generate and post recurring free text invoices
----------------------------------------------

Recurring invoices are used to invoice customers regularly for the same amount.
This recording uses the USMF demo company. The recording is intended for the
person responsible for managing and processing A/R invoices.

1.  Go to **Accounts receivable \> Invoices \> Recurring invoices \> Post
    recurring invoices**. Use this page to view and print recurring invoices
    that have already been generated.

2.  In the list, select the recurring invoice group.

3.  Click **Totals**. Verify totals for the recurring invoice group.

4.  Click **Close**. Each line below is a recurring free text invoice. You can
    select a line and click 'Details' button to view free text invoice details.

5.  Click **Validate**. Verify that the selected invoices do not have errors,
    but do not post the invoices.

6.  Click **Post**. Post the selected invoices.

Create an invoice from a sales order
------------------------------------

1.  In **USMF**, Go to **Accounts receivable \> Orders \> Shipped but not
    invoiced sales orders**.

2.  Select a sales order in the list.

3.  On the Action Pane, click **Invoice**.

4.  Click **Invoice**. Note that this sales order has multiple packing slips
    associated with it. It will only show the word instead of the packing slip
    number.

5.  Expand the **Parameters** section. Posting must be set to **Yes** to post
    the invoice. You can also turn off posting and just print the invoice.
    However, you can accomplish the same result by creating a proforma invoice
    instead of an invoice. This option is used for batch jobs. The query is run
    when the batch job is run.

6.  In the **Print** field, select **'After'**.

7.  Select **Yes** for **Print invoice**.

    -   Print management can print multiple copies of the invoice and also send
        the invoice via email as a PDF file.

8.  In the **Print charges** field, select **'Summarize'**.

9.  In the **Check credit limit** field, select **'Balance'**.

10. Click **Cancel**.

Combine orders into a single invoice
------------------------------------

1.  Go to **Accounts receivable \> Orders \> All sales orders**.

2.  Locate a customer that has multiple invoices open.

3.  Select an open sales order.

4.  Select another open sales order for the same customer.

5.  On the Action Pane, click **Invoice**.

6.  Click **Invoice**.

7.  Expand the **Parameters** section.

8.  In the **Quantity** field, select **'All'**. Note that there are two
    invoices listed in the overview section. Now let's merge them into a single
    invoice.

9.  In the **Summary update for field**, select 'Invoice account'.

10. Click Arrange to merge the sales orders into a single invoice. The two sales
    orders are now merged into a single invoice.

11. Click **Cancel**.

12. Click **Yes**.

Post invoices in a batch
------------------------

1.  Go to **Accounts receivable \> Invoices \> Batch invoicing \> Invoice**.

2.  Click **Select**.

3.  Click **OK**.

4.  Click **Batch**.

5.  Click on **Yes** to turn on batch processing.

6.  Click **Recurrence**.

7.  Select **Days**

8.  Click **OK**.

9.  Click **OK**.

10. Click **Cancel**.

11. Click **Yes**.

Exercise: Process invoice and settle it against a payment
=========================================================

1.  Go to **Accounts receivable \> Invoices \> All free text invoices**.

2.  Click **New**.

3.  In the **Customer account** field, enter or select **US-013**.

4.  In the **Date** field, enter todays date

5.  In the **Description** field, type **'Selling Old Computers'**.

6.  In the **Main account** field, specify the value **110180**

7.  Set **Quantity** to '5'.

8.  Set **Unit price** to '375'.

9.  Click **Totals**.

10. Click **Post**.

11. Click **OK**.

12. Go to **Accounts receivable \> Payments \> Customer payment journal**.

13. Click **New**.

14. In the **Name** field, enter or select **CustPay** then press tab

15. Click **Enter customer payments**.

16. In the **Customer** field, select **US-013**

17. Set **Amount** to '**1,912.50'**.

18. Click **Save in journal**.

19. Close the page.

20. Click **Lines**.

21. Click **Validate**.

22. Click **Validate**.

23. Click **Post**.

24. Close all pages.
