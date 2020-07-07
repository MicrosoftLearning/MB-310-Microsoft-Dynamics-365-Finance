**Before you begin**

To get the most benefit from this and other exercises in this module, we
recommend that you have the standard sample data available in Finance and
Operations that is installed by using Lifecycle Services (LCS).

Exercise – Set up credit and collections in Finance and Operations
==================================================================

In this exercise, you will perform the following tasks to set up credit and
collections in Finance and Operations:

-   Set up collections parameters

-   Set up a collection letter sequence on the posting profile

-   Set up the customer to control collection letters at the customer level

-   Create customer pools

-   Create collection agents

-   Create an aging period definition

-   Create an interest code with a range

-   Create a collection letter sequence

Set up collections parameters
-----------------------------

1.  Go to **Credit and collections \> Setup \> Accounts receivable parameters**.

2.  Select the **Collections** tab.

3.  Expand or collapse the **Collections** defaults section.

4.  Select an aging period definition for the default aging snapshot that will
    be used in the **Collections** page.

5.  Select a team that collections agents are assigned to in the **Collections
    agent** page. Only teams that have a team type of collections are displayed
    in the list.

6.  Expand or collapse the **Write-off** section.

7.  Select the journal name, which is set up for daily ledger journals, to use
    when a transaction is written off by using the **Collections** page or
    related list pages.

8.  Select the default reason code to use when write-off transactions are
    created by using the **Collections** page or related list pages.

9.  Select this option to create a separate journal line for sales tax amounts
    when write-off transactions are created by using the **Collections** page or
    related list pages. If you select this option, you can easily track the
    sales tax amounts that are involved in write-off transactions. You can track
    the sales tax amounts separately to help you more easily adjust your sales
    tax liability for the affected period.

10. Expand or collapse the **Email template** section.

11. Select the email template to use when you send an email message by using the
    **E-mail \> Transactions to contact** action in the **Collections** page.

12. Select the email template to use when you send a customer statement as an
    attachment to an email message by using the **E-mail \> Statement to
    contact** action in the **Collections** page.

13. Select the email template to use when you send an email message by using the
    **E-mail \> Transactions to salesperson** action in the **Collections**
    page.

Set up a collection letter sequence on the posting profile
----------------------------------------------------------

1.  Go to **Credit and collections \> Setup \> Customer posting profiles**.

2.  Select **Edit**.

3.  Select a collection letter sequence from the drop-down list. If you do not
    want to generate collection letters for transactions by using this posting
    profile, leave the field blank.

4.  Expand the **Table restriction** tab to change the way that collection
    letters are processed. If this field is set to **Yes**, then collection
    letters will be created for this posting profile.

Set up the customer to control collection letters at the customer level
-----------------------------------------------------------------------

1.  Go to **Credit and collections \> Setup \> Accounts receivable parameters**
    and select the **Collections** tab.

2.  Change the value of **Create collection letter per** to **Customer**.

3.  Go to **Credit and collections \> Collection letter \> Review and process
    collection letters**. Only one collection letter will be generated for a
    customer with all the overdue transactions.

Create customer pools
---------------------

1.  Go to **Credit and collections \> Setup \> Customer pools**. Use this page
    to set up customer pools, which are queries that define a group of customer
    accounts that can be displayed and managed for collections or aging
    processes. Use customer pools to filter information on the **Collections**
    list page and on related list pages. You can also use customer pools to
    filter the customer accounts that are included when aging snapshots are
    created.

2.  Click **New**.

3.  In the **Pool ID** field, type a value.

4.  In the **Pool description** field, type a value.

5.  Click **Select pool criteria**.

6.  In the **Criteria** field, type a value.

7.  Click **OK**.

8.  Click **Preview customer pool**.

Create collections agents
-------------------------

1.  Go to **Credit and collections \> Setup \> Collections agents**.

2.  Select **New**.

3.  Select **Add**.

4.  Select the users of your choice.

5.  Select **Add**.

6.  Under **Collection agent pools**, select **Add**.

7.  In the **Pool ID** field, select the drop-down button to open the lookup.

8.  In the list, find and select the desired record.

9.  Select or clear the **Default pool** check box. Select this option to
    include all customer pools in filter lists for the selected collection
    agent. If this option is not selected, only the customer pools that are
    assigned to the collection agent are available in filter lists.

Create an aging period definition
---------------------------------

1.  Go to **Credit and collections \> Setup \> Aging period definitions**.

2.  Select **New**.

3.  In the **Aging period definition** field, type a value.

4.  In the **Description** field, type a value.

5.  Specify the period name, unit, interval, and aging indicator for each aging
    period to include in the aging period definition. The line that has 0 (zero)
    in the **Unit** field represents the date that the analysis is run. Lines
    before zero will have -1, and lines after zero will have 1 as a default
    entry in the **Unit** field, but can be changed. Select the **Up** and
    **Down** buttons to rearrange the lines. The 0 (zero) line cannot be moved.

6.  Place the pointer where you want to insert a new line and then Select **Add
    above** or **Add below**.

7.  Select an indicator to represent the aging period in the **Collections**
    page and **Collections** list page.  
    ‎For example, you might select a green indicator for a current period, a
    yellow indicator for a 30-days-past period, and a red indicator for a
    90-days-past period.

8.  Select the printing direction for the aging period definition. This
    selection determines the order in which the columns appear on the Customer
    aging report or the Vendor aging report.

    -   **Forward** – Print columns in the same order in which the headings
        appear in the table, starting with the top row.

    -   **Backward** – Print columns in the reverse order in which the headings
        appear in the table, starting with the bottom row.

Create an interest code with a range
------------------------------------

1.  Go to **Credit and collections \> Interest \> Set up interest codes**.

2.  Click **New**.

3.  In the **Interest code** field, enter **3M-9%.**

4.  In the **Description** field, enter **9% after 3 months**.

5.  Expand the **Earnings** section.

6.  In the **Ledger posting account** field, specify **130500**.

7.  In the **Interest by range** field, select **Months**.

8.  Expand the **Earnings by currency** section.

9.  Select **Add**.

10. In the **Description** field, enter a **US dollar**.

11. Select **Save**.

12. Select **Ranges**.

13. Select **New**.

14. Enter the **From** value as **0** and then enter the interest percent per
    month that will be used to calculate the interest. For our example, it is
    **1.5**.

15. Select **New**.

16. Enter the next **From** value as **3**, which is the first month that you
    will be calculating a new interest amount.

17. Enter the interest percent per month that will be used to calculate the
    interest starting in month **3**. For this example, it is **2.5**.

18. Select **New**.

19. Enter the next **From** value as **6**, which is the next month that you
    will be calculating a new interest amount.

20. Enter the interest percent per month that will be used to calculate the
    interest starting in month 7. For this example, it is 5.

21. Select **Close**.

Create a collection letter sequence
-----------------------------------

1.  Go to **Credit and collections \> Setup \> Set up collection letter
    sequence**.

2.  Select **New**.

3.  In the **Collection letter sequence** field, enter a sequence ID that will
    represent the sequence. It will be used when you set up a posting profile.

4.  In the **Description** field, type a value.

5.  The terms of payment is optional. If you enter a value here, the collection
    letter fee invoice will use these terms of payment instead of the terms of
    payment stored with the customer.

6.  In the **Collection letter code** field, select the code for the first
    collection letter that you want to send.

7.  The first collection letter is created according to the due date on the
    invoice, the value that you enter for the grace period in the **Days** field
    on this line, and other information that you enter on this line.

8.  In the **Description** field, type a value.

9.  The currency for the fee defaults to the customer currency. This currency
    code can be different than the invoice currency.

10. Select **Add** to add the next collection letter that will be sent in the
    sequence.

11. In many cases, the first collection letter is just a warning. You can add
    fees if needed.

12. In the **collection letter code** field, select the next collection letter
    that will be sent in the sequence.

13. In the **Description** field, type a value.

14. In the **main account** field, select the revenue account that will be used
    for fees.

15. Enter the fee that will be charged when this collection letter is posted.

16. In the **Item sales tax group** field, select the drop-down button to open
    the lookup.

17. Select an item sales tax group if sales taxes must be calculated on the fee.

18. In the list, click the link in the selected row.

19. Enter the minimum overdue balance required before a collection letter is
    sent.

20. Enter the number of grace days that you will allow. This is the number of
    days after the due date that a collection letter can be generated.

21. Select **Add** to add the last collection letter in the sequence. You can
    add up to five collection letter codes for a collection letter sequence. In
    the **Collection letter code** field, select the next collection letter that
    will be sent in the sequence.

22. In the **Description** field, type a value.

23. In the **Main account** field, specify the desired values.

24. In the **Fee in currency** field, enter a number.

25. In the **Item sales tax group** field, click the drop-down button to open
    the lookup.

26. In the list, click the link in the selected row.

27. In the **Minimum overdue balance** field, enter a number.

28. In the **Days** field, enter a number.

29. Select this check box to stop the customer from additional deliveries and
    invoicing.

30. To unblock the account, select **No** in the **Invoicing and delivery on
    hold** field in the **Customers** page.

31. Expand the **Note** FastTab.

32. Enter the text to appear on the collection letter for the selected
    collection letter code.

33. You can translate this text into multiple languages by using the
    **Translations** menu above the note box.

Exercise - Create a write-off journal for a customer
====================================================

In this exercise, you will set up the write-off parameters and write off a
customer balance from the **Aged balances** page.

Set up the write-off parameters
-------------------------------

1.  Go to **Credit and collections \> Setup \> Accounts receivable parameters**.

2.  Select the **Collections** tab.

3.  Expand or collapse the Write-off section.

4.  The Write-off journal is the general journal that will hold the write-off
    transactions that you create. You can attach a reason code to every
    write-off. The write-off account will be used as the expense account or
    reserve adjustment in the general journal.

5.  You can override this default at the time of the write-off. Set the
    **Separate sales tax** field to **Yes** if you want to separate the sales
    tax from the original transaction in the write-off.

6.  Close the page.

Write off a customer balance from the aged balances page
--------------------------------------------------------

1.  Go to **Credit and collections \> Collections \> Aged balances**.

2.  Select the row for the customer that you want to write off. For example,
    select the line with **Birch Company** on it.

3.  On the Action Pane, select **Collect**.

4.  Select **Write off**.

5.  Select **OK**.

6.  Close the page.

7.  Go to **General ledger \> Journal entries \> General journals**.

8.  Select the journal batch number for the journal that contains your
    write-off.

9.  Note that one line is created to reverse the customer balance. One or more
    lines are created to post the write-off to the write-off account.

10. Close all pages.
