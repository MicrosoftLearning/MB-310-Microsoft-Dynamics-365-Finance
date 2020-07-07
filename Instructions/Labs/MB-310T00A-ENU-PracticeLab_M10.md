**Before you begin**

To get the most out of this exercise, we recommend that you have the standard
sample data available in Finance and Operations that is installed via Lifecycle
services.

Exercise: Set up and use intercompany accounting
================================================

You need to set up and use intercompany accounting between **USP2** and
**USMF**. These companies are using the same chart of accounts.

In this exercise, you will:

1.  Configure intercompany accounting.

2.  Use intercompany accounting with general journals.

3.  Use audit trails to verify the intercompany accounting posting.

Configure intercompany accounting
---------------------------------

1.  Select **USP2** from the company’s dropdown.

2.  Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**.

3.  Click **New**.

4.  In the **Main account** field, type **100100**.

5.  In the **Name** field, type **Due to USMF**.

6.  In the **Main account type** field, select **Balance sheet**.

7.  Click **New**.

8.  In the **Main account** field, type **100101**.

9.  In the **Name** field, type **Due from USMF**.

10. In the **Main account type** field, select **Balance sheet**.

11. Click **Save**.

12. Close all pages.

13. Change company to **USMF**.

14. Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**.

15. Verify the two accounts that you created in the steps 4 and 8 are listed
    considering that the two companies are sharing the same chart of account.

16. Click **New**.

17. In the **Main account** field, type **100106**.

18. In the **Name** field, type **Due to USP2**.

19. Click **New**.

20. In the **Main account** field, type **100107**.

21. In the **Name** field, type **Due from USP2**.

22. Close the page.

23. Go to **General ledger \> Posting setup \> Intercompany accounting**.

24. Click **New**.

25. In the **Originating company** field, select **USMF**.

26. In the **Debit account** field, select **Due from USP2**.

27. In the **Credit account** field, select **Due to USP2**.

28. In the **Destination company** field, select **USP2**.

29. In the **Debit account** field, select **Due to USMF**.

30. In the **Credit account** field, select **Due from USMF**.

31. In the **Journal** field, enter or select a daily journal name from
    **USP2**.

32. Click **Create reciprocal relationship**.

33. In the **Journal** field, enter or select a daily journal name from
    **USMF**.

34. Click **Save**.

35. Close the page.

Use intercompany accounting with general journals
-------------------------------------------------

1.  Go to **General ledger \> Journal entries \> Global general journals.**

2.  Click **New journal** to open the drop dialog.

3.  In the **Company** field, select **USMF**.

4.  In the **Name** field, select a daily journal name.

5.  Click **OK**.

6.  Click **Lines**.

7.  In the **Account type** field, select **Bank**.

8.  In the **Account** field, specify the values **USMF OPER**.

9.  In the **Description** field, type **Wire**.

10. Set **Credit** to **1000000**.

11. In the **Offset company** field, select **USP2**.

12. In the **Offset account type** field, select **Bank**.

13. In the **Offset account** field, specify the values **USP2 OPER**.

14. Click **Inquiries**.

15. Click **Balance control**.

16. View the results.

17. Click **Close**.

18. Click **Validate**.

19. Click **Validate**.

20. Click **Post**. Two vouchers have been posted, one per legal entity.

21. Close the page.

22. **Refresh** the page.

23. Close the page.

Use audit trails to verify the intercompany accounting posting
--------------------------------------------------------------

1.  Go to **General ledger \> Inquiries and reports \> Audit trail**.

2.  Click **Voucher transactions**. Review the intercompany transactions.

3.  Click **Related voucher** to view the intercompany in the destination
    company.

4.  Close the **Related voucher** page.

5.  Close the **Voucher transactions** page.

6.  **Refresh** the page.Switch to **USP2** company.

7.  Go to **General ledger \> Inquiries and reports \> Audit trail**.

8.  Click **Voucher transactions**. Review the intercompany transactions.

9.  Close the **Voucher transaction** page.

10. Close the **Audit trail** page.

11. Go to **Cash and bank management \> Bank accounts \> Bank accounts**.

12. Click **Balance**.

13. Click **OK**.

14. Click **Transactions**.

15. Click **Voucher**.

16. Close all pages.
