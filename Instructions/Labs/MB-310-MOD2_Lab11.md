---
lab:
    title: 'Exercise 11: Create a bank group and bank account'
    module: 'Module 2: Set up and configure financial management'
---


## Exercise 11: Create a bank group and bank account

**USMF** has opened a new bank account. The bank account will operate primarily in British pound (GBP) but may operate in other currencies. Annie, the bookkeeper, must create a new bank group and new bank account in Dynamics 365 Finance for this bank. Annie does not have address information for the bank account, but she does have the following specifications:



For the bank group:

- The bank group name is RBUK for Royal Bank of UK.

- The bank group routing number is 8117.

 

For the bank account:

- The bank account name is Bank Account - GBP.

- The bank account is part of the Royal Bank of UK group.

- The bank account number is 57252193.

- Postings should use a new main account 110150 called Bank account - GBP

As a finance consultant follow the instructions below to help Annie.

### Create a new account for Cash in bank - GBP to the Chart of accounts.

1. Navigate to **General ledger &gt; Chart of accounts &gt; Accounts &gt; Main accounts**.

2. Verify to see if you have the account **110150** **– Bank Account GBP**. If it exists skip to step 9.

3. Select the **New** button to create a new record.

4. In the **Main account** field, enter **110150**.

5. In the **Name** field, enter **Bank Account – GBP**.

6. In the **Main account type** field, select **Asset**.

7. In the **Default Currency** field, and then select **GBP**.

8. Close the form

### Create the new bank group and assign the British pound (GBP) to it.

9. Navigate to **Cash and bank management &gt; Setup &gt; Bank groups**.

10. Select the **New** button to create a new record.

11. In the **Bank groups** field, enter **RBUK**.

12. In the **Routing number** field, type **200395**.

13. In the **Description** field, enter **Royal Bank of UK**.

14. Select the **General** FastTab.

15. From the **Currency** list select **GBP**.

16. Close the **Bank groups** form.

### Create the new bank account that is part of the RBUK bank group.

17. Navigate to **Cash and bank management &gt; Bank accounts &gt; Bank accounts**.

18. Select the **New** button to create a new record.

19. In the **Bank account** field, enter **GBPBANK**.

20. In the **Name** field, enter **Bank Account -** **GBP**.

21. In the **Bank groups** dropdown, select **RBUK**.

22. The **Routing number** field automatically will display **200395**.

23. The **Currency** field automatically displays **GBP**, which defaults from the bank group.

24. In the **Bank account number** field, enter **57252193**.

25. In the **Main account** field, select **110150**.

26. In the **Allow transactions in additional currencies** field, select the **Yes** to enable posting in more than one currency for this bank account.

27. Close the form

 

### Create a direct debit mandate for a customer

28. Navigate to **Accounts receivable &gt; Customers &gt; All customers**.

29. Select a customer, for example, select **US-001.**

30. On the Action Pane, select **Customer**.

31. Select **Bank accounts** in the Setup group.

32. Select **New**

33. In the **Bank account** field, type a value such as **CustBank1**.

34. In the **Name** field, type a value such as **Customer Bank 1**.

35. In the **Bank account number** field, enter **55555555.**

36. In the **Routing number** field, enter **202015.**

37. I the **IBAN** field, type **GB33BUKB20201555555555**.

38. In the **Currency** field, type **GBP**.

39. Select **Save**

40. Close all pages

41. Navigate to **Cash and bank management &gt; Bank accounts &gt; Bank accounts**.

42. In the list, find and select **GBPBANK**.

43. Select **Edit**

44. Expand the **Additional identification** section.

45. In the **Direct debit ID** field, type a value of **US001**.

46. In the **IBAN** field, type **GB33BARC20039557252193**.

47. Close all pages

### Define the electronic payment method

48. Navigate to **Accounts receivable &gt; Payments setup &gt; Methods of payment**.

49. Select **New**

50. In the **Method of payment** field, type a value such as **AREL**.

51. In the **Description** field, type a value such as **AR Electronic payment**.

52. In the **Payment type** field, select **Electronic payment.** Note that payment type for a direct debit mandate method of payment must be **Electronic** **payment**.

53. In the **Require mandate** field, select **Yes**.

54. Close the page

### Add a direct debit mandate to a customer

55. Navigate to **Accounts receivable &gt; Customers &gt; All customers**.

56. Select customer **US-001**

57. Select **Edit**

58. Expand the **Payment defaults** section.

59. In the **Method of payment** field, enter or select **AREL**.

60. Expand the **Direct debit mandates** section.

61. Select **Add**

62. In the **Bank account** field, note that **CustBank1** is automatically selected.

63. In the **Creditor bank account** field, select **GBPBANK**.

64. Enter the number of payments that you expect to process for this mandate, such as 10, in **Expected number of payments**.

65. Select **OK**

66. Note that the value of **Mandate status** column is set to incomplete.

67. Select **Print** in the Direct debit mandates section and select **Mandate report**.

68. Review the **SEPA Direct Debit Mandate** report.

69. Close the page

70. Select **Edit**

71. In the **Signature date** field, enter a date in future.

72. Select **Yes**

73. Enter the location where the mandate was signed. Select **London.**

74. Select **OK**

75. Note the value of Mandate status column is set to **New**.

76. Close the page
