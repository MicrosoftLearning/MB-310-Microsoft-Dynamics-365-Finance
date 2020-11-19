---
lab:
    title: 'Exercise 4: Create a payment calendar'
    module: 'Module 3: Implement and manage shared configuration for AP and AR'
---


## Exercise 4: Create a payment calendar

### Set up a payment calendar

1. Select Accounts payable > Payment **setup** > Payment calendar or select Accounts receivable > Payments setup> Payment calendar.

2. Select New.

3. In the Payment calendar field, enter the name of the payment calendar.

4. To create a calendar for a specific country or region, select the Location calendar slider bar. Then, select the country or region in the Country/region field.

5. In the Standard business week field group, select the business days in a standard work week.

6. In the Filter to calendar year field, enter the fiscal year to create the payment calendar for.

7. To specify exception dates for the calendar year, select Add. In the Date field, select the date.

8. In the Type field, specify whether the exception date is a business day or a holiday

### Configure payment calendar rules

1. Select Accounts payable > Payment **setup** > Payment calendar configuration or select Accounts receivable > Payments setup > Payment calendar configuration. 

2. Select New.

3. In the Rule name field that is displayed, enter an identifier for the rule.

4. In the Rule type field, select one of the following types:

	- Specific – Create a payment calendar rule for a specific combination of the method of payment and terms of payment. When you select this type of rule, the Method of payment and Terms of payment fields are displayed. You can use all combinations or a specific combination of the method of payment and terms of payment for the rule.

	- Customer/vendor location – Create a payment calendar rule for a specific country or region. When you select this type of rule, the Customer - location or Vendor location field group is displayed. Location information will be retrieved from the documents in the order in which you arrange the documents in the list that is displayed. You can select Move up and Move down to arrange the documents.

	- Company location – Create a payment calendar rule for the primary address that is specified for the legal entity.

5. Select Create rule.

6. In the Define rules area, select Active to use the rule for the selected payment calendars. The rule becomes active when you close the form.

7. Select a **Payment calendar**.

8. In the Prioritize rules tab, select the rule and then select Move up or Move down to move the rule up or down in the list.

9. If you are setting up a payment calendar rule for a country or region, in the Select calendars area, select the check box for each calendar that you want the rule to apply to.