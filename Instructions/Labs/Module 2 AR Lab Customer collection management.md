---
lab:
    title: 'Lab: Customer collection management'
    module: 'Module 2: Accounts receivable, credit and collections'
---


# Lab: Customer collection management

## Objective

In this lab, we will generate an aging report and process a collection letter.

- In the first scenario, we will create a new payment term for net 3 days. We will also create a new customer. For this customer, we will create a sales order and associate the new payment terms. We will process the entire sales order and generate the invoice. The due date of the invoice will be three days from the current date. We will run the aging report for the new customer.

-  In the second scenario, we will create another sales order for the new customer, where payment terms will be COD (cash on delivery). We will complete the processing of the sales order and generate the invoice. The due date of the invoice will be the current date. We will run the collection report for the new customer.

Open your Dynamics 365 Finance environment and change the legal entity to USMF.

## Exercise 1: Create a new payment term

1. Navigate to Modules > **Accounts receivable &gt; Payments setup** > **Terms of payment**.

2. Select the **+New** button in the action pane to create a new payment term.

3. Enter this data into the following fields:

	- **Terms of payment**: Net3

	- **Description**: Net 3 days

	- **Payment method**: Net

	- **Days**: 3

4. Select the **Save** button in the action pane and close the page.

## Exercise 2: Create a new customer

1. Navigate to **Accounts receivable &gt; Customers** > **All customers**.

2. Select the **+New** button in the action pane to create a new customer.

3. In the **Create customer** dialog, enter the following values:

	- **Customer account**: Cust-01

	- **Name**: Customer 01

	- **Customer group**: 10

4. Select the Save button to save the new record and close the page.

## Exercise 3: Create and process a new sales order

1. Navigate to **Accounts receivable &gt; Orders** > **All sales orders**.

2. Select the **+New** button in the action pane to create a new sales order.

3. In the **Create sales order** dialog, enter the following values:

	- **Customer account:** Cust-01

4. Select the **OK** button.

5. In the **Sales order** lines, enter the following values:

	- **Item number**: 1000

	- **Quantity**: 1

	- **Site**: 1

	- **Warehouse**: 13

	- **Unit price** (auto-populated): 1900

	- **Net amount** (auto-populated): 1900

6. Select the **Header** tab of the Sales order and navigate to the **Price and discount** FastTab. In the **Payment** field, enter Net3.

7. Select the **Save** button in the action pane to save the sales order.

	![Select the Header tabpage of the Sales order and navigate to the Price and discount fasttab](images/AR_Lab_Customer_collection_management_image1.png)

8. In the action pane, select the **Sell** button and confirm the sales order by selecting **Confirm sales order** under the **Generate** section.

9. In the **Confirm sales order** dialog, select the **OK** button, and **OK** again.

10. In the action pane, select the **Pick and pack** button, followed by selecting the **Generate picking list** under **Generate** section.

11. In the **Posting picking list** dialog, select the **OK** button, and **OK** again.

12. In the action pane, under the **Pick and pack** button, select **Picking list registration** under **Generate** section.

13. The **Picking list registration** page will appear, where you should select the **Update all** button under the **Updates** button in the action menu. The **Handling status** field in the **Lines** FastTab will change to **Completed**.

14. Close the **Picking list registration** page and you will be at the sales order you created.

15. In the action pane, under the **Pick and pack** button, select **Post Packing slip** under the **Generate** section.

16. In the **Packing slip posting** dialog, select the **OK** button, and **OK** again.

17. In the action pane, select the **Invoice** button, followed by selecting **Invoice** under **Generate** section.

18. In the **Posting invoice** dialog, select the **OK** button, and **OK** again.

## Exercise 4: Create a Customer pool

1. Navigate to **Credit and collections &gt; Setup** > **Customer pools**.

2. Select the **+New** button in the action pane to create a new customer pool.

3. Add the following values in the fields below:

	- **Pool ID**: New-aging

	- **Pool description**: New customer aging

	- **Pool type**: Aging snapshot

4. Select the **Select pool criteria** link and update **Customer account** with Cust-01. Select the OK button.

	![Select the Select pool criteria link and update Customer account with Cust-01.](images/AR_Lab_Customer_collection_management_image2.png)
 
5. Select the **Save** button in the action pane and close the page.

## Exercise 5: Create an Aging period definition

1. Navigate to **Credit and collections &gt; Setup** > **Aging period definitions**.

2. Select the **+New** button in the action pane to create a new aging period definition.

3. Create a record as shown below:

	- Aging period definition: 7 and 30 days

	- Description: after 7/30 days

	- Remove the existing periods and add:
	<html>
	<table>
	<tr><th>Period</th><th>Unit</th><th>Interval</th><th>Aging indicator</th></tr>
	<tr><td>30+</td><td>-1</td><td>Unlimited</td><td>Red diamond</td></tr>
	<tr><td>7</td><td>-7</td><td>Day</td><td>Yellow triangle</td></tr>
	<tr><td>Current</td><td>0</td><td>Unlimited</td><td>Green check mark</td></tr>
	</table>

	![Navigate to Credit and collections -> Setup and open Aging period definitions](images/AR_Lab_Customer_collection_management_image3.png)

4. The **Printing direction** should be Backward for all the lines in the **Period** section.

5. Select the **Save** button in the action pane and close the page.

## Exercise 6: Run aging balance

1. Navigate to **Credit and collections &gt; Setup** > **Credit and collections parameters**.

2. Under the **Collections** tab in the **Collections defaults** section, select the value 7 and 30 days in the **Aging period definition** field.

3. Save the record by selecting the **Save** button in the action pane and close the page.

4. Navigate to **Credit and collections &gt; Periodic tasks** > **Age customer balances**.

5. In the **Create a customer aging snapshot** dialog, enter the following values and select the **OK** button:

	- **Aging period definition**: 7 and 30 days

	- **Pool ID**: New-aging

	- **Criteria**: Due date

	- **Aging as of**: Selected date

	- In the **selected date** field, select a date more than 30 days ahead of your current date.

	- **Update collection status**: Yes

	- **Include customers with zero balance**: Yes

	- **Bypass credit limit calculations during aging**: No

	- **Batch processing** (under Run in the background): No

6. Navigate to **Credit and collections &gt; Collections** > **Aged balances**.

7. You should see an aging status for Customer 01 with a red diamond, and 1,900.00 in the **30**+ bucket.

	![Navigate to Credit and collections -> Collections and open Aging balances.](images/AR_Lab_Customer_collection_management_image4.png)

8. Navigate back to **Credit and collections &gt; Periodic tasks** > **Age customer balances**.

9. In the **Create a customer aging snapshot** dialog, enter the following values and select the **OK** button:

	- **Aging period definition**: 7 and 30 days

	- **Pool ID**: New-aging

	- **Criteria**: Due date

	- **Aging as of**: Selected date

	- In the **selected date** field, select a date less than 30 days and more than 7 days ahead of your current date.

	- **Update collection status**: Yes

	- **Include customers with zero balance**: Yes

	- **Bypass credit limit calculations during aging**: No

	- **Batch processing**: No

10. Navigate to **Credit and collections &gt; Collections** > **Aged balances**.

11. You should see an aging status for Customer 01 with a yellow triangle, and 1,900.00 in the **7** bucket.

	![Navigate to Credit and collections -> Collections and open Aging balances](images/AR_Lab_Customer_collection_management_image5.png)

12. Navigate back to **Credit and collections &gt; Periodic tasks** > **Age customer balances**.

13. In the **Create a customer aging snapshot** dialog, enter the following values and select the **OK** button:

	- **Aging period definition**: 7 and 30 days

	- **Pool ID**: New-aging

	- **Criteria**: Due date

	- **Aging as of**: Selected date

	- In the **selected date** field, select a date less than 7 days ahead of your current date.

	- **Update collection status**: Yes

	- **Yes**

	- **No**

	- **Batch processing**: No

14. Navigate to **Credit and collections &gt; Collections** > **Aged balances**.

15. You should see an aging status for Customer 01 with a green checkmark, and 1,900.00 in the **Current** bucket.

	![Navigate to Credit and collections -> Collections and open Aging balances](images/AR_Lab_Customer_collection_management_image6.png)

## Exercise 7: Setup collection letter sequence

1. Navigate to **Credit and collections &gt; Collection letter** > **Set up collection letter sequence**.

2. Select the **+New** button in the action pane and create a collection letter sequence as below:

	- Collection letter sequence: Medium

	- Description: Medium priority

	- Lines:


	<html>
	<table>
	<tr><th>Collection letter code</th><th>Description</th><th>Main account</th><th>Fee in currency</th><th>Minimum overdue balance</th><th>Days</th><th>Block</th></tr>
	<tr><td>Collection letter 1</td><td>First notification</td><td>&nbsp;</td><td>0.00</td><td>0.00</td><td>1</td><td></td></tr>
	<tr><td>Collection letter 2</td><td>Second notification</td><td>403150</td><td>25.00</td><td>100.00</td><td>3</td><td></td></tr>
	<tr><td>Collection</td><td>Final notification</td><td>403150</td><td>50.00</td><td>100.00</td><td>7</td><td>(checked)</td></tr>
	</table>

	- Add a note to the first notification saying “Hello, this is the first reminder for paying your balance.” 

	![Navigate to Credit and collections -> Collection letter and open Set up collection letter sequence.](images/AR_Lab_Customer_collection_management_image7.png)

3. Select the **Save** button in the action pane and close the page.

## Exercise 8: Create an interest code

1. Navigate to **Credit and collections &gt; Interest** > **Set up interest codes**.

2. Select the **+New** button in the action pane and create an interest code.

3. Enter the following values in the **interest code** page:

	- Interest code: 7D-1.5%

	- Description: 1.5% after 7 days

	- Interest type: Single rate

	- Grace period: 0

	- Effective: 2/5/2023

	- Expiration: Never

	![Navigate to Credit and collections -> Interest and open Set up interest codes](images/AR_Lab_Customer_collection_management_image8.png)

4. Enter the following values in the **Earnings** FastTab of the **interest** page.

	- Calculate interest every: 1

	- Ledger posting account: 700200 

	![Enter the following values in the Earnings & Payments fasttab of the interest code page](images/AR_Lab_Customer_collection_management_image9.png)

5. Select the **Save** button in the action pane and close the page.

## Exercise 9: Configure the Customer posting profile

1. Navigate to **Credit and collections &gt; Setup** > **Customer posting profiles**.

2. Select the existing record **GEN** and select the **Add** button in the **Setup** FastTab.

3. Add a new record and enter values as shown below:

	- **Account code**: Table

	- **Account/Group number**: Cust-01

	- **Summary account**: 133300

	- **Collection letter sequence**: Medium

	- **Interest code**: 7D-1.5%

	![Navigate to Credit and collections -> Setup and open Customer posting profiles](images/AR_Lab_Customer_collection_management_image10.png)

4. Select the **Save** button in the action pane and close the page.

## Exercise 10: Create and process a new sales order

1. Navigate to **Accounts receivable &gt; Orders** > **All sales orders**.

2. Select the **+New** button in the action pane to create a new sales order.

3. In the **Create sales order** dialog, enter **Cust-01** for the **Customer account** and select **1000** .
  
4. In the **Sales order** lines, enter the following values:

	- **Item number**: 1000

	- **Quantity**: 1

	- **Site**: 1

	- **Warehouse**: 13

	- **Unit price** (auto-populated): 1900

	- **Net amount** (auto-populated): 1900

5. Select the **Header** tab of the Sales order and navigate to the **Price and discount** FastTab. In the **Payment field**, select COD.

6. Navigate to the **Delivery** FastTab. In the **Mode of delivery** field, select **Truck-Truc**. 

7. Select the **Save** button in the action pane and save the sales order. Select **OK** to update the order lines.

8. In the action pane, select the **Sell** button and confirm the sales order by selecting **Confirm sales order** in the **Generate** section.

9. In the **Confirm sales order** dialog, select **OK** and **OK** again.

10. In the action pane, select the **Pick and pack** button, followed by selecting **Generate picking list** under **Generate**.

11. In the **Posting picking list** dialog, select **OK** and OK again.

12. In the action pane, under the **Pick and pack** button, select **Picking list registration** under **Generate**.

13. The **Picking list registration** page will appear, where you should select Updates > **Update all** n the action menu. The **Handling status** field in the **Lines** FastTab will change to **Completed**.

14. Close the **Picking list registration** page and you will be in the sales order you created.

15. In the action pane, under the **Pick and pack** button, select **Post Packing slip** under **Generate**.

16. In the **Packing slip posting** dialog, select **OK** button, and **OK** again.

17. In the action pane, select the **Invoice** button, followed by selecting **Invoice** under **Generate** section.

18. In the **Posting invoice** dialog, select **OK**, and **OK** again.

19. In the action pane, select the **Invoice** button, followed by selecting **Open transactions** in the **Settle** section.

	![You will find two open invoices for settlement:
	The first one with due date three days from current date
	The second one with current date as due date 
	](images/AR_Lab_Customer_collection_management_image11.png)

20. You will find two open invoices for settlement:

	- The first one with a due date three days from the current date.

	- The second one with the current date as the due date .

21. Select **OK**.

## Exercise 11: Create a collection letter

1. Navigate to **Credit and collections &gt; Collection letter** > **Create collection letters**.

2. A dialog will pop up to run the collection letter process. Add the following **parameters** in the **Creation of collection letter** dialog:

	- **Invoice**: Yes

	- **Collection letter**: Collection letter 1

	- **Collection letter date**: Current date + 1 (tomorrow)

	- **Use posting profile from**: Account

	- **Posting profile**: GEN

	- From the Filter option, select **customer account** Cust-01 and select **OK**

	- **Batch processing** (in the **Run in the background** section): **No**

	![Navigate to Credit and collections -> Collection letter and open Create collection letters.](images/AR_Lab_Customer_collection_management_image12.png) 

3. Select the **OK** button to execute the collection letter creation process.

4. Navigate to **Credit and collections &gt; Collection letter** > **Review and process collection letters**.

5. You will be able to see a collection letter is created notifying the customer that payment is requested for the overdue invoice.

	![Navigate to Credit and collections -> Collection letter and open Review and process collection letters.](images/AR_Lab_Customer_collection_management_image13.png)

6. You can post the collection letter by selecting it and selecting the **Post** button in the action pane.

 
