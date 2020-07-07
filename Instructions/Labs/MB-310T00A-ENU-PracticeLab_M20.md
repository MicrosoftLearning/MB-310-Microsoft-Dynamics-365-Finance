Exercise 1: Set up post-dated checks
====================================

The role of this procedure is Treasurer. This procedure uses the USMF demo
company.

Set up postdated checks
-----------------------

1.  Go to **Cash and bank management \> Setup \> Cash and bank management
    parameters**.

2.  Click the **Postdated checks** tab.

3.  Enable or disable the **Enable postdated checks** option.

4.  Enable or disable the **Post journal entries for postdated checks** option.

5.  In the **Clearing account for issued checks** field, specify the desired
    values.

6.  In the **Clearing account for received checks** field, specify the desired
    values.

7.  In the **General journal for clearing entries** field, type a value.

8.  In the **Transfer postdated checks to this vendor payment journal** field,
    type a value.

9.  In the **Withholding tax clearing account** field, specify the desired
    values.

10. Click **Save**.

11. Close the page.

12. Go to **Accounts payable \> Payment setup \> Methods of payment**.

13. Click **New**.

14. In the **Method of payment** field, type a value.

15. Select the **Postdated check clearing posting** option to indicate that the
    check amount is posted to a clearing account.

16. In the Account type field, select 'Bank'. The offset account of the payment
    method will be a bank.

17. In the **Payment account** field, specify the desired values. Select the
    bank account that is used to deduct the invoice amount.

18. Close the page.

19. Go to **Accounts receivable \> Payment setup \> Methods of payment**

20. Click **New**.

21. In the **Method of payment** field, type a value.

22. Select the **Postdated check clearing posting** option to indicate that the
    check amount is posted to a clearing account.

23. In the Account type field, select 'Bank'. The offset account of the payment
    method will be a bank.

24. In the **Payment account** field, specify the desired values. Select the
    bank account that is used to deduct the invoice amount.

25. Close the page.

Register the details of postdated check for a customer
------------------------------------------------------

1.  In USMF, navigate to **Accounts receivable \> Payments \> Payment journal**.

2.  Click **New**.

3.  In the **Name** field, type a value.

4.  Click **Lines**.

5.  In the **Account** field, specify the desired values.

6.  In the **Credit** field, enter the amount specified in the postdated check.

7.  Click the **Payment** tab.

8.  In the Method of payment field, select the method of payment for the
    postdated check.

9.  Click the **Postdated checks** tab.

10. In the **Maturity date** field, enter the date when the postdated check is
    due for payment.

11. In the **Issuing bank branch** field, enter the bank details of the
    postdated check.

12. In the **check number** field, type a value.

13. In the **Issuing bank name** field, enter the bank details of the postdated
    check.

14. Click **Post**.

15. Close the page.

A Treasurer should follow the steps below to register the details of postdated check for a vendor
-------------------------------------------------------------------------------------------------

1.  Go to **Accounts payable \> Payments \> Payment journal**

2.  Click **New**.

3.  In the **Name** field, type 'VendPay'.

4.  Click **Lines**.

5.  In the **Account** field, specify the desired values.

6.  In the **Debit** field, enter a number.

7.  In the **Method of payment** field, select the method of payment for the
    postdated check

8.  In the list, find and select the desired record.

9.  Click the **Postdated checks** tab.

10. In the **Check number** field, enter or modify the number of the postdated
    check.

11. In the **Issuing bank name** field, enter the bank details for the issuing
    bank.

12. Click the **List** tab.

13. Click **Post**.

14. Close the page.

15. Click the **Postdated checks** tab.

16. Go to **Credit and collections \> Inquiries and reports \> Payments \>
    Customer postdated checks**.

17. Click **Settle**.

18. Click **Settle clearing entries**, settle the customer account for the check
    transaction.

19. Close the page.

20. Go to **General ledger \> Journal entries \> General journals**.

21. In the **Show** field, select an option.

22. Enable or disable the **Show user-created** only option.

23. In the list, find and select the desired record.

24. Click **Lines**.

25. Click **Voucher**.

26. Close the page.

27. Go to **Accounts payable \> Payments \> Vendor postdated checks**.

28. Click **Settle**.

29. Click **Settle clearing entries**. Settle the vendor account for the check
    transaction.

30. Close the page.

31. Go to **General ledger \> Journal entries \> General journals**.

32. In the **Show** field, select 'All'.

33. Enable or disable the **Show user-created only** option.

34. Click **Lines**.

35. Click **Voucher**.

36. Close the page.
