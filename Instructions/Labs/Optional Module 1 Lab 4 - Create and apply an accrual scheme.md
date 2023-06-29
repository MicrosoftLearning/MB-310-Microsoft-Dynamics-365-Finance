---
lab:
    title: 'Lab: Accrual schemes'
    module: 'Optional LP 1: Set up and configure financial management'
---

# Lab: Accrual schemes

You create accrual schemes to set up deferred revenue and costs. Ledger accruals redistribute the costs or revenue of a journal line so that the costs and revenues are recognized in the appropriate periods. 

In the **Accrual schemes** page, you specify the debit and the credit accounts that will be used when the accrual scheme is applied. 

- **Debit** - The main account that you define will replace the debit main account on the journal voucher line. This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.

- **Credit** - the main account that you define will replace the credit main account on the journal voucher line. This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.

## Objective 

In this lab, you will set up a ledger accrual scheme and use the accrual scheme in a journal. 

### Scenario 

The accounting manager at Contoso Ltd. wants to redistribute the costs of an insurance policy throughout the year. The cost of the insurance policy is $5,520.00. Use the following information to set up a ledger accrual for the insurance policy: 

- Pay the total amount for the policy at one time. 

- Divide the invoice into twelve payments. 


1.  Open your **Dynamics 365 Finance** environment and using the **Company picker**, change the legal entity to **USMF**. 


## Exercise 1: Create an Accrual scheme

In this exercise you set will up a ledger accrual scheme. 

1.  In the **General ledger** module, select **Journal Setup** > **Accrual schemes**. 

2.  Select the **+New** button. 

    ![](../images/Module_1_Activity_1_-_Create_and_apply_an_accrual_scheme_image1.png) 

3.  Enter `M_INS` in the **Accrual identification** field. Enter **Monthly Insurance** as the **Description of accrual scheme*. 

4.  Select account number `200190` for the **Debit** and **Credit** fields. 

5.  For **Voucher**, select **New voucher for accrual transactions**. 

6.  Select or enter `APInv_01` for **Number sequence code**.  

7.  Select `Calendar` as **Accrual basis**. 

8.  Select `Monthly` as the **Period frequency**. 

9.  Enter `12` as **Number of occurrences by period**. 

10. Select `Month` for **Post transactions**. 

11. Select `Beginning` in the **Post in week, month or quarter** field. 

12. Select `Evenly` in the **Spread month and quarter values** field.

    ![](../images/Module_1_Activity_1_-_Create_and_apply_an_accrual_scheme_image2.png)

13. **Save** and **close** the form. 


## Exercise 2: Apply the accrual scheme 

In this exercise you will apply the accrual scheme from exercise 1 in a journal.

1.  In the **General ledger** module, select **Journal entries** > **General journals**. 

    ![](../images/Module_1_Activity_1_-_Create_and_apply_an_accrual_scheme_image3.png)

2.  Select the **+New** button in the action pane to create a new journal. 

3.  Select or enter `GenJrn` in the **Name** field. 

    ![](../images/Module_1_Activity_1_-_Create_and_apply_an_accrual_scheme_image4.png)

4.  Select the **Lines** button in the action pane. 

5.  Enter `1/31/2022` in the **Date** field. 

6.  Enter `606200--` in the **Account** field, you can leave the dimensions fields empty. 

7.  Enter `5520.00` in the **Debit** field. 

8.  Select or enter main account `200190--` in the **Offset account**. 

9.  In the **Functions** menu on the toolbar, select **Ledger accruals**. 

    ![](../images/Module_1_Activity_1_-_Create_and_apply_an_accrual_scheme_image5.png)

10. In the Accrual identification field, select or enter `M_INS` 

11. Set the start date to `1/31/2022` 

    ![](../images/Module_1_Activity_1_-_Create_and_apply_an_accrual_scheme_image6.png)

12. Select **Transactions** and verify the costs are divided over the 12 defined periods. 

    ![](../images/Module_1_Activity_1_-_Create_and_apply_an_accrual_scheme_image7.png)

13. **Close** the screen, you will return to the previous screen. 

14. Select **OK** to accept the transactions and return to the journal line. 

15. **Post** the journal. 

16. Select **Voucher** in the toolbar. 

    ![](../images/Module_1_Activity_1_-_Create_and_apply_an_accrual_scheme_image8.png)

17. Select **Transaction origin** in the action pane to see the different journal lines per period. 

    ![](../images/Module_1_Activity_1_-_Create_and_apply_an_accrual_scheme_image9.png)

    ![](../images/Module_1_Activity_1_-_Create_and_apply_an_accrual_scheme_image10.png)

18. **Close** all forms.

