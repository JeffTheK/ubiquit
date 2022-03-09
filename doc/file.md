# File

Library `File`. Loaded and used by default.

### `File`

### Functions

* `String read()` - returns string with contents of the file
* `String get_extension()` - returns extension of the file with the dot or empty string if no extension
* `void append(String text)` - writes text to the end of the file
* `void delete_contents()` - empties the file
* `void delete()` - deletes the file and it's contents
* `void rename(String new_name)` - gives file a new name, raises if string is not a valid name
* `void move(String path)` - moves file to a new path relative to the current directory
