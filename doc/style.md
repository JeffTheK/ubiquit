# Style

### Files

All ubiquit source code files should be in lower case and use underscores for spaces and end with `.ubi` extension.

example: `foo.ubi`, `person_utility.ubi`

### Variables

Variables should be in lowercase. Assign the with default values as much as possible.

example: `foo_bar = 0`

### Functions

Functions should be in lowercase. Use `is_` for bool returning functions. Define them in one line if the code is very small.  Add comments above declaration to document them.

example:

````
function static say_hello() { print('Hello!') }

// returns one plus one
function static do_thing() {
	// note: this is a brace style used by standard libraries
	return 1 + 1
}
````

