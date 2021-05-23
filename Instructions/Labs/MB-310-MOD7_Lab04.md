---
lab:
    title: 'Exercise 4: Configure Budget planning, create and use a planning process'
    module: 'Module 7: Configure and manage budgeting'
---

## Exercise 4: Configure Budget planning, create and use a planning process

The goal of the lab exercise is to apply the knowledge we’ve learned regarding the configure and test budget planning components. 

### Instructions

The objective of this lab is to provide a guided view of Microsoft Dynamics 365 Finance functionality updates in Budget planning area. The intent of this lab is to illustrate a quick configuration example of budget planning module and showcase how budget planning can be accomplished using this configuration. 

This lab will focus specifically on the following business processes or tasks:

- Creating organizational hierarchy for budget planning and configuring user security

- Defining budget plan scenarios, budget plan columns, layouts and Excel templates

- Creating and activating budget planning process

- Creating budget plan document by pulling in actuals from General ledger

- Using allocations to adjust budget plan document data

- Editing budget plan document data in Excel

### Prerequisites

You’ll need to access the Dynamics 365 Finance environment with demo data and be provisioned as an administrator on the instance. If you sign into the Dynamics 365 Finance using a browser other than IE, then you’ll be prompted to sign in within the Excel App. When you select “Sign in” in the Excel App, an IE popup window will open and when signing in you **MUST** check the “Keep me signed in” checkbox. If selecting “Sign in” in the Excel App doesn’t appear to do anything, then you should clear the IE cookie cache.

### Scenario overview

Julia works as a finance manager in Contoso Entertainment Systems USA (**USMF**). As FY2020 approaches, she needs to work on setting up the company’s budget for the upcoming year based on fiscal year 2016. Budget preparation looks as follows:

- Julia uses previous year actuals amounts as a starting point to create the budget.

- Based on the previous year actuals, she creates estimates for 12 months in the upcoming year.

- Julia reviews the budget with CFO. Once done she makes necessary adjustments for the budget plan and finalizes budget preparation. Julia uses an Excel template to prepare the budget.

### Configuration

#### Create organizational hierarchy

As all the budgeting process happens in` the Finance department, therefore Julia needs to create a very simple organizational hierarchy, consisting of Finance department only. 

1. Navigate to **Organization administration &gt; Organizations &gt; Organization hierarchies**.

2. Select the **+New** button.

3. In the **Name** field, enter **MyBudgetPlanningH**.

4. Select the **Assign purpose** button.

5. Select the **Budget planning** purpose so that it is highlighted.

6. Select the **Add** button and select the newly created organizational hierarchy **MyBudgetPlanningH**.

7. Select **OK**.

8. Highlight the **MyBudgetPlanningH** and select **Set as default** button. 

9. Close the form.

10. Select **Refresh** button. Note that **Budget planning** purpose is assigned as purpose for **MyBudgetPlanningH**.

11. In the Organizational Hierarchies form select the **View** button. 

12. Select **Edit** in the Hierarchy designer and create a hierarchy by selecting button **Insert &gt; Department**.

13. Select the **Finance** department for the budgeting hierarchy.

14. Select **OK** if necessary.

15. Select **Publish** and enter 1/1/2020 in the **Effective date** field for hierarchy publishing.

16. Select **Publish**.

17. Select **Close**.

18. Close all pages.

#### Configure user security

Budget planning uses special security policies to configure access to budget plans data. Julia needs to give access to Finance budget plans for herself.

1. In **USMF**, navigate to **Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration**.

2. In **Parameters** tab, set the **Security model** value to **Based on security organizations**.

3. Select **Save**.

4. Close the page.

5. Navigate to **System administration &gt; Users &gt; Users**.

6. Select the link for **UserID** field with value of **Admin**.

7. Select **Edit** button.

8. Select **USMF** for the **Company** field.

9. Give user **Admin** the **Budget manager** role by selecting **Assign role** and select **OK**.

10. Highlight the **Budget manager** role and select **Assign organizations** button.

11. Select “**Grant access to specific organizations individually**”.

12. In the **Select organization hierarchy** field select **Budgeting - Departments**.

13. Select the **Finance** node and select the **Grant** **with children** button.

14. Close all pages.

### Use existing scenarios

1. In **USMF**, navigate to **Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration**. 

2. Select the **Scenarios** tab and note that you will use **Previous year actuals** and **Budgeted**.

#### Create budget plan columns

Budget plan columns are either Monetary or quantity-based columns that can be used in budget plan document layout. In our example, we need to create a column for Previous year actuals and 12 columns to represent each month in a budgeted year. 

Columns can be created either by simply selecting Add button and filling in the values, or with a help of Data entity. In this lab, we will use Data entity to fill in the values.

3. Select the **Columns** tab. 

4. Select the **Office** button on the top right corner of the form and choose **Budget plan** **columns (unfiltered)**.

5. Select **Download**.

6. Select **Open**. The system will open an Excel workbook to be used for filling in the values. 

7. If prompted, select **Allow**.

8. If prompted with Microsoft Office Activation Wizard dialog box, select **Close**. 

9. If prompted, select **Enable Editing** and **Trust this add-in**.

10. You need to sign in using the same alias as you log in to the Dynamics 365 Finance.

11. Select **Design** on the right-side pane to add the columns to the grid.

12. Select the little pencil button next to **Budget plan columns** to see the available columns to add to the grid from the **Data connector**.

13. Select all available fields and select **Update**.

14. Select **Done**.

15. Select **Refresh** button.

16. Select **Yes**.

17. Select **Publish**. Close Excel without saving.

18. Switch to Dynamics 365 Finance and refresh the page. 

19. The published values will appear in Dynamics 365 Finance after a page refresh.

#### Create budget plan document layouts and templates

Layout defines how budget plan document lines grid is going to look like when user opens budget plan document. It is also possible to switch the layout for budget plan document to see the same data in different angles. 

Now, as you’ve got columns defined to be used with our budget plan document, Julia needs to create a budget plan document layout, that would look similar to the Excel table she uses to create budget data.

20. Select the **Layouts** tab. 

21. Select **+Add** on the **Budget plan layouts** area to create a new layout for monthly budget entry; enter **MyLayout** in the **Name** field; choose the **MA+BU** value in the **Ledger dimension set** field to include Main accounts and Business units to the layout. 

22. Under the **Layout element** section, select **Add** and select **Actuals to date** in the **Elements** section. 

23. Select **Editable**.

24. Select **Descriptions** button in the **Budget plan layouts** area to select which financial dimensions should display Descriptions in the grid. Based on the budget plan layout definition, we can create an excel template to be used as an alternative way to edit budget data. As an excel template must match the budget plan layout definition. You won’t be able to edit the budget plan layout after generating an excel template; therefore, this task should be done after all layout components are defined. Don’t make the elements editable.

25. Select **Main** **Account** and **BusinessUnit** and select à to add them to the **Selected Fields** section.

26. Select **OK**.

27. For the layout created, select **Template &gt; Generate** in the **Budget plan layouts** area.

28. Read the message and select **Yes**.

29. To view the template, select **Template &gt; View** in the **Budget plan layouts** area.

30. Make sure to select “**Save as**” and select the place where template should be stored in order to edit it. If user selects “Open” in the dialog without saving, the changes done to the file will not be retained when the file is closed. **Open** the file.

31. If prompted, select **Enable Editing**.

32. Select **Refresh**.

33. Review the results.

34. Close Excel workbook.

35. Close all pages in Dynamics 365 Finance.

### Create a budget planning process

Julia needs to create and activate a new budget planning process combining all the setup above to start entering budget plans. Budget planning process defines what budgeting organizations, workflow, layouts, and templates will be used for creating budget plans. By using the following information to create a budget planning process:

- Budget planning process – USMF budgeting FY2020

- Budget cycle – FY2020

- Ledger – USMF

- Default account structure – Manufacturing P&L

- Organization hierarchy – pick the hierarchy created in the beginning of the lab

- Budget planning workflow – assign Auto – Approve workflow for finance department

- In budget planning stage rules and templates, for each workflow budget planning stage, pick if adding lines and modifying lines is allowed and what layout should be used by default.

1. Navigate to **Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning process**.

2. Select **Next year OPEX budget**.

3. Review values of all fast tabs.

4. Close all pages.

### Generate initial data for budget plan from General ledger

1. Navigate to **Budgeting &gt; Periodic &gt; Generate budget** **plan from General ledger**. 

2. In the **Fiscal year** field, select **2016**.

3. In the **From period** field, select **January**.

4. In the **To period** field, select **December**.

5. In the **ACCOUNT TYPE** list area, select check box next to **Account type** to select all account types.

6. In the **Historical** field, select **Yes**.

7. In the **Budget planning process** field, select **Next year OPEX budget**.

8. In the **Budget plan name** field, enter **MyBudgetPlan1**.

9. In the **Budget plan scenario** field select **Department approved**.

10. In the **Factor** field enter **1.2**.

11. Select button **Generate**.

12. Navigate to **Budgeting &gt; Budget plans** to find a budget plan created by Generate process.

13. You need to refresh the page until you see Budget plan name **MyBudgetPlan1**. The first time this runs, it will take a few moments.

14. Open document details by selecting Document number hyperlink. Budget plan is displayed as defined in the layout created during this lab. Scroll right to see more columns of data.

15. Select **Budget plan hierarchy** button.

16. Review results.

17. Close all the pages.

### Create budget register entry from budget plan

1. Navigate to **Budgeting &gt; Periodic &gt; Generate budget register entry**.

2. In the Budget planning process field, select **Next year OPEX budget**.

3. In the document number use the dropdown to select **MyBudgetPlan1** as the budget plan name.

4. In the **Budget plan scenario** field, select **Department approved**.

5. In the **Budget model** field select, **FY2021**.

6. In the **Budget code** field, select **Original budget**.

7. Select **Generate**.

8. Navigate to **Budgeting &gt; Budget register entries**.

9. You need to refresh the page until you see the budget register entries for **FY2021**. The first time this runs, it will take a few moments.

10. Select the hyperlink for the **FY2021** budget register entry and view results.

 
