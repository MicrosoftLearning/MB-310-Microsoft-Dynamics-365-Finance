---
lab:
    title: 'Exercise 12: Make deposits and perform payment reversals'
    module: 'Module 2: Set up and configure financial management'
---


## Exercise 12: Make deposits and perform payment reversals

You will deposit funds into a bank and cancel it by using deposit slips.

### Create a deposit slip



1. Navigate to **Accounts receivable &gt; Payments &gt; Customer payment journal**.

2. Select the **+New** button to create a new record.

3. In the **Name** field, select journal name **CustPay**.

4. Select the **Lines** button to access the Journal voucher form.

5. From the Journal voucher form, in the **Account** field, select customer **US-003**.

6. In the **Description** field type **Deposit** to attach information about the transaction.

7. In the **Credit** field, type the deposit amount of **4100**.


8. Place a check mark in the **Use a deposit slip** field.


9. In the **Offset account type** field, note that the **Bank** is selected.

10. In the **Offset account** field, note that **USMF OPER** is selected.


11. In the **Currency** field, note that **USD** is selected.

12. In the **Method of payment** field, **Check** is selected.

13. In the **Payment reference** field, enter a reference for the payment such as **DEP001**.

14. Select the **Post** button.

15. Select **Functions**, and then select **Deposit slip**.

16. In the dialog box, enter today’s date in the **Date** field.

17. Select **OK** to generate the deposit slip. 

18. Select **OK** to view the deposit slip.

19. Close all pages

### Cancel a Deposit Slip Payment



20. Navigate to **Cash and bank management &gt; Setup &gt; Cash and bank management parameters.**

21. Expand the **General** FastTab, check that the value of the **Use review process for deposit slip payment cancellations** field is set to **Yes**. 

22. Navigate to **Cash and bank management &gt; Payment reversals &gt; Deposit slips**.

23. Select the line with the deposit slip with the amount of **4,100.00** to cancel. 

24. Select the **Cancel payment** button.

25. In the **Cancel payment** form, select a reason for cancellation from the **Reason code** list such as **ERROR**.

26. Accept the default value or modify the value in the **Reason comment** field.

27. In the **Journal name** field select **DepRev.** 

28. Note that If you would have selected **OK** without specifying a journal name**,** you would have posted the cancellation immediately, but since you specified a Journal name, and then select **OK** Dynamics 365 Finance will send the cancellation for review.

29. Navigate to **Cash and bank management &gt; Payment Reversal approvals &gt; Deposit slip payment reversal**

30. Select the journal and select **Post &gt; Post** to complete the deposit slip reversal.


 
