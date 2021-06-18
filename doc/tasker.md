# Tasker

Library `CoreTasker`. Provides make like utility.

### Special tasks

Already included. You can extend them.

* `default` - runs when no arguments are passed
* `test` - runs tests
* `task_not_found` - runs when given task name is not found

### Example

````
func default {
	Tasker.run_task("print_hello")
}

func print_hello {
	print("hello, world!")
}
````

