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

Scenario: Addition of fractions ({+ve,+ve},{-ve,+ve},{-ve,-ve})

  Given The calculator is turned on able to enter fraction
  When I type in "positive fraction number"
  And I press "plus"
  And I type in "positive fraction number"
  And I press "equals"
  Then I see the "added number" as the result

Scenario: Addition of +ve and -ve number
  
  Given The calculator is turned on able to enter number
  When I type in "positive number"
  And I press "plus"
  And I type in "negative number"
  And I press "equals"
  Then I see the "added number" as the result

Scenario: Addition of decimals({+ve,+ve},{+ve,-ve},{-ve,-ve})
  
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
  Then I see the "added number" as the result by doing modulo by maximum number as we have to build a cost effective calculator also

Scenario: 6+* is provided as input?
  Given The calculator is turned on able to enter number
  When I type in "number"
  And I press "plus"
  And I press "multiple"
  And I press "equals"
  Then it will check that that operator is (+,-) if the operators are not + or - the wait for other operand. 

Scenario: Identify operation
  Given The calculator is turned on able to enter number
  When I type in "Identity"
  And I press "plus"
  And I type in "number"
  And I press "equals"
  Then I see the "added number" as the result
  
Scenario: Converse operation
  Given: the calculator is turned ON
  When: I type operand2 + operan1
  Then: I get the same answer as that of operand1 + operand2
