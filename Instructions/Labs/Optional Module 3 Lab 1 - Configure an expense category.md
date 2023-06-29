---
lab:
    title: 'Lab 1: Configure an expense category'
    module: 'LP 3 Optional'
---

# Lab: Configure an expense category 

## Objective

Employees must assign their expenses to predefined categories when they are completing expense reports. You can create the following types of expense categories:

- Categories for use by a single company - This type of category includes information about payment methods, expense types, cost splitting, and subcategories. These expense types can be used only for expenses that are charged to the company in which they are created.

- Shared categories - Any legal entity in your enterprise can use shared expense categories.

### Scenario 

A financial controller at Contoso is setting up a new expense category that allows employees to declare representation costs (for example, a business lunch with a potential customer and costs for business events such as conferences or promotional gifts).

1.  Open your **Dynamics 365 Finance** environment and using the **Company picker**, change the legal entity to **USMF**. 


## Exercise 1: Configure a shared category 

You must create a category named **Representation costs** and track these costs a miscellaneous expense type with a default method of payment method of Company Credit Card. These expenses must be posted to account 601600, Promotional Expenses.

1.  In the **Expense management** module, select **Setup** > **General** > **Shared categories**. 

2.  Select **+New** to create a new shared category. 

3.  Enter `Representation` in the **Category ID** field. 

4.  Enter `Representation Costs` in the **Category name** field. 

5.  Set the **Can be used in Expense** field to **Yes**. 

6.  Select or enter `Miscellaneous` in the the **Expense type** field. 

7.  **Save** the data and **close** the form. 

    ![](../images/Module_2_Activity_2_-_Create_and_use_an_expense_category_image1.png)


## Exercise 2: Configure an expense category

1.  In the **Expense management** module, select **Setup** > **General** > **Expense categories**. 

2.  Select **+New** to create a new expense category. 

3.  Enter `Representation` in the **Category ID** field. 

4.  Expand the **Expense** FastTab and select **CreditCard** in the **Default payment method** field. 

5.  Enter `601600` in the **Main account** field. 

6.  **Save** the data and **close** the form. 

    ![](../images/Module_2_Activity_2_-_Create_and_use_an_expense_category_image2.png)
 

## Exercise 3: Create an expense report that uses the new expense category

1.  In the **Expense management** module, select **My expenses** > **Expense reports**. 

2.  Select **+New expense report** to create a new report. 

3.  Select or enter `Customer visit` in the **Purpose** field. 

4.  Select or enter `MainOffice` in the **Location** field. 

5.  Select **OK**. 

6.  Enter `2/1/2022` as the **Transaction date**. 

7.  Select or enter `Representation` in the mandatory **Expense category** field. 

8.  Enter `150.00` in the mandatory **Transaction amount** field. 

9.  **Save** the data. 

10. Select the **Workflow** menu in the action pane. You may need to select the **More menu (...)** to see the option. 

11. Select **Submit**. 

12. Enter `Dinner with a potential customer` in the comment field. 

13. **Submit** the expense report. 

    ![](../images/Module_2_Activity_2_-_Create_and_use_an_expense_category_image3.png)

    The approval status of the expense report will change to **In review**. 

    ![](../images/Module_2_Activity_2_-_Create_and_use_an_expense_category_image4.png)

