# Load

 The load keyword is used to load additional source code files using a `library/filles` way. Raises if file not found. Loading files without he `.ubi` extension will not raise error if it is a work on multi language supported platform.

### Syntax

`load '*library*/\*file\*'

### Example

````
load 'tasker/utils.ubi'
````





## Load Relative

Loads file realtive to the current path. syntax is the  same, except you have to specify the relative path instead.

### Example

````
load '../some_dir/my_file.ubi'
````

