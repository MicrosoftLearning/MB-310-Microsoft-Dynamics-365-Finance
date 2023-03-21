---
lab:
    title: 'Lab 1: Create and post vendor, customer, general ledger payments'
    module: 'Module 1 Optional'
---

# Lab - Create and post vendor, customer, general ledger payments

## Objective

Heather, the bookkeeper at Contoso, must post a bank statement manually. Two customers paid an invoice, Heather needs to post payments to two vendors, and she also needs to post on main account 605160 for costs which are costs paid directly from the bank. If there are many bank transactions on a bank statement, these are normally imported. 

Due to the **segregation of duties**, Heather needs to post the vendor invoices from the **Accounts payable** module, the customer invoices are posted from the **Accounts receivable** module, and costs paid directly from the bank should be posted in a general journal.

1.  Open your **Dynamics 365 Finance** environment and using the **Company picker**, change the legal entity to **USMF**. 


## Exercise 1: Determine open transaction Vendors

First, we need to find an open transaction for a vendor. 

1.  In the **Accounts payable** module, navigate to **Inquiries and reports** > **Vendor reports** > **Vendor balance list**.

    **Note:** This is just one report to check, there are other inquiries and reports that will give similar results. 

2.  In the **Vendor balance list** pane, enter `1/1/2016` in the field **From date**. 

3.  Enter `1/1/2016` in the field **Report period start date**. 

4.  Enter **To date** as `12/31/2021`. 

5.  Select **OK**. 

    ![](../images/Module_7_Activity_1_-_Create_and_post_a_bankjournal_image1.png)

    We will see the following open transactions (total amounts) for Vendor accounts **1001** and **1002**. 

    **Note:** If the report comes out completely blank, then the **Feature management** setting for **Report PDF viewer** may be set incorrectly. Select the **Export** menu from the action pane and select **PDF**. Open the file and you will see the results.
    
    Heather will pay the two Vendors by bank transfer. 

    | Vendor account | Name                     | Total         |
    |----------------|--------------------------|---------------|
    | 1001           | Acme Office Supplies     | -48,674.19    |
    | 1002           | Lande Packaging Supplies | -18,460.35    |

	![](../images/Module_7_Activity_1_-_Create_and_post_a_bankjournal_image6.png)


## Exercise 2: Determine open transaction Customers 
 
We will do the same for the customers. 

1.  In the **Accounts Receivable** module, navigate to **Inquiries and reports** > **Customers** > **Customer account statement (internal)**.  

    **Note:** This is just one report to check, there are other inquiries and reports that will give similar results. 
 
2.  Enter `1/1/2016` in the **From date** field. 

3.  Enter `12/31/2021` in the **To date** field. 

4. Set the **Only open** field to **Yes** and select **OK**. 

    ![](../images/Module_7_Activity_1_-_Create_and_post_a_bankjournal_image2.png)
	
	Customers account statement (internal), both Customers have an open balance to Contoso. 

    | Customer account | Name                     | Total         |
    |------------------|--------------------------|---------------|
    | US-001           | Contoso Retail San Diego | 341.75        |
    | US-003           | Forest Wholesales        | 67,834.18     |

 
## Exercise 3: Create vendor payment journal

1.  In the **Accounts Payable** module, navigate to **Payments** > **Vendor payment journal**. 

2.  To create a new journal, select **+New** in the action pane. 

3.  Select or enter the journal `VendPay` in the **Name** field. 

4.  **Navigate** to **Lines** in the action pane. 

5.  In the **Account** field, enter or select Vendor `1001`.

6.  In the **Description** field, Enter `Payment`. 

7.  Select **Settle transactions** from the toolbar. 

    **Note:** If you have chosen a vendor, you will only see the open transactions for that vendor. If you do not select a vendor, you will see all open transactions. 

8.  Select the following lines by checking the **Mark** box: 

	| Invoice   | Due date  | Cash discount date | Amount    | Currency | Amount to settle | Amount to settle in USD |
	| -------   | --------- | ------------------ | --------- | -------- | ---------------- | ----------------------- |
	| 10017     | 7/30/2017 | 7/10/2017          | 578.09    | USD      | -575.20          | -575.20                 |
	| 10012     | 7/28/2017 | 7/13/2017          | 23,109.90 | USD      | -22,647.70       | -22,647.70              |
	| **TOTAL** |           |                    |           |          |                  | -23,222.90              |

9.	Select **OK** and you will return to the Vendor payment journal lines. 

10. To add a new line, select **+New** in the toolbar on the **List** tab. 

11. For the **Account** field, select or eneter `1002`.  

12. In the **Description** field, Enter `Payment`. 

13. Select **Settle transactions** from the toolbar. 

14. Select the following lines by checking the **Mark** box: 

| Invoice   | Due date  | Cash discount date | Amount   | Currency | Amount to settle | Amount to settle in USD |
| -------   | --------  | ------------------ | -------- | -------- | ---------------- | ----------------------- |
| 1002809   | 7/29/2017 | 7/29/2017          | 4,536.89 | USD      | -4,446,15        | -4,446,15               |
| 7919      | 7/15/2017 | 7/5/2017           | 4,509.00 | USD      | -4,328.64        | -4,328.64               |
| **TOTAL** |           |                    |          |          |                  | **-8,774.79**           |

15. Select **OK** and you will return to the vendor payment journal lines. 

    ![](../images/Module_7_Activity_1_-_Create_and_post_a_bankjournal_image3.png)

16. Back on the **Vendor payments > List** tab, for the **Offset account** field, verify **USMF OPER** is selected for both lines, and if not, select `USMF OPER`. 

17. For the **Method of payment** field, ensure **CHECK** is selected for both lines, and if not, select `CHECK`. 

18. Select **Generate payments** in the action pane. 

19. On the **Generate payments** pane, for the **Method of payment** field, select or enter `CHECK`. 

20. Select `USMF OPER` in the field **Bank account**. 

21. Select **OK**. 

22. On the **Payment by check** Pane, make a note of the number which is shown in the **From** field (e.g. 792).

23. Select **OK** and the process will start (in the background, the checks will be generated). 

24. The error **Unable to find printer with path** will appear. **Close** the notification, you will be able to continue the exercise. 

25. Check the **Payment status** of the payments. If the status is **Sent**, you can **Post** the journal. The **Check number** fields will display.


## Exercise 4: Create customer payment journal

1.  In the **Accounts receivable** module, navigate to **Payments** > **Customer payment journal**. 

2.  To create a new journal, select **+New** in the action pane. 

3.  Select or enter `CustPay` in the **Name** field. 

4.  Select the **Enter customer payments** button in the action pane. 

5.  In the **Customer** field, select `US-001` and in the **Amount** field, enter `341.75`. 

6.  The open transactions of customer US-001 will appear in the grid. **Select** the following lines by checking the **Mark** box: 

	| Transaction identifier | Identifier type   | Due date  | Amount available to pay | Currency | Cash discount | Amount to pay |
	| ---------------------- | ----------------- | --------- | ----------------------- | -------- | ------------- | ------------- |
	| FTI-00000009           | Invoice           | 6/10/2017 | 321.75                  | USD      | 0             | 321.75        |
	| 000020                 | Collection letter | 7/22/2017 | 20.00                   | USD      | 0             | 20.00         |
	| **TOTAL**              |                   |           |                         |          |               | **341.75**    |

7.  Select **Save in journal** in the action pane. 

8.  In the **Customer** field, select or enter `US-003` and in the **Amount** field, enter `67,834.18`. 

9.  The open transactions of customer US-003 will appear in the grid. **Select** the following lines by checking the **Mark** box: 

 	| Transaction identifier | Identifier type   | Due date  | Amount available to pay | Currency | Cash discount | Amount to pay |
	| ---------------------- | ----------------- | --------- | ----------------------- | -------- | ------------- | ------------- |
    | CIV-000715             | Invoice           | 2/10/2017 | 67,814.18               | USD      | 0             | 67,814.18     |
    | 000021                 | Collection letter | 8/26/2017 | 20.00                   | USD      | 0             | 20.00         |
    | **TOTAL**              |                   |           |                         |          |               | **67,834.18** |

10. Select **Save in journal** in the action pane. 

11. **Close** the form, you will return to the **Customer payment journal**. 

12. **Post** the journal. 


## Exercise 5: Create journal for costs paid directly from the bank

1.  In the **General ledger** module, navigate to **Journal entries** > **General journals**. 

2.  To create a new journal, select **+New** in the action pane. 

3.  Select or enter the journal `GenJrn` in the **Name** field. 

4.  Select **Lines** in the action pane. 

5.  In the **Account** field, select the drop-down and enter MainAccount: `605160`, BusinessUnit: `001`, Department: `024`. 

6.  Enter **electricity costs** in the **Description** field. 

7.  Enter `1,200` in the **Debit** field. 

8.  Select or enter `Bank` in the **Offset account type** field. 

9.  Select or enter `USMF OPER` in the **Offset account** field. 

10. **Post** the journal. 


## Exercise 6: Check postings on the bank account

1.  In the **Cash and bank management** module, navigate to **Inquiries and reports** > **Bank transactions**.

2.  Select or enter `USMF OPER` in the field **Bank account** Criteria. 

3.  Select **OK**. 

4.  In the **Bank transactions** list that is generated, at the top, you will see the General ledger posting and the Customer payments posting. The Vendor payments are shown as well, but with another date (Check date). You can use a filter (For example on **Payment reference**), to show the payments to the vendors: 

5.  In the **Accounts payable** module, navigate to **Vendors** > **All vendors**. 

6.  Open the Vendor `1001`. 

7.  Select the **Vendor** tab in the action pane. 

8.  Select **Transactions** in the **Transactions** section. 

9.  Select the **Invoice 10012** row. 

10. Select the **Payment** tab from the toolbar. 

11. Note the value in the **Payment reference** field. Use this to filter the Bank transactions. The value is the value you wrote down in exercise 3 – line 8. (e.g. 792). 

    **Note:** If the field is empty, make sure you posted the journal in exercise 3. 

    ![](../images/Module_7_Activity_1_-_Create_and_post_a_bankjournal_image4.png)

12. In the **Cash and bank management** module, navigate to **Inquiries and reports** > **Bank transactions**. 

13. Select or enter `USMF OPER` in the field **Bank account** Criteria. 

14. Select **OK**. 

15. In the list that is generated, select the **Payment reference** column header. 

16. Change the **Payment reference** filter drop-down to **is exactly**, enter `792` and select **Apply**. 

21. Only one line is shown, this means that the payment to the vendor is also included in the bank transactions and has therefore been paid. 

    **Note:** If you do not find it, go back to Exercise 3 and **Post** it.

    ![](../images/Module_7_Activity_1_-_Create_and_post_a_bankjournal_image5.png)

