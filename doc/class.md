# Class

Default Constructor that requires parameters according to variables and initializes them is provided. Constructors can't be static. Gives error if `static func constructor()`  is found.

### Syntax

````
class *NameHere* {
	static some_var = 0
	other_var = "foo"
	
	func constructor(_other_var) {
		other_var = _other_var
	}
	
	func say_hello() {
		// ...
	}
}
````

### Default Functions

* constructor() - regular constructor that has variables_ parameters. Initializes class variables with parameters.