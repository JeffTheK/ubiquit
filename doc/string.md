# String

Library `CoreString`. Represents one or more characters. Loaded and used by default. Enclosed either in `''` or `""`. Special characters are escaped using `\`. Multiline strings are enclosed in `"""`.

### V.ariables

* `Integer size = 0` - number of characters

### Functions

* `Array to_array(String split = '')` - returns array of strings by splitting the string
* `String interpolate(Hash variables)` - interpolates between Hash where key => String, value => Object

### Example

````
s1 = 'hello'
s2 = "hello"
s3 = 'jeff\'s world'
s4 = "hello, world\n"

multi_string = """
hello, world!
I hope you like it!
"""
````



