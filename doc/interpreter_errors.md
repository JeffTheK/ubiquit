# Interpreter Errors



## `Non static function in a static class` 

When non static function is found in a static class.

example:

````
static class Foo {
	func baz() {} // error here
}
````



## `Access of non static variables in a static function`

When static function tries to access non static variables

example:

````
class Counter {
	count = 0
	
	static func increase_count() {
		count += 1 // error, count is not static
	}
}
````

