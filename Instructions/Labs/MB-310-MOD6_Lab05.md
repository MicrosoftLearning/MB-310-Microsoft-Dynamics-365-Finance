---
lab:
    title: 'Exercise 5: Create and process free text invoices'
    module: 'Module 6: Implement and manage accounts receivable and credit and collections'
---

## Exercise 5: Create and process free text invoices

The goal of the lab exercise is to apply the knowledge we’ve learned regarding the Invoice to cash processes. 

### Instructions

1. In **USMF**, Navigate to **Accounts receivable &gt; Invoices &gt; All free text invoices**.

2. Select **+New**.

3. In the **Customer account** field, select **US-003**. The invoice account will default to the same account used for the customer account.

4. Note the value of **Accounting status** field. The accounting status starts with **In process** if the invoice is not posted, and the invoice number will be assigned when the invoice is posted.

5. In the **Description** field in the **Invoice lines** section, type **Selling old computers**.

6. In the **Main account** field, specify account number **130700**.

7. The sales tax group is populated from the customer. If the customer does not have a sales tax group, the sales tax group from the main account is used.

8. The **Item sales tax group** is populated from the main account. If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.

9. In the **Quantity** field, enter **15**. The value of quantity field is optional.

10. In the **Unit price** field, enter **128**. The value of unit price is optional.

11. The amount is calculated as the quantity times the unit price. However, you can override that calculation and enter an amount.

12. Select **Sales tax** in the action pane to view the sales tax calculated for your invoice.

13. View the sales tax amounts in this page or you can override the amounts on the **Adjustment** tab.

14. Select **OK**.

15. Select **Charges** in the action pane to add a charge to your invoice.

16. In the **Charges code** field, select **FREIGHT**.

17. In the **Charges value** field, enter **150**.

18. Close the page.

19. Select **Totals** to view the summary invoice details and totals.

20. Select **Close**.

21. Expand the **Line details** FastTab so you can add dimensions to your main account.

22. Select the **Financial dimensions line** tab.

23. In the **Cost center** field select 007. The dimension values are for the selected line only.

24. Select **Post** to post the invoice. You will be able to cancel before you post.

25. To change the timing of your invoice printing: in the **Print** field select **Current** to print each invoice as it is updated or select **After** to print after all invoices have been updated.

26. If you want to change how the customer's credit limit is checked before posting, change the **Credit limit type** field.

27. If you want to print the invoice, select **Yes**.

28. If the **Posting** field is enabled, the free text invoices that are selected will be posted when you select **OK**. To print a pro forma invoice, clear this option and select the Print invoice option.

29. Select **OK**.

30. Select **Payment journal**.

31. Select **New**.

32. In the **Name** field, enter or select **CustPay**.

33. Select **Enter customer payments**.

34. In the **Customer** field, specify the values **'US-003'**.

35. In the list, find and select the row with the value of 2,209.20 in the **amount available to pay** field.

36. Select **Mark selected**.

37. Set **Amount** field to **'2198.85'**.

38. Select **Save in journal**. Close the page. 

39. Select Lines.

40. Select the **Bank** tab.

41. Select **Yes** in the **Use a deposit slip** field.

42. In the **Payment reference** field, type **'FreeText Payment'**. 

43. Select **Post**.

44. Close all pages.

### Generate and post recurring free text invoices

Recurring invoices are used to invoice customers regularly for the same amount. This recording uses the USMF demo company. The recording is intended for the person responsible for managing and processing A/R invoices.

1. Navigate to **Accounts receivable &gt; Invoices &gt; Recurring invoices &gt; Generate recurring invoices**. Use this page to generate recurring invoices.

2. In the **Invoice date** field select today’s date.

3. In the **Template** field select **Dues** and select the **Select** button.

4. Select **OK**.

5. Navigate to **Accounts receivable &gt; Invoices &gt; Recurring invoices &gt; Post recurring invoices**. Use this page to view and print recurring invoices that have already been generated.

6. Note that you have an invoice generated resulting from previous steps.

7. Select the generated invoice.

8. Select **Validate**. Verify that the selected invoices do not have errors, but do not post the invoices.

9. Select **Totals**. Verify totals for the recurring invoice.

10. Select **Close**.

11. Select **Post**. Post the selected invoices.

  
‎ 

1. Navigate to **Accounts receivable &gt; Invoices &gt; All free text invoices**. 

2. Select **+New**.

3. In the **Customer account** field, enter or select **US-013**.

4. In the **Date** field, enter today’s date.

5. In the **Description** field in the **Invoice lines** section, type **'Selling Old Computers'**.

6. In the **Main account** field, specify the value **110180**.

7. Set **Quantity** to '5'.

8. Set **Unit price** to '375'.

9. Select **Totals**. Close.

10. Select **Post**.

11. Select **OK**.

12. Navigate to **Accounts receivable &gt; Payments &gt; Customer payment journal**.

13. Select **+New**.

14. In the **Name** field, enter or select **CustPay** then press tab.

15. Select **Enter customer payments**.

16. In the **Customer** field, select **US-013**.

17. Set **Amount** to '**1,912.50'**.

18. Select **Save in journal** in the action pane.

19. Close the page.

20. Select **Lines**.

21. Select **Validate**.

22. Select **Validate**.

23. Select **Post**.

24. Close all pages.

  
‎ 

1. Select **Accounts receivable &gt; Charges setup &gt; Charges code**.

2. Select **+New**. In the **Charges code** field, type a code for the charge.

3. In the **Description** field, type a description of the charge.

4. Optional: In the **Item sales tax group** field, select a sales tax group.

5. If you set the **Prorate** field to **Yes**, the calculated charges are prorated down to the sales line level. Because these charges are at the line level and not kept at the header level, a more specific link is made between the item and the charge value that calculated for it. This behavior can be useful in partial return scenarios, where an organization wants to refund only part of the charge instead of the whole charge when only some items are returned. 

6. On the **Posting** FastTab, specify how the charge is automatically debited and credited.

7. If you selected **Ledger account** as the debit type or credit type, specify a posting type in the **Debit posting** and **Credit posting** fields, and specify the main account in the **Debit account** and **Credit account** fields.

### Create charges groups for customers

1. Select **Accounts receivable &gt; Charges setup &gt; Customer charge groups**.

2. Select **+New**.

3. In the **Charges group** field, enter a code for the charges group. The code can contain both letters and numbers.

4. In the **Description** field, enter a description of the charges group.

5. Close the form to save your changes.

### Create item charges groups

1. Select **Accounts receivable &gt; Charges setup &gt; Item charge groups**.

2. Select **+New** to create an item charge group.

3. In the **Charges group** field, enter a code for the group. The code can be alphanumeric.

4. In the **Description** field, enter a description for the group.

5. Close the form to save your changes.

### Set up collections parameters

1. Navigate to **Credit and collections &gt; Setup &gt; Credit and collections parameters**.

2. Select the **Collections** tab.

3. Expand the **Collections** defaults section.

4. Select an **Aging period definition** for the default aging snapshot that will be used in the Collections form.

5. Select a **Team** that collections agents are assigned to in the Collections agent form. Only teams that have a team type of Collections are displayed in the list.

6. Expand the **Write-off** section.

7. In the field **Write-off journal**, select the journal name which is set up for daily ledger journals, to use when a transaction is written off by using the Collections form or related list pages.

8. Select the **Separate sales tax** option to create a separate journal line for sales tax amounts when write-off transactions are created by using the Collections page or related list pages. If you select this option, you can easily track the sales tax amounts that are involved in write-off transactions. You can track the sales tax amounts separately to help you more easily adjust your sales tax liability for the affected period.

9. Select the **Default write-off reason** code to use when write-off transactions are created by using the Collections form or related list pages.

10. Expand the **Email template** section.

11. In **Transactions to contact**, select the email template to use when you send an email message by using the **E-mail &gt; Transactions** to contact action in the **Collections** form.

12. In **Statement to contact**, select the email template to use when you send a customer statement as an attachment to an email message by using **the E-mail &gt; Statement** to contact action in the collections form.

13. In **Transactions to sales person**, select the email template to use when you send an email message by using the **E-mail &gt; Transactions** to salesperson action in the collections form.

### Set up a collection letter sequence on the posting profile

1. Navigate to **Credit and collections &gt; Setup &gt; Customer posting profiles**.

2. Select **Edit**.

3. Select a **Collection letter sequence** from the drop-down list. If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.

4. Expand the table restriction tab to change the way that collection letters are processed. If this field is set to **Yes**, then collection letters will be created for this posting profile.

### Set up the customer to control collection letters at the customer level

1. Navigate to **Credit and collections &gt; Setup &gt; Credit and collections parameters**. (Depending on your version, you might navigate to **Credit and collections &gt; Setup &gt; Accounts receivable parameters** and select the **Collections** tab instead.)

2. Change the value of **Create collection letter per** to **Customer**.

3. Navigate to **Credit and collections &gt; Collection letter &gt; Review and process collection letters**. Only one collection letter will be generated for a customer containing all the overdue transactions.

### Create customer pools

1. Navigate to **Credit and collections &gt; Setup &gt; Customer pools**. Use this page to set up customer pools, which are queries that define a group of customer accounts that can be displayed and managed for collections or aging processes. Use customer pools to filter information on the Collections list page and on related list pages. You can also use customer pools to filter the customer accounts that are included when aging snapshots are created. You can use customer pools to filter the customer accounts that are included when aging snapshots are created.

2. Select **+New**.

3. In the **Pool ID** field, type a value.

4. In the **Pool description** field, type a value.

5. Select **Select pool criteria**.

6. In any **Criteria** field, select a value.

7. Select **OK**.

8. Select **Preview customer pool**.

### Create collections agents

1. Navigate to **Credit and collections &gt; Setup &gt; Collections agents**. Use this page to set up workers as collections agents and optionally assign customer pools to them. A collections agent is a person who works with customers to make sure that payments are collected in a timely manner. Collections agents that are set up in this page are automatically added to a collections team. If a team is selected in the Team field in the Accounts receivable parameters page, collections agents are added to that team. If a team is not selected, a new team named Collections is created automatically and the collections agents are added to that team.

2. Select **+New**.

3. Select **+Add**.

4. Select the users of your choice.

5. Select **+Add**.

6. Under Collection agent pools select **+Add**.

7. In the **Pool ID** field, select the drop-down button to open the lookup.

8. In the list, find and select the desired record.

9. Select or clear the **Default pool** check box. Select this option to include all customer pools in filter lists for the selected collections agent. If this option is not selected, only the customer pools that are assigned to the collections agent are available in filter lists.

### Create aging period definition

1. Navigate to **Credit and collections &gt; Setup &gt; Aging period definitions**. You can use aging period definitions to analyze the maturity of customer accounts and vendor accounts, based on a date that you enter. Each aging period that you set up for the aging period definition corresponds to a column on the list page or in the form or report when the analysis is performed.

2. Select **+New**.

3. In the **Aging period definition** field, type a value.

4. In the **Description** field, type a value.

5. Specify the period name, unit, interval and aging indicator for each aging period to include in the aging period definition. The line that has 0 (zero) in the Unit field represents the date that the analysis is run. Lines before zero will have -1, and lines after zero will have 1 as a default entry in the Unit field but can be changed. Select the Up and Down buttons to rearrange the lines. The 0 (zero) line cannot be moved.

6. Place the pointer where you want to insert a new line and then select Add above or Add below.

7. Select an indicator to represent the aging period in the Collections form and list page. For example, you might select a green indicator for a current period, a yellow indicator for a 30-days-past period, and a red indicator for a 90-days-past period.

8. Select the printing direction for the aging period definition. This selection determines the order in which the columns appear on the Customer aging report or the Vendor aging report. **Forward** – Print columns in the same order in which the headings appear in the table, starting with the top row. **Backward** – Print columns in the reverse order in which the headings appear in the table, starting with the bottom row.

### Create an interest code with a range

1. Navigate to **Credit and collections &gt; Interest &gt; Set up interest codes**.

2. Select **+New**.

3. In the **Interest code** field, enter **3M-9%**.

4. In the **Description** field, enter **9% after 3 months**.

5. Expand the **Earnings** section.

6. In the **Ledger posting account** field, specify **130500**.

7. In the **Interest by range** field, select **'Months'**.

8. Expand the **Earnings by currency** section.

9. Select **+Add**.

10. In the **Description** field, enter a **US dollar**.

11. Select **Save**.

12. Select **Ranges**.

13. Select **+New**.

14. Enter the **From** value as **0** and then enter the interest percent per month that will be used to calculate the interest. For our example, it is **1.5**.

15. Select **+New**.

16. Enter the next **From** value as **3**, which is the first month that you will be calculating a new interest amount.

17. Enter the interest percent per month that will be used to calculate the interest starting in month **3**. For this example, it is **2.5**.

18. Select **+New**.

19. Enter the next **From** value as **6**, which is the next month that you will be calculating a new interest amount.

20. Enter the interest percent per month that will be used to calculate the interest starting in month 7. For this example, it is **5**. 

21. Select **Close**.

### Create a collection letter sequence

1. Navigate to **Credit and collections &gt; Setup &gt; Set up collection letter sequence**.

2. Select **+New**.

3. In the **Collection letter sequence** field, enter a sequence ID that will represent the sequence. It will be used when you set up a posting profile.

4. In the **Description** field, type a value.

5. The **Terms of payment** is optional. If you enter a value here, the collection letter fee invoice will use these terms of payment instead of the terms of payment stored with the customer.

6. In the **Collection letter code** field, select the code for the first collection letter that you want to send.

7. The first collection letter is created according to the due date on the invoice, the value that you enter for the grace period in the Days field on this line, and other information that you enter on this line.

8. In the **Description** field, type a value.

9. The currency for the fee defaults to the customer currency. This currency code can be different than the invoice currency.

10. Select **+Add** to add the next collection letter that will be sent in the sequence.

11. In many cases, the first collection letter is just a warning. You can add fees if needed.

12. In the **collection letter code** field, select the next collection letter that will be sent in the sequence.

13. In the **Description** field, type a value.

14. In the **Main account** field, select the revenue account that will be used for fees.

15. Enter the fee that will be charged when this collection letter is posted.

16. In the **Item sales tax group** field, select the drop-down button to open the lookup. 

17. Select an item sales tax group if sales taxes must be calculated on the fee.

18. Enter the **Minimum overdue balance** required before a collection letter is sent.

19. Enter the number of grace **Days** that you will allow. This is the number of days after the due date that a collection letter can be generated. 

20. Select **+Add** to add the last collection letter in the sequence. You can add up to five collection letter codes for a collection letter sequence. In the collection letter code field, select the next collection letter that will be sent in the sequence.

21. In the **Description** field, type a value.

22. In the **Main account** field, specify the desired values.

23. In the **Fee in currency** field, enter a number.

24. In the **Item sales tax group** field, select the drop-down button to open the lookup.

25. In the list, select the link in the selected row.

26. In the **Minimum overdue balance** field, enter a number.

27. In the **Days** field, enter a number.

28. Select the **Block** check box to stop the customer from additional deliveries and invoicing. 

29. To unblock the account, select No in the **Invoicing and delivery on hold** field in the Customers page.

30. Expand the **Note** FastTab.

31. Enter the text to appear on the collection letter for the selected collection letter code. 

32. You can translate this text into multiple languages using the Translations menu above the note box.

### Set up the write off parameters

1. Navigate to **Credit and collections &gt; Setup &gt; Credit and collections parameters**.

2. Select the **Collections** tab.

3. Expand the **Write-off** section.

4. The **Write-off journal** is the general journal that will hold the write-off transactions that you create. You can attach a reason code to every write-off. The write-off account will be used as the expense account or reverse adjustment in the general journal.

5. You can override this default at the time of the write-off. Set **Separate sales tax** field to Yes if you want to separate the sales tax from the original transaction in the write-off.

6. Close the page.

### Write off a customer balance from the aged balances page

1. Navigate to **Credit and collections &gt; Collections &gt; Aged balances**.

2. Mark the row for the customer that you want to write off. For example, mark the line with **Contoso Europe** on it.

3. On the Action Pane, select **Collect**.

4. Select **Write off**.

5. Select **OK**.

6. Close the page.

7. Navigate to **General ledger &gt; Journal entries &gt; General journals**.

8. Select the journal batch number for the journal that contains your write-off. Note that one line is created to reverse the customer balance. One or more lines are created to post the write-off to the write-off account.

9. Close all pages.

### Write off a customer balance from the aged balances page

As a collection agent in **USMF**, you need to create a write off journal, since the Birch company is not going to pay the balance due to defective products that were shipped to them.

1. Navigate to **Credit and collections &gt; Collections &gt; Aged balances**.

2. Mark the row for the customer that you want to write off. For example, mark the line with **Birch Company** on it.

3. On the Action Pane, select **Collect**.

4. Select **Write off**.

5. Select **OK**.

6. Close the page.

7. Navigate to **General ledger &gt; Journal entries &gt; General journals**.

8. Select the journal batch number for the journal that contains your write-off. One line is created to reverse the customer balance. One or more lines are created to post the write-off to the write-off account.

9. Close all forms.

### Write off transactions from the collections form.

1. Navigate to **Credit and collections &gt; Collections &gt; Aged balances**.

2. Select the name of the customer that has the transactions that you want to write off. For example, select the link for Cave Wholesales (**US-004**).

3. Mark the row for the first transaction.

4. Select **Write off**.

5. Select **OK**.

6. Close all pages.

7. Navigate to **General ledger &gt; Journal entries &gt; General journals**.

8. Select the journal batch number for the journal that contains your write-off and view the **Lines**. One line is created to reverse the customer balance. One or more lines are created to post the write-off to the write-off account.

9. Close all pages.

### Write off an invoice from the Open customers invoices page

1. Navigate to **Accounts receivable &gt; Invoices &gt; Open customer invoices**.

2. Mark the line for an invoice. For example, mark the line for **CIV-000715**.

3. On the Action Pane, select **Invoice**.

4. Select **Write off**.

5. Select **OK**.

6. Close the page.

### Write off a customer balance from the customer page

1. Navigate to **Accounts receivable &gt; Customers &gt; All customers**.

2. Select a customer account. For example, select **US-001** (Contoso Retail San Diego).

3. On the Action Pane, select **Collect**.

4. Select **Write off**.

5. Select **OK**.

6. Close the page.

### Age customer balance

As a collection agent in **USMF**, you need to identify delinquent customers’ balances, and send collection letters to them.

1. Navigate to **Credit and collections &gt; Periodic tasks &gt; Age customer balances**.

2. In the **Aging period definition** field select **30_60_90_180**.

3. Leave the **Pool Id** field blank to create an aging snapshot for all customers. If a customer pool is selected, the aging snapshot process is applied only to the customer accounts that are part of the customer pool. The selected customer pool must be of the Aging snapshot type.

4. In the **Criteria** field select **Due date**. Other choices are: **Transaction date** – Age each transaction based on its transaction date, and **Document date** – Age each transaction based on its document date.

5. In the **Aging as of** field select **Today's date**. You can choose **Selected date** to enter an aging date.

6. Select **OK**.

### View aged customer balances

1. Navigate to **Credit and collections &gt; Collections &gt; Aged balances**.

2. Select the customer **US-003 Forest Wholesales** 

3. Expand the **Contact** FactBox in the **Related information** bar.

4. View the collection contact for the customer, and default salesperson for the customer.

5. Expand the **Credit limit** FactBox.

6. Use the **Credit limit** FactBox to view the credit limit and current balance information for the customer.

### View customer collections details

1. In the aged balances list, select the link for **Forest Wholesales** in the selected row to open the detail page.

2. Expand the **Related information** on the right side.

3. Expand the **Address** FactBox. View the customer’s address.

4. Expand the **Contact** FactBox. View the customer’s contact.

5. Expand the **Aging** FactBox. View the customer’s aged balances.

6. Expand the **Credit limit** FactBox. View the credit limit and current balance information for the customer.

7. On the Action Pane, select **Collect**.

8. Select **Update aging** button to update the snapshot for the customer.

9. Under the **View** group, select **Statement** to open a dialog box. This allows you to view the customer’s statement in Microsoft Excel format.

10. Select **OK**.

11. Open Excel to view customer’s statement.

12. Close Excel and return to **Dynamics 365 Finance**.

13. On the Action Pane, select **Communicate**.

14. Select the **Statements** button.

15. In the **Show credit limit** field select **Yes**.

16. Select **OK**.

17. View the report; Optionally you can export the report into different formats such as pdf, Excel, and Word. 

18. Close all pages.

### Create collection letters

1. Navigate to **Credit and collections &gt; Collection letter &gt; Create collection letters**.

2. In the **Collection letter date** field enter today’s date.

3. Expand the **Records to include** section.

4. Select **Filter**.

5. In the **Criteria** field, enter a Customer ID. For example, enter 'US-003'.

6. Select **OK**.

7. Select **OK**.

### Print collection letters

1. Navigate to **Credit and collections &gt; Collection letter &gt; Review and process collection letters**.

2. In the **Status** field, select **Created**.

3. In the **Printed** field, select **Not printed**.

4. Select **Print**.

5. Select **Collection letter note**.

6. In the **Postings were considered until** field, enter today’s date.

7. Select **OK** to print the collection letter.

8. View the collection letter, then close the form.

### Post the collection letter

9. Select **Post**.

10. Select **OK**.

11. In the **Status** field, select **Posted**.

12. In the **Printed** field, select **Printed**.

13. View the results.

14. Close all pages.

### Calculate interest

1. Navigate to **Credit and collections &gt; Interest &gt; Create interest notes**.

2. Select **Interest** field to be **Yes**.

3. Expand or collapse the Records to include section.

4. Select Filter.

5. In the Criteria field, enter a Customer ID. For example, enter 'US-003'.

6. Select **OK**.

7. Select **OK**.

### Print interest notes

1. Navigate to **Credit and collections &gt; Interest &gt; Review and process interest notes**.

2. In the **Status** field, select **'Created'**.

3. In the **Printed** field, select **'Not printed'**.

4. If you find any: select **Print**.

5. **Select OK**.

6. View the report. Optionally you can export the report into different formats such as pdf, excel, and word.

7. Close the page.

### Post the interest note

8. In the **Status** field, select **'Created'**.

9. In the **Printed** field, select **'Printed'**.

10. If you find any: select **Post**.

11. In the **Posting date** field enter today’s date.

12. Select **OK**.

13. In the **Status** field, select **'Posted'**.

14. View the results.

15. Close all pages.

### Process Collection Letters

Connie, the Credit and Collections Manager at Contoso, must process and post the first collection letter for customer Shrike Retail (US-023).

- Run a collection letter job for the first collection letter. 

- Use 8/28/2017 as the date. 

- Print the letter

- Post the collection letter. 

### Create a collection letter

1. Select **Credit and collections**, select **Collection letter**, select **Create Collection letters**.

2. Set the **Invoice** field to **Yes**. 

3. In the **Collection letter date** field, enter **8/28/2017**. 

4. Select the **Use posting profile from** dropdown, and then select **Select**. 

5. Select the **Posting profile** dropdown, and then select GEN. 

6. Open the **Records to include** form.

7. Select the **Filter** icon.

8. Enter **US-023** into the Criteria column on the **Customer account** row, and then select **OK**. 

9. Select **OK** to process the **Creation of collection letter** job. 

10. Follow these steps to review, print, and post the collection letter.

11. Select **Credit and collections**, select **Collection letter**, and then select **Review and process collection letters**. 

12. Select the collection letter previously created for customer US-023, select the **Print** button, and then select **Collection letter note**. 

13. Select **OK**

14. Review the collection letter. 

15. **Close** the collection letter. 

16. Note that the **Printed** field is **Yes**. 

17. Select the collection letter previously created for customer **US-018**, and then select the **Post** button. 

18. Enter **9/29/2017** in the **Posting date** field. 

19. Select **OK** 

20. Close the **Review and Process Collection Letters** form.

 
