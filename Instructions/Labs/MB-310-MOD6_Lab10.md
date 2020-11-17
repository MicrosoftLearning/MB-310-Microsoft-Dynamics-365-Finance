---
lab:
    title: 'Exercise 10: Process credit and collections'
    module: 'Module 6: Implement and manage accounts receivable and credit and collections'
---

## Exercise 10: Process credit and collections

### Age customer balance

As a collection agent in **USMF**, you need to identify delinquent customers’ balances, and send collection letters to them.

1. Navigate to **Credit and collections &gt; Periodic tasks &gt; Age customer balances**.

2. In the **Aging period definition** field select **30_60_90_180**.

3. Leave the **Pool Id** field blank to create an aging snapshot for all customers. If a customer pool is selected, the aging snapshot process is applied only to the customer accounts that are part of the customer pool. The selected customer pool must be of the Aging snapshot type.

4. In the **Criteria** field select **Due date**. Other choices are: **Transaction date** – Age each transaction based on its transaction date, and **Document** **date** – Age each transaction based on its document date.

5. In the **Aging as of** field select **Today's date.** You can choose **Selected date** to enter an aging date.

6. Select **OK**.

### View aged customer balances

1. Navigate to **Credit and collections &gt; Collections &gt; Aged balances**.

2. Select the customer **US-003 Forest Wholesales**.

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

4. Select **Print**

5. Select **Collection letter note**.

6. In the **Postings were considered until** field, enter today’s date.

7. Select **OK** to print the collection letter.

8. View the collection letter, then close the form.

### Post the collection letter.

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

3. In the **Printed** field, select **'Not** **printed'**.

4. If you find any: select **Print**.

5. Select **OK**.

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

- Print the letter.

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

13. Select **OK**.

14. Review the collection letter.

15. **Close** the collection letter.

16. Note that the **Printed** field is **Yes**.

17. Select the collection letter previously created for customer **US-018**, and then select the **Post** button.

18. Enter **9/29/2017** in the **Posting date** field.

19. Select **OK**.

20. Close the **Review and Process Collection Letters** form.

 
