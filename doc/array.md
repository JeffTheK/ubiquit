# Array

Library `CoreArray`. Loaded and used by default. Indexes start at 0.

### Variables

* `Integer size = 0`

### Functions

* `Bool ==(other)`
* `Object [](Integer index)` - returns element at index or null if out of bounds, raises if index < 0
* `Array select_if(Function fun)` - returns a new array of elements that passed the function check
* `Null []=(Integer index, Object new_value)`
* `Null delete_if(Function fun)` - deletes elements if passed function will return true
* `Null clear()` - deletes all elements 