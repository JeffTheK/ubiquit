# Interpreter Errors



## `Non static function in a static class` 

When non static function is found in a static class.

example:

````
static class Foo {
	func baz() {} // error here
}
````

