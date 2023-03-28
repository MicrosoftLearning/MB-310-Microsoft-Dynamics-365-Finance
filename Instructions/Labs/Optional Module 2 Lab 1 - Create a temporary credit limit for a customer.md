---
lab:
    title: 'Lab 1: Create a temporary credit limit for a customer'
    module: 'Module 2 Optional'
---

# Lab Create a temporary credit limit for a customer

## Objective

Temporary credit limits override customer credit limits for a defined period. You can add temporary credit limits by using credit limit adjustments. These adjustments let credit managers update the credit limits and end dates of a single customer, a group of customers, or all customers through a posting process. 

### Scenario 

You need to set up a temporary credit limit for customer **US-003** in legal entity **USMF**. The current credit limit for the customer is $400,000, until the end of next month, the limit is $500,000. 

1.  Open your **Dynamics 365 Finance** environment and using the **Company picker**, change the legal entity to **USMF**. 


## Exercise 1: Add a temporary credit limit for a customer

In this exercise you will set up a temporary credit limit for a customer of Contoso, Ltd. 

### Task 1: Identify the current credit limit for the customer

1.  In the **Credit and collections** module, select **Customers** > **All customers**. 

2.  Select customer `US-003` 

3.  Review the **Credit and Collections** FastTab. The total credit limit is $400,000. Do not navigate away from this page. 

    ![](../images/Module_3_Activity_1_-_Create_a_temporary_credit_limit_for_a_customer_image1.png) 


### Task 2: Create a temporary credit limit adjustment

1.  Select the **Credit management** tab on the action pane. 

    > **Note:** You may need to select the **More (...)** menu to reveal this tab. 

    ![](../images/Module_3_Activity_1_-_Create_a_temporary_credit_limit_for_a_customer_image2.png)
 
2.  Under the **New** section, select **Credit limit adjustments**. 

3.  Select **+New** in the action pane. 

    ![](../images/Module_3_Activity_1_-_Create_a_temporary_credit_limit_for_a_customer_image3.png)

4.  Select or enter `Temporary credit limit` in the **Credit limit adjustment type** field. 

    ![](../images/Module_3_Activity_1_-_Create_a_temporary_credit_limit_for_a_customer_image4.png)

5.  Enter the text `Temporary credit limit` for the **Description**. 

6.  Select **Lines** in the action pane. 

    ![](../images/Module_3_Activity_1_-_Create_a_temporary_credit_limit_for_a_customer_image5.png)

7.  Select or enter `US-003` in the **Customer account** field.

8.  Enter `450,000` in the **New credit limit** field. 

9.  Select **any date last month** in the **New from date** field. 

10. Select **any date next month** in the **Expiration date** field. These two dates ensure that the current date is between the **New from date** and the **Expiration date** of the temporary credit limit. 

11. **Save** the data and **Post** the journal. 

    ![](../images/Module_3_Activity_1_-_Create_a_temporary_credit_limit_for_a_customer_image6.png)

12. **Close** the form. 


### Task 3: Verify the temporary credit limit

1.  In the **Credit and collections** module, select **Customers** > **All customers**. 

2.  Select customer `US-003` 

3.  Review the **Credit and collections** FastTab. Verify the **Total credit limit** is $450,000. The **Temporary credit limit** has been added. 

    ![](../images/Module_3_Activity_1_-_Create_a_temporary_credit_limit_for_a_customer_image7.png)

