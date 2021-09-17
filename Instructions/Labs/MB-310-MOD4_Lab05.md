---
lab:
    title: 'Exercise 5: Use the vendor invoice matching policy'
    module: 'Module 4: Implement and manage accounts payable'
---

## Exercise 5: Use the vendor invoice matching policy

You must have completed exercise 4. This exercise will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (Three-way matching).

### Create a purchase order and change the line matching policy

1. Navigate to **Accounts payable &gt; Purchase orders &gt; Purchase orders received but not invoiced**.

2. Select the purchase order that you created. You have made a note of the purchase order number in exercise 4.

3. On the Action Pane, select **Invoice**.

4. Select **Invoice**.

5. In the **Number** field, verify the value **RainInv1** is saved from exercise 4. This can be modified.

6. In the **Invoice description** field, enter **Invoice matching demo**.

7. In the **Invoice date** field, enter today’s date, or enter ‘t’ and tab for it to fill today. 

8. In the **Unit price** field in the **Lines** section, enter 1200.

9. Select **Add line**.

10. In the **Item number** field, select the drop-down button to open the lookup.

11. In the list, find the **item number** S0001 installation service.

12. Note the **Match status** field. The matching has not been performed.

13. Select **Update match status**. Note the **Match status** field, the status is failed.

14. On the Action Pane, select **Review**.

15. Select **Matching details**. The new line with services does not need to be matched so the status stays "Not performed". Also, A0001 has a price discrepancy.

16. Close the form. 

17. Select the invoice line for item A0001 that you have received. The line with the product receipt was matched but there is a mismatch of quantity or price, so it fails.

18. In the **Unit price** field, **12**. 

19. Select **Update match status**. 

20. Now that the unit price matches, the **Match status** field is updated to **Passed**. If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.

21. Select **Post**.

22. The page automatically closes.

23. Note that the purchase order is no longer listed in **Purchase orders received but not invoiced** list page since it has been now posted.

 

