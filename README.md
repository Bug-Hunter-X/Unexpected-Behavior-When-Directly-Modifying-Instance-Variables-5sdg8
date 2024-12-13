# Unexpected Behavior When Directly Modifying Instance Variables in Ruby

This repository demonstrates a potential issue in Ruby when directly modifying instance variables using `instance_variable_set` instead of using accessor methods (getters and setters).  Direct manipulation can lead to unexpected behavior and inconsistencies if other parts of your code rely on those accessor methods.

The example showcases a class with a getter method for accessing an instance variable. When the instance variable is modified directly, the getter method is bypassed, potentially leading to discrepancies between the actual value and the value accessed through the getter.

This practice can make debugging more difficult and introduce subtle bugs. It's good practice to always use accessor methods for managing the internal state of a class.

## How to reproduce

1. Clone this repository.
2. Run `ruby bug.rb`
3. Observe that the output shows the value changing even though the getter is not used to set the value. This behavior might be unexpected if you rely on the getter for managing changes to the value.