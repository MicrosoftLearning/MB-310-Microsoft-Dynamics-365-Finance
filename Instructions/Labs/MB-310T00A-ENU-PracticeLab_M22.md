Exercise: Configure Budget planning, create and use a planning process 
=======================================================================

>   The goal of the lab exercise is to apply the knowledge we’ve learned
>   regarding the configure and test budget planning components.  

>   Instructions 

>   The objective of this lab is to provide a guided view of Microsoft Dynamics
>   365 for Finance and Operations functionality updates in Budget planning
>   area. The intent of this lab is to illustrate a quick configuration example
>   of budget planning module and showcase how budget planning can be
>   accomplished using this configuration.  

>   This lab will focus specifically on the following business processes or
>   tasks: 

-   Creating organizational hierarchy for budget planning and configuring user
    security 

-   Defining budget plan scenarios, budget plan columns, layouts and Excel
    templates 

-   Creating and activating budget planning process 

-   Creating budget plan document by pulling in actuals from General ledger 

-   Using allocations to adjust budget plan document data 

-   Editing budget plan document data in Excel 

>   Prerequisites 

>   You’ll need to access the Finance and Operations environment with demo data,
>   and be provisioned as an administrator on the instance. Do not use In
>   Private browser mode for this lab - sign out from any other account in the
>   browser if needed and sign in with Finance and Operations administrator
>   credentials. When signing into Finance and Operations, you **MUST** check
>   the “Keep me signed in” checkbox.  

>   This creates a persistent cookie that the Excel App currently needs. If you
>   sign in to the Finance and Operations using a browser other than IE, then
>   you’ll be prompted to sign in within the Excel App. When you click “Sign in”
>   in the Excel App, an IE popup window will open and when signing in
>   you **MUST** check the “Keep me signed in” checkbox. If clicking “Sign in”
>   in the Excel App doesn’t appear to do anything then you should clear the IE
>   cookie cache. 

>   **Scenario overview** 

>   Julia works as a finance manager in Contoso Entertainment Systems in Germany
>   (DEMF). As FY2016 approaches, she needs to work on setting up the company’s
>   budget for the upcoming year. Budget preparation looks as follows: 

1.  Julia uses previous year actuals amounts as a starting point to create the
    budget. 

2.  Based on the previous year actuals, she creates estimates for 12 months in
    the upcoming year 

3.  Julia reviews the budget with CFO. Once done she makes necessary adjustments
    for the budget plan and finalizes budget preparation. Julia uses an Excel
    template to prepare the budget: 

>    

>   Configuration 

Create organizational hierarchy 
--------------------------------

>   As all the budgeting process happens in the Finance department, therefore
>   Julia needs to create a very simple organizational hierarchy, consisting of
>   Finance department only.  

1.  Navigate to Organization administration \> Organizations \> Organization
    hierarchies 

2.  Click New button 

3.  Type the name for the organizational hierarchy and click button Assign
    purpose 

4.  Select Budget planning purpose, click button Add and assign newly created
    organizational hierarchy. 

5.  Repeat the step above for Security organizational purpose.  

6.  Close the page when done. 

7.  In the Organizational Hierarchies page click button View. Click Edit in the
    Hierarchy designer and create a hierarchy by clicking button Insert. 

8.  Select Finance department for the budgeting hierarchy. 

9.  When done, click button Publish and Close. Select 1/1/2019 as effective date
    for hierarchy publishing. 

>    

Configure user security 
------------------------

>   Budget planning uses special security policies to configure access to budget
>   plans data. Julia needs to give access to Finance budget plans for herself. 

1.  In DEMF, navigate to **Budgeting \> Setup \> Budget planning \> Budget
    planning configuration**.  

2.  In **Parameters** tab, set the **Security model** value to **Based on
    security organizations** 

3.  Navigate to **System administration \> Users \> Users**.  

4.  Give user **Admin** (Julia Funderburk) **Budget manager role**. 

5.  Pick user role and **click Assign organizations** 

6.  Select “Grant access to specific organizations”.  

7.  Pick Organizational hierarchy created in the first step.  

8.  Pick **Finance** node and click **Grant** with children button 

>   Please note that you may need to refresh your browser to have the
>   **eXtensible Data Security (**XDS) policy take effect the next time you
>   login to Dynamics 365 for Finance and Operations.

Create scenarios 
-----------------

1.  In DEMF, navigate to Budgeting\>Setup \> Budget planning \> Budget planning
    configuration.  

2.  In the Scenarios page, you will use Previous year actuals and Budgeted. 

Create budget plan columns 
---------------------------

>   Budget plan columns are either Monetary or quantity-based columns that can
>   be used in budget plan document layout. In our example we need to create a
>   column for Previous year actuals and 12 columns to represent each month in a
>   budgeted year.  

>   Columns can be created either by simply clicking Add button and filling in
>   the values, or with a help of Data entity. In this lab we will use Data
>   entity to fill in the values. 

1.  in DEMF, navigate to **Budgeting\>Setup \> Budget planning \> Budget
    planning configuration** 

2.  Select **Columns** page.  

3.  Click **Office** button on the top right corner of the page and pick Columns
    (unfiltered) 

4.  System will open Excel workbook to be used for filling in the values. If
    prompted, click Enable Editing and Trust this app 

5.  We will need more columns to fill the values in. Click **Design** on the
    right-side pane to add the columns to the grid. 

6.  Click the little pencil button next to PlanColumns to see available columns
    to add to the grid 

7.  Double click on each available field to add them to Selected fields and
    click **Update** 

8.  In Excel table add all the columns that need to be created. Use AutoFill
    feature in Excel to add the lines quickly. Make sure the lines are added as
    a part of the table (when using vertical scroll, you should be able to see
    column headers on the top of the grid) 

9.  Return to Finance and Operations and refresh the page. Published values will
    appear in Finance and Operations. 

>    

Create budget plan document layouts and templates 
--------------------------------------------------

>   Layout defines how budget plan document lines grid is going to look like
>   when user opens budget plan document. It is also possible to switch the
>   layout for budget plan document to see the same data in different angles. 

>    

>   Now, as you’ve got columns defined to be used with our budget plan document,
>   Julia needs to create a budget plan document layout, that would look similar
>   to the Excel table she uses to create budget data. 

>   1. In DEMF, navigate to **Budgeting\>Setup \> Budget planning \> Budget
>   planning configuration.**  

>   2. Click **Layouts** page.  

>   3. Create a new layout for Monthly budget entry; Pick MA+BU dimension set to
>   include Main accounts and Business units to the layout. Then List all budget
>   plan columns created in the previous step in the Elements section. Make all
>   but Previous year actuals editable. 

>   4. Click **Descriptions** button to select which financial dimensions should
>   display Descriptions in the grid. 

>   Based on the budget plan layout definition we can create an Excel template
>   to be used as an alternative way to edit Budget data. As Excel template has
>   to match budget plan layout definition, you won’t be able to edit budget
>   plan layout after generating Excel template, therefore this task should be
>   done after all layout components are defined. 

>   6. For the layout created, click button **Template \> Generate**.  

>   7. Confirm the warning message.  

>   8. To view the template, click **Template \> View**. 

>   Make sure to select “Save as” and select the place where template should be
>   stored in order to edit it. If user selects “Open” in the dialog without
>   saving, the changes done to the file will not be retained when the file is
>   closed.* * 

Create a budget planning process 
---------------------------------

>   Julia needs to create and activate a new budget planning process combining
>   all the setup above to start entering budget plans. Budget planning process
>   defines what budgeting organizations, workflow, layouts and templates will
>   be used for creating budget plans. 

>   Navigate to **Budgeting \> Setup \> Budget planning \> Budget planning
>   process** and create a new record, by using the following information to
>   create a new record: 

-   Budget planning process – DEMF budgeting FY2016 

-   Budget cycle – FY2016 

-   Ledger – DEMF 

-   Default account structure – Manufacturing P&L 

-   Organization hierarchy – pick the hierarchy created in the beginning of the
    lab 

-   Budget planning workflow – assign Auto – Approve workflow for Finance
    department 

-   In budget planning stage rules and templates, for each workflow Budget
    planning stage pick if Adding lines and Modifying lines is allowed and what
    Layout should be used by default 

Budget planning workflow stages 
--------------------------------

>   Budget planning workflow are used together with budgeting workflows stages
>   to manage the creation and progress of budget plans.  

>   It is important to consider that the workflow you create will reflect what
>   you designed in your schema when you first started the planning. 

>   The Budget planning workflow consists of an ordered set of stages that a
>   budget plan moves through. Each budget planning workflow is associated with
>   a budgeting workflow. Budgeting workflows are one of the types of workflow
>   that are used throughout Finance and Operations. The budgeting workflow
>   routes the budget plans, together with worksheets, justifications, and
>   attachments, through the organization for review and approval. 

>   You create the budget planning workflow in the Workflow stages section of
>   the **Budget planning configuration** page. There, you can select the stages
>   and the budgeting workflow that will be used, and also configure additional
>   settings. 

>   A good practice is to create a budget planning workflow for each level of a
>   budgeting hierarchy. You then assign a Budgeting workflow that contains
>   elements that correspond to the stages in the budget planning workflow. In
>   the example schema that appears earlier in this article, one budget planning
>   workflow would be created for the sales departments, and another would be
>   created for the headquarters. A Budgeting workflow moves the budget plans
>   through the stages. 

>   You create the Budgeting workflow for budget planning on the Budgeting
>   workflows page. The process resembles the process for creating other
>   workflows in Finance and Operations. The following illustration shows an
>   example of a Headquarters workflow. 

![](media/2dd6e00c370b7dd79ebcc020291d43b6.png)

>   Workflow: Start \> Allocate to sales department \> Sales Department \>
>   Transition to HQ Rollup \> Aggregate submissions \> Transition to BM Review
>   \> Budget manager review \> Transition to CFO Review \> CFO Approval \>
>   Transition to Final Budget \> End

>   The workflow includes elements for allocation to sales departments and
>   aggregation of their submissions, review by the budget manager, approval by
>   the CFO, and stage transitions between each stage. 

>   You assign the Budgeting workflow to each budget planning workflow in the
>   Workflow stages section of the **Budget planning configuration** page. 

>   Then select **Actions \> Activate** to activate this budget planning
>   workflow. 

>    

Generate initial data for budget plan from General ledger 
----------------------------------------------------------

>   Navigate to **Budgeting \> Periodic \> Generate budget plan from General
>   ledger**.  

>   Fill in the periodic process parameters and click button Generate. 

>    Navigate to **Budgeting \> Budget plans to find a budget plan created by
>   Generate process.** 

>   Open document details by clicking on Document number hyperlink. Budget plan
>   is displayed as defined in the layout created during this lab. 

>    

Create current year budget based on previous year actuals 
----------------------------------------------------------

>   Allocation methods can be used in budget plan to easily copy information for
>   budget plans from one scenario to another/ spread them across periods/
>   allocate to dimensions. We will use allocations to create current year
>   budget from previous year actuals. 

1.  Pick all lines in the budget plan document grid and click button allocate
    budget 

2.  Select allocation method, Period key, Source and destination scenarios and
    click Allocate 

3.  The previous year actual amounts will be copied to current year budget and
    allocate them across periods using Sales curve period key. 

>    

Adjust budget plan document using Excel and finalize the document 
------------------------------------------------------------------

1.  Click Button worksheet to open document contents in Excel 

2.  When Excel workbook opens, adjust the numbers in budget plan document and
    click button Publish. 

3.  Return to budget plan document in Finance and Operations. Click Workflow \>
    Submit to Auto-approve the document 

4.  Once workflow completes, budget plan document stage changes to Approved.  
