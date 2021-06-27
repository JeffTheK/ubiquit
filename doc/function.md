# Functions

Functions with no return statement return `null`.

### Syntax

````
fun *return_type* *name_here*(*arguments*) {
	// code
}
````

### Return Statement

`return` is used to return values. Having a return that is impossible to achieve will raise warning.

### Example

````
fun void swap(number& x, number& y) {
	number tmp = x;
	x = y;
	y = tmp;
}

fun void quicksort(number[]& arr, number begin, number end, number(number, number) comp) {
	if (end - begin < 2)
		return;
	
	number pivot = arr[end-1];

	number i = begin;
	
	for (number j = begin; j < end-1; ++j)
		if (comp(arr[j], pivot))
			swap(&arr[i++], &arr[j]);
	
	swap (&arr[i], &arr[end-1]);

	quicksort(&arr, begin, i, comp);
	quicksort(&arr, i+1, end, comp);
}
````

