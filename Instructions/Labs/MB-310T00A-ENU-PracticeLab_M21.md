### Before you begin

To get the most out of this exercise and the other exercises that are included
with this module, we recommend that you have the standard sample data available
in Finance and Operations that is installed using Lifecycle services (LCS).

Exercise - Configure basic budgeting components
===============================================

You need to configure the basic budgeting for your company. Select **USMF** to
practice and learn how.

1.  Open **Budgeting \> Setup \> Basic budgeting \>Dimensions for budgeting**

2.  Select the financial dimensions in the **Chart of accounts** dimension list.

3.  Click the **\<** arrow button to move the financial dimensions to the
    **Budget dimension** list.

4.  Open **Budgeting \> Setup \> Basic budgeting \> Budget models**.

5.  Click **New** to create a budget model.

6.  Enter an identifier and a name for the budget model.

7.  Enter other details about the model as needed, and add any submodels.

8.  Open **Budgeting \> Setup \> Basic budgeting \> Budget codes**.

9.  Click **New** and enter a code and a description, such as Expense Transfer
    and Expense to Expense.

10. Select a budget type, such as **Original budget**, **Revisions** and
    **Transfer**.

11. If this code should be the default code when documents of the selected
    budget type are automatically created, select the **Set as default code**
    check box.

12. Optionally, select a **Reason code**.

13. Optionally, select a Workflow. If a workflow is selected, every budget
    register entry that uses this code is submitted to workflow.

14. Open **Budgeting \> Setup \> Basic budgeting \> Budget transfer rules**.

15. Click **New** and enter an identifier and a description for the budget
    transfer rule, and then select an Account structure.

16. Click **Add** to define the financial dimension criteria for a rule member.
    For example, you could define criteria for the Sales department. If a
    transfer is entered that has budget account entries that do not contain the
    Sales department financial dimension, the rule would stop the transfer.

17. If workflow is activated for the budget code that is associated with the
    budget type, the transfer is submitted for approval.

18. You can click **Add** again to add multiple rule members to the same rule.
    You cannot specify the same financial dimension criteria in more than one
    rule member for a transfer rule. However, you can have overlaps in financial
    dimension criteria across budget transfer rules so that the same financial
    dimension value can belong to multiple budget transfer rules.

19. To enable the budget transfer rules that you defined, select Use rules for
    budget transfers in the **Budgeting \> Setup \> Basic budgeting \> Budget
    parameters** form.

20. Open **Budgeting \> Setup \> Basic budgeting \> Budget allocation terms**.

21. Click **New** and enter an identifier and a description for the budget
    allocation term.

22. Click **Add** and enter an allocation percentage of the total amount.

23. Click **Copy** to select an existing allocation term to copy for this budget
    allocation term.

24. Click the percentage and select a value for one or more financial
    dimensions.

25. Repeat steps 21 through 24 for each budget allocation term to set up.

Exercise - Configure budget control components
==============================================

You need to configure the budget control for your company. Select USMF to
practice and learn how.

1.  Open **Budgeting \> Setup \> Budget control \> Budget cycles**

2.  Click **New** and enter a name for the budget cycle time span.

3.  Select a fiscal calendar to associate with the budget cycle time span.

4.  In the **Length of budget cycle** field, select **Specify number of
    periods** or **Map to fiscal year**.

5.  If you select **Specify number of periods**, enter the number of accounting
    periods for the budget cycle.

6.  If you select **Map to fiscal year**, the budget cycle time span uses the
    fiscal year that is defined by the starting and ending periods for the
    budget cycle.

7.  Click **Add**. Enter the name of the first period in the budget cycle time
    span and enter the date when that period starts. The ending date for the
    budget cycle is determined automatically based on the number of fiscal
    periods in the budget cycle time span.

8.  Open **Budgeting \> Setup \> Budget control \> Budget control
    configuration**.

9.  Select an **Account structure** If you have multiple active account
    structures in the chart of accounts, select the account structure that will
    be used for profit and loss or expense accounts. This account structure
    includes the main account range for expense accounts.

10. After you select an account structure, all the financial dimensions in that
    account structure and advanced rules that are defined for budgeting are
    displayed in the Budget dimensions list.

11. Select a financial dimension and move it to the **Budget control
    dimensions** list.

12. Select a **Budget control interval**, such as Fiscal year or Fiscal year to
    date. The budget control interval works with the budget cycle to determine
    how amounts are aggregated for budget checking.

For example, if you select Fiscal year, all the funds for the fiscal year are
aggregated for budget checking. If you select Fiscal year to date or Budget to
date, the ending date is determined from the fiscal period and the accounting
date of the source document or accounting journal that is being checked.

1.  Select the **Budget cycle time span**, which defines the length of the
    budget cycle.

2.  Select a **Budget manager**, which is a user who can approve budget
    workflows. Another budget manager can be defined by using a budget control
    rule.

3.  In the **Budget threshold** field, enter the percentage of the budget that
    can be spent. The threshold can be used to provide warning messages or to
    define budget permissions to prevent specific user groups from exceeding the
    budget threshold. This threshold can exceed 100 percent.

4.  Select the **Display a message when exceeding budget threshold** check box
    to display messages when the budget threshold is exceeded.

5.  Click the **Over budget permissions** tab.

6.  Click **Add** to create a new rule.

7.  Select the desired **User group**.

8.  Select the **Over budget** option.

9.  Click the **Activate budget control** tab.

10. Click **Budget funds available**, and select desired check boxes to
    formulate how the available funds gets calculated.

11. Click **Documents and journals**.

12. Select the **Purchase requisitions** check box. The **Purchase orders** and
    **Vendor invoices** check boxes are automatically selected.

13. If you do not select the **Purchase requisitions** check box and you instead
    select the **Purchase orders** check box, the **Vendor invoices** check box
    is automatically selected.

14. You can select **Vendor invoices**, Travel requisitions, and Expense reports
    independently of the other source documents.

15. For each source document, you can select the **Enable budget control** for
    line item on entry check box to enable budget checking for each line as the
    line is entered and saved.

16. Click the **Assign budget models** tab.

17. Click **Add** and then select a **budget cycle time span**.

18. Select a **Budget cycle**.

19. Select a **Budget model**. Only budget models that do not contain submodels
    are available for budget control.

20. Click **Define budget control rules**. Define rules as desired.

21. Click **Select main accounts**.

22. Select the check boxes to select the main accounts or click Select all to
    select all the main accounts.

23. Click **Activate budget control**.

24. Click **Activate** to make the draft version of the budget control
    configuration active. The Date when last activated field displays the
    current date, and the Activated by field displays your user ID.

25. Click **Turn on** to start budget control by using the active configuration.
    The budget control status changes to Turned on, and the Turn on button is
    replaced with Turn off.

Exercise – Create a budget register entry
=========================================

You need to configure the budget control for your company. Select USMF to
practice and learn how.

1.  Open **Budgeting \> Budget register entries.**

2.  Click **New**.

3.  In the **Budget model**, select a budget model.

4.  In the **Budget code**, select a value.

5.  Optionally, specify a **Reason code** for the budget register entry.

6.  Click **Add line.**

7.  The **Date for the budget register entry line** determines the period that
    the budget will be recorded to.

8.  Select an **Account structure.**

9.  Enter the **Dimension values** for the budget enabled dimensions. The order
    in which the dimensions are entered is based on the order in which the
    dimensions appear within the account structure.

10. Enter the budget **Amount** and the budget **Amount type**. The budget
    amount type will default to expense, but can be changed. The amount type is
    needed since the main account is not a required element for budgeting.

11. Specify the transaction **Currency**

12. Click **Update the budget balances** on the Action Pane. By taking this
    action, the budget balance for the budget model and dimension combination
    will be updated based on the amount for the period in which the line date
    falls.
