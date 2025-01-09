# Unexpected Behavior with Ruby Accessor Methods

This repository demonstrates a common, yet subtle, error in Ruby related to accessor methods and instance variable modification.  Direct assignment to a method that only acts as a getter does not modify the underlying instance variable unless a corresponding setter method is explicitly defined.

The `bug.rb` file shows the problematic code, while `bugSolution.rb` presents the corrected version.

## Bug
The unexpected behavior arises when trying to modify the instance variable `@value` indirectly through the `value` method.  Since there's no `value=` setter method, the assignment `my_object.value = 30` has no effect on `@value`.