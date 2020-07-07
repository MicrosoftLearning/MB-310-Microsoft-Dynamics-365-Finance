Exercise: Set up Funds
======================

Create a fund type in the public sector
---------------------------------------

1.  Go to **General ledger \> Chart of accounts \> Funds \> Fund types**.

2.  Click **New**.

3.  In the **Fund type** field, type **DEBT SERV**.

4.  In the **Description** field, type **Foreclosure Loan Services**.

5.  Click **Save**.

6.  Click **Close**.

Set up a fund in the public sector
----------------------------------

Fund types must be created before you set up funds. Each fund must have a name
and a unique number, and must be assigned a fund type and fund class.

1.  Go to **General ledger \> Chart of accounts \> Funds \> Funds**.

2.  Click **New**.

3.  In the **Fund number** field, type **1050**.

4.  In the **Fund name** field, type **Foreclosure Loans Fund**.

5.  In the **Fund type** field, click the drop-down button to open the lookup.

6.  In the list, select the fund type **DEBT SERV**.

7.  In the **Fund class** field, select **Fiduciary**.

8.  Set the **Non-reporting fund** option to **No**.

9.  Set the **Major fund** option to **No**.

10. Click **Save**.

11. Click **Close**.

Exercise: Derived financial hierarchies
=======================================

Create a category hierarchy
---------------------------

1.  Go to **Product information management \> Setup \> Categories and attributes
    \> Category hierarchies**.

2.  Click **New**.

3.  In the **Name** field, type **GTL-Derived Hierarchy**.

4.  In the **Description** field, type **Derived Hierarchy**.

5.  Click **Create**.

6.  Click **New category node**.

7.  In the **Name** field, type **GTL-Custom**.

8.  In the **Code** field, type **0819**.

9.  Click **New category node**.

10. In the **Name** field, type **GTL-Education**.

11. In the **Code** field, type **08191**.

12. Select **GTL-Custom**

13. Click **New category node**.

14. In the **Name** field, type **GTL-Public Service**.

15. In the **Code** field, type **08192**.

16. Click Save.

17. Close all forms.

Assign the Derived financial hierarchy category type
----------------------------------------------------

1.  Go to **Product information management \> Setup \> Categories and attributes
    \> Category hierarchy role associations**.

2.  Click **New**.

3.  In the **Category hierarchy type** field, select **'Derived financial
    hierarchy'**.

4.  In the **Category hierarchy** field, click the drop-down button to open the
    lookup.

5.  In the list, click the Category hierarchy **GTL-Derived Hierarchy**.to
    associate with the Derived financial hierarchy type.

6.  Click **Save**.

7.  Close all forms.

Associate the derived financial hierarchy with a legal entity
-------------------------------------------------------------

1.  Go to **General ledger \> Chart of accounts \> Dimensions \> Associate
    financial hierarchies**.

2.  Click **New**.

3.  In the **Legal entity** field, click the drop-down button to open the
    lookup.

4.  In the list, select the **USMF** legal entity to associate with the derived
    financial hierarchy.

5.  In the **Derived financial hierarchy** field, click the drop-down button to
    open the lookup.

6.  In the list, select the **GTL-Derived Hierarchy** derived financial
    hierarchy to associate with the legal entity.

7.  Click **Save**.

8.  Close all forms.

Create filter rules for the derived financial hierarchy
-------------------------------------------------------

1.  Go to **General ledger \> Chart of accounts \> Dimensions \> Derived
    financial hierarchies**.

2.  In the Derived financial hierarchy field, click the drop-down button to open
    the lookup.

3.  In the list, click the **GTL-Derived Hierarchy** to create filter rules for.

4.  In the tree, select 'In the tree, select **GTL-Education**

5.  Click **Edit filter**.

6.  Click **Add new criteria** to begin adding rules to the filter.

7.  For example, have rule for where Department is between and includes 024
    through 029.

8.  After you've added all of the criteria, click **Activate filter**.

Exercise: Configure and test Billing codes for free text invoices
=================================================================

To create a custom field, follow these steps:
---------------------------------------------

1.  Navigate to **Accounts receivable\>Setup\>Billing code custom fields**

2.  Click **New**.

3.  In the **Name** field, type '**Emergency**'.

4.  In the **Type** field, select **'Boolean'**.

5.  Click **Save**.

6.  Click **New**.

7.  In the Name field, type **'Lease amount**'.

8.  In the **Type** field, select **'Currency'**.

9.  Select **Yes** in the **Enforce minimum value** field.

10. Set **Default** to '6700.00'.

11. Set **Minimum value** to '5000.00'.

12. Click **Save**.

13. Close the page.

To create a billing code, follow these steps:
---------------------------------------------

The City of Maple has decided to implement a new licensing requirement for
business owners. There is a flat charge of \$30 U.S. dollars (USD) for the
license. Ken, the Controller, identifies the ledger account to use for the new
revenue. He determines that no taxes apply to the revenue. He passes this
information on to Phyllis, the Accounting Manager, and asks her to set up a new
billing code for the business license.

1.  To open the Billing codes form, click **Accounts receivable \>Setup \>
    Billing codes.**

2.  Click **New**.

3.  To create a unique ID for the billing code, in the Billing code field, type
    “**Biz Lic**”.

4.  In the **Description** field, type “Business License 2019”.

5.  To enter an effective date that is different from the current date, click
    the **Effective field** and select the required date. The current date is
    the default effective date.

6.  To avoid applying any taxes and interest, on the **Taxes and Interests**
    FastTab, Set **the Use interest from billing classification** option to
    **No**. Set this option to **Yes** in order to use the interest code
    specified on the billing classification when calculating interest for this
    billing code. If this option is not selected, and the Interest code is not
    specified, interest will not be calculated.

7.  To distribute the financial consequence of the transaction to ledger
    accounts, on the **Accounting distribution** FastTab, click **Add**, and
    then in the Ledger account field, type “110180-078-024-”.

8.  To define and evaluate a rate expression, on the **Rate** FastTab, in the
    Billing code determines field, select **Line amount.**

9.  In the amount field type 650.00

10. On the **Custom fields** FastTab click **Add**

11. Select Emergency and Lease amounts in the **Billing code custom fields**
    form and click **Add**.

12. Click **OK**.

13. Close all forms.

Setup Billing Classifications
-----------------------------

To create a billing classification and associate a billing code to this
classification, follow these steps:

The City of Maple has hired an administrator to handle all transactions related
to business. Phyllis, the Accounting Manager, needs to create a setup for the
administrator where accounts receivable for business invoices and charges are
easily separable from other invoices.

In addition to hiring a new administrator, the City of Maple will soon begin
adding a separate charge for business licenses on specific invoices. For
consistent invoicing for this new charge, Phyllis has already created a billing
code named “Biz Lic”. Now, she has to associate this new billing code with the
BUSINESS billing classification. Finally, she also wants to ensure that these
business license-related invoices are settled before general invoices.

1.  To open the **Billing classifications** form, click **Accounts receivable \>
    Setup \> Billing classifications**.

2.  Click **New**.

3.  In the Billing classification field, type “**BUSINESS**”.

4.  In the **Description** field, type “**Business invoices and charges**”.

5.  On the **Policies** FastTab, in the **Terms of payment** field, select
    **Net30**.

6.  To determine the interest, enable the **Use interest code from posting
    profile** option.

7.  To determine the collection letter sequence, enable the **Use collection
    letter sequence from posting profile** option.

8.  Click **Save**.

9.  To associate a billing code with this billing classification, on the Billing
    codes FastTab, click **Add**, and then in the Billing code field, select
    **Biz Lic**.

10. Close all forms.  
    ‎

### To create a free text invoice using billing codes, follow these steps:

Arnie, the Accounts Receivable Administrator for the City of Maple, has to
charge the Oak Company for renting the city’s golf course in zip code 98052 over
the weekend as a part of its annual corporate sports event.

1.  To open the Free text invoices list page, click **Accounts receivable \>
    Invoices** \>**All free text invoices**.

2.  To open the Free text invoice form, on the **Action Pane**, in the **New**
    group, click **Free text invoice**.

3.  In the **Customer account** field and select **Cave Wholesales** as the
    customer.

4.  To select the Parks classification, in the **Billing classification** field,
    select **BUSINESS**.

5.  To add the billing code, in the **Invoice lines** grid, click **Add line.**

6.  Click the arrow in the **Billing code** field and select the **Biz Lic**
    billing code.

7.  Enter 5 in the **Quantity** field.

8.  Enter 14.95 in the **Unit price** field

9.  Click **Custom fields**

10. In the **Emergency** field, select **Yes.**

11. In the **Lease amount** field, type **5200.**

12. Click **OK**.

13. Close all forms.  
    ‎
