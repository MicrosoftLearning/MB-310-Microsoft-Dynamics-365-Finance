---
lab:
    title: 'Exercise 4: Record vendor invoice and match against received quantity'
    module: 'Module 4: Implement and manage accounts payable'
---


## Exercise 4: Record vendor invoice and match against received quantity

The goal of the lab exercise is to apply the knowledge we’ve learned regarding the Use reversals in Accounts payable. 

### Scenario

When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment. Before you begin, make sure that the Invoice matching configuration key is selected.

In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.

This procedure uses the USMF demo company. The accounts payable manager or accounting manager role would perform these steps.

### Create a purchase order

1. Navigate to **Accounts payable &gt; Purchase orders &gt; All purchase orders**.

2. Select **+New**.

3. In the **Vendor account** field, select the drop-down button to open the lookup.

4. Select **US-103 Rain Projectors**.

5. Select **OK**.

6. Make a note of the **purchase order number**, you will need this for Exercise 5. 

7. Navigate to the **Purchase order lines** section.

8. In the Item number field, select **A0001**.

9. Select a **Warehouse**.

10. In the **Quantity** field enter **60**.

11. In the Line details section Product tab, select a **Location** if there isn’t one.

12. On the Action Pane, select **Purchase**.

13. Select **Confirm**.

### Post a product receipt

14. On the Action Pane, select **Receive**.

15. Select **Product receipt**.

16. In the **Product receipt** field, enter **RainPR1**.

17. Select **OK**.

Record and match a vendor invoice to a product receipt

18. On the Action Pane, select **Invoice**.

19. Select **Invoice**.

20. In the Number field, enter **RainInv1**.

21. Select **Default from**: to open the drop dialog.

22. In the **Default quantity** for lines field, select **Product receipt** **quantity**.

23. Select **OK**.

24. If you get a message indicating that “**If you change this setting, unsaved changes that you made to the lines in this form will be discarded. If the invoice is on hold or in a pending state, the saved changes will not be affected. Are you sure that you want to change this setting?”** select **Yes**.

25. Select **Match product receipts**.

26. Verify the status of **Match product receipts to invoice**.

27. Select **OK**.

28. On the Action Pane, select **Review**, perhaps in the ellipsis.

29. Select **Matching details**.

30. Verify results.

31. Do NOT **Post** the invoice.

32. Close all pages.

 
