---
lab:
    title: 'Exercise 4: Create and configure customer posting profile'
    module: 'Module 6: Implement and manage accounts receivable and credit and collections'
---

## Exercise 4: Create and configure customer posting profile

**Note**: You need to complete Exercise 2

1. Navigate to **Accounts receivable &gt; Setup &gt; Customer posting profiles**.

2. Select **New**.

3. In the **Posting profile** field, type **'ARPP'**.

4. In the **Description** field, type 'Customer posting profile'.

5. Add a Table profile:

	- Select **Add**.

	- In the **Account/Group number** field, type **US-0017**.

	- In the **Summary account** field, specify the values **'130100'**.

	- In the **Collection letter sequence** field, enter or select **Low**.

	- In the **Interest code** field, enter or select **2M-5%**.

6. Add a Group profile for 30:

	- Select **Add**.

	- In the **Account code** field, select **'Group'**.

	- In the **Account/Group number** field, type **'30'**.

	- In the **Collection letter sequence** field, enter or select **High**.

	- In the **Interest code** field, enter or select **1M-3%**.

7. Add a Group profile for 90:

	- Select **Add**.

	- In the **Account code** field, select **'Group'**.

	- In the **Account/Group number** field, type **'90'**.

	- In the **Summary account** field, specify the values **'130300'**.

8. Add an All profile:

	- Select **Add**.

	- In the **Account code** field, select **'All'**.

	- In the **Summary account** field, specify the values **'130100'**.

	- In the **Liquidity account** for payments field, specify the values **'110110'**.

	- In the **Collection letter sequence** field, enter or select **High**.

	- In the **Interest code** field, enter or select **1M-2%**.

	- Select **Save**.

	- Close the page.

9. Navigate to **Accounts receivable &gt; Setup &gt; Accounts receivable parameters**.

10. Select the **Ledger and sales tax** tab.

11. In the **Posting profile** field, enter or select **ARPP**.

12. Close the page.

