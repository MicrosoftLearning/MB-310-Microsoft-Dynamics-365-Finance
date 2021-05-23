---
lab:
    title: 'Exercise 6: Record invoice by using Invoice register, approval and Invoice journals'
    module: 'Module 4: Implement and manage accounts payable'
---


## Exercise 6: Record invoice by using Invoice register, approval and Invoice journals

The following steps show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.

### Create and post and invoice

1. In **USMF**, navigate to **Accounts payable &gt; Invoices &gt; Invoice register**.

2. Select **+New**.

3. Select the name of the invoice register that you want to use.

4. Select **Lines** to open the register and enter expense lines.

5. Select a vendor. For example, enter or select **US-104**.

6. In the **Invoice** field, enter a value.

7. In the **Description** field, enter a value.

8. In the **Credit** field, enter a number.

9. In the **Approved by** field in the **Invoice** section, select the drop-down button to open the lookup.

10. Highlight an approver and select **Select** to select that approver.

11. Select **Post**.

12. Close all pages.

### Approve an invoice

1. Navigate to **Accounts payable &gt; Invoices &gt; Invoice approval**.

2. Select **+New**.

3. Select the name of the invoice approval journal that you want to use.

4. Select lines to display a page where you will be able to select the invoices that you want to approve.

5. Select **Find Vouchers** to display all of the invoices that are ready for approval.

6. Mark the invoice that you created, ensuring that the checkmark is on the left.

7. Select **Select**. The vouchers that you selected above are moved to this list after you select them.

8. Select **OK**.

9. Select the **account number** field to add an expense account to the invoice.

10. Enter an account number and tab off of the field. For example, enter 600120.

11. Select **Post**.

12. Select **Voucher** from the middle section to view the entries that were posted. The Invoice Pending Approval account is reversed and replaced with the actual expense account.

13. Close all pages.

Record a vendor invoice in the invoice journal

Let’s now see how to record vendor invoices that are not associated with purchase orders. Examples of this type of invoice include expenses for supplies or services. This recording uses the USMF demo company.

1. Navigate to **Accounts payable &gt; Workspaces &gt; Vendor invoice entry**.

2. Select **+New invoice journal**.

3. Select **N+ew**.

4. In the **Name** field, enter the journal name or select the drop-down button to open the lookup.

5. In the **Description** field, enter a value.

6. Select **Lines**.

7. In the **Date** field, enter the posting date that will update General Ledger.

8. In the **Account** field, specify the **Vendor account**.

9. In the **Invoice** field, enter the invoice number.

10. In the **Description** field, enter a value.

11. In the **Credit** field, enter a number.

12. In the **Offset account** field, select an expense account number.

13. The Sales tax group will default from the vendor account.

14. The Item sales tax group will default from the main account specified in the Offset account field.

15. The Due date will be calculated based on the Terms of payment.

16. The Cash discount will default from the Vendor account.

17. Select **Post**.

18. Close the page.

 
