# Ubiquit

# What Is This About?
This book covers my own scripting language, or more specifically, it’s design ideas. It’s just another one of my writing projects. That’s why I probably won’t actually make an implementation for it. If you want to make one, then go ahead.



# File extensions
`.ub`  is used for all files



# Keywords

Here's a list of reserved words.

* `class`
* `func`
* `return`
* `if`
* `else`
* `for`
* `static`
* `do`
* `while`
* `true`
* `false`
* `try`
* `null`
* `super`

# Functions

Functions with no return statement return `null`.

### Syntax

````
func *name_here* {
	// code
}
````





# Class

### Syntax

````
class *NameHere* {
	static some_var = 0
	other_var = "foo"
	
	func say_hello() {
		// ...
	}
}
````



# Static Class

Can't be instantiated. Can only have static functions and variables.

### Syntax

````
static class *NameHere* {
	// code
}
````



# Object class

Library `CoreObject`. loaded and used by default

### Functions

* `static Array get_member_functions()` - returns an array containing strings named after member functions
* `static Array get_static_functions()` - returns an array containing strings named after static functions
* `String to_string()` - returns strings of class alongside with it's values of variables



# Integer Class

### Variables

* `static Integer max_value`
* `static Integer min_value`

### Functions

* `Float to_float()` - returns integer converted to float
* `String to_string()` - converts to string



# Float Class

### Variables

* `static Float max_value`
* `static Float min_value`

### Functions

* `Integer to_int()` - returns float converted to integer
* `String to_string()` - converts to string



# String

Library `CoreString`. Represents one or more characters. Loaded and used by default.

### Variables

* `Integer size = 0` - number of characters

### Functions

* `Array to_array(String split = '')` - returns array of strings by splitting the string
* `String interpolate(Hash variables)` - interpolates between Hash where key => String, value => Object



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

# Hash

Library `CoreHash`. Loaded and used by default.

### Variables

* `Integer size = 0`
* `Array keys`
* `Array values`

### Functions

* `Bool ==(other)`
* `Object [](Object key)`
* `null []=(Object key, Object new_value)`
* `null clear()` - deletes all elements

# File

Library `CoreFile`. Loaded and used by default.

### `File`

### Variables

* `Date birth_time` - date when file was created
* `Date access_time = null` - last time file was accessed or null
* `String name` - full name
* `String directory` - where file is located
* `Integer size = 0` - size in bytes

### Functions

* `String read()` - returns string with contents of the file

* `String get_extension()` - returns extension of the file with the dot or empty string if no extension

* `void append(String text)` - writes text to the end of the file

* `void delete_contents()` - empties the file

* `void delete()` - deletes the file and it's contents

* `void rename(String new_name)` - gives file a new name, raises if string is not a valid name

* `void move(String path)` - moves file to a new path relative to the current directory

  

# Input Output

Library `CoreIO`. loaded and used by default

### Variables
* `static Bool echo = true` - controls whether the input should be written back


### Functions

* `static void print(Object)` - prints passed in object/text
* `static String get_line()` - returns string line
* `static String get_char()` - returns pressed character



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



# Random

Library `CoreRandom`. Used for random number generation.

### Variables

* `static Integer seed = 0`

### Functions

* `static Integer get_integer()` - returns random integer
* `static Integer get_integer(Integer min, Integer max)` - returns number in `min` to `max` range
* `static Float get_float()` - returns random float
* `static Float get_float(Float min, Float max)` - returns float in `min` to `max` range

### Example

````
num1 = Random.get_integer() // => 7148
num2 = Random.get_integer(0, 0) // => 0
num3 = Random.get_integer(3, 7) // => 6
````



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





# Library Structure

### File Structure

Here is shown a `foo_bar` package example

````
foo_bar
|	readme.md
|	code_of_conduct.md
| 	license.txt
|	package.json
|	taskfile
|	.gitignore
|
|___src
|		foo.ub
|		bar.ub
|
|___test
|		test_foo.ub
|		test_bar.ub
|
|___doc
|		doc1.md
|		doc2.md


````

### Package specification

Contains useful information about the library.

#### Required Properties:

* `name` - this package's name
* `author` or `authors` - a list of creators
* `version` - current package version

#### Recommended Properties:

* `email`
* `homepage`
* `license`
* `description`



### `package.json` Structure Example	

````json
{
    "package": {
        "name": "foo_bar",
        "version": "1.0.0",
        "license": "MIT",
        "authors": [
            "JeffTheK",
            "Shwaika"
        ],
        "email": "jeff@example.com",
        "homepage": "https://github.com/jeff/foo_bar",
        "ubiquit_version": "3.*",
        "description": "Provides foo and bar"
        "runtime_dependencies": [
            {
                "name": "some_library",
                "version": "1.6.*"
            },
            {
                "name": "other_tool",
                "version": "*"
            }
        ],
        "development_dependencies": [
            {
               	"name": "fast_test",
                "version": "2.0.1"
            }
        ],
        "executables": [ "foo" ],       
        "post_install_message": "Thanks for installing!",
        "requirements": [
            "A good graphics card"
        ]
    }
}
````







