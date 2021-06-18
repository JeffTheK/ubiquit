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