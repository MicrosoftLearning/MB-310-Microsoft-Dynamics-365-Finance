---
lab:
    title: 'Exercise 7: Configure and test Accrual schemes'
    module: 'Module 2: Set up and configure financial management'
---

## Exercise 7: Configure and test Accrual schemes

You need to assist Sabrina, the accountant in USMF how to configure and use accrual schemes in Finance and Operations. She wants to lease a vehicle from a vendor for the amount of $81,720 and record accruals in Finance and Operations within the terms of lease of 24 months. She likes to understand the monthly and number of day option in the accrual schemes. 

 

### Create accrual schemes.



1. Navigate to **General ledger &gt; &gt; Journal setup &gt; &gt; Accrual schemes**.

2. Select **New**

3. In the **Accrual identification** field, type '24M'.

4. In the **Description** **of accrual scheme** field, type '2 Year Lease'.

5. In the **Debit** account field, specify the values '420100.'

6. In the **Credit** account field, specify the values '420200.'

7. In the **Voucher field**, select 'New voucher for each accrual transaction date'

8. In the **Number sequence code** field, enter or select a value.

9. In the **Period** **frequency** field, select 'Monthly.'

10. In the **Number of occurrences by period** field, enter '24'.

11. In the **Post transactions** field, select 'Month.'

12. In the **Post in week, month or quarter** field, select 'Middle.'

13. Close the page


### Create general journal to test accrual schemes.



1. Navigate to **General ledger &gt; &gt; Workspaces &gt; &gt; General journal processing**.

2. Select **New journal**.

3. In the **Name** field, enter or select **GenJrn** 

4. In the **Description** field, type **'General Daily Journal - Accruals Demo**.'

5. Select **Lines**

6. In the **Account type** field, select **'Vendor**.'

7. In the **Account field**, specify a vendor account of your choice, such as 1001 Acme Office Supplies

8. Set **Debit** to **'81720**.'

9. In the **Offset account** field, specify the values ‘**605160-001-023--**'.

10. In the **Offset transaction** text field, type **'Accruals Demo**.'

11. From the **List** tab in the line section, select **Functions**.

12. Select **Ledger** **accruals**

13. In the **Accrual** **identification** field, enter or select 24M

14. Select **Transactions**.

15. Review the values. The total amount is distributed evenly.

16. Close the page

17. Select to follow the hyperlink in the **Accrual identification** field, or right click and view details

18. In the **Spread month and quarter values** field, select 'Number of days'.

19. Close the page

20. Select **Cancel**

21. Select **Yes**

22. From the **List** tab in the line section, select **Functions**.

23. Select **Ledger accruals**

24. In the **Accrual identification** field, enter or select 24M then press tab

25. Select **Transactions**. Note that amounts have been prorated per number of days.

26. Close the page and select **Cancel** and **Yes**.

27. Select **Payment** tab

28. In the **Method of payment** field select ‌ELECTRONIC

29.  

30. Select **Validate &gt; Validate**.

31. Select **Post**

32. Close all forms

33. Navigate to **General ledger &gt; &gt; Inquiries and reports &gt; &gt; Audit trail**.

34. Find the journal you just posted. It should be the last record, or you can filter by many options. Select the line.

35. Select **Voucher transactions**.

36. Select **Transactions**

37. Review and analyze posted transactions. As you see the original transactions have been reversed and accruals have been posted through 24 months.

38. Close all forms


 
