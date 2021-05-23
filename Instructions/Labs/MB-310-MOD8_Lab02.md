---
lab:
    title: 'Exercise 2: Set up and create depreciation profiles'
    module: 'Module 8: Configure and manage fixed assets'
---

## Exercise 2: Set up and create depreciation profiles

Depreciation profiles determine the type and the frequency of depreciation for an asset. As accountant role, perform the following:

### Create a depreciation profile

1. Navigate to **Fixed assets &gt; Setup &gt; Depreciation profiles**.

2. Select **+New**.

3. In the **Depreciation** profile field, enter a value.

4. In the **Name** field, enter a value.

5. In the **Method** field, select an option. If selecting reducing balance, you will need to enter a percentage in the Percentage field.

6. In the **Depreciation** **year** field, select an option.

7. In the **Period** **frequency** field, select an option.

8. Close the form.

### Create a book

1. Navigate to **Fixed assets &gt; Setup &gt; Books**.

2. Select **+New**.

3. In the **Book** field, enter a value.

4. In the **Description** field, enter a value.

5. If Calculate depreciation is selected, the associated asset book will be included in depreciation proposals. If it is not selected, the asset book will not be automatically depreciated.

6. Select **Yes** in the **Calculate depreciation** field.

7. In the **Depreciation profile** field, enter or select a value.

8. Select **Yes** in the **Create depreciation adjustments with basis adjustments** field.

9. By default, fixed asset book transactions will post to the general ledger. You can disable posting to the general ledger for the book by setting the **Post to general ledger** field to **No**.

10. Books that do not post to the general ledger are typically used for tax reporting purposes. This gives you additional flexibility to delete historical transactions for the asset book because they have not been committed to the general ledger.

11. The **Posting layer** defaults to the Current layer if the book posts to general ledger, and None if it does not post to general ledger. Update the **Posting layer** field if you need transactions for this book to be posted to a different layer.

12. In the **Calendar** field, enter or select a value.

13. Derived books will post transactions to different books at the same time. You create the transactions with the primary book, and during posting, an exact copy of the transaction is posted to the derived book. There is no recalculation with derived book transactions, so it should not be used for depreciation transactions.

### Associate the book with a fixed asset group

1. Select **Fixed asset groups**.

2. In the **Fixed asset group** field, enter or select a value.

3. In the **Service life** field, enter a number.

4. Note that **Depreciation** periods is calculated after setting the Service life.

5. You can set the depreciation convention as required for tax purposes.

 
