---
lab:
    title: 'Exercise 3: Configure and maintain customers'
    module: 'Module 6: Implement and manage accounts receivable and credit and collections'
---

## Exercise 3: Configure and maintain customers

The goal of the lab exercise is to apply the knowledge we’ve learned regarding the Configure and manage customers.

### Customer posting profiles

Phyllis, the Accounting Manager at Contoso, has asked Arnie, the Accounts Receivable Clerk, to set up a new posting profile for a group of retail customers.

Select the appropriate options to ensure the following:

- Entries will be created using this profile for automatic settlement.

- The application will calculate interest on outstanding balances for customers who have this profile.

- A collection letter may be issued for customers who have this profile.

- When transactions are settled in full, the transactions should not change to another posting profile.

- Transactions for the retail customers group will post to the summary account 130100 and settle account 110110.

 

1. In **USMF**, Navigate to **Accounts receivable &gt; Setup &gt; Customer posting profiles**.

2. Select **New**.

3. In the **Posting Profile** field, type **Prom**.

4. In the **Description** field, type **Promotion**.

5. On the **Table restrictions** tab, make sure that **Allow automatic settlement** to **Yes**.

6. Set the **Interest** and **Collection letter** options to **Yes**.

7. Verify that the **Close** field is blank.

8. In the Setup FastTab:

	- Select **Add**.

	- In the **Account code** field, select **group**.

	- In the **Account\Group Number** field, select **30 Retail Customers**.

	- In the **Summary account** field, select **130100**.

	- In the **Liquidity account for payments** field, select **110110**.

	- In the **Collection letter sequence** field, select **High**.

9. Close the form.

### Establish customer payment terms

1. Set up payment days:

	- In **USMF**, navigate to **Accounts receivable &gt; Payments setup &gt; Payment days**.

	- Select **New**.

	- In the **Payment day** field, enter **17** for the Payment day in the payment day field.

	- In the **Description** field, enter **17**<sup data-htmlnode="">**th**</sup> **of the month**.

	- In the **Week/Month** field, select **Month**.

	- In the **Day of month** field, enter **17**.

	- Select **Save**.

	- Close the page.

2. Set up Payment Terms:

	- Navigate to **Accounts receivable &gt; Payments setup &gt; Terms of payment**.

	- Select **New**. 

	- Terms of payment is used to define how the due dates will be calculated. The cash discount date setup is defined in a separate page.

	- In the **Terms of payment** field, enter **AWC-45**.

	- In the **Description** field, enter **Net 45 days**.

	- In the **Setup** section, select a payment method **Current month**. The payment method is used to define the start of how the due will be calculated. For example, **Net** is used if the due date is always a set number of months or days after the invoice date. **COD** can be used too when payment is required upon invoice, so a due date wouldn't be calculated. 

	- Select **Save**.

	- Close the page.

3. Set up cash discount:

	- Navigate to **Accounts receivable &gt; Payments setup &gt; Cash discounts**.

	- Select **New**.

	- In the **Cash discount** field, enter **AWC-15D5%**.

	- In the **Description** field, enter **Offer 5% if paid within 15 days**.

	- In the **Setup** section, enter the number of days used to calculate the cash discount date in **Days**. Enter **15**. If Net principle is selected, the number of days will be added to the invoice date to calculate the cash discount date.

	- Enter the **percentage** of the cash discount in **Discount percentage**. Enter **5**.

	- In **Main account for customer discounts**, enter the main account to which the cash discount will post for customer invoices. Select **403300**.

	- In the **Discount offset accounts** field, select an option. If you select 'Accounts on the invoice lines,' the cash discount will post to the same asset/expense main account on the lines of the Customer invoice. If you select **'Use main account for Customer invoices'**, the cash discount will post to the main account you define in the **Main account for vendor discounts**. For this example, select **'Use main account for vendor discounts'**.

	- Enter the **Main account for vendor discounts**, to which the cash discount will post. Select **520200**.

	- Select **Save**.

### Create a method of payment for customer payments

1. In **USMF**, Navigate to **Accounts receivable &gt; Payments setup &gt; Methods of payment**.

2. Select **New**.

3. In the **Method of payment** field, enter **AWC-EP**. The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.

4. In the **Description** field, enter **Electronic payments**.

5. Select how customers payments should be created for invoices. In the **Period** field select **Total**. This option is only used when running a payment proposal. A payment proposal could be used for customer payments when doing direct debits and pulling the funds from the customers' bank accounts.

6. Select what **Payment status** is required in order for payments to be posted. Select **Approved**.

7. When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.

8. Select the **Payment type** as **Electronic payment**. The payment type will help determine whether some validation will occur or not on the payment.

9. Navigate to the **General** FastTab.

10. Select what **Account type** payments will post to. Select **Bank**. 

11. Select the bank account into which this payment will be recorded under **Payment account**. Choose **USMF OPER**.

12. Enter the **Bank transaction type** to identify the type of payment used by your bank. Select **Deposit**. The bank transaction type is used during the bank reconciliation process and can make reconciliation easier.

13. This payment method will temporarily post to a bridging account. Set the **Bridging posting** to **Yes**. The payment will temporarily post to a Ledger account until it clears the bank at which time the payment will move to the bank account you defined here.

14. Enter the main account used for the **Bridging account** posting. Select **130730**. This is the main account to which the payment will temporarily post if using bridging.

15. Use the **File formats** tab to define setting for electronic payments.

16. Use the **Payment control** tab to define fields that are mandatory. For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.

17. Use the **Payment attributes** tab to define which payment attributes you want to use for this method of payment.

18. Select **Save**.

### Create payment fees for customer payments

1. Create the payment fee:

	- In **USMF**, Navigate to **Accounts receivable &gt; Payments setup &gt; Payment fee**.

	- Select **New**.

	- In the **Fee ID** field, enter **W01**. The **Fee ID** displays on payment journals, so make it descriptive to understand what fee is being assessed.

	- In the **Name** field, enter **Wire**.

	- In the **Fee description** field, enter **Bank fee for wire transfer**.

	- Select whether the fee will be charged to the **Customer** or a **Ledger account**.

	- If the customer is assessed the fee, select **Customer**. If the fee will be charged to your organization as an expense, select **Ledger**. For this task, select **Customer**.

	- Select the type of journal that can use this payment fee. If these fees are used for customer payments, the journal type will likely be **Customer payment**.

	- Select **Save**.

2. Set up the payment fee:

	- Select **Payment fee setup**. The Payment fee setup is used to define the criteria for when the payment fee will be assessed. For example, you can define that the fee will be calculated if the bank account is **USMF OPER**, and the method of payment is **check**.

	- Select either **Table**, **Group** or **All** to define which bank accounts will be assessed this fee. If you select **All**, all bank accounts could be assessed this fee. If you select **Table**, only the bank account you select could be assessed this fee. If you select **Group**, only the bank accounts in the selected bank group could be assessed this fee.

	- Select either a **bank group** or a **bank account** for the **Bank relation**. If you selected **Table**, the lookup will display bank accounts. If you selected **Group**, the lookup will display **bank groups**.

	- Select the **Method of payment** for which this fee will be assessed. For example, you may assess a fee to your customers if they send payments as a check, rather than as an electronic payment.

	- Enter a **payment currency**. The payment currency is used as an additional criterion for whether the fee will be assessed. For example, your bank may charge an extra fee for payments received in **USD** currency, since they normally only transact in **EUR** currency.

	- Select whether the fee will be a **percent**, **amount** or **interval**. Enter either **percentage** or **amount** of the fee. If the **Percentage/Amount** field is **Percent**, then the value enter here will be a percentage. If the **Percentage/Amount** field is **Amount**, then the value you enter here will be an amount. If the **Percentage/Amount** field is **Interval**, use the **Interval** tab to define the tiers.

	- In the **Fee currency** field, select the currency of the fee. This is the currency in which the fee will be created.

	- Select **Save**.

### Create a Customer

USMF has begun working with a new customer, Woodgrove Bank. Arnie, the Accounts Receivable Clerk, must set up this new customer.

1. Navigate to **Accounts receivable &gt; Customers &gt; All customers**.

2. Select **New**.

3. In the **Customer account** field, enter **US-069**.

4. In the **Type** field, select **Organization**.

5. In the **Name** field, type **Woodgrove Bank**.

6. In the **Customer group** field, select customer group **20**.

7. Select **Save**.

8. Select the **Credit and collections** FastTab.

9. In the **Credit limit** field, enter **10000**.

10. Select the **Invoice and delivery** FastTab.

11. In the **Mode of delivery** field, select **20**, Air.

12. In the **Sales tax group** field, select **CA**.

13. Select the **Payment defaults** FastTab.

14. In the **Terms of payment** field, select **Net10**.

15. In the Method of payment field, select **CHECK**.

16. Close the form.

 
