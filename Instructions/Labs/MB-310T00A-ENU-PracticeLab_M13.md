Exercise: Configure accounts payable components
===============================================

This exercise shows how to configure the components of Accounts payable in the
USMF demo company. You will perform the following tasks:

-   Define vendor payment fees.

-   Set up charge codes for Accounts payable.

-   Create charges groups for vendors.

-   Create item charges groups.

-   Define auto charges.

Define vendor payment fees
--------------------------

1.  Go to **Accounts payable \> Payment setup \> Payment fee**.

2.  Click **New**.

3.  In the **Fee ID** field, type a value. This field should describe when this
    fee will be used, such as "EFT_Fee".

4.  In the **Name** field, type a value.

5.  In the **Fee description** field, type a value. This description provides
    more detail about when the fee is assessed.

6.  In the **Charge** field, select either **Vendor** or **Ledger**. **Vendor**
    is used when the fee will be assessed to the vendor. **Ledger** is used when
    the fee will be expensed to your organization.

7.  Enter a main account for where the fee will be expensed. This option is only
    available when selecting **Ledger** as the **Charge** option.

8.  Select the journal on which this fee can be used. For a vendor payment fee,
    you would select the journal **Vendor disbursement**.

9.  Click **Save**.

10. Click **Payment fee setup**.

11. Continue to **Payment fee setup** to define when the fee should default onto
    the journal you selected.

12. Select either **Table**, **Group,** or **All**. **Table** is used to select
    a single bank account, **Group** is used to select a bank group, and **All**
    is to use this fee setup for all bank accounts

13. Select either a bank group or a bank account. The lookup will show bank
    group if you selected **Group**, and will show bank accounts if you selected
    **Table**.

14. Select the **Method of payment** for when this fee will be assessed.

15. Select the **Payment specification** for the selected method of payment. The
    **Payment specification** is used with electronic fund transfer methods of
    payment.

16. Select whether the fee is a percentage, amount, or interval.

17. Enter the percentage or amount of the fee. If the fee is a percentage, enter
    the percentage. If the fee is an amount, enter the amount of the fee. If the
    fee is an interval, use the **Interval** tab to defined the tiered fees.

18. In the **Fee currency** field, select the currency in which the fee will be
    assessed. This currency is for the fee. The payment currency is used to
    define when the fee rule should be assessed based on the payment's currency.
    For example, your bank might charge a fee when a payment is made in **EUR**,
    but all other payments aren't assessed a fee.

19. Click **Save**.

Set up charge codes for Accounts payable
----------------------------------------

1.  Go to **Accounts payable \> Charges setup \> Charges code**.

2.  Click **New**. In the **Charges code** field, type a code for the charge.

3.  In the **Description** field, type a description of the charge.

4.  Optional: In the **Item sales tax group** field, select a sales tax group.

5.  Optional: In the **Maximum amount** field, type the maximum amount that is
    allowed for this charges code. This field is used to validate charges for
    vendor invoices. You can enable the validation of charges using the
    **Accounts payable parameters** page. In the **Invoice validation** area,
    enable the **Enable invoice matching validation** option.

6.  On the **Posting** FastTab, specify how the charge is automatically debited
    and credited.

7.  If you selected **Ledger account** as the debit type or credit type, specify
    a posting type in the **Debit posting** and **Credit posting** fields, and
    specify the main account in the **Debit account** and **Credit account**
    fields.

8.  To enable the comparison of charges values for an invoice that contains the
    charges from the corresponding purchase order header or lines, enable the
    **Compare purchase order and invoice values** option.

Create charges groups for vendors.
----------------------------------

1.  Go to **Accounts payable \> Charges setup \> Vendor charges group**.

2.  In the **Charges group** field, enter a code for the charges group. The code
    can contain both letters and numbers.

3.  In the **Description** field, enter a description of the charges group.

4.  Close the page to save your changes.

Create item charges groups
--------------------------

1.  Go to **Accounts payable \> Charges setup \> Item charge groups**.

2.  Click **New** to create an item charges group.

3.  In the **Charges group** field, enter a code for the group. The code can be
    alphanumeric.

4.  In the **Description** field, enter a description for the group.

5.  Close the page to save your changes.

Define auto charges
-------------------

1.  Go to **Accounts payable \> Charges setup\> Auto charges**.

2.  Click **New** to define a new auto charge.

3.  In the **Level** field, select the level to apply the auto charge to from
    the following values:

    -   **Main** - Applies charges to the order header.

    -   **Line** - Applies charges to the order lines.

4.  Select an account in the **Account code** field.

    -   **Table** - To assign charges to a specific vendor.

    -   **Group** - To assign charges to a miscellaneous charges group.

    -   **All** – To assign charges to all vendors.

5.  In the **Vendor relation** field, select a specific vendor if you selected
    **Table**, or select a vendor charges group if you selected **Group**.

6.  In the **Item code** field, select an item code. You can select an item code
    only when you define auto charges at the lines level. If you select
    **Table**, the system assigns charges to a specific item, **Group** assigns
    charges to an item charges group, or **All** assigns charges to all items.

7.  In the **Item relation** field, select a specific item if you selected
    **Table**, or select an item charges group if you selected **Group**.

8.  Expand the **Lines** FastTab to define the charges and the charges rates to
    use when the current auto charge is applied.

9.  In the **Currency** field, select the currency to use to calculate the
    charge.

10. In the **Charges code** field, select the code for the charge.

11. Specify how to calculate the charge in the **Category** field and enter a
    value in the **Charges value** field.
