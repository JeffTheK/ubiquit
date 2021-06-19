# Unit Tests

Library `CoreTest`.

### Functions

* `static void assert(expression)` - raises exception if expression not true
* `static void assert_raise(expression)` - raises exception if expression doesn't raise

### Naming

Tests files should start with `test_`. Test functions start with `test_`. Files should reside in the `/test/` directory.

### Running

Run `test` tasker task. It will execute all files in the `/test/` directory.

### Example

````
func test_one_plus_one {
	assert(1 + 1 == 2)
}
````

# 