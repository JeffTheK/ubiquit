# Console

Library `CoreConsole`.

`static class Console`

### Variables

* `static Color foreground_color`
* `static Color background_color`

### Functions

* `static String get_key()` - returns pressed key
* `static Integer get_cursor_x`
* `static Integer get_cursor_y`
* `static Null beep()` - plays a beep sound
* `static Null clear()` - clears the console buffer

### Key Codes

These are the strings returned by `get_key()`.

* `"backspace"`

* `"tab"`

* `"enter"`

* `"shift"`

* `"ctrl"`

* `"alt"`

* `"pause"`

* `"caps"`

* `"escape"`

* `"page_up"`

* `"page_down"`

* `"end"`

* `"home"`

* `"arrow_left"`

* `"arrow_right"`

* `"arrow_up"`

* `"arrow_down"`

* `"insert"`

* `"delete"`

* `"0"`

* `"1"`

* `"2"`

* `"3"`

* `"4"`

* `"5"`

* `"6"`

* `"7"`

* `"8"`

* `"9"`

* `"numpad0"`

* `"numpad1"`

* `"numpad2"`

* `"numpad3"`

* `"numpad4"`

* `"numpad5"`

* `"numpad6``

* `"numpad7"`

* `"numpad8"`

* `"numpad9"`


## Example

````
Console.get_key() // => "5"
````

