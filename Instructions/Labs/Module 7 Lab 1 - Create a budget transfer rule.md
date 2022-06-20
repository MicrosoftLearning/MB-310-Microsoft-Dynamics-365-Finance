---
lab:
    title: 'Lab: Create a budget transfer rule'
    module: 'Module 7: Configure and manage budgeting'
---

# Lab: Create a budget transfer rule

You can use the **Budget transfer rules** form to define budget transfer rules
and determine when budget transfers are allowed between financial dimension
values. For example, budget transfers in a specific department might be allowed
without approval, but transfers across departments might need to be reviewed and
approved before the budget balance is adjusted. If a budget register entry is
submitted and it violates the budget transfer rules, the transfer can be
completed only if it is approved through a Budgeting workflow.

A budget manager has been analyzing recent travel expenses and wants to make
some changes to the budget to better align the budgets with the travel policies
of the company. You need to set up transfer rules. You must be able to review
and approve transfer requests.

This lab uses the demo company **USMF**.

Exercise 1 Define dimensions for budgeting
==========================================

1.  Navigate to **Budgeting** and select **Setup**. Select **Basic budgeting**
    and then select **Dimensions for budgeting**.

2.  Determine whether the **Department** financial dimension is selected as a
    budget dimension. In this example the department is set up as a budget
    dimension.

3.  Select **OK** to close the form.

![](media/d4d942bf236b32a985273f2efb2ff6e3.png)

Exercise 2 Define budget transfer rules
=======================================

In this exercise you will set up a rule that does not allow budget transfers
outside of the rule members unless you use a workflow to approve the transfer.
If no criteria are specified, the rule applies to all dimension values.

1.  Navigate to **Budgeting** and select **Setup**. Select **Basic budgeting**
    and then select **Budget transfer rules**.

2.  Select **New** to create a new budget transfer rule.

3.  Enter CLIENT for the Budget transfer rule.

4.  Enter the description **Client Services**.

5.  Select the **Manufacturing P&L** account structure.

6.  Select **Add** to add a new rule and enter **CLIENT** in the **Rule member**
    field.

7.  Navigate to the **Allow transfers when** section.

8.  Select **Add new criteria** by selecting the link.

9.  In the **Where** field select **Department**, select **is** in the Operator
    field, and enter **028** in the Value field.

10. Select **Save.**

11. **Close** the form.

![](media/0688afdbed8bf0a49e938971505d648a.png)

Exercise 3 Define budget parameter for budget transfer rules
============================================================

In this exercise you enable a budget workflow for the budget transfer rule.

1.  Navigate to **Budgeting** and select **Setup**. Select **Basic budgeting**
    and then select **Budgeting parameters**.

2.  Navigate to **Use rules for budget transfers** and set the field to **Yes**.

3.  Select **Save**.

4.  Close the form.

![](media/983d010d9a76dab64ed1afe2316a7bb3.png)

Exercise 4 Validate the budget register entry workflow
======================================================

1.  Navigate to **Budgeting** and select **Setup**. Select **Basic budgeting**
    and then select **Budgeting workflows**. Note that the budget register entry
    workflow has been created and is active.

2.  **Close** the form.

Exercise 5 Define budget code
=============================

In this exercise you configure a budget code for the budget type transfer.

1.  Navigate to **Budgeting** and select **Setup.** Select **Basic budgeting**
    and then select **Budget codes**.

2.  Select **New** to create a new budget code.

3.  Enter **Transfer** in the budget code field.

4.  Enter T**ransfer of travel expenses** in the description field.

5.  Select **Transfer** in the Budget type field.

6.  Select **000001 Budget register entry workflow** in the workflow field.

7.  Select **Save**.

8.  Close the form.

![](media/d2d5198d500fa65f8e7f4c4b60c21cb6.png)

Exercise 6 Create a budget register entry
=========================================

In this exercise you will see what happens when you we enter a budget register
entry.

Task 1
------

In this task you will add a budget register entry.

1.  Navigate to **Budgeting** and select **Budget register entries**.

2.  Select **New** to create a new budget register entry.

3.  Select **FY2021** in the budget model field.

4.  Select **Transfer** in the Budget Code field.

5.  Navigate to the **Budget account entries** tab.

6.  Select **Add line** to create a new line.

7.  Select **1/1/2021** in the date field.

8.  Select **Manufacturing P&L** in the account structure field.

9.  Select **601506-001-028--** in the dimension value field.

10. Enter **1000** in the amount field.

Task 2
------

In this task you will add a second line for the same dimension combination.

1.  Select **Add line** to create a new line.

2.  Select **1/1/2021** in the date field.

3.  Select **Manufacturing P&L** in the account structure field.

4.  Select **601505-001-022** in the dimension value field.

5.  Enter **-1000** in the amount field.

6.  Select **Save**.

    ![](media/a00250a27a0f20364bee458da1cc2d55.png)

7.  The following message should display: This budget transfer violates a budget
    transfer rule and is not allowed unless you use workflow to approve the
    transfer appears.

8.  **Close** the message box.

9.  Select **Workflow** in the Action Pane.

10. Select **Submit** budget revision for approval.

11. A message box appears where you can leave a comment. Enter the text
    **Approval needed** and select **Submit**. The workflow is started.
