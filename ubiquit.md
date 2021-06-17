# Ubiquit

# What Is This About?
This book covers my own scripting language, or more specifically, it’s design ideas. It’s just another one of my writing projects. That’s why I probably won’t actually make an implementation for it. If you want to make one, then go ahead.



# File extensions
`.ub`  is used for all files



# Object class
Library CoreObject

loaded and used by default

## Member Functions

* Array get_member_functions() - returns an array containing strings named after member functions

## Static Functions

* Array get_static_functions() - returns an array containing strings named after static functions



# Input Output
Library `CoreIO`

loaded and used by default

## Static Variables
* Bool echo = true - controls whether the input should be written back


## Functions

* void print(Object) - prints passed in object/text
* String get_line() - returns string line
* String get_char() - returns pressed character