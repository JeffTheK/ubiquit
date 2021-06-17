# Ubiquit

# What Is This About?
This book covers my own scripting language, or more specifically, it’s design ideas. It’s just another one of my writing projects. That’s why I probably won’t actually make an implementation for it. If you want to make one, then go ahead.



# File extensions
`.ub`  is used for all files



# Object class

Library `CoreObject`. loaded and used by default

### Functions

* `static Array get_member_functions()` - returns an array containing strings named after member functions

* `static Array get_static_functions()` - returns an array containing strings named after static functions



# Integer Class

### Functions

* `static Integer max_value()` - returns maximum possible value
* `static Integer min_value()` - returns minimum possible value
* `Float to_float()` - returns integer converted to float



# Float Class

### Functions

* `static Float max_value()` - returns maximum possible value
* `static Float min_value()` - returns minimum possible value
* `Integer to_int()` - returns float converted to integer

# Input Output
Library `CoreIO`. loaded and used by default

### Variables
* `static Bool echo = true` - controls whether the input should be written back


### Functions

* `static void print(Object)` - prints passed in object/text
* `static String get_line()` - returns string line
* `static String get_char()` - returns pressed character

