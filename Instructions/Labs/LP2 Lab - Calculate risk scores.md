---
lab:
    title: 'Lab 2: Calculate risk scores'
    module: 'Learning Path 02: Configure credit and collections'
---

**MB-310: Microsoft Dynamics 365 Financial Consultant**


# Change Record

<html>
<table><tr><th>Version</th><th>Date</th><th>Change</th></tr>
<tr><td>1.0</td><td>13 Sep 2024</td><td>Initial release</td></tr>
<tr><td>1.1</td><td>25 Sep 2024</td><td>Corrected title</td></tr>
<tr><td>1.2</td><td>10 Dec 2024</td><td>Workaround for expired certificate</td></tr>
</table>
</html>


# Objective
You can define and assign risk assessments to customers based on their risk
score. A risk score is calculated by comparing customer information to each
scoring group. The scores are summed, and the total score is compared to the
values in the risk group setup to identify the risk group that the customer
belongs to. The risk group score is then used to define credit management
blocking and exclusion rules for the customer.

Risk scores can help determine the level of risk associated with a customer,
which provides you with the ability to hold orders and generate automatic credit
limits based on that risk. Risk scores are based on scoring groups that you
create.

Use the USMF company for the exercises in this lab.

## Exercise 1 Configure a scoring group 

During this lab, you will configure a scoring group, add the new group to a
customer, and calculate the risk group classification to determine how risky the
customer is.

### Scenario 

At Contoso, Ltd., the credit management manager wants to configure a new scoring
group that must be used to calculate the customer’s risk.

*Note:* If you get a "Your connection isn't private" error on browser opening, then select the **Advanced** link, select to **Continue**, then wait 2-3 minutes.

1.  Navigate to **Credit and collections** \> **Setup \> Credit management setup
    \> Risk \> Scoring groups** and select **New**.
![The Scoring groups page is open. New is selected to create a new scoring group.](images/LP201.png)

1.  In the **Scoring group** field, enter **CM Group**.

2.  In the **Description** field, enter **Credit management group**.

3.  In the **Group type** field, select the **Credit management group** value.

4.  Navigate to **Lines** \> **Add**.
![The Scoring groups page is open. Add is selected to add a new line to a scoring group.](images/LP202.png)

1.  In the **Value** field, select I**ndie**.

2.  In the **Risk contribution score** field, enter **30**.

3.  Select **Add** to add a new line.

4.  In the **Value** field, select the **Major customer** value.

5.  In the **Risk contribution score** field, enter **10**.

6.  Close the form.

## Exercise 2 Add the new scoring group to a customer

1.  Navigate to **Accounts receivable** \> **Customers** \> **All customers**
    and select customer **US-027 Birch Company**.

2.  Select **Edit** in the Action Pane.
![The Vendor page is open. Customer US-027 is selected for an adjustment.](LP203.png)

1.  Navigate to the **Credit and collections** FastTab.
![The Vendor page is open. The Credit and collections FastTab is selected. ](images/LP204.png)

2.  In the **Credit Management group** field, select the **Independent
    Customer** value.
![The Vendor page is open to the customer on the Credit and collection FastTab. The value Indie is selected in the Credit management group.](images/LP205.png)

1.  Select **Save** in the Action Pane.
![The Vendor page is open. Save is selected in the Action Pane.](images/LP206.png)

1.  Close the form.

## Exercise 3 Configure risk classification

1.  Navigate to **Credit and collections** \> **Setup** \> **Credit management
    setup** \> **Risk** \> **Risk classification**.
![The Risk classification page is open.](images/LP207.png)

1.  Select **Edit** in the Action Pane.
![The Risk classification page is open and Edit in the Action Pane is selected.](images/LP208.png)

1.  Under **Risk group**, select **Medium**. Then in the **To** field, enter
    **49.99**.

2.  Select **New** in the Action Pane to add a new line.
![The Risk classification page is open and New in the Action Pane is selected.](images/LP209.png)

1.  In the **Risk group** field, enter **Med-High**.

2.  In the **Description** field, enter **Medium-High**.

3.  In the **From** field, enter **50**.

4.  In the **To** field, enter **59.99**.

5.  In the **Risk group indicator** field, select the **Orange** value.

6.  Select **Save** in the Action Pane.
![The Risk classification page is open and Save in the Action Pane is selected.](images/LP210.png)

7.  Close the form.

## Exercise 4 Check the risk group of the customer

1.  Navigate to **Accounts receivable** \> **Customers** \> **All customers**,
    and then select customer **US-027 Birch Company**.

2.  Open the **Related information** pane by pressing Ctrl+F2.
![The Vendor page and the Related information pane are open.](images/LP211.png)

1.  Expand **Credit statistics** and select **Refresh**.
![Credit statistics](images/LP212.png)

1.  Note that the risk group is **Empty**.

>   In exercise 1, you configured a new scoring group, and then in exercise 2,
>   you added the group to a customer. The new configuration places this
>   customer in a risk group. The new configuration will be apparent after the
>   periodic task **Update risk scores** is performed.

1.  Close the form.

## Exercise 5 Update risk scores

1.  Navigate to module **Credit and collections** \> **Periodic tasks** \>
    Credit management \> **Update risk scores**, and then select Records to
    include \> **Filter**.
![The period task Update risk scores is open and the filter is selected.](images/LP213.png)

1.  In the **Criteria** field for Customer account, enter the value **US-027**.
![In the Criteria field, value US-027 is selected.](images/LP214.png)

1.  Select **OK,** and **OK**.

## Exercise 6 Check the risk group of the customer

1.  Navigate to **Accounts receivable** \> **Customers** \> **All customers**,
    select customer **US-027 Birch Company.**

2.  Open the **Related information Pane** by pressing **Ctrl+F2**.

3.  Expand **Credit statistics**.

4.  Select **Refresh**. Note that the risk group is changed to **Medium**.
![The Customer page is open and in the Related information pane, the Risk group is highlighted.(images/LP215.png)

1.  Select the **Credit management** tab in the Action Pane.

2.  Select **Risk score**.

3.  View the details of the risk score calculation.
![The Vendor page is open and on the Credit management tab, Risk score is selected.](images/LP216.png)

1.  Close the form.
