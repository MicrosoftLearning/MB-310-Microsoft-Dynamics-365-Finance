---
lab:
    title: 'Exercise 16: Configure Indirect sales tax'
    module: 'Module 2: Set up and configure financial management'
---


## Exercise 16: Configure Indirect sales tax

The goal of the lab exercise is to apply the knowledge we’ve learned regarding the configuration of tax components. This recording uses the **USMF** demo company.

### Set up Ledger posting groups for sales tax

1. Navigate to **Tax &gt; Setup &gt; Sales tax &gt; Ledger posting groups**.

2. Select **New**

3. In the **Ledger posting group** field, type **DynLPG**.

4. In the **Description** field, type **Demo Tax ledger** **posting**.

5. In the **Sales tax payable** field, select the main account **202100** for outgoing sales taxes that are payable to the tax authority.

6. In the **Sales tax receivable** field, if available, select the main account **202700** for incoming taxes that are received from the tax authority.

7. In the **Use tax expense** field, if available, select the main account **222100** for posting deductible Use taxes that are not claimed or reported to the tax authority by vendors as part of EU reverse charge VAT. 

8. In the **Use tax payable** field, select the main account **222100** for posting incoming Use taxes that are payable to tax authorities.

9. In the **Settlement account** field, select the main account **222100** that the net balance of the ledger accounts specified in the Use tax payable and Sales tax receivable fields will be posted.

10. In the **Vendor cash discount** field, select the main account **520200** to post cash discount for Sales tax codes associated with this Ledger posting group.

11. In the **Customer cash discount** field, select the main account **403300** to post cash discount for Sales tax codes associated with this Ledger posting group.

12. Select Save

### Set up sales tax authorities

1. Navigate to **Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities**.

2. Select **New**

3. In the **Authority** field, type **DynA**.

4. In the **Name** field, type **Demo Tax Authority**.

5. In the **Vendor account** field, select **US_TX_001** California State Tax Authority.

6. In the **Report layout** field, select **U.S. report layout**.

7. Select **Save**

  
‎ 

### Set up sales tax settlement periods

1. Navigate to **Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax settlement periods**.

2. Select **New**

3. In the **Settlement period** field, type **DynSP**.

4. In the **Description** field, type **Demo Settlement period**.

5. In the **Authority** field, select **DynA**.

6. In the **Period interval unit** field select **Months**.

7. In the **Period interval duration** field type **3** to represent a quarter.

8. Set the **Use batch processing for sales tax settlement** field to **Yes**. The settlement process for the settlement period can be processed as batch job in the background. This is recommended for a large number of tax transactions within a period interval.

9. Set the **Prevent generating offset tax transactions** field to **Yes**. By default, the system generates offset tax transactions during the settlement process, which can cause a performance issue if there are a large number of tax transactions within a period interval. Select this check box to prevent generating offset tax transactions.

10. Expand the **Period intervals** tab.

11. Select **Add**

12. In the **From date** field, enter **01/01/2020**.

13. In the **To date** field, **03/31/2020**.

14. Select **New period interval**. Once the first period interval has been entered, new periods can be created automatically. You can come back and add new period intervals as required.

15. Repeat step 14 until you have created period intervals that includes today’s date.

16. Close the page

 

### Set up sales tax codes

Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.

1. Navigate to **Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax codes**.

2. Select **New**

3. In the **Sales tax code** field, type **DynSTC**.

4. In the **Name** field, type **Demo Sales Tax Code**.

5. Select **DynSP** in the **Settlement period** field.

6. Select **DynLPG** as the **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.

7. Expand the **Calculation** FastTab. Verify the fields that control how sales tax amounts will be calculated.

8. On the Action Pane, Select **Sales tax code**.

9. Select **Values**

10. In the **Value** field type 7.27.

11. Select **Save**

12. Close the page

13. Select **Save**

14. Close the page

### Set up sales tax groups and item sales tax groups

1. Navigate to **Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax groups**.

2. Select **New**

3. In the **Sales tax group** field, type **DynSTG**.

4. In the **Description** field, type **Demo Sales tax group**.

5. Expand the **Setup** section.

6. Select **Add**

7. In the **Sales tax code** field, select **DynSTC**.

8. Select **Save**

9. Close the page

10. Navigate to **Tax &gt; Indirect taxes &gt; Sales tax &gt; Item sales tax groups**.

11. Select **New**

12. In the **Item sales tax group** field, type **DynISTG**.

13. In the **Description** field, type **Demo Item sales tax group**.

14. Select **Add**

15. In the **Sales tax code** field, type **DynSTC**.

16. Select **Save**

17. Close the page

### Set up sales tax reporting codes

1. Navigate to **Tax &gt; Setup &gt; Sales tax &gt; Sales tax reporting codes**.

2. Select **New**

3. In the Report layout field select **U.S. report layout**.

4. In the **Reporting code** field type **102020.** 

5. In the **Report text** field, enter a description to display on reports such as **Dynamics 365 Sales Tax Demo**.

6. In the **Brief description** field, enter a description for internal purposes such as **Demo Sales Tax**.

7. Select **Save**

8. Close the page

### Set up withholding tax

1. Navigate to **Tax &gt; Indirect taxes &gt; Withholding tax &gt; Withholding tax codes**.

2. Select **New**

3. In the **Withholding tax code** field, type **DynWH**.

4. In the **Withholding tax name** field, enter **Demo** **withholding tax code**.

5. In the **Main account** field, select the main account **200180** for posting the withholding tax liability.

6. Select **Save**

7. Select **Values**

8. In the **Value** field, enter a percentage used for the calculation of the withholding tax. For example, type **31**.

9. Select **Save**

10. Close the page

11. Select **Save**

12. Close the page

13. Navigate to **Tax &gt; Indirect taxes &gt; Withholding tax &gt; Withholding tax groups**.

14. Select **New**

15. In the **Withholding tax group** field, enter **DynWHG**.

16. In the **Description** field, enter **Demo** **withholding tax group**.

17. In the **Withholding tax code** field, select **DynWH**.

18. Select **Save**

19. Close the page

 

### View posted sales tax transactions

You can view posted sales tax transactions from various page depending on what you need to view. 

1. Navigate to **Tax &gt; Inquiries and reports &gt; Sales tax inquiries &gt; Posted sales tax**.

2. View the results

3. Close the page

4. Navigate to **Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax settlement periods**.

5. Expand the **Period intervals** section.

6. Select the interval you are interested in to display posted sales tax transactions for the selected settlement period interval. You can further filter the list of posted sales tax transactions.

7. Select the **Posted sales tax** button.

8. View the results

9. Close the page

10. Navigate to **Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax codes**.

11. On the Action Pane, select **Sales tax code**.

12. Select **Posted sales tax**.

13. View the results.

14. Close the page

