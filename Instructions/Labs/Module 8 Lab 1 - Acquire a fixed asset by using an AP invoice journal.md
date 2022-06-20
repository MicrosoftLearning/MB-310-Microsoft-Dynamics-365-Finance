---
lab:
    title: 'Lab: Acquire a fixed asset by using an AP invoice journal'
    module: 'Module 8: Configure and manage fixed assets'
---

# Lab - Acquire a fixed asset by using an AP invoice journal 

 
Contoso, Ltd. purchases a new laptop for an employee who will start next month. You receive notification from the warehouse manager that the laptop has been received at the warehouse. You must create and record the fixed asset for the laptop. 

This lab uses the USMF company. 

## Exercise 1:Set Fixed assets parameters

It is possible to automatically create a fixed asset during the purchasing process. You can set this up in the parameters in the fixed assets module.

1. Navigate to **Fixed Assets**, select **Setup**, and then select **Fixed Assets** **Parameters**. 

2. Expand the **Purchase orders** FastTab.

3. Select the **Allow asset acquisition from Purchasing** checkbox.

4. Select the **Create asset during product receipt or invoice posting** checkbox.
![](../images/Module_4_Activity_1_-_Acquire_a_fixed_asset_by_using_an_AP_invoice_journal_image1.png)

 
## Exercise 2:Create a purchase order for a fixed asset

1. Navigate to **Accounts Payable**, select **Purchase orders**, and then select **All purchase orders**.

2. Select **New** to create a new purchase order.

3. Select vendor **US-101** in the vendor field. Most fields are automatically populated.

4. Navigate to the Warehouse field in the General fasttab and select **13**. 

5. Select **OK**. 

6. Select item **1000** (FastTab Purchase order lines).

7. Expand the **Line details** FastTab.

8. Select the **Fixed assets** tab (you may need to scroll right).

9. Set the New fixed asset to **Yes**.

10. In the Fixed asset group field, select the drop-down list to open the lookup. Select the **COMP** group.

11. **Save** the purchase order. 

12. Write down the Purchase order number. You will use this number in the next exercise.

13. Close the form.
![](../images/Module_4_Activity_1_-_Acquire_a_fixed_asset_by_using_an_AP_invoice_journal_image2.png)

## Exercise 3 : Confirm the purchase order

The purchase order has been approved. You must now select and approve the order.

1. Navigate to **Accounts Payable**, select **Purchase orders**, and then select **All purchase orders**.

2. Select the PO number that you wrote down in exercise 2, step 12.

3.  Select the **Purchase** tab in the Action pane.

4. Navigate to the **Actions** section and select **Confirm**. The status of the Purchase order will change from Approved to Confirmed. 

5. **Close** the form.

## Exercise 4: Confirm receipt of the laptop
The vendor delivers the laptop. The warehouse manager posts the product receipt and lets you know that the laptop is received in the warehouse.

1. Navigate to **Accounts Payable**, select **Purchase orders**, and then select **All purchase orders**.

2. Select the PO number that you wrote down in exercise 2, step 12.

3. Select the **Receive** tab in the Action pane.

4. Navigate to the **Generate** section and select **Product receipt**. 

5. Enter **12345** in the Product receipt field.

6. Select **OK**. The following warning will display: The shipment for load could not be confirmed because it is in Shipped status.   
You can continue the exercise. The status of the Purchase order will change from Approved to Confirmed. 

7. Expand the Line details FastTab.

8. Select the **Fixed assets** tab.

10. Notice the **Fixed Asset number** field. This field is populated after receiving the item in the warehouse. 

11. Close the form.

## Exercise 5 : Register and post the vendor invoice

In this exercise you will register and post the vendor invoice for the laptop. In this example, you will perform this operation from the purchase order.

1. 'Go to Navigation pane > **Modules** > **Accounts Payable** > **Purchase orders** > **All purchase orders**.

2. Select the PO number that you wrote down in exercise 2, step 12.

3. Select the **Invoice** tab in the Action pane.

4. Navigate to the section Generate and select **Invoice**. You will see that the status of the Purchase order is **Not performed**.

5. Select **Update match status.** The status changes to Passed. 

6. Navigate to the **Number** field in the Invoice identification section and enter **456-123**.

7. Navigate to the **Invoice description** field and enter **Laptop-finance department**.

8. Navigate to the **Invoice date** field in the Invoice dates section and enter today's date.

9. Select **Post** in the Action pane. The following message displays: The vendor invoice posting process is complete for Vendor US-101, invoice 456-123. The fixed asset is acquired. 

11. Close the form.


## Exercise 6: Check the fixed asset

In this exercise you will validate that you entered the fixed asset in the system correctly. 

1. Navigate to the **Fixed Asset management** Workspace.

2. Select the **Acquired this year** tile. You will see the fixed asset. 

3. Select **Valuations** in the Action Pane to check the acquisition price.

4. Close the view.

5. Close the form.

![](../images/Module_4_Activity_1_-_Acquire_a_fixed_asset_by_using_an_AP_invoice_journal_image3.png)
