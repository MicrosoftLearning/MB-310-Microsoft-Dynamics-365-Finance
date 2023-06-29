---
lab:
    title: 'Lab 3: Configure tax ledger posting groups'
    module: 'LP 1 Optional'
---

# Lab: Configure tax ledger posting groups

## Objective 

You have a new customer in Arizona. You need to create the customer in the system. You must set up a ledger account to ensure that tax is posted to main account named Arizona State Tax Payable. You must also set up a new sales tax code and use the new sales tax code in a free text invoice. 

Sales tax is calculated and posted to main accounts that are specified in Ledger posting groups. Ledger posting groups are attached to each sales tax code. You can set up individual ledger posting groups for each sales tax code, use one ledger posting group for all sales tax codes or assign multiple ledger posting groups to the sales tax codes. 

1.  Open your **Dynamics 365 Finance** environment and using the **Company picker**, change the legal entity to **USMF**. 


## Exercise 1: Set up the main account

1.  In the **General ledger** module, select **Chart of accounts** > **Accounts** > **Main accounts**. 

2.  Select **+New**. 

3.  Enter `120105` in the **Main account** field. 

4.  Enter `Arizona State Tax Payable` in the **Name** field. 

5.  Select `Liability` in the **Main account type** field. 

6.  Select `TAXPAY` in the Main account category field. 

    > **Note:** The main account category is used in the default financial reports and Power BI dashboard content. 

7.  Scroll down and expand the **Posting validation** FastTab. 

8.  Select `Sales Tax` in the **Posting Type** field. 

9.  Select **Save** and **close** the form. 


## Exercise 2: Setup a ledger posting group

Now we have set up the main account, we can set up a ledger posting group. 

1.  In the **Tax** module, navigate to **Setup** > **Sales tax** > **Ledger posting groups**. 

2.  Select **+New**. 

3.  Enter `AZ_State` in the **Ledger posting group** field. 

4.  Enter `Arizona State tax` in the **Description** field. 

5.  Select main account `120105` in the **Sales tax payable** field. 

6.  Select main account `222100` in both the **Use tax payable** and **Settlement account** fields. 

7.  Select **Save** and **close** the form. 


To use the **AR_State** ledger posting group you must: 

- Set up a sales tax code for Arizona (Exercise 3). 

- Create a sales tax group (Exercise 4). 

- Adjust an item sales tax group (Exercise 5). 

- Create a customer that uses the new sales tax code (Exercise 6). 

- Create a free text invoice (Exercise 7). 


## Exercise 3: Create a sales tax code

1.  In the **Tax** module, navigate to **Indirect taxes** > **Sales tax** > **Sales tax codes**. 

2.  Select **+New**. 

3.  Enter `AV_ARIZ` in the **Sales tax code** field. 

4.  Enter `Arizona State - Retail Prod` in the **Name** field. 

5.  Enter `GEN` in the **Settlement period** field. 

6.  Select `AZ_State` in the **Ledger posting group** field to specify the main account for posting sales tax to the general ledger. 

7.  On the **Sales tax code** in the action pane, select **Values** in the **Sales tax code** section.

8.  Enter `5.6` in the **Value** column. 

9.  Select **Save** and **close** the Sales tax code values form.

10. **Close** the Sales tax codes form. 


## Exercise 4: Expand the sales tax group

1.  In the **Tax** module, select **Indirect taxes** > **Sales tax** > **Sales tax groups**. 

2.  Select **+New**. 

3.  Enter `AZ` in the **Sales tax group** field. 

4.  Enter `Arizona` in the **Description** field. 

5.  Expand the **Setup** FastTab and select **+Add** from the toolbar. 

6.  Select or enter the Sales tax code `AV_ARIZ`.

7.  Select **Save** and **close** the form. 


## Exercise 5: Adjust an item sales tax group

1.  In the **Tax** module, select **Indirect taxes** > **Sales tax** > **Item sales tax groups**. 

2.  Select the **AU/VI** Item sales tax group from the list. 

3.  Navigate to the **Setup** FastTab and select **+Add** from the toolbar. 

4.  Select or enter `AV_ARIZ` in the **Sales tax code** field. 

5.  Select **Save** and **close** the form. 


## Exercise 6: Create a customer

1.  In the **Accounts receivable** module, select **Customers** > **All customers**. 

2.  Select **+New** to create a new customer. 

3.  Enter `US-036` in the **Customer account** field. 

4.  Select **Organization** in the **Type** field. 

5.  Enter `Contoso Retail Arizona` in the **Name** field. 

    > **Note:** If a dialog displays a list of current customers, select **Cancel**. 

6.  Select `90` in the **Customer group** field. 

7.  Select `USD` as the **Currency**. 

8.  Select `Net10` as **Terms of payment**. 

9.  Select `AZ` as the **Sales tax group**. 

10. Select `USA` as the **Country**.

11. Select `AZ` as the **State**. 

12. Select **Save** and **close** the customer form. 


## Exercise 7: Create a free text invoice

In this exercise, you generate a free text invoice and check the voucher to ensure that that the tax amount is posted on main account 120105.

1.  In the **Accounts receivable** module, select **Invoices** > **All free text invoices**. 

2.  Select **+New** to create a new invoice. 

3.  In the **Customer account** field, enter `US-036`. 

4.  In the **Invoice lines** grid, enter `Services FY2022` in the **Description** field. 

5.  Select main account `401200`. The **Sales tax group** and **Item sales tax group** fields are automatically populated. 

6.  Enter `4500` for the **Unit price** field. 

7.  Select **Save**. 

8.  Select **Post** to post the journal. Select **OK** to confirm. 

9.  Select the **Sales tax** button in the action pane. 

10. Select **View accounting**. In the **Subledger journal** verify the **Sales Tax** amount is posted to **Ledger account** 120105--. 

    ![](../images/Module_7_Activity_2_-_Configure_tax_ledger_posting_group_image1.png)

