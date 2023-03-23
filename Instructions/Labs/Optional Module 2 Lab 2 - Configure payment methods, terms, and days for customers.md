---
lab:
    title: 'Lab 2: Configure payment methods, terms, and days for customers'
    module: 'Module 2 Optional'
---

# Lab: Configure payment methods, terms, and days for customers

## Objective

Payment terms determine how you manage due dates. The same payment terms are available for sales and purchase documents. When you post an invoice, the due date is calculated based on the payment terms. Each payment type that a company accepts must be configured when the system is set up. 

You can use payment days to define the payment day used for calculating the due date. Payment day can be specified for either a day in the week or in the month. This helps payment proposal to suggest those customer invoices that should be brought into the customer payment journal for posting. 

In this this lab you will set up a payment method for customers. You will then set up terms of payment. Finally, you will set up a payment day. 

### Scenario 

You need to set up a new payment method for the customers so that they can use PayPal as a payment method. You also need to configure terms of payment for net payment within five days. You must configure a payment date for the first of each month. 

1.  Open your **Dynamics 365 Finance** environment and using the **Company picker**, change the legal entity to **USMF**. 


## Exercise 1: Configure a payment method

1.  In the **Accounts receivable** module, select **Payments setup** > **Methods of payment**. 

2.  Select **+New** to create a new method of payment. 

3.  Enter `PayPal` in the **Method of payment** field. 

4.  Select **Invoice** in the **Period** field. 

    > **Note:** This setting means one payment transfer for each invoice.

5.  Enter `PayPal` in the **Description** field. 

6.  Select **Other** in the **Payment type** field.

7.  In the **General** FastTab, select **Bank** in the **Account type** field. 

8.  Select or enter `USMF OPER` in the **Payment account** field. 

9.  **Save** the data and **close** the form. 

    ![](../images/Module_3_Activity_2_-_Configure_payment_methods,_terms,_and_days_image1.png)


## Exercise 2: Configure terms of payment

1.  In the **Accounts receivable** module, select **Payments setup** > **Terms of payment**. 

2.  Select **+New** to create new terms. 

3.  Enter `Net5` in the **Terms of payment** field. 

4.  Enter `Net 5 days` in the **Description** field. 

5.  In the **Setup** FastTab, enter `5` in the **Days** field.  

6.  **Save** the data and **close** the form. 

    ![](../images/Module_3_Activity_2_-_Configure_payment_methods,_terms,_and_days_image2.png)  


## Exercise 3: Configure Payment days

1.  In the **Accounts receivable** module, select **Payments setup** > **Payment days**. 

2.  Select **+New** to create a new Payment day. 

3.  Enter `1st` in the **Payment day** field. 

4.  Enter `1st day of the month` in the **Description** field. 

5.  In the **Payment day lines** grid, select or enter `Month` in the **Week/Month** field. 

6.  Enter `1` in the **Day of the month** field. 

7.  **Save** the data and **close** the form. 

    ![](../images/Module_3_Activity_2_-_Configure_payment_methods,_terms,_and_days_image3.png)


## Exercise 4: Add the new settings to a customer

1.  In the **Accounts receivable** module, select **Customers** > **All customers**. 

2.  Select `US-040`

3.  Navigate to and expand the **Payment defaults** FastTab. 

4.  Select or enter `Net5` in the **Terms of payment** field. 

5.  Select or enter `PayPal` in the **Method of payment** field. 

6.  Select or enter `1st` in the **Payment day** field. 

7.  **Save** the data and **close** the form.  

