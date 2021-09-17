---
lab:
    title: 'Exercise 1: Configure fixed assets components'
    module: 'Module 8: Configure and manage fixed assets'
---

## Exercise 1: Configure fixed assets components

The goal of the lab exercise is to apply the knowledge we’ve learned regarding the configure and test Fixed assets components.

### Instructions

#### Set up fixed asset posting profiles

This task guide will set up Fixed asset posting profiles. It uses the Accountant role and demo data for the USMF legal entity. Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.

1. Navigate to **Fixed assets &gt; Setup &gt; Fixed asset posting profiles**.

2. Select **New**.

3. In the **Posting profile** field, enter a value.

4. In the **Description** field, enter a value. You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets. Let’s start with the **Acquisition** transaction type.

5. Select **Add**.

6. In the **Book** field, select a value.

7. The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group). For this task guide, we will leave the value set to “All” to apply to all fixed assets with the specified Book.

8. In the **Main account** field, specify the desired value.

9. For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.

10. In the **Transaction type** dropdown where it says **Acquisition**, select **'Acquisition adjustment'**.

11. For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.

12. Select **Add**.

13. In the **Book** field, select a value.

14. In the **Main account** field, specify the desired value.

15. For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.

16. In the **Transaction type** dropdown which says **Acquisition adjustment**, select 'Depreciation'.

17. Select **Add**.

18. In the **Book** field, select a value.

19. In the **Main account** field, specify the desired value.

20. In the **Offset account** field, specify the desired value.

21. In the **Transaction type** dropdown, select 'Depreciation adjustment'.

22. For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.

23. Select **Add**.

24. In the **Book** field, enter or select a value.

25. In the **Main account** field, specify the desired values.

26. In the **Offset account** field, specify the desired values.

27. In the **Transaction type** field, select 'Disposal - sale'.

28. Select **Add**.

29. In the **Book** field, enter or select a value.

30. In the **Main account** field, specify the desired values.

31. For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.

32. In the **Transaction type** field, select 'Disposal - scrap'; you will use the same accounts as for Disposal sale.

33. Select **Add**.

34. In the **Book** field, select a value.

35. In the **Main account** field, specify the desired value.

36. For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.

37. Expand the **Disposal** section. You must set up disposal posting profiles for both sale and scrap. 

38. We will start with disposal sale transactions. Select **Add**.

39. In the **Book** field, enter or select a value.

40. In the **Post value** field, select 'Acquisition value'.

41. Acquisition value will address Acquisition and Acquisition adjustment values for all years. You can also define accounts for these transaction types separately.

42. You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss. We will set the Sales value type to “All” to use the same accounts for all types of disposals.

43. In the **Main account** field, specify the desired value.

44. In the **Offset account** field, specify the desired value.

45. Select **Add**.

46. In the **Book** field, enter or select a value.

47. In the **Post value** field, select 'Depreciation (prior years)'.

48. In the **Main account** field, specify the desired value.

49. In the **Offset account** field, specify the desired value.

50. Select **Add**.

51. In the **Book** field, enter or select a value.

52. In the **Post value** field, select 'Depreciation (this year)'.

53. In the **Main account** field, specify the desired value.

54. In the **Offset account** field, specify the desired value.

55. Select **Add**.

56. In the **Book field**, enter or select a value.

57. In the **Post value** field, select 'Depreciation adjustments (prior years)'.

58. In the **Main account** field, specify the desired value.

59. In the **Offset account** field, specify the desired value.

60. Select **Add**.

61. In the **Book** field, enter or select a value.

62. In the **Post value** field, select 'Depreciation adjustments (this year)'.

63. In the **Main account** field, specify the desired values.

64. In the **Offset account** field, specify the desired values.

65. Select **Add**.

66. In the **Book** field, enter or select a value.

67. In the **Post value** field, select 'Net book value'.

68. In the **Main account** field, specify the desired values.

69. In the **Offset account** field, specify the desired values.

70. In the **Sale** or **scrap** field, select 'Scrap'.

71. Select **Add**.

72. In the **Book** field, enter or select a value.

73. In the **Post** value field, select 'Acquisition value'.

74. In the **Main account** field, specify the desired values.

75. In the **Offset account** field, specify the desired values.

76. Select **Add**.

77. In the **Book** field, enter or select a value. In Post value field, select 'Depreciation (prior years)'.

78. In the **Main account** field, specify the desired values.

79. In the **Offset account** field, specify the desired values.

80. Select **Add**.

81. In the **Book** field, enter or select a value.

82. In the **Post** value field, select 'Depreciation (this year)'.

83. In the **Main account** field, specify the desired values.

84. In the **Offset account** field, specify the desired values.

85. Select **Add**.

86. In the **Book** field, enter or select a value.

87. In the **Post** value field, select 'Depreciation adjustments (prior years)'.

88. In the **Main account** field, specify the desired values.

89. In the **Offset account** field, specify the desired values.

90. Select **Add**.

91. In the **Book** field, enter or select a value.

92. In the **Post** value field, select 'Depreciation adjustments (this year)'.

93. In the **Main account** field, specify the desired values.

94. In the **Offset account** field, specify the desired values.

95. Select **Add**.

96. In the **Book** field, enter or select a value.

97. In the **Post** value field, select 'Net book value'.

98. In the **Main account** field, specify the desired values.

99. In the **Offset account** field, specify the desired values.

#### Create and acquire assets from Accounts payable

##### Set Fixed assets parameters

1. Navigate to **Fixed assets &gt; Setup &gt; Fixed assets parameters**.

2. Expand the **Purchase orders** section in the **Fixed assets** tab.

3. Enable the **Allow asset acquisition from Purchasing** option.

4. Enable the **Create asset during product receipt or invoice posting** option.

##### Create a new vendor invoice

1. Navigate to **Accounts payable &gt; Workspaces &gt; Vendor invoice entry**.

2. Select **New vendor invoice**.

3. In the **Invoice account** field, select the drop-down to open the lookup.

4. In the list, select the selected row.

5. In the **Number** field, enter a value.

6. In the **Posting date** field, enter a date.

7. Select **Add line**.

8. In the **Item number** field, select the drop-down button to open the lookup. Either non-stocked items or procurement categories can be used for fixed asset acquisition.

9. In the list, select the selected row.

10. In the **Quantity** field, enter a number.

11. One invoice line will only create one fixed asset, regardless of quantity. The invoice quantity field value will be transferred to the fixed asset quantity.

12. In the **Unit price** field, enter a number.

13. Expand the **Line details** section.

14. Select the **Fixed assets** tab.

15. Enable the **Create a new fixed asset** option.

16. In the **Fixed asset group** field, select the drop-down button to open the lookup.

17. In the list, select the fixed asset group to be used when creating the new fixed asset.

18. Select **Post**. The fixed asset will be created and acquired when the invoice is posted.

 
