# Addition

Addition of two positive numbers Given The calculator is turned on

When I type in "positive number"
And I press "plus"
And I type in "positive number"
And I press "equals"

Then I see the "added number" as the result

Scenario: Addition of two negative numbers
  
  Given The calculator is turned on
  When I type in "positive number"
  And I press "plus"
  And I type in "positive number"
  And I press "equals"
  Then I see the "added number" as the result

Scenario: Addition of fractions 

  Given The calculator is turned on able to enter fraction
  When I type in "positive fraction number"
  And I press "plus"
  And I type in "positive fraction number"
  And I press "equals"
  Then I see the "added number" as the result

Scenario: Addition of pos and neg number
  
  Given The calculator is turned on able to enter number
  When I type in "positive number"
  And I press "plus"
  And I type in "negative number"
  And I press "equals"
  Then I see the "added number" as the result

Scenario: Addition of decimals
  
  Given The calculator is turned on able to enter decimal number
  When I type in "positive decimal number"
  And I press "plus"
  And I type in "positive decimal number"
  And I press "equals"
  Then I see the "added number" as the result

Scenario: Typing operator more than once

  Given The calculator is turned on able to enter operator and number
  When I type in "number"
  And I press "plus"
  And I press "minus"
  And I type in "number"
  And I press "equals"
  Then I see the "added number" as the result as it will prefer the first operator

Scenario: Addition of more than 2 numbers

  Given The calculator is turned on able to enter number
  When I type in "number"
  And I press "plus"
  And I type in "number"
  And I press "plus"
  And I type in "number"
  And I press "equals"
  Then I see the "added number" as the result

Scenario: Adding numbers where the result goes out of range

  Given The calculator is turned on able to enter big number
  When I type in "number"
  And I press "plus"
  And I type in "number"
  And I press "equals"
  Then I see the result within the range

Scenario: 6+* is provided as input?
  Given The calculator is turned on able to enter number
  When I type in "number"
  And I press "plus"
  And I press "multiple"
  Then I will wait for next operand

Scenario: Identify operation
  Given The calculator is turned on able to enter number
  When I type in "Identity"
  And I press "plus"
  And I type in "number"
  And I press "equals"
  Then I see the "added number" as the result
  
Scenario: Converse operation
  Given: the calculator is turned ON
  And I type in "number"
  And I press "plus"
  And I type in "number"
  Then I see the "added number" as the result
