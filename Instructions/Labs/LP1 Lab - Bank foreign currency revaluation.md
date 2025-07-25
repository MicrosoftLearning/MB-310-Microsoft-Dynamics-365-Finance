---
lab:
    title: 'Lab 1: Bank foreign currency revaluation'
    module: 'Learning Path 01: Set up and configure financial management; work with General Ledger'
---

**MB-310: Microsoft Dynamics 365 Financial Consultant**

# Lab 1 Bank foreign currency revaluation

# Change Record

<html>
<table><tr><th>Version</th><th>Date</th><th>Change</th></tr>
<tr><td>1.0</td><td>13 Sep 2024</td><td>Initial release</td></tr>
<tr><td>1.1</td><td>10 Dec 2024</td><td>Workaround for expired certificate</td></tr>
<tr><td>1.2</td><td>13 Jan 2025</td><td>Added business scenario</td></tr>
<tr><td>1.3</td><td>19 Feb 2025</td><td>Added The Why</td></tr>
<tr><td>1.4</td><td>25 Jul 2025</td><td>Corrected exercise 3</td></tr>
</table>
</html>


# The Why
Understanding how to perform bank foreign currency revaluation is crucial for anyone working in finance or accounting within a global business environment. This hands-on lab will equip you with the practical skills needed to manage and revalue foreign currency transactions accurately, ensuring financial statements reflect true economic conditions. By mastering these techniques, you'll be able to mitigate risks associated with currency fluctuations, enhance financial reporting accuracy, and contribute to more informed decision-making within your organization. This lab is not just an academic exercise; it's a vital competency that will empower you to handle real-world financial challenges with confidence and precision.


# Business scenario

Imagine you are an accountant for a company that conducts international business. The company maintains bank accounts in various currencies to facilitate these transactions. Due to fluctuations in exchange rates, the value of the foreign currency holdings can change over time relative to the company's home currency. This can cause discrepancies between the book value (recorded value in the company's financial statements) and the fair value (market value) of the foreign currency holdings.

To address this issue, companies must periodically revalue their foreign currency bank accounts. This hands-on exercise will guide you through the process of revaluing bank foreign currency in Microsoft Dynamics 365 Finance.

By following the steps in this exercise, you will learn how to:

- Set up the accounting and reporting currencies for bank accounts.
- Update currency exchange rates.
- Execute the foreign currency revaluation process.

This process will ensure that the company's financial statements accurately reflect the current value of its foreign currency holdings.


Use the **USMF** company for the exercises in this lab.

## Exercise 1 Create a transaction that can be revalued 

During this lab, you will first enter a transaction in a bank journal that can
be revalued. The second step is to prepare foreign currency revaluation. After
you configure the foreign currency revaluation, you run the process and then
review the results.

**Scenario**

Contoso, Ltd. has a new financial controller who plans to run a foreign currency
revaluation of bank account USMF EUR as part of the period end. To test the
process, the financial controller first creates a general journal with a
transaction that can be revalued.

*Note:* If you get a "Your connection isn't private" error on browser opening, then select the **Advanced** link, select to **Continue**, then wait 2-3 minutes.

1.  In the **USMF** company, navigate to **General Ledger** \> **Journal
    entries** \> **General journals**.

2.  Select the **New** button to create a new journal.
![General journals page with New highlighted and three unposted journals displayed.](images/LP101.png)


1.  Select **GenJrn** in the **Name** field.
![General journals page with GenJrn selected in the Names list](images/LP101.png)

1.  Select the **Lines** button in the Action Pane.
![General journals page with GenJrn selected and the Lines button selected](images/LP103.png)

1.  In the **Date** field, enter **7/1/2024**.

2.  In the **Account** field, select **600155** for the **MainAccount, 001** for
    the **BusinessUnit,** and **022** for the **Department**.

3.  In the **Debit** field, enter `1,000.00`.

4.  In the **Offset account type** field, select **Bank**.

5.  In the **Offset account** field, select **USMF EUR**.
![Journal voucher page with the GenJrn voucher journal line displayed](images/LP104.png)

1.  In the **Currency** field, select **EUR**.
![Journal voucher page with EUR selected in the Currency field](images/LP105.png)

1.  Select **Post** in the Action Pane to post the journal.
![Journal voucher page with Post highlighted in the Action Pane](images/LP106.png)

1.  Close the form.

Information: Prepare the foreign currency revaluation
-----------------------------------------------------

Note: This is for informational purposes only; the configuration is already done
in USMF.

1.  In the **USMF** company, navigate to **General Ledger** \> **Ledger setup**
    \> **Ledger**, and then expand the **Currency** tab.

2.  In the **Accounting currency exchange rate type** field, display the
    **Default** value.

3.  Select **Accounts for currency revaluation**.

4.  Review the values for realized gain, realized loss, unrealized gain, and
    unrealized loss accounts for the currency revaluation.
![Ledger page with Accounts for currency revaluation area displayed.](images/LP108.png)

5.  Navigate to **Cash and Bank management** \> **Setup** \> **Cash and bank
    management parameters**.

6.  Select the **Number sequence** tab.

7.  Review the number sequence for **Foreign currency revaluation**.
![Cash and bank management parameters page with Bank_290 entered in the Number sequence column for Foreign currency revaluation](images/LP109.png)



## Exercise 2 Update currency exchange rate

1.  Navigate to **General ledger** \> **Currencies** \> **Currency exchange
    rates**.

2.  In the **Exchange rate type** list, select **Default**.

3.  Select the line with **USD** in the **From currency** field and **EUR** in
    the **To currency.**

4.  Select **Add** to enter a new exchange rate.
![Currency exchange rates page with EUR selected for the To currency type.](images/LP110.png)

5.  In the **Start date** field, enter **7/15/2024**.

6.  In the **Exchange rate** field, enter `91.8000`.
![Currency exchange rates page with the Start date, Exchange rate, and Exchange value fields highlighted](images/LP111.png)

1.  Select **Save** in the Action Pane.

2.  Close the form.

<s>## Exercise 3 Execute the foreign currency revaluation

1.  Navigate to **General Ledger** \> **Currencies** \> **Foreign currency
    revaluation**.

2.  Select the **Foreign currency revaluation** button in the Action Pane.
![Foreign currency revaluation page with the Foreign currency revaluation button selected](images/LP112.png)

1.  In the **From date** field, enter **7/1/2024.**

2.  In the **To date** field, enter **7/31/2024**.

3.  In the **Date of rate** field, enter **7/21/2024**.

4.  In the **Currencies to revalue** list, select **EUR**.

5.  Switch **Preview before posting** to **Yes**.

6.  Select **Filter**.
![Foreign currency revaluation pane with Filter highlighted.](images/LP113.png)

7.  In the **Criteria** field, select the **Main account 110130**.
![Filtered Inquiry information with the Range tab displayed. The criteria 110130 is entered for Main account.](images/LP114.png)

1.  Select **OK** and **OK**.

    The message “Operation completed” appears in the message bar.
![Foreign currency revaluation preview displaying Operation completed in the message bar.](images/LP115.png)

>   **Calculation**

| **Date**     | **Currency EUR-100USD** | **Currency 1 EUR – USD**         | **Currency 1,000 EUR - USD**                               |
|--------------|-------------------------|----------------------------------|------------------------------------------------------------|
| 12/1/2013    | 73 EUR = 100 USD        | 1 EUR = (1 / 0.73) 1.36986 USD   | 1000 EUR = (1000 \* 1.36986) = 1,369.86 USD                |
| 7/15/2024    | 91.80 EUR = 100 USD     | 1 EUR = (1 / 0.9180) 1.08932 USD | 1000 EUR = (1000 \* 1.08932) = 1.089,32 USD                |
| Today’s date |                         | Exchange rate gain               | Revalued amount = 1,089.32 USD – 1,369.86 USD = 280.54 USD |

11.  **Post** the journal.
![Foreign currency revaluation preview page displaying the posted journal.](images/LP116.png)
</s>

## Exercise 3 Execute the bank foreign currency revaluation

1. Navigate to **Cash and bank management** > **Periodic tasks** > **Foreign currency revaluation**.
2. On the Action Pane, select **Foreign currency revaluation**.
3. In the **On date** field, enter **7/31/2024**.
4. In the **Exchange rate date** field, enter **7/21/2024**.
5. In the bank‑accounts grid, select the line for **USMF EUR**.
6. Switch **Preview before posting** to **Yes**.
7. Select **OK** to run the revaluation preview.
8. When you see **“Operation completed”** in the message bar, select **Post** to record the unrealized gain or loss.
   
## Exercise 4 Review the voucher and balance of the foreign currency bank account

1.  Select the **Voucher transactions** button in the Action Pane.
![Foreign currency revaluation page with the Voucher transactions button highlighted.](images/LP117.png)

1.  Review the voucher transactions.
![Voucher transactions page with four posted voucher transactions](images/LP118.png)

>   The currency EUR has decreased, which is an exchange rate gain for USMF.

1.  Navigate to **General ledger** \> **Inquiries and reports** \> **Trial
    balance**.

2.  In the **From date** field, enter **1/1/2024**.

3.  In the **To date** field, enter **12/31/2024**.

4.  Select **Calculate balances**.
![Trial balance page with the From date and To date fields and the Calculate balances button highlighted.](images/LP119.png)

1.  View the balance of main account **110310**.
![Trial balance page with the balance information for main account 110310 displayed.](images/LP120.png)

1.  Close the form.
