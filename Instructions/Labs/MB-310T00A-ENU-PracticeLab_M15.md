### Before you begin

To get the most out of this exercise and the other exercises that are included
with this module, we recommend that you have the standard sample data available
in Finance and Operations that is installed using Lifecycle Services (LCS).

Exercise - Record a vendor invoice and match it against a received quantity
===========================================================================

When you receive an invoice from a vendor for goods or services on a purchase
order, the business processes might require that the goods or services be
received before the invoice can be approved for payment.

Make sure that the **Invoice matching** configuration key is selected.

On the **Accounts payable parameters** page, ensure that the **Enable invoice
matching validation** option is selected, the **Post invoice with
discrepancies** field is set to **Require approval**, and the **Line matching
policy** field is set to **Three-way matching**.

This exercise uses the USMF demo company.

The accounts payable manager or accounting manager role would perform these
steps.

Create a purchase order
-----------------------

1.  Go to **Accounts payable \> Purchase orders \> All purchase orders**.

2.  Click **New**.

3.  In the **Vendor account** field, click the drop-down button to open the
    lookup.

4.  In the **Vendor account** field, select **US-103 Rain Projectors**.

5.  In the **Warehouse** field select 11

6.  Click **OK**.

7.  Make a note of the **purchase order number**, you will need this for the
    next exercise. The purchase order number will be shown on the upper right of
    the page, as shown below.

![Accounts payable \> Purchase Orders \> All purchase orders. 00001126 : US-103 - Rain Projectors](media/c27cb9802ff12464dd9297f1b4445e05.jpg)

1.  Click **Add line**.

2.  In the **Item number** field, select A1000.

3.  In the **Quantity** field type 60.

4.  On the Action Pane, click **Purchase**.

5.  Click **Confirm**.

Post a product receipt
----------------------

1.  On the Action Pane, click **Receive**.

2.  Click **Product receipt**.

3.  In the **Product receipt** field, type **RainPR1**.

4.  Click **OK**.

Record and match a vendor invoice to a product receipt
------------------------------------------------------

1.  On the Action Pane, click **Invoice**.

2.  Click **Invoice**.

3.  In the **Number** field, type **RainInv1**.

4.  Click **Default from** to open the drop-down menu.

![Default quantity for lines \> Product receipt quantity](media/deb91754f0685e159efe03e06260a0bd.png)

1.  In the **Default quantity** for lines field, select **Product receipt
    quantity**.

2.  Click **OK**.

3.  In the message about changing the setting, click **Yes**.

4.  Click **Match product receipts**.

5.  Verify the status of **Match product receipts to invoice**.

![Match product receipts to invoice \> Overview \> Match checkbox checked](media/985131a3f4b2ffade6767df0c1b2635d.jpg)

1.  Click **OK**.

2.  On the Action Pane, click **Review**.

3.  Click **Matching details**.

4.  Verify results.

5.  Do **NOT** post the invoice.

6.  Close all pages.

Exercise - Use the vendor invoice matching policy 
==================================================

You must complete the previous exercise before starting this one. 

This exercise will help you create a vendor invoice from a purchase order and
view the results of matching the purchase order, receipt, and invoice (three-way
matching). 

 

Create a purchase order and change the line matching policy 
------------------------------------------------------------

1.  Go to **Accounts payable \> Purchase orders \> Purchase orders received but
    not invoiced**. 

2.  Select the purchase order that you created and noted in the previous
    exercise. 

3.  On the Action Pane, click **Invoice**. 

4.  Click **Invoice**. 

5.  In the **Number** field, verify the value **RainInv1** is saved from
    exercise 1. This can be modified. 

6.  In the **Invoice description** field, type **Invoice matching demo**. 

7.  In the **Invoice date** field, enter today’s date.  

8.  In the **Unit price** field, enter 1200. 

9.  Click **Add line**. 

10. In the **Item number** field, click the drop-down button to open the
    lookup. 

11. In the list, find the **item number** S0001 installation charge 

12. Note the **Match status** field. The matching has not been performed. 

13. Click **Update match status**. Note the **Match status** field, the status
    is **Failed**. 

14. On the Action Pane, click **Review**. 

15. Click **Matching details**. The new line with services does not need to be
    matched so the status stays **Not performed**. Also, A0001 has a price
    discrepancy. 

16. Close the page.  

17. Select the invoice line for item A0001 that you have received. The line with
    the product receipt was matched but there is a mismatch of quantity or
    price, so it fails. 

18. In the **Unit price** field, enter **12**.  

19. Click **Update match status**.  

20. Now that the unit price matches, the **Match status** field is updated to
    **Passed**. If your policy allows discrepancies or if matching is only a
    warning, you can still post the invoice. 

21. Click **Post**. 

22. The page automatically closes. 

23. Note that the purchase order is no longer listed on the **Purchase orders
    received but not invoiced** page because it has been now posted. 
