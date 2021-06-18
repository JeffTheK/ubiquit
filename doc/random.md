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
