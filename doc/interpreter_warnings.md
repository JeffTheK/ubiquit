# Interpreter Warnings



### `Unreachable Return Statement`

When a return statement is impossible to achieve.

example:

````
static func do_thing() {
	return 7
	return "Hello" // We exit the func after the first one. Raise warning
}
````

