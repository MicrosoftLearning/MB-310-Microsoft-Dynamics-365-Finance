---
lab:
    title: 'Exercise 9: Set up and use Intercompany accounting'
    module: 'Module 2: Set up and configure financial management'
---

## Exercise 9: Set up and use Intercompany accounting

You need to set up and use intercompany accounting between **USRT** and **USMF**. These companies are using the same chart of accounts.

### Create intercompany journal name in USMF

1. Select **USMF** company.

2. Navigate to **General ledger &gt; Journal setup &gt; Journal names**

3. Select **+New**

4. In the **Name** field type **USMFIntJ**

5. In the **Description** type ‘Intercompany Journal demo’

6. In the **Voucher series** field select a value.

7. Close the form

### Create intercompany journal name in USP2

1. Select **USP2** company

2. Navigate to **General ledger &gt; Journal setup &gt; Journal names**

3. Select **+New**

4. In the **Name** field type **USP2IntJ**

5. In the **Description** type ‘Intercompany Journal demo’

6. In the **Voucher series** field select a value such as **Bank_02**. The voucher series must be set to continuous. 

7. Close the form

 

### Configure Intercompany accounting

1. Select **USP2** from the company’s dropdown.

2. Navigate to **General ledger &gt; Chart of accounts &gt; Accounts &gt; Main accounts**.

3. Select **+New**

4. In the Main account field, type **'100100'**.

5. In the Name field, type **'Due to USMF**'.

6. In the Main account type field, select **'Balance sheet'**.

7. Select **+New**

8. In the Main account field, type '**100101**'.

9. In the Name field, type **'Due from USMF**'.

10. In the **Main account type** field, select **'Balance sheet'**.

11. Select **Save**

12. Close the page

13. Change company to **'USMF'**

14. Navigate to **General ledger &gt; Chart of accounts &gt; Accounts &gt; Main accounts**.

15. Verify the two accounts that you created in the steps 4 and 8 are listed since the two companies are sharing the same chart of account.

16. Select **+New**

17. In the **Main** account field, type **'100106'**.

18. In the **Name** field, **'Due to USP2**.

19. Select **Ne**w

20. In the **Main account field**, type **'100107'**.

21. In the **Name** field, type **'Due from USP2'**.

22. Close the page

23. Navigate to **General ledger &gt; Posting setup &gt; Intercompany accounting**.

24. Select **+New**

25. In the **Originating company** field, select ‘**USMF**'.

26. In the **Debit account** dropdown, select the **Due from USP2** value 100107.

27. In the **Credit account** dropdown, select the **Due to USP2** value 100106.

28. In the **Destination company** field, select **USP2**.

29. In the **Debit account** field, select the **Due to USMF** value 100100.

30. In the **Credit account** field, select the **Due from USMF** value 100101.

31. In the **Journal** field, enter or select **USP2IntJ** a daily journal name from **USP2**.

32. Select **Create reciprocal relationship**.

33. In the **Journal field**, enter or select **USMFIntJ** journal name from **USMF**.

34. Select **Save**

35. Close the page

### Use Intercompany accounting by general journals 

1. Navigate to **General ledger &gt; Journal entries &gt; Global general journals.**

2. Select **New** **journal** to open the **New journal** dialog box.

3. In the **Company** field, **USMF**.

4. In the **Name** field, select **IntJrn**.

5. Select **OK**

6. Select **Lines**

7. In the **Account type** field, select **'Bank.'**

8. In the **Account field**, specify the values **'USMF OPER.'**

9. In the **Description** field, type **'Wire.** '

10. Set **Credit** to '**1000000**'.

11. In the **Offset company** field, select **USP2**.

12. In the **Offset account** field, specify the values ‘**100100--'** due to USMF.

13. Select **Inquiries**

14. Select **Balance control**.

15. View the results.

16. Select **Close**

17. Select **Validate &gt; Validate.**

18. Select **Validate &gt; Simulate Posting**.

19. Select **Post**; two vouchers have been posted one per legal entity.

20. Close all pages

### Test the Audit trails to verify the intercompany accounting posting

1. Navigate to **General ledger &gt; Inquiries and reports &gt; Audit trail**.

2. Select **Voucher transactions**. Review the intercompany transactions

3. Select **Related voucher** to see the intercompany in the destination company.

4. Close all pages

5. Switch to **USP2** company

6. Navigate to **General ledger &gt; Inquiries and reports &gt; Audit trail**.

7. Select **Voucher** **transactions**. 

8. Select **Related voucher** to see the intercompany in the destination company.

9. Close all pages

  
‎ 

 
