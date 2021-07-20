---
lab:
    title: 'Exercise 10: Create bank transaction types and bank transaction groups'
    module: 'Module 2: Set up and configure financial management'
---

## Exercise 10: Create bank transaction types and bank transaction groups

Annie, the bookkeeper at **USMF**, must create a bank transaction type for cash withdrawals. In addition, **USMF** wants the option to analyze the total charges paid to each bank. Annie will create an additional bank transaction group for bank fees and interest charges.

Follow the steps below to help Annie:

### Create a bank transaction type for cash withdrawals

1. Navigate to **Cash and bank management**, expand **Setup**, and then select **Bank transaction types**.

2. Select the **New** button to insert a new record.

3. In the **Bank transaction type** field, enter 20.

4. Enter the name Cash Withdrawal in the **Name** field.

5. Type in **110110** in the **Main account** field.


6. Close the **Bank transaction type** form.


### Create a bank transaction group for bank charges.

7. Navigate to **Cash and bank management**, expand **Setup**, and then select **Bank transaction groups**.

8. Select the **New** button to insert a new record.

9. In the **Bank transaction groups** field, enter 80.

10. Enter Bank Charges in the **Description** field.


11. In the **Bank transaction groups** form, navigate to the **Type** FastTab (section).


12. Select the **Bank transaction type** dropdown and select the bank transaction type of 07 for Fees. 

13. Verify that the **Name** field is automatically populated with the Bank transaction type name.

14. Select the **Add** button to insert a new record.

15. Select the **Bank transaction type** dropdown and select the bank transaction type of 08 for Interest charges. 

16. The **Name** field is automatically populated with the Bank transaction type name.


17. Close the form


### Define Cash and Bank Parameters

18. Navigate to **Cash and bank management**, expand **Setup**, and then select **Cash and bank management parameters**.

19. Select the **General** link if is not automatically selected.

20. Select the **Bank transaction type** that is used for **Non-Sufficient Funds** (NSF) from the **NSF** list.

21. Select the **Allow checks for bank or ledger accounts** check box to indicate whether a check can be printed for a bank or ledger account.

22. Select the **Allow check reuse** check box to indicate whether a check number can be reused if the check was printed incorrectly or the check stock was not used.

23. To require reason codes for bank transactions, select one or more of the check boxes in the **Reason code requirements** for **Require reasons for payment reversals** and **Require reasons for deposit slip payment cancellations**
