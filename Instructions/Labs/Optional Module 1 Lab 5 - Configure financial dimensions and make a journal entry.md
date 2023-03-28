---
lab:
    title: 'Lab 5: Configure a dimension value'
    module: 'Module 1 Optional'
---

# Lab: Configure a dimension value

## Objective

You can use the Financial dimensions page to create financial dimensions and use these dimensions as account segments for charts of accounts. If you created a financial dimension, you can use the Financial dimension values page to assign additional properties to each financial dimension.

There are two types of financial dimensions: custom dimensions and entity-backed dimensions. Custom dimensions are shared across legal entities, and the values are entered and maintained by users. For entity-backed dimensions, the values are defined somewhere else in the system, such as in Customers or Stores entities.

### Scenario

Contoso, Ltd. has a new Sales and Marketing department. You need to set up the department as a cost center so that you can create a report of advertising costs for the cost center. This cost center is an example of an entity-backed dimension. The value of this dimension is defined somewhere else in the system. 

1.  Open your **Dynamics 365 Finance** environment and using the **Company picker**, change the legal entity to **USMF**. 


## Exercise 1: Create a new dimension value

During this lab you are going to add a new financial dimension value to an existing financial dimension. 

1.  In the **Organization administration** module, select **Organizations** > **Operating units**. 

2.  Select the **New** menu on the action pane to create a new **Cost center**. 

    ![](../images/Module_1_Activity_2_-_Configure_financial_dimensions_and_make_a_journal_entry_image2.png)

3.  Enter `Advertising` in the **Name** field. 

4.  Enter `250` in the **Cost center number* field. 

5.  Select **Save**. 
 
    ![](../images/Module_1_Activity_2_-_Configure_financial_dimensions_and_make_a_journal_entry_image3.png)


## Exercise 2: Verify the value has been created correctly

1.  In the **General ledger** module, select **Chart of Accounts** > **Dimensions** > **Financial dimensions**. 

2.  Select the **CostCenter** dimension from the list. 

    ![](../images/Module_1_Activity_2_-_Configure_financial_dimensions_and_make_a_journal_entry_image4.png)

3.  Select the **Dimension values** button in the action pane. 

    ![](../images/Module_1_Activity_2_-_Configure_financial_dimensions_and_make_a_journal_entry_image5.png)
 
4.  Enter `250` in the **Filter** field. 

5.  Select **Dimension value** in the **Filter**. 

    ![](../images/Module_1_Activity_2_-_Configure_financial_dimensions_and_make_a_journal_entry_image6.png)

6.  Verify the **Dimension value** 250, with **Description** `Advertising` appears in the list. 

    > **Note:** You cannot enter a dimension value for the financial dimension cost center because this is an **entity-backed** dimension. 


## Exercise 3: Add the value to the account structure

In USMF, the Manufacturing P&L account structure is set up as profit and loss main accounts. You need to make a journal entry for the cost center that you created in the account structure. 

1.  In the **General ledger** module, select **Chart of accounts** > **Structures** > **Configure account structures**. 

2.  Open the **Manufacturing P&amp;L** record.  

    ![](../images/Module_1_Activity_2_-_Configure_financial_dimensions_and_make_a_journal_entry_image7.png)

3.  Select **Edit**. 

    > **Note:** The new Cost Center 250 Advertising already belongs to the Sales and Marketing department 022. You need to adjust the line in the **Segments and allowed values** grid which refers to department 022. The purpose here is to configure the account structure so that if the sales and marketing dimension is selected in a journal line, only the cost centers 007 Trade Shows, 008 Marketing campaign, and 250 Advertising will be available for selection. 

4.  Enter the following information in 022's Cost Center field: **"";007..008;250** and make sure to check the **Blank Values are allowed("")** under the **Allowed value details** FastTab. 

    > **Note:** The following symbols are used in the **Cost Center** column: 

    | **Symbol** | **Meaning** |
    | ---------- | ----------- |
    | ""         | *Blank values are allowed.* |
    | ..         | *A range of values is allowed.* For the entry in step 4, the range of numbers from 007 to 008 is allowed |
    | ;          | *And.* For the entry in step 4, blank values are allowed and the range of numbers from 007 to 008 is allowed. |

    ![](../images/Module_1_Activity_2_-_Configure_financial_dimensions_and_make_a_journal_entry_image8.png)

5.  Select **Activate** in the action pane. 

6.  To start the process, select **Activate** in the **Activate account structure** pane. 

7.  **Close** the form. 

8.  You need to give the system time to activate the account structure. **Wait at least one minute** before you continue with the next exercise. 


## Exercise 4: Apply the new financial dimension value in a Journal

1.  In the **General ledger** module, select **Journal entries** > **General journals**. 

2.  Select the **+New** button to create a new journal. 

3.  Select `GenJrn` in the **Name** field. 

    ![](../images/Module_1_Activity_2_-_Configure_financial_dimensions_and_make_a_journal_entry_image9.png)

4.  Select the **Lines** button in the action pane. 

5.  Change the **Date** field to `1/5/2022`

6.  Enter `601600-001-022-250-` in the **Account** field. 

    > **Note:** Hovering over the **Account** field will show the **Segment** and **Names** of the selected Account dimensions.

7.  Enter `1500` in the **Debit** field. 

    ![](../images/Module_1_Activity_2_-_Configure_financial_dimensions_and_make_a_journal_entry_image10.png)

9.  Select main account `200190` in the **Offset account** field. 

10. **Save** and **Post** the journal. 

11. **Close** the form. 

