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
* `String class` - returns class name



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





# Dir

Library `CoreDir`. Loaded and used by default.



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



# Console

Library `CoreConsole`.

`static class Console`

### Variables

* `static Color foreground_color`
* `static Color background_color`

### Functions

* `static Integer get_cursor_x`
* `static Integer get_cursor_y`
* `static Null beep()` - plays a beep sound
* `static Null clear()` - clears the console buffer

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







