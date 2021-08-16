---
lab:
    title: 'Exercise 7: Process Vendor payment by using a Payment journal'
    module: 'Module 4: Implement and manage accounts payable'
---

## Exercise 7: Process Vendor payment by using a Payment journal

Sometimes you might make a payment to a vendor that is less than the amount of an invoice. This article describes the various options for handling this situation. The options that are available to you depend on your business requirements and configuration.

This task guide will walk you through various methods used to create vendor payments, including how to use a payment proposal or manually enter a one-off payment. This procedure uses the USMF demo company.

1. Navigate to **Accounts payable &gt; Payments &gt; Vendor payment journal**.

2. Select **New**.

3. Select the payment journal in which to save the vendor payments.

4. Select the journal **Name** or manually enter it.

5. Select **Lines**.

6. Select **Payment proposal**.

7. Select **Create payment proposal**. The payment proposal is a query used to select invoices for payment. You can edit the list of invoices to pay before creating or generating the vendor payments.

8. **Select invoices** for payment **by** due date, cash discount, or both.

9. Enter the date for comparing to the due date or cash discount.

10. **Optional**: Enter a payment date used for all payments. The date entered here will be the payment date for all payments created, regardless of the due date or cash discount date.  
‎

11. **Optional**: Enter a **minimum payment date** which may be used as the payment date. The **minimum payment date** will be the earliest date used when creating payments. For example, if an invoice has a due date after the minimum payment date, the due date will become the payment date instead of the minimum payment date in order to pay the invoice on the latest possible date.  
‎

12. Enter additional query restrictions under **Records to include**. The filter is often used to restrict the invoices selected for payment by vendor group or method of payment. For example, you may add a filter to only pay invoices by check in this pay run.  
‎

13. Enter additional query restriction or payment defaults. The additional parameters can be used to define the payment currency or to enable centralized payments for this pay run.  
‎

14. Select **OK**. After selecting **OK**, the results of the query will appear. If you don't want to preview the list of invoices selected to pay, you can go back to the Parameters fast tab and change the setting **Create payments without invoice preview** = Yes.

15. Choose the **Show payment overview** button to view the payments that will be created for the vendor on the invoice selected.  
‎

16. Choose the **Hide payment overview** button to hide the payments.

17. Select **Create payments**. Before choosing Create payments, you can right select the grid and export the list of invoices to Excel. The Create payments button will create the vendor payments in the payment journal.



18. Scan your payments and make sure the method of payment is defined for all payments. If you generate the payments, such as printing a check or creating an electronic payment, the method of payment must be defined. The method of payment will also default from the bank account from the payment will be made.  
‎

19. Select **New** to create a one-off payment. A one-off payment can be added to a payment journal at any time prior to posting. This is done by selecting the New button and adding the payment information manually, rather than using the Payment proposal.  
‎

20. Select the vendor to whom the payment will be made.

21. If an invoice exists to pay, select **Settle transactions** to select the invoice for payment. If this is a prepayment, this step is optional. You can create the payment without selecting any invoices.  
‎

22. Mark any invoices that will be paid. If you use the Settle transactions to select the invoices for payment, the payment amount will automatically be calculated based on what invoices you mark for payment, and what amount you enter in the Amount to settle.

 

23. Select **OK**.

24. If you want to delete a payment, mark the row.

25. Select **Delete**. Deleting a payment will only delete the payment. Any invoices marked for payment will still be available to be paid by another payment.

 

26. Select **Yes**.

27. Choose **Generate payments** to print Checks or create the electronic payment file.

28. Select the method of payment that you want to generate. The payment journal can contain payments for both Checks and electronic payments, but you can only generate one payment type at a time.

 

29. Select the bank account from which to generate the payments.

30. Select **OK**. Payments will only be generated for payments that match the Method of payment and Bank account you selected.

 

31. If you are generating Checks, choose Document to ensure the correct print destination for the Checks.

32. Select **OK**.

33. Select **OK** to generate the payments.

34. Select Post if all the payments are approved and generated.

 

