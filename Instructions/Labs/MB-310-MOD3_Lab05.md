---
lab:
    title: 'Exercise 5: Configure Payment fees'
    module: 'Module 3: Implement and manage shared configuration for AP and AR'
---


## Exercise 5: Configure Payment fees

### Set up vendor payment fees. This task uses the USMF demo company.

1. Navigate to **Accounts payable &gt; Payment setup &gt; Payment fee**.

2. Select **+New**.

3. In the **Fee ID** field, type a value. This field should describe when this fee will be used, such as "EFT_Fee".

4. In the **Name** field, type a value.

5. In the Fee description field, type a value. This description to provide more detail on when the fee is assessed.

6. In the **Charge** field, select either **Vendor** or **Ledger**. **Ledger** is used when the fee will be expensed to your organization. **Vendor** is used when the fee will be assessed to the vendor.

7. Enter a main account for where the fee will be expensed. This option is only available when selecting Ledger as the Charge option.

8. Select the journal on which this fee can be used. For a vendor payment fee, you would select the journal 'Vendor disbursement.'

9. Select **Save**.

10. Select **Payment fee setup** to define when the fee should default onto the journal you selected.

11. Select either **Table**, **Group** or **All**. **Table** is used to select a single bank account, **Group** is used to select a bank group, and **All** is to use this fee setup for all bank accounts

12. Select either a bank group or a bank account. The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.

13. Select the **Method of payment** for when this fee will be assessed.

14. Select the **Payment specification** for the selected method of payment. The **Payment specification** is used with electronic fund transfer methods of payment.

15. Select whether the fee is a percentage, amount or interval.

16. Enter the percentage or amount of the fee. If the **Fee** is a percentage, enter the percentage. If the Fee is an amount, enter the amount of the fee. If the Fee is an interval, use the Interval tab to defined the tiered fees.

17. In the Fee currency field, select the currency in which the fee will be assessed. This currency is for the fee. The payment currency is used to define when the fee rule should be assessed based on the payment's currency. For example, your bank may charge a fee when a payment is made in **EUR**, but all other payments aren't assessed a fee.

18. Select **Save**.



  
‎ 

### Set up Customer payment fees. This task uses the USMF demo company.

1. Navigate to **Accounts receivable &gt; Payments setup &gt; Payment fee**.

2. Select **+New**.

3. In the **Fee ID** field, type a value. This field should describe when this fee will be used, such as "Wire".

4. In the **Name** field, type a value.

5. In the **Fee description** field, type a value. This description provides more detail on when the fee is assessed.

6. In the **Charge** field, select either **Customer** or **Ledger**. **Ledger** is used when the fee will be expensed to your organization. **Customer** is used when the fee will be assessed to the Customer.

7. Enter a main account for where the fee will be expensed. This option is only available when selecting Ledger as the Charge option.

8. Select the journal on which this fee can be used. For a Customer payment fee, you would select the journal 'Customer payment.'

9. Select **Save**.

10. Select **Payment fee setup** to define when the fee should default onto the journal you selected.

11. Select either **Table**, **Group** or **All**. **Table** is used to select a single bank account, **Group** is used to select a bank group, and **All** is to use this fee setup for all bank accounts.

12. Select either a bank group or a bank account. The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.

13. Select the **method of payment** for when this fee will be assessed.

14. Select the **Payment specification** for the selected method of payment. The **Payment specification** is used with electronic fund transfer methods of payment.

15. Select whether the fee is a percentage, amount or interval.

16. Enter the percentage or amount of the fee. If the **Fee** is a percentage, enter the percentage. If the Fee is an amount, enter the amount of the fee. If the Fee is an interval, use the Interval tab to defined the tiered fees.

17. In the **Fee currency** field, select the currency in which the fee will be assessed. This currency is for the fee. The payment currency is used to define when the fee rule should be assessed based on the payment's currency. For example, your bank may charge a fee when a payment is made in **EUR**, but all other payments aren't assessed a fee.

18. Select **Save**.

 
