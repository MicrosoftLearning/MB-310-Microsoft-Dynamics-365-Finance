---
lab:
    title: 'Exercise 3: Create and configure vendor posting profile'
    module: 'Module 4: Implement and manage accounts payable'
---


## Exercise 3: Create and configure vendor posting profile

**Note**: You need to complete Exercise 2

1. Navigate to **Accounts payable &gt; Setup &gt; Vendor posting profiles**.

2. Select **+New**.

3. In the **Posting profile** field, enter **'APVP'**.

4. In the **Description** field, enter **'AP Vendor Posting profile'**.

5. Add a Table setup:

	a. Select **+Add**.

	b. In the **Account/Group number** field, enter or select **US-0069** Adventure Works Blue Yonder.

	c. In the **Summary account** field, specify the values **'200100'**.

	d. In the **Liquidity account for payments** field, specify the values **'110110'**.

	e. Select **Add**.

	f. In the **Account code** field, select **'Group'**.

	g. In the **Account/Group** number field, enter **'40'**.

	h. In the **Summary account** field, specify the values **'200110'**.

	i. In the **Liquidity account for payments** field, specify the values **'110110'**.

	j. In the **Arrival** field, specify the values **'200130'**.

	k. In the **Offset account** field, specify the values **'200125'**.

6. Add a Group setup:

	a. Select **+Add**.

	b. In the **Account code** field, select **'Group'**.

	c. In the **Account/Group** number field, enter **'50'**.

	d. In the **Summary account** field, specify the values **'200100'**.

	e. In the **Liquidity account for payments** field, specify the values **'110110'**.

7. Add an All setup:

	a. Select **+Add**.

	b. In the **Account code** field, select **'All'**.

	c. In the **Summary account** field, specify the values **'200100'**.

	d. In the **Liquidity account for payments** field, specify the values **'110110'**.

	e. In the **Arrival** field, specify the values **'200130'**.

	f. In the **Offset account** field, specify the values **'200125'**.

	g. Select **Save**.

	h. Close the page.

8. Navigate to **Accounts payable &gt; Setup &gt; Accounts payable parameters**.

9. Select the **Ledger and sales tax** tab.

10. In the **Posting profile** field, enter or select **APVP**.

11. Select **Save**.

12. Close all pages.
