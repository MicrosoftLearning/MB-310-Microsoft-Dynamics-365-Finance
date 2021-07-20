---
lab:
    title: 'Exercise 9: Manage charges'
    module: 'Module 4: Implement and manage accounts payable'
---

## Exercise 9: Manage charges

### Create a Charges Code

You are the Accounts Payable Coordinator at Contoso Entertainment Systems USA, and you must create a new charges code for transport charges that will be added to various items and charged by the vendor.

Create a new charge for transportation fees with the following specifications:

- Name of the charges code: TRANSTO

- Description: Transportation Fee to our sites

- Account: 411400

This fee does not require an item sales tax group.

### Create a charges code.

1. Navigate to **Accounts payable** **&gt;** **Setup &gt; Charges setup &gt; Charges code**.

2. Select **New**.

3. Charges code: Enter **TRANSTO.**

4. Description: Enter **Transportation Fee to our sites**.

5. Change to the **Debit** section in the **Posting** FastTab.

6. **Type**: Select **Ledger account.**

7. **Posting**: Select **Payment fee.**

8. **Account**: Select **411400.**

9. Change to the **Credit** section.

10. **Type**: Select **Customer/Vendor.**

11. Select **Save**.

### Create a Vendor Charges Group

Vendor Fabrikam has two vendor accounts that we purchase items from. They have decided to add an additional 15 percent freight charges for all our purchase orders.

As the Accounts Payable Administrator, you are asked to set up a new vendor charges group and assign the code to vendors US-101 and US-104. The name of the new charges group is "06" and the description is "Freight 15%".

### Create a vendor charges group.

1. Navigate to **Accounts payable &gt;** **Setup &gt;** **Charges setup** **&gt;** **Vendor charges group**.

2. Select **New**.

3. Charges group: Enter **06**. 

4. Description: Enter **Freight 15%**. 

5. Select **Save**.

 

### Update vendors to use the new vendor charges group.

1. Navigate to **Accounts payable** > **Vendors** > **All** **vendors**.

2. Open the vendor record for vendor **US-101** (Fabrikam Electronics).

3. Select **Edit**.

4. Open the **Purchase order defaults** FastTab.

5. Charges group: Select **06** (Freight 15%).

6. Select **Save**.

7. Close the vendor record.

8. Open the vendor record for vendor **US-104** (Fabrikam Supplier).

9. Select **Edit** if available.

10. Open the **Purchase order defaults** FastTab.

11. Charges group: Enter or select **06** (Freight 15%).

12. Select **Save**.

13. Close the vendor record.

 

### Create an Item Charges Group

Because of the large quantity and weight of items bought, Datum Receivers (US-105) applies a 15 percent freight charge for all orders.

### Create an item charges group.

1. Navigate to **Accounts payable** **&gt;** **Charges setup**, and then to **Item charge groups**.

2. Select **New**.

3. Charges group: enter **123**.

4. Description: enter **15% Freight Charge**.

5. Select **Save**.

### Create an Automatic Charge

You have a certain set of charges that apply on all purchases from certain vendors.

Set up an automatic charge that will apply automatically to all purchases, where it will charge 15% delivery charge to all orders at the line level and applies for only a certain vendor charges group (06) and a certain item charges group (123).

1. Navigate to **Accounts payable &gt;** **Charges setup**, and then to **Automatic charges**.

2. **Level**: Select **Line**.

3. Select **New**.

4. **Account code**: select **Group**.

5. **Vendor relation**: select **06** (Freight 15%)

6. **Item code**: select **Group**.

7. **Item Relation**: select **123** (15% Freight Charge).

8. Select **Save**.

9. In the **Lines** FastTab Charges code: select **TRANSTO** (Transportation Fee).

10. Category: select **Percent**.

11. Charges value: enter **15.00**.

12. Select **Save**.

 

 

### How to: Create charges groups for vendors.



1. Select **Accounts payable &gt; Charges setup &gt; Vendor charges group**.

2. Select **+New** and in the **Charges group** field, enter a code for the charges group. The code can contain both letters and numbers.

3. In the **Description** field, enter a description of the charges group.

4. Close the form to save your changes.


 

### How to: Create item charges groups



1. Select **Accounts payable &gt; Charges setup &gt; Item charge groups**.

2. Select **New** to create an item charges group.

3. In the **Charges group** field, enter a code for the group. The code can be alphanumeric.

4. In the **Description** field, enter a description for the group.

5. Close the form to save your changes.


### How to: Define auto charges



1. Select **Accounts payable &gt; Charges setup &gt; Automatic charges**.

2. Select **New** to define a new auto charge.

3. In the **Level** field on the left, select the level to apply the auto charge to from the following values: **Header** which applies charges to the order header, and **Line** that apply charges to the order lines.

4. Select an account in the **Account code** field to be **Table**, to assign charges to a specific vendor, **Group** to assign charges to a miscellaneous charges group, or **All** which assigns charges to all vendors.

5. In the **Vendor relation** field, select a specific vendor if you selected **Table**, or select a vendor charges group if you selected **Group**.

6. In the **Item code** field, select an item code. You can select an item code only when you define auto charges at the lines level. If you choose **Table** system assigns charges to a specific item, or **Group** to assign charges to an item charges group, or **All** to assign charges to all items.

7. In the **Item relation** field, select a specific item if you selected **Table**, or select an item charges group if you selected **Group**.

8. Expand the **Lines** FastTab to define the charges and the charges rates to use when the current auto charge is applied.

9. In the **Currency** field, select the currency to use to calculate the charge.

10. In the **Charges code** field, select the code for the charge.

11. Specify how to calculate the charge in the **Category** field and enter a value in the **Charges value** field.
