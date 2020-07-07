Exercise: Configure and test Electronic Reporting
=================================================

Download Electronic reporting configurations from Lifecycle Services
--------------------------------------------------------------------

Go to **Organization administration \> Electronic reporting**.

In the **Configuration providers** section, select the **Microsoft** tile.

1.  On the **Microsoft** tile, click **Repositories**.

2.  On the **Configuration repositories** page, in the grid, select the existing
    repository of the [LCS](https://lcs.dynamics.com/) type. If this repository
    doesn't appear in the grid, follow these steps:

3.  Click **Add** to add a new repository.

4.  Select **LCS** as the repository type.

5.  Click **Create repository**.

6.  If prompted, follow the authorization instructions.

7.  Enter a name and description for the repository.

8.  Click **OK** to confirm the new repository entry.

9.  In the grid, select the new repository of the LCS type.

10. Click **Open** to view the list of ER configurations for the selected
    repository.

11. In the configurations tree in the left pane, select the ER configuration
    that you require.

12. On the **Versions** FastTab, select the required version of the selected ER
    configuration.

13. Click **Import** to download the selected version from LCS to the current
    Finance and Operations instance.

Depending on the ER settings, configurations are validated after they are
imported. You might be notified about any inconsistency issues that are
discovered. You must resolve those issues before you can use the imported
configuration version.

ER Design domain specific data model
------------------------------------

Consider the following scenario:

As a user with either System Administrator or Electronic Reporting Developer
role assigned to, you need to create a configuration for Seahorse Retailers
(SRHQ). You can create configuration from any company since ER configurations
are shared across legal entities. To complete these steps, you must first have
created a configuration provider and mark it as active”

1.  Navigate to **Organization administration \> Workspaces \> Electronic
    reporting** and select the configuration provider for Seahorse Retailers
    (SRHQ).

2.  Click **Reporting configurations.**

3.  You will create a configuration that contains a data model for electronic
    payment documents. This data model will be used later as a data source when
    you create the format for the payment documents.

4.  In order to create a new data model configuration, click **Create
    configuration**

![Electronic reporting Create Configuration \> Root](media/f2c128e553ff30dad9ac4ab248f4f1ea.png)

1.  Select **Root**.

2.  In the **Name** field, type 'Payments (simplified model)'.

3.  In the **Description** field, type 'Payment model configuration'

4.  Select **Configuration provider**

5.  Click ‘**Create configuration’**

### Create a data model

1.  Click **Designer**

2.  Click **New**.

3.  In the **Name** field, type 'Party'.

4.  Click **Add**.

5.  Click **New**.

6.  In the **Name** field, type 'Name'.

7.  In the **Item type** field, select 'String'.

8.  Click **Add**.

9.  In the **Find** field, type 'Party'.

10. Click **Find previous**.

### Define the bank structure for this model

1.  Click **New**.

2.  In the **Name** field, type 'Agent'.

3.  In the **Item type** field, select 'Record'.

4.  Click **Add**.

5.  In the **Description** field, enter 'Financial institution (for instance, a
    bank) servicing an account for the party (debtor/creditor).'.

6.  Click **New**.

7.  In the **Name** field, type 'Name'.

8.  In the **Item type** field, select 'String'.

9.  Click **Add**.

10. Click **New**.

11. In the **Name** field, type 'SWIFT'.

12. Click **Add**.

13. In the **Description** field, enter 'Bank identification code'.

14. Click **New**

15. In the **Name** field, type 'RoutingNumber'.

16. Click **Add**.

17. In the **Description** field, enter 'Routing number'.

18. Click **Find previous**.

### Define the bank account structure for this model

1.  Click **New**.

2.  In the **Name** field, type 'Account'.

3.  In the **Item type** field, select 'Record'.

4.  Click **Add**.

5.  In the **Description** field, enter 'Identification of an account of a party
    in a financial institution (for instance, a bank).'.

6.  Click **New**.

7.  In the **Name** field, type 'Currency'.

8.  In the **Item type** field, select 'String'.

9.  Click **Add**.

10. In the **Description** field, enter 'Currency code'.

11. Click **New**.

12. In the **Name** field, type 'Number'.

13. Click **Add**.

14. Click **New**.

15. In the **Name** field, type 'IBAN'.

16. Click **Add**.

17. In the **Description** field, enter 'International bank account number'.

### Define the payment message structure for credit transfer payment type

1.  Click **New**.

2.  In the **New** node as a field, enter 'Model root'.

3.  In the **Name** field, type 'CustomerCreditTransferInitiation'.

4.  Click **Add**.

5.  In the **Find** field, type 'CustomerCreditTransferInitiation'.

6.  Click **Find previous**.

7.  Click **New**.

8.  In the Name field, type 'MessageIdentification'.

9.  Click **Add**.

10. In the **Description** field, enter 'The point-to-point reference assigned
    by the instructing party (and sent to the next party) to identify a
    message.'.

11. Click **New**.

12. In the **Name** field, type 'ProcessingDateTime'.

13. In the **Item type** field, select 'DateTime'.

14. Click **Add**.

15. In the **Description** field, enter 'Date and time at which the payment
    message was created.'.

16. Click **New**.

### Define the payment transaction structure for this model.

1.  In the **Name** field, type 'Payments'.

2.  In the Item type field, select 'Record list'.

3.  Click **Add**.

4.  In the **Description** field, enter 'Payment lines of the current message'.

5.  Click **New**.

6.  In the **Name** field, type 'Creditor'.

7.  In the **Item type** field, select 'Record'.

8.  Click **Add**.

9.  In the **Description** field, enter 'Party to which an amount of money is
    due.'.

10. Click **Switch item reference**.

11. In the **Find** field, type 'Party'.

12. Click **Find next**.

13. Click **OK**.

14. In the **Find** field, type 'Payments'.

15. Click **Find next**.

16. Click **New**.

17. In the **Name** field, type 'Debtor'.

18. Click **Add**.

19. In the **Description** field, enter 'Party that owes an amount of money to
    the (ultimate) creditor.'.

20. Click **Switch item reference**.

21. In the **Find** field, type 'Party'.

22. Click **Find next**.

23. Click **OK**.

24. Click **Find next**.

25. Click **New**.

26. In the Name field, type 'Description'.

27. In the Item type field, select 'String'.

28. Click **Add**.

29. Click **New**.

30. In the Name field, type 'Currency'.

31. Click **Add**.

32. In the **Description** field, enter 'Currency code'.

33. Click **New**.

34. In the **Name** field, type 'TransactionDate'.

35. In the **Item type** field, select 'Date'.

36. Click **Add**.

37. In the **Description** field, enter 'Transaction date'.

38. Click **New**.

39. In the **Name** field, type 'InstructedAmount'.

40. In the **Item type** field, select 'Real'.

41. Click **Add**.

42. In the **Description** field, enter 'The amount of money to be moved between
    the debtor and creditor, before deduction of charges. The amount should be
    expressed in the currency as ordered by the initiating party.'.

43. Click **New**.

44. In the **Name** field, type 'End2EndID'.

45. In the **Item type** field, select 'String'.

46. Click **Add**.

47. In the **Description** field, enter 'The unique identification assigned by
    the initiating party. This identification is passed on, unchanged,
    throughout the entire end-to-end chain.'.

48. In the **Name** field, type 'PaymentModel'. The PaymentModel name aligns
    with predefined interfaces of payment forms.

49. Click **Save**.

50. Close all forms.

Define ER model mappings and select data sources for them
---------------------------------------------------------

The data sources will be bound to individual components of the selected data
model at design time and populate business data to that data model at run-time.
In this example, you will select data sources for an existing data model that
has been created for Seahorse Retailers (SRHQ).

1.  Go to **Organization administration \> Workspaces \> Electronic reporting**.

2.  Click **Reporting configurations**.

### Insert a new model mapping

1.  In the tree, select 'Payments (simplified model)'.

2.  Click **Designer**.

3.  Click **Map model to datasource**.

4.  Click **New**.

This will create a new record that will map the data model to data sources. In
this example, you will map the data model to data sources for the desired
payment type: credit transfer. It is possible to design more than one mapping
for a particular data model.

For example, you could create a mapping for the different types of payments,
such as for direct debit or for credit transfers. In this example, you will
create a mapping for credit transfers.

1.  In the **Name** field, type 'CT mapping'.

2.  In the **Description** field, type 'Payment model mapping CT'.

3.  In the **Definition** field, type 'CustomerCreditTransferInitiation'.

4.  Click **Save**.

### Define required data sources for the current model mapping

1.  Click **Designer**.

2.  In the tree, select 'Dynamics 365 for Finance and Operations\\Table
    records'.

3.  Click **Add root**. Enter this data source to access payment transactions.

4.  In the **Name** field, type 'Transactions'.

5.  In the **Label** field, enter 'Transactions'.

6.  In the **Help** field, enter 'Ledger journal lines'.

7.  Select **Yes** in the Ask for query field.

8.  In the Table field, type 'LedgerJournalTrans'.

9.  Click OK.

10. Select the LedgerJournalTrans table as a data source for the current data
    model.

11. In the tree, select 'Functions\\Calculated field'.

12. Click **Add** to add a new calculated field.

13. In the **Name** field, type '\$EndToEndID'.

14. Click **Edit formula**.

15. In the tree, select 'String\\CONCATENATE'.

16. Click **Add** function.

17. In the tree, expand 'Transactions'.

18. In the tree, select 'Transactions\\Voucher'.

19. Click **Add data source**.

20. In the **Formula** field, enter 'CONCATENATE(Transactions.Voucher, "-", '.

21. In the tree, select 'String\\TEXT'.

22. Click **Add** function.

23. In the tree, select 'Transactions\\Record-ID(RecId)'.

24. Click **Add data source**.

25. In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-",
    TEXT(Transactions.RecId))'.

26. Click **Save**.

27. Close the page.

28. Click **OK**.

29. Click **Add**.

30. In the **Name** field, type '\$Amount'.

31. Click **Edit formula**.

32. In the tree, expand 'Transactions'.

33. In the tree, select 'Transactions\\Debit(AmountCurDebit)'.

34. Click **Add** data source.

35. In the **Formula** field, enter 'Transactions.AmountCurDebit - '.

36. In the tree, select 'Transactions\\Credit(AmountCurCredit)'.

37. Click **Add data source**.

38. Click **Save**.

39. Close the page.

40. Click **OK**.

41. In the tree, select 'Transactions\$Amount'.

42. In the tree, expand 'Transactions'.

43. In the tree, expand or collapse 'Transactions\$Amount'.

44. In the tree, expand or collapse 'Transactions'.

45. In the tree, select 'Dynamics 365 for Operations\\Table records'.

46. Click **Add root**.

47. In the **Name** field, type 'BankAccount'.

48. In the **Label** field, enter 'Bank Account'.

49. In the **Help** field, enter 'Bank Account'.

50. Select **Yes** in the Ask for query field.

51. In the **Table** field, type 'BankAccountTable'.

52. Click **OK**.

53. Click **Add root**.

54. In the **Name** field, type 'Company'.

55. In the **Label** field, type a value.

56. In the **Help** field, enter 'Company information'.

57. Select **Yes** in the Ask for query field.

58. In the **Table** field, type 'CompanyInfo'.

59. Click **OK**.

60. In the tree, select 'Functions\\Calculated field'.

61. Click **Add root**.

62. In the **Name** field, type 'ProcessingDateTime'.

63. In the **Label** field, enter 'Processing date & time'.

64. Click **Edit formula**.

65. In the tree, select 'Date/time\\SESSIONNOW'.

66. Click **Add** function.

67. Click **Save**.

68. Close the page.

69. Click **OK**. Add the ProcessingDateTime calculated field as a data source
    for the current data model.

70. Click **Save**.

71. Close all forms.

ER Map data model to selected data sources
------------------------------------------

Now you map a data model for Seahorse Retailers (SRHQ) to data sources.

1.  Go to **Organization administration \> Workspaces \> Electronic reporting**.

2.  Click **Configurations**.

### Select created model mapping

1.  In the tree, select 'Payments (simplified model)'.

2.  Click **Model designer**.

3.  Click **Map model to datasource**.

4.  Select the 'CT mapping' record.

### Bind created data sources to data model elements

1.  Click **Designer**.

2.  In the tree, select 'Processing date & time(ProcessingDateTime)'.

3.  In the tree, select 'Processing date(ProcessingDateTime)'.

4.  Click **Bind**.

5.  In the tree, select 'Payment message identification(MessageIdentification)'.

6.  In the tree, expand 'Transactions'.

7.  In the tree, select 'Transactions\\Journal batch number(JournalNum)'.

8.  Click **Bind**.

9.  In the tree, select 'Payments'.

10. In the tree, select 'Transactions'.

11. Click **Bind**.

12. In the tree, expand 'Payments= Transactions'.

13. In the tree, expand 'Payments= Transactions\\Creditor'.

14. In the tree, expand 'Payments= Transactions\\Creditor\\Account'.

15. In the tree, select 'Payments= Transactions\\Creditor\\Account\\Currency
    code(Currency)'.

16. In the tree, expand 'Transactions\\vendBankAccountInTransactionCompany()'.

17. In the tree, **select**
    'Transactions\\vendBankAccountInTransactionCompany()\\Currency(CurrencyCode)'.

18. Click **Bind**.

19. In the tree, select 'Payments= Transactions\\Creditor\\Account\\IBAN
    code(IBAN)'.

20. In the tree, select
    'Transactions\\vendBankAccountInTransactionCompany()\\IBAN(BankIBAN)'.

21. Click **Bind**.

22. In the tree, select 'Payments= Transactions\\Creditor\\Account\\Number'.

23. In the tree, select
    'Transactions\\vendBankAccountInTransactionCompany()\\Bank account
    number(AccountNum)'.

24. Click **Bind**.

25. In the tree, expand 'Payments= Transactions\\Creditor\\Agent'.

26. In the tree, select 'Payments= Transactions\\Creditor\\Agent\\Name'.

27. In the tree, select
    'Transactions\\vendBankAccountInTransactionCompany()\\Name'.

28. Click **Bind**.

29. In the tree, select 'Payments= Transactions\\Creditor\\Agent\\Routing
    number(RoutingNumber)'.

30. In the tree, select
    'Transactions\\vendBankAccountInTransactionCompany()\\Routing
    number(RegistrationNum)'.

31. Click **Bind**.

32. In the tree, select 'Payments= Transactions\\Creditor\\Agent\\SWIFT
    code(SWIFT)'.

33. In the tree, select
    'Transactions\\vendBankAccountInTransactionCompany()\\SWIFT code(SWIFTNo)'.

34. Click **Bind**.

35. In the tree, select 'Payments= Transactions\\Creditor\\Name'.

36. In the tree, expand 'Transactions\\findVendTable()'.

37. In the tree, select 'Transactions\\findVendTable()\\name()'.

38. Click **Bind**.

39. In the tree, select 'Payments= Transactions\\Currency code(Currency)'.

40. In the tree, expand 'Transactions\>Relations'.

41. In the tree, expand 'Transactions\>Relations\\Currency table(Currency)'.

42. In the tree, select 'Transactions\>Relations\\Currency
    table(Currency)\\Currency code(CurrencyCodeISO)'.

43. Click **Bind**.

44. In the tree, expand 'Payments= Transactions\\Debtor'.

45. In the tree, expand 'Payments= Transactions\\Debtor\\Account'.

46. In the tree, select 'Payments= Transactions\\Debtor\\Account\\Currency
    code(Currency)'.

47. In the tree, select 'Bank Account(BankAccount)'.

48. In the tree, expand 'Bank Account(BankAccount)'.

49. In the tree, select 'Bank Account(BankAccount)\\Currency(CurrencyCode)'.

50. Click **Bind**.

51. In the tree, select 'Bank Account(BankAccount)\\IBAN'.

52. In the tree, select 'Payments= Transactions\\Debtor\\Account\\IBAN
    code(IBAN)'.

53. Click **Bind**.

54. In the tree, select 'Payments= Transactions\\Debtor\\Account\\Number'.

55. In the tree, select 'Bank Account(BankAccount)\\Bank account
    number(AccountNum)'.

56. Click **Bind**.

57. In the tree, expand 'Payments= Transactions\\Debtor\\Agent'.

58. In the tree, select 'Payments= Transactions\\Debtor\\Agent\\Name'.

59. In the tree, select 'Bank Account(BankAccount)\\Name'.

60. Click **Bind**.

61. In the tree, select 'Payments= Transactions\\Debtor\\Agent\\Routing
    number(RoutingNumber)'.

62. In the tree, select 'Bank Account(BankAccount)\\Routing
    number(RegistrationNum)'.

63. Click **Bind**.

64. In the tree, select 'Payments= Transactions\\Debtor\\Agent\\SWIFT
    code(SWIFT)'.

65. In the tree, select 'Bank Account(BankAccount)\\SWIFT code(SWIFTNo)'.

66. Click **Bind**.

67. In the tree, select 'Payments= Transactions\\Debtor\\Name'.

68. In the tree, select 'Company information(Company)'.

69. In the tree, expand 'Company information(Company)'.

70. In the tree, select 'Company information(Company)\\Name'.

71. Click **Bind**.

72. In the tree, select 'Payments= Transactions\\Description'.

73. In the tree, select 'Transactions\\Description(Txt)'.

74. Click **Bind**.

75. In the tree, select 'Payments= Transactions\\End to end identification
    code(End2EndID)'.

76. In the tree, select 'Transactions\$EndToEndID'.

77. Click **Bind**.

78. In the tree, select 'Payments= Transactions\\Instructed
    amount(InstructedAmount)'.

79. In the tree, select 'Transactions\$Amount'.

80. Click **Bind**.

81. In the tree, select 'Payments= Transactions\\Transaction
    date(TransactionDate)'.

82. In the tree, select 'Transactions\\Date(TransDate)'.

83. Click **Bind**.

84. Click **Validate**.

85. Click the arrow to expand or collapse the Error List section.

86. Click **Save**.

87. Close all forms.

### Change the status of the current version of model configuration

1.  Click **Change status**.

2.  Click **Complete**.

3.  Select **Complete**.

4.  In the **Description** field, type 'version 1'.

5.  Click **OK**.

6.  Select the completed version of the current configuration. Note that the
    created configuration is saved as completed version 1.

ER Create a format configuration
--------------------------------

You will create a format configuration for Seahorse Retailers (SRHQ)

### Create a new format configuration

1.  Go to **Organization administration \> Workspaces \> Electronic reporting**.

2.  Click **Reporting configurations**.

3.  In the tree, select Payments (simplified model).

4.  Click **Create configuration** to open the drop dialog.

5.  If you don't see **Create configuration**, you must enable design mode on
    the Electronic reporting parameters page

6.  In the **New** field, enter Format based on data model PaymentModel.

7.  In the **Name** field, type BACS (UK fictitious).

8.  In the **Description** field, type BACS vendor payment format (UK
    fictitious).

9.  The active configuration provider is automatically entered here. This
    provider will be able to maintain this configuration. Other providers can
    use this configuration, but will not be able to maintain it. A particular
    format of electronic document can be defined. Leave this field blank if you
    want to select a format at run-time

10. In the **Data model definition** field, enter or select a value

11. Click **Create configuration**. A new configuration has been created. The
    draft version can be used to store the design format for managing electronic
    documents.

### Design the format of an electronic document

1.  Click **Designer**.

2.  Click **Add root** to open the drop dialog.

3.  In the tree, select Common\\File.

4.  In the **Name** field, type Xml.

5.  In the **Encoding** field, type UTF-8.

6.  Click **OK**.

7.  Click **Add**.

8.  In the tree, select XML\\Element.

9.  In the Name field, type Message.

10. Click **OK**.

11. In the tree, select Xml\\Message.

12. Click **Add Element**.

13. In the **Name** field, type ProcessingDate.

14. Click **OK**.

15. Click **Add Element**.

16. In the **Name** field, type MessageId.

17. Click **OK**.

18. Click **Add Element**.

19. In the **Name** field, type Payments.

20. Click **OK**.

21. In the tree, select Xml\\Message\\Payments.

22. Click **Add Element**.

23. In the **Name** field, type Item.

24. Click **OK**.

25. In the tree, select Xml\\Message\\Payments\\Item.

26. Click **Add**.

27. In the tree, select XML\\Attribute.

28. In the Name field, type Id.

29. Click **OK**.

30. Click **Add**.

31. In the tree, select XML\\Element.

32. In the **Name** field, type Vendor.

33. Click **OK**.

34. In the tree, select Xml\\Message\\Payments\\Item\\Vendor.

35. Click **Add** Element.

36. In the **Name** field, type Name.

37. Click **OK**.

38. Click **Add** Element.

39. In the **Name** field, type Bank.

40. Click **OK**.

41. In the tree, select Xml\\Message\\Payments\\Item\\Vendor\\Bank.

42. Click **Add** Element.

43. In the Name field, type RoutingNumber.

44. Click **OK**.

45. Click **Add Element**.

46. In the **Name** field, type AccountNumber.

47. Click **OK**.

48. In the tree, select Xml\\Message\\Payments\\Item\\Vendor.

49. Click **Copy**.

50. In the tree, select Xml\\Message\\Payments\\Item.

51. Click **Paste**.

52. In the **Name** field, type Payer.

53. In the tree, select Xml\\Message\\Payments\\Item.

54. Click **Add Element**.

55. In the **Name** field, type Currency.

56. Click **OK**.

57. Click Add Element.

58. In the Name field, type Description.

59. Click OK.

60. Click Add Element.

61. In the Name field, type TransDate.

62. Click OK.

63. Click Add Element.

64. In the Name field, type Amount.

65. Click OK.

### Prepare format components for mapping to data model elements

1.  In the tree, select **Xml\\Message\\ProcessingDate**.

2.  Click **Add**.

3.  In the tree, select **Text\\DateTime**.

4.  In the **Format** field, type **yyyy-MM-dd**.

5.  Click **OK**.

6.  In the tree, select **Xml\\Message\\Payments\\Item\\TransDate**.

7.  Click **Add DateTime**.

8.  In the **Format** field, type **yyyy-MM-dd**.

9.  In the **DateTime** type field, select **Date**.

10. Click **OK**.

11. In the tree, select **Xml\\Message\\MessageId**.

12. Click **Add**.

13. In the tree, select **Text\\String**.

14. Click **OK**.

15. In the tree, select **Xml\\Message\\Payments\\Item\\Vendor\\Name**.

16. Click **Add String**.

17. Click **OK**.

18. In the tree, select
    **Xml\\Message\\Payments\\Item\\Vendor\\Bank\\RoutingNumber**.

19. Click **Add String**.

20. Click **OK**.

21. In the tree, select
    **Xml\\Message\\Payments\\Item\\Vendor\\Bank\\AccountNumber**.

22. Click **Add String**.

23. Click **OK**.

24. In the tree, select **Xml\\Message\\Payments\\Item\\Payer\\Name**.

25. Click **Add String**.

26. Click **OK**.

27. In the tree, select
    **Xml\\Message\\Payments\\Item\\Payer\\Bank\\RoutingNumber**.

28. Click **Add String**.

29. Click **OK**.

30. In the tree, select
    **Xml\\Message\\Payments\\Item\\Payer\\Bank\\AccountNumber**.

31. Click **Add String**.

32. Click **OK**.

33. In the tree, select **Xml\\Message\\Payments\\Item\\Currency**.

34. Click **Add String**.

35. Click **OK**.

36. In the tree, select **Xml\\Message\\Payments\\Item\\Description**.

37. Click **Add String**.

38. Click **OK**.

39. In the tree, select **Xml\\Message\\Payments\\Item\\Amount**.

40. Click **Add String**.

41. Click **OK**.

42. Click **Save**.

43. Close the page.

ER Map components of the created format to data model elements
--------------------------------------------------------------

### Select a format configuration

1.  Go to **Organization administration \> Workspaces \> Electronic reporting**.

2.  Click **Reporting configurations**.

3.  In the tree, expand 'Payments (simplified model)'.

4.  In the tree, select 'Payments (simplified model)\\BACS (UK fictitious)'.

5.  Click **Designer**.

### Map format components to data model elements

1.  Click the **Mapping** tab.

2.  In the tree, expand 'model'.

3.  In the tree, select 'Xml\\Message\\ProcessingDate\\DateTime'.

4.  In the tree, select 'model\\ProcessingDateTime'.

5.  Click **Bind**.

6.  In the tree, select 'Xml\\Message\\MessageId\\String'.

7.  In the tree, select 'model\\MessageIdentification'.

8.  Click **Bind**.

9.  In the tree, expand 'model\\Payments'.

10. In the tree, select 'Xml\\Message\\Payments\\Item\\Amount\\String'.

11. In the tree, select 'model\\Payments\\InstructedAmount'.

12. Click **Bind**.

13. In the tree, select 'Xml\\Message\\Payments\\Item\\TransDate\\DateTime'.

14. In the tree, select 'model\\Payments\\TransactionDate'.

15. Click **Bind**.

16. In the tree, select 'Xml\\Message\\Payments\\Item\\Description\\String'.

17. In the tree, select 'model\\Payments\\Description'.

18. Click **Bind**.

19. In the tree, select 'Xml\\Message\\Payments\\Item\\Currency\\String'.

20. In the tree, select 'model\\Payments\\Currency'.

21. Click **Bind**.

22. In the tree, select 'Xml\\Message\\Payments\\Item\\Id'.

23. In the tree, select 'model\\Payments\\End2EndID'.

24. Click **Bind**.

25. In the tree, expand 'model\\Payments\\Creditor'.

26. In the tree, expand 'model\\Payments\\Creditor\\Account'.

27. In the tree, expand 'model\\Payments\\Creditor\\Agent'.

28. In the tree, select 'Xml\\Message\\Payments\\Item\\Vendor\\Name\\String'.

29. In the tree, select 'model\\Payments\\Creditor\\Name'.

30. Click **Bind**.

31. In the tree, select
    'Xml\\Message\\Payments\\Item\\Vendor\\Bank\\RoutingNumber\\String'.

32. In the tree, select 'model\\Payments\\Creditor\\Agent\\RoutingNumber'.

33. Click **Bind**.

34. In the tree, select
    'Xml\\Message\\Payments\\Item\\Vendor\\Bank\\AccountNumber\\String'.

35. In the tree, select 'model\\Payments\\Creditor\\Account\\Number'.

36. Click **Bind**.

37. In the tree, select 'Xml\\Message\\Payments\\Item\\Payer\\Name\\String'.

38. In the tree, expand 'model\\Payments\\Debtor'.

39. In the tree, expand 'model\\Payments\\Debtor\\Account'.

40. In the tree, expand 'model\\Payments\\Debtor\\Agent'.

41. In the tree, select 'model\\Payments\\Debtor\\Name'.

42. Click **Bind**.

43. In the tree, select
    'Xml\\Message\\Payments\\Item\\Payer\\Bank\\RoutingNumber\\String'.

44. In the tree, select 'model\\Payments\\Debtor\\Agent\\RoutingNumber'.

45. Click **Bind**.

46. In the tree, select
    'Xml\\Message\\Payments\\Item\\Payer\\Bank\\AccountNumber\\String'.

47. In the tree, select 'model\\Payments\\Debtor\\Account\\Number'.

48. Click **Bind**.

49. In the tree, select 'Xml\\Message\\Payments\\Item'.

50. In the tree, select 'model\\Payments'.

51. Click **Bind**.

52. Click **Save**.

53. Click **Validate**.

54. Validate the new mapping to ensure that all bindings are okay.

55. Close the page.

### Change status of the current version of format configuration

1.  Click **Change status**.

2.  Click **Complete**.

3.  In the **Description** field, type 'version 1'.

4.  Click **OK**.

5.  Select completed version of the current configuration. Note that the
    configuration is saved as completed version 1.1: version 1 of the format
    based on the version 1 of the data model.

ER Generate electronic documents for payments using a format configuration
--------------------------------------------------------------------------

### Change the configuration of the electronic payment method

1.  Go to **Accounts payable \> Payment setup \> Methods of payment**.

2.  Toggle the **File format** section to expand it, if needed.

3.  Use the Quick Filter to find records. For example, filter on the Method of
    payment field with a value of **'Electronic'**.

4.  Click **Edit**.

5.  Set the **General electronic reporting** field to **Yes** to use the General
    electronic reporting pattern for payment files generation.

6.  In the **Name** field, click the drop-down button to open the lookup.

7.  Select BACS (UK fictitious) format configuration.

8.  Click **Save**.

9.  Close the page.

### Test the format of generated payment files

1.  Go to **Accounts payable \> Payments \> Payment journal**.

2.  Click **New**.

3.  In the **Name** field, select VendPay.

4.  Click **Save**.

5.  Click **Lines**.

6.  In the **Company** field, type 'DEMF'.

7.  In the **Account** field, specify the values 'DE-01001'.

8.  In the **Description** field, type 'Payment'.

9.  In the **Debit** field, enter a number.

10. Click the **Payment** tab.

11. In the **Method of payment** field, select the **Electronic**.

12. Click **Save**.

13. Click **Generate payments**.

14. In the **Method of payment** field, select the **Electronic**.

15. In the **File name** field, type 'payments'.

16. In the **Bank account** field, select the **OPER**..

17. Click **OK**.

18. Click **OK**.

19. Analyze the created payment file in XML format. Compare it with the designed
    document layout and defined payment transaction attributes.

ER Upgrade your format by adopting a new, base version of that format
---------------------------------------------------------------------

You need to create a custom version based on the format received from a
configuration provider (CP) and adopt a new, base version of that format.

### Select format configuration for customization

1.  Go to **Organization administration \> Workspaces \> Electronic reporting**.

In this example, Seahorse Retailers (SRHQ).
([http://www.SeahorseRetailersInternational.com](http://www.SeahorseRetailersInternational.com/)
) will act as a configuration provider that supports format configurations for
electronic payments for a particular area. Sample company Proseware, Inc.
([http://www.proseware.com](http://www.proseware.com/) ) will act as a consumer
of the format configuration that SRHQ provided. Proseware, Inc. uses formats in
certain regions.

1.  Click **Reporting configurations**.

2.  Click **Show filters**.

3.  Apply the following filters:

    1.  Enter a filter value of "BACS (UK fictitious)" on the "Name" field using
        the "begins with" filter operator BACS (UK fictitious) The selected
        format configuration BACS (UK fictitious) is owned by provider Litware,
        Inc.

4.  Click **Show filters**.

5.  In the list, find and select the desired record. The version of the format
    with the status of Completed will be used by Proseware, Inc. for
    customization.

6.  Close the page.

### Create a new configuration for your custom format of electronic document

1.  Select Proseware, Inc. to make it an active provider.

2.  Click **Set active**.

3.  Click **Reporting configurations**.

4.  In the tree, expand 'Payments (simplified model)'.

5.  In the tree, select 'Payments (simplified model)\\BACS (UK fictitious)'.

6.  Select the BACS (UK fictitious) configuration from Litware, Inc. Proseware,
    Inc. will use version 1.1 as a base for the custom version.

7.  Click **Create configuration**. This lets you create a new configuration for
    a custom payment format.

8.  In the **New** field, enter 'Derive from Name: BACS (UK fictitious),
    Litware, Inc.'.

9.  Select the **Derive** option to confirm the usage of BACS (UK fictitious) as
    the base for creating the custom version.

10. In the **Name** field, type 'BACS (UK fictitious custom)'.

11. In the **Description** field, type 'BACS vendor payment (UK fictitious
    custom)'.

12. The active configuration provider (Proseware, Inc.) is automatically entered
    here. This provider will be able to maintain this configuration. Other
    providers can use this configuration, but will not be able to maintain it.

13. Click **Create configuration**.

### Customize your format for the electronic document

1.  Click **Designer**.

2.  In the tree, select 'Xml\\Message\\Payments\\Item\\Vendor\\Bank'.

3.  Click **Add**.

4.  In the tree, select 'XML\\Element'.

5.  In the **Name** field, type 'IBAN'.

6.  Click **OK**.

7.  In the tree, select 'Xml\\Message\\Payments\\Item\\Vendor\\Bank\\IBAN'.

8.  Click **Add**.

9.  In the tree, select 'Text\\String'.

10. Click **OK**.

11. In the tree, select 'Xml\\Message\\Payments\\Item\\Vendor\\Name\\String'.

12. In the Maximum length field, enter '60'.

13. Click the **Mapping** tab.

14. In the tree, expand 'model'.

15. In the tree, expand 'model\\Payments'.

16. In the tree, expand 'model\\Payments\\Creditor'.

17. In the tree, expand 'model\\Payments\\Creditor\\Account'.

18. In the tree, select 'model\\Payments\\Creditor\\Account\\IBAN'.

19. In the tree, select 'Xml\\Message\\Payments\\Item =
    model.Payments\\Vendor\\Bank\\IBAN\\String'.

20. Click **Bind**.

21. Click **Save**.

22. Click **Validate**. Validate the customized format layout and data mapping
    changes to make sure that all bindings are okay.

23. Close the page.

### Change the status of the current version of the custom format configuration

1.  Click **Change status**. Note that the current version of the selected
    configuration is in **Draft** status.

2.  Click **Complete**.

3.  In the **Description** field, type a value.

4.  Click **OK**.

5.  In the list, find and select the desired record. Note that the created
    configuration is saved as completed version 1.1.1. This means it is version
    1 of the custom BACS (UK fictitious custom) format, which is based on
    version 1 of the BACS (UK fictitious) format, which is based on version 1 of
    the Payments (simplified model) data model.

6.  Close the page.

### Update the existing locally specific configuration

1.  Select Litware, inc. provider.

2.  Click Set active.

3.  Click Reporting configurations.

4.  In the tree, expand 'Payments (simplified model)'.

5.  In the tree, select 'Payments (simplified model)\\BACS (UK fictitious)'.

    1.  The draft version owned by Litware, Inc. provider BACS (UK fictitious)
        is selected to bring in changes to support new locally specific
        requirements.

### Localize the base format of the electronic document

1.  Click **Designer**.

2.  In the tree, select 'Xml\\Message\\Payments\\Item\\Vendor\\Bank'.

3.  Click **Add**.

4.  In the tree, select 'XML\\Element'.

5.  In the **Name** field, type 'SWIFT'.

6.  Click **OK**.

7.  In the tree, select 'Xml\\Message\\Payments\\Item\\Vendor\\Bank\\SWIFT'.

8.  Click **Add**.

9.  In the tree, select 'Text\\String'.

10. Click **OK**.

11. In the tree, select 'Xml\\Message\\Payments\\Item\\Vendor\\Name\\String'.

12. In the **Maximum length** field, enter '100'.

13. Click the **Mapping** tab.

14. In the tree, expand 'model'.

15. In the tree, expand 'model\\Payments'.

16. In the tree, expand 'model\\Payments\\Creditor'.

17. In the tree, expand 'model\\Payments\\Creditor\\Agent'.

18. In the tree, select 'model\\Payments\\Creditor\\Agent\\SWIFT'.

19. In the tree, select 'Xml\\Message\\Payments\\Item
    =model.Payments\\Vendor\\Bank\\SWIFT\\String'.

20. Click **Bind**.

21. Click **Save**.

22. Click **Validate**.

23. Close the page.

### Change the status of the current version of the base format configuration

1.  Click **Change status**. Note that the current version of the selected
    configuration is in **Draft** status.

2.  Click **Complete**.

3.  In the **Description** field, type a value.

4.  Click **OK**.

### Change the base version for the custom format configuration

1.  Go to **Organization administration \> Workspaces \> Electronic reporting**.

2.  Select the Proseware, Inc. provider to mark it as active.

3.  Click **Set active**.

4.  Click **Reporting configurations**.

5.  In the tree, expand 'Payments (simplified model)'.

6.  In the tree, expand 'Payments (simplified model)\\BACS (UK fictitious)'.

7.  In the tree, select 'Payments (simplified model)\\BACS (UK fictitious)\\BACS
    (UK fictitious custom)'.

8.  Select the BACS (UK fictitious custom) configuration, which is owned by
    Proseware, Inc.

9.  Use the draft version of the selected configuration to introduce required
    changes.

10. Click **Rebase**.

11. Select the new version 1.2 of the base configuration to be applied as a new
    base for updating the configuration.

12. Click **OK**. Note that some conflicts have been discovered between merging
    the custom version and a new base version representing some format changes
    that can’t be merged automatically.

### Resolve rebase conflicts

1.  Click Designer. Note that changes to the vendor’s name text length limit
    couldn’t be resolved automatically. Therefore, this is presented in a
    conflicts list.

2.  For each conflict of type Update, the following options are available:

3.  Apply a prior base value (button on top of the grid) to bring in the
    previous base version value (0 in our case).

4.  Apply a base value (button on top of the grid) to bring in the new base
    version value (100 in our case).

5.  Keep your own (custom) value (60 in our case).

6.  Click Apply base value to apply a locally specific limit of 100 characters
    for vendor’s name text length.

7.  Note that Proseware, Inc. and Litware, Inc. have custom and local versions
    of this format using IBAN and SWIFT codes with related components that are
    automatically merged in the managing format.

8.  Click Apply base value. This applies the locally specific limit of 100
    characters for vendor names.

9.  Click Save. Saving the format will remove resolved conflicts from the
    conflicts list.

10. Close the page.

### Change the status of the new version of the custom format configuration

1.  Click **Change status**.

2.  Change the status of the updated, custom format configuration from **Draft**
    to **Completed**. This will make the format configuration available for
    generating payment documents. Note that the current version of the selected
    configuration is in **Draft** status.

3.  Click **Complete**.

4.  In the **Description** field, type a value.

5.  Click **OK**.

Note that the created configuration is saved as completed version 1.2.2: version
2 of base BACS (UK fictitious custom) format, which is based on version 2 of
base BACS (UK fictitious) format, which is based on version 1 of Payments
(simplified model) data model.

ER Configure destinations
-------------------------

The format used in this example is ISO20022 Credit transfer, but you can use any
format that you have already imported. Note, this procedure is an example of a
single file and a single destination setup.

1.  In **DEMF**, Go to **Organization administration \> Electronic reporting \>
    Electronic reporting destination**.

2.  Click **New** to create a new set of destinations for a format.

3.  In the **Reference** field, select a format for which you want to configure
    destinations. If you don't have a value to select, it means that you have
    not imported any Electronic reporting format configurations. You must import
    a format configuration before setting up destinations.

4.  Click **New** to create a new file destination. You can create one file
    destination for each output component of the same format, such as a folder
    or a file. You will be able to enable and disable destinations separately in
    the settings.

5.  In the **Name** field, enter the user-friendly name of output component. We
    recommend that you use meaningful names, such as "Payment file" or "Control
    report". These names will be presented to users at configuration runtime
    along with the destination settings.

6.  In the **File name**, select a file or folder that is specific to the
    format.

7.  Click **Settings**.

8.  Select **Yes** in the **Enabled** field. The Enabled option on each tab
    enables and disables each destination separately. In this example, you'll
    enable sending an output file to a mail recipient when the file is
    generated.

9.  Click **Edit**, to set up email recipients.

10. Click **Add**.

11. Click **Print Management email**.

12. In the **Email source** field, select an option. You can select different
    email source types, such as a customer or a vendor type. This defines the
    type of argument that will be returned by the Email source account formula.
    The Email source account formula, described in a following step, is the
    place where you bind an email source. Select Vendor if your formula will
    return a vendor account. Use Vendor if you are using the ISO 20022 Credit
    Transfer configuration example.

13. Click **Email source bind** button.

14. In the **Formula**, enter a document-specific reference to a party type that
    you selected earlier. Instead of typing, you can find a data source node
    that represents the party account, and click the **Add data source** button
    to update the formula. For example, if you use the ISO 20022 Credit Transfer
    configuration, the node representing a vendor account is
    '\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID. Otherwise,
    enter any string value, such as "DE-001", to save a formula.

15. Click **Save**.

16. Close the page.

17. Click **Edit** to configure contact details for the party.

18. Select **Yes** in the **Primary contact** field. You may use different
    options to indicate what contact type of the party should be used as an
    email address for this destination. We use primary contact in this example.

19. Click **OK**.

20. Click **OK**.

21. In the **Subject** field, type a value.

22. Click **OK**.
