Exercise: Create Fiscal establishment (Brazil)
==============================================

As a functional consultant for **BRMF** company, you are responsible to create
one or more fiscal establishments for a legal entity located in Brazil. A fiscal
establishment requires a Cadastro Nacional da Pessoa Jurídica (CNPJ) or
Inscrição Estadual (IE) tax registration number. You can group fiscal
establishments and set up tax groups for each fiscal establishment group in the
Taxes matrix page.

1.  Navigate to **Organization administration \> Organizations \> Legal
    entities**.

2.  Select the **BRMF** entity.

3.  Expand the **Addresses** section.

4.  Click **Add**.

5.  In the **Name** or **description** field, type a value.

6.  In the **Purpose** field, enter or select a value.

7.  In the **Country/region** field, type a value.

8.  Click **Yes**.

9.  In the **ZIP/postal code** field, type a value.

10. In the **Street number** field, type a value.

11. Click **OK**.

12. Close all forms.

13. Navigate to **Organization administration \> Organizations \> Fiscal
    establishments \> Fiscal establishment group**s.

14. Create new fiscal establishment group.

15. In the **Fiscal establishment group** field, type a value.

16. In the **Description** field, type a value.

17. Click **Save**.

18. Close the page.

19. Go to **Organization administration \> Organizations \> Fiscal
    establishments \> Fiscal establishments**.

20. Create new fiscal establishment.

21. In the **Fiscal establishment ID** field, type a value.

22. In the **Fiscal establishment group** field, enter or select a value.

23. In the **CNPJ** field, enter the **CNPJ** of the new fiscal establishment.

24. Expand the **Address** section.

25. In the **Name** field, enter or select a value.

26. In the **IE** field, enter the **IE** of the fiscal establishment based on
    the state in the address.

27. Click **Save**.

28. Close the page.

29. Go to **Inventory management \> Setup \> Inventory breakdown \> Sites**.

30. Click **New**.

31. In the **Site** field, type a value.

32. In the **Name** field, type a value.

33. In the **Fiscal establishment ID** field, enter or select a value.

34. Expand the **Financial dimensions** section.

35. Click to follow the link in the **Filial** field.

36. Click **New**.

37. In the **Dimension value** field, type a value.

38. In the **Description** field, type a value.

39. Click **Add** to open the drop dialog.

40. Click **Add**.

41. Click **Save**.

42. Close the page.

43. In the **Filial** field, enter or select a value.

44. Click **Save**.

45. Close the page.

46. Go to **Organization administration \> Organizations \> Fiscal
    establishments \> Fiscal establishments**.

47. Open the advanced row selection dialog

48. Apply the following filters: Enter a filter value of "NovaFilial" on the
    "Fiscal establishment ID" field using the "is exactly" filter operator

49. Click **Fiscal document types.**

50. Click **New**.

51. In the **Fiscal document type** field, type a value.

52. In the **Name** field, type a value.

53. In the **Series** field, type a value.

54. In the **Fiscal document number sequence** field, enter or select a value.

55. In the **Document model** field, enter or select a value.

56. Click **Save**.

57. Close all forms.

Exercise: Configure and test Electronic invoices (CFDI)
=======================================================

MX-00010 E-invoicing CFDI
-------------------------

You can create and post multiple sales orders as electronic invoices and send
the .pdf and .xml files

1.  In **MXMF**, Go to **Accounts receivable \> Orders \> All sales orders**.

2.  Click **New**.

3.  In the **Customer account** field, click the drop-down button to open the
    lookup.

4.  In the list, find and select the desired record.

5.  Click **OK**.

6.  In the **Item number** field, click the drop-down button to open the lookup.

7.  Select an item.

8.  In the **Unit price** field, enter a number.

9.  Expand or collapse the **Line details** section.

10. Click the **Setup** tab.

11. In the **Sales tax group** field, click the drop-down button to open the
    lookup.

12. In the list, click the link in the selected row.

13. In the **Item sales tax group** field, click the drop-down button to open
    the lookup.

14. In the list, find and select the desired record.

15. Click the **Product** tab.

16. In the **Warehouse** field, click the drop-down button to open the lookup.

17. In the list, find and select the desired record.

18. Click **OK**.

19. In the **Custom number** field, type a value.

20. Enter the number of the customs document that was generated when the item
    was imported.

21. In the **Custom date** field, enter a date.

22. Select the date when the item was imported.

23. In the **Custom name** field, type a value.

24. Enter the name of the customs authority in the country/region that the item
    was imported from. If you enter values in the **Custom number, Custom date,
    and Custom name** fields, you cannot enter a value in the Property number
    field.

25. In the **Unit price** field, enter a number.

26. Expand or collapse the Sales order header section.

27. On the **Action Pane**, click **Sell**.

28. Click **Confirm** sales order.

29. Click **OK**.

30. Click **OK**.

31. On the Action Pane, click **Invoice**.

32. Click Invoice.

33. Expand the **Parameters** section to review the parameters before posting.

34. Click **OK**.

35. After you press **OK**, the customer invoice is posted and scheduled in a
    specific batch processing for issuing electronic invoices (CFDI).

36. Click **OK**.

37. Go to **Accounts receivable \> Invoices \> E-Invoices \> Export/import
    electronic invoice process**.

38. Click **OK**.

39. This batch job initiates the connection with the PAC web services to get the
    approval or cancellation of an electronic invoice (CFDI). The task in the
    batch can run manually or it can be scheduled by specific period of time.
    After you press OK, the validation and the digital signature will be
    retrieved from the PAC. If the electronic invoice is approved, the PAC send
    the response XML message and the status of the electronic invoice will
    update to be Approved. An email is automatically sent out to the customer
    with the XML and PDF file attached. The Send mail and Send report file - PDF
    sliders must be set to "Yes" on the electronic invoice parameters page.
    Otherwise, you can email or print PDF report based on the customer's request
    by using the Inquire and Reports \> CFDI (electronic invoices) menu.

40. Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic
    invoices).**

41. In the list, click the electronic invoice to review. as email attachments to
    customers.

MX-00010 Inquire and print an electronic invoice
------------------------------------------------

Use the CFDI – Electronic invoices form to view, email, export, or print an
already-generated CFDI electronic invoice based on a customer’s request. The
printed CFDI electronic invoice includes two-dimensional bar code in accordance
with the format of QR Code (Quick Response Code) that is described in the
standard ISO/IEC18004.

1.  In **MXMF**, Go to **Accounts receivable \> Inquiries and reports \> CFDI
    (electronic invoices).**

2.  In the list, click the link in the selected row.

3.  You will be able to see some details of the **CFDI electronic invoice** as
    **UUID** and **status**.

4.  On the Action Pane, click **Functions**.

5.  Click **View XML file**.

6.  Close the page.

7.  On the Action Pane, click **Functions**.

8.  Click **Export XML**.

9.  You will be prompted to download the file to a specific location.

10. On the Action Pane, click **Functions**.

11. Click **Send e-mail**.

12. Close the page.

13. Refresh the page.

Import a configuration including XML formats
--------------------------------------------

1.  Go to **Organization administration \> Workspaces \> Electronic reporting**.

2.  In the **Configuration providers** list, click **Set active** on the
    **Microsoft provider** box. If the Microsoft provider is already the active
    provider, you can skip this step.

3.  Click **Reporting configurations**

4.  Click **Exchange** and select the option **Load from XML file**

5.  Select and browse the XML model file previously downloaded from LCS and then
    click **OK** to confirm

6.  Repeat the steps 4 and 5 to import the rest of XML file formats

You will be able to see one (1) model and the four (4) XML formats that you
previously imported.

Configure general ledger parameters for electronic reporting mapping
--------------------------------------------------------------------

1.  Go to **General ledger \> Ledger setup \> General ledger parameters**.

2.  In the **Trial balance** field, click the drop-down button to open the
    lookup.

3.  In the list, select the **Trial Balance XML format**

4.  In the **Auxiliary ledger** field, click the drop-down button to open the
    lookup.

5.  In the list, select the **Auxiliary ledger XML format**

6.  In the **Ledger entries** field, click the drop-down button to open the
    lookup.

7.  In the list, select the Journal XML format

8.  In the **Chart of accounts** field, click the drop-down button to open the
    lookup.

9.  In the list, select the Chart of **Account XML format**.

10. Click **Save**.

Generate XML files
------------------

1.  Go to **General ledger \> Inquiries and reports \> Ledger reports \>
    Electronic ledger accounting statement.**

2.  In the **SAT consolidation account group** field, click the drop-down button
    to open the lookup.

3.  In the list, find and select the desired record.

4.  In the **Period** field, enter a date.

5.  Check or uncheck the **Trial Balance opcion** This option generates the
    **Chart of Account and Trial Balance XM**L files.

6.  Select or clear the **Ledger entries** check box.

7.  Select or clear the **Auxiliary ledger** check box.

8.  In the **Request type** field, select an option.

9.  In the **Order number** field, type a value.

10. Click **OK**.
