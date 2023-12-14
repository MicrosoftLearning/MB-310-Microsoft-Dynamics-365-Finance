---
lab:
    title: 'Lab: Fixed asset transactions'
    module: 'LP 5: Manage fixed assets'
---

# Lab: Fixed asset transactions

### Change log

14Dec2023 Tested against 10.0.37

19Jul2023 Tested against 10.0.32

Updated 19Jul2023 Ex4 Step 6 Corrected navigation

## Objective

In this lab, we will test fixed asset acquisition, depreciation and split.

- In the first scenario, we will create a fixed asset and post an acquisition transaction that will be six months old. There will be a depreciation transaction on the same fixed asset on current date.

-  In the second scenario, we will create another fixed asset and post an acquisition transaction on current date. We will split a portion of the previous fixed asset and merge it with the new fixed asset. We will examine the net asset value of both the fixed assets after this transaction.

1.  Open your **Dynamics 365 Finance** environment and using the **Company picker**, change the legal entity to **USMF**. 


## Exercise 1: Create a new fixed asset

1.  In the **Fixed assets** module, expand **Fixed assets** and open **Fixed assets**. 

2.  To create a new Fixed asset, select the **+New** button in the action pane. 

3.  Enter data into the following fields, as follows: 

    - **Fixed asset group**: `OFFICE`

    - **Number**: [Auto-generated]

    - **Name**: `Office equipment - `[Year/Quarter as of six months ago]

    - **Type**: Tangible

4.  Select the **Save** button in the action pane and close the page. 


## Exercise 2: Create a new vendor invoice

1.  In the **Accounts payable** module, navigate to **Invoices** and open **Pending vendor invoices**. 

2.  To create a new vendor invoice, select the **+New** button in the action pane. 

3.  In the **Vendor invoice** page, enter the following values: 

    - **Invoice account**: `1001` 

    - **Number**: `1234` 

    - **Invoice description**: `Office equipment - `[Year/Quarter as of six months ago] 

    - **Invoice date**: [Six months ago from date from current date] 

    - **Posting date**: [Same as Invoice date] 

4.  Under the **Lines** section, select the **+ Add line** button in the toolbar and enter the following values: 

    - **Procurement category**: Select `Computers` under OFFICE MACHINES

    - **Quantity**: `10`

    - **Unit**: `ea`

    - **Unit price**: `1000`

    - **Line net amount** (Auto-updated): 10000

5.  Select the **Financials** tab in the action pane [Which may be in the ellipsis menu ...] and select **View accounting** under the **Accounting** section. 

	![Select the Add line button in the Lines fasttab of the Vendor invoice page and enter given values.](../images/FA_Lab_Fixed_asset_transations_image1.png)

6.  Take a note of the **Ledger account** for the **Posting type** *Purchase expenditure for expense* and close the **Subledger journal** page. 

7.  To post the vendor invoice journal, select the **Post** button in the action pane. 

8.  Close the **Pending vendor invoices** page. 


## Exercise 3: Post acquisition journal

1.  In the **Fixed assets** module, navigate to **Journal entries** and open **Fixed assets journal**. 

2.  Select the **+New** button in the action pane to create a new fixed asset journal and enter `FACur` for **Name**. 

3.  Select the **Lines** button in the action pane to open the journal lines. 

4.  In the journal lines, enter the following values: 

    - **Date**: [Enter the posting date that you entered in Exercise 2, which is six months ago]

	- **Voucher**: [Auto-generated]

	- **Transaction type**: Acquisition

	- **Account**: [Select the newly created fixed asset, which will be the last asset in the Fixed asset group OFFICE]

	- **Book**: 200_SLLR

	- **Debit**: 10000

	- **Offset account type**: Ledger

	- **Offset account**: [Ledger account you noted in step 6 of Exercise 2]

5.  Select the **Post** button in the action pane and close the **journal** page.

6.  In the **Fixed assets** module, navigate to **Fixed assets**, select **Fixed assets** and open the newly created fixed asset. 

7.  Select the **Valuations** button in the action pane and in the **200_SLLR book**, verify an **Acquisition** value of **10,000.00** has been made for the new fixed asset.


## Exercise 4: Post depreciation journal

1.  In the **Fixed assets** module, navigate to **Journal entries** and open **Create depreciation proposal**. 

2.  In the **Depreciation proposal** dialog, enter the following values: 

	- **Posting layer**: `Current`

	- **Legal entities**: `USMF`

	- **Name of journal**: FACur

	- **To date**: Select the calendar icon and select **Today**.

	- **Fixed asset number**: [Select the newly created fixed asset] in USMF

	- **Fixed asset group**: OFFICE in USMF

	- **Book**: 200_SLLR in USMF

	- **Run in the background** &gt; **Batch processing**: No

3.  Select the **Create journal** button to process the proposal.

4.  In the **Fixed assets** module, navigate to **Journal entries** and open **Fixed assets journal**. 

5.  A new depreciation journal will be created. Select **Lines** in the action pane to review the depreciation lines till the current date. 

6.  Select the **Post** button in the action pane. 

7.  In the **Fixed assets** module, navigate to **Fixed assets**, open **Fixed assets** and open the newly created fixed asset. 

8.  Select the **Valuations** button in the action pane and in the **200_SLLR book**, verify the **Net book value** has changed based on the added **Depreciation** calculation.


## Exercise 5: Create another new fixed asset 

**Hint:** See Exercises 1-3 for the detailed steps. 

1.  Create another new fixed asset under the fixed asset group `OFFICE` with **Name**: `Office equipment - `[Year/Quarter based on current date]. 

2.  Create and Post a new **Pending vendor invoice**, Invoice account `1001`, incrementing the **Invoice Number**, for the current date. 

    - **Procurement category**: Select `Computers` under OFFICE MACHINES 

    - **Quantity**: `10` 

    - **Unit**: `ea` 

    - **Unit price**: `500` 

3.  Create an **Acquisition journal** based on the current date. 

4.  Check the **Valuations** of the new fixed asset, verify the **Net book value** is **5,000.00**. 


## Exercise 6: Split the old fixed asset 

1.  In the **Fixed assets** module, navigate to **Fixed assets**, open **Fixed assets** and open the fixed asset created first. 

2.  Select the **Books** button in the action pane and navigate to book **200_SLLR**. 

3.  In the action pane, under the **Functions** menu, select **Split fixed asset**. 

	![Select Split fixed asset under Functions button.](../images/FA_Lab_Fixed_asset_transations_image2.png)

4.  Enter the following data in the **Split fixed asset** dialog: 

	- **To fixed asset**: [Newly created fixed asset]

	- **To book**: `200_SLLR`

	- **Transaction date**: Select the calendar icon and select **Today**. 

	- **Percent**: `75`

	- **Journal name**: `FACur`

5.  Select the **OK** button. 

5.  In the **Fixed assets** module, navigate to **Journal entries** and open **Fixed assets journal**. 

6.  Select **Lines** in the action pane, verify there are four transactions. There will be two **Acquisition** and **Depreciation** transactions for the new fixed asset. There will also be two **adjustment** transactions for the old fixed asset. 

	![In the journal lines, you will find four transactions. There will be two acquisition and depreciation transactions for the new fixed asset. There will also be two adjustment transactions for the old fixed asset.](../images/FA_Lab_Fixed_asset_transations_image3.png)

7.  Select the **Post** button in the action pane and close the **Fixed asset journal** page. 

8.  In the **Fixed assets** module, navigate to **Fixed assets**, open **Fixed assets** page and open both new fixed assets. 

9.  Select the **Valuations** button in the action pane and in the **200_SLLR** book, verify the **Net book value** has changed for both the fixed assets after the split transaction. 
