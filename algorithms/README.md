# Analysis of Algorithms Sprint Challenge

## Exercise 1

```
	a) a = 0;
	   while (a < n * n * n)
	   		a = a + n * n;

	   ## O(n)

	b) // input array is of length n
	   i = array.length - 1;
	   while (array[i] > x && i >= 0)
	   		i = i/2;
	   ## O(n)

	c) sum = 0;
	   for (i = 0; i < Math.sqrt(n) / 2; i++)
	   		for ( j = i; j < 8 + i; j++) 
	   			for (k = j; k < 8 + j; k++)
	   				sum ++;
	   ## O(n^3)

	d) sum = 0;
	   for (i = 1; i < n; i *= 2)
	   		for (j = 0; j < n; j++)
	   			sum++;
	   ## O(n^2)

	e) sum = 0;
			for (i = 0; i < n; i++)
				for (j = i + 1; j < n; j++)
					for (k = j + 1; k < n; k++)
						for (l = k + 1; l < 10 + k; l++)
							sum++;
	   ## O(n^4)

	f) bunnyEars = function (bunnies) { // here bunnies === n
			if (bunnies === 0) return 0;
			return 2 + bunnyEars(bunnies - 1);
		}

		## O(n)

	g) search = function (array, arraySize, target) { // here arraySize === n
		if (arraySize > 0) {
			if (array[arraySize-1] === target) return true;
			else return search(array, arraySize - 1; target);
		}
		return false;
	   }

	   ## O(n)
```

## Exercise 2

```
	// Given an array of n numbers, design a linear running time algorithm to find the 
	// maximum value of a[j] - a[i], where j >= i.

	// sort numbers from lowest to highest
	// subtract lowest from highest and return the difference

	**const maxDifference = (array) => {
			array.sort();
			return array[array.length - 1] - array[0];
		}**

	// Suppose that you have an n-story building and plenty of eggs. Suppose also that an egg 
	// is broken if is thrown off floor f or higher, and unbroken otherwise. Devise a 
	// strategy to determine the value of f such that the number of dropped eggs is minimized.
```

## Exercise 3

```
	function quicksort(array)
		if length(array) <= 1
			return array
		select and remove a pivot element pivot from array
		create empty lists less and greater
		for each x in array
			if x <= pivot then append x to less
			else append x to greater
		return concatenate(quicksort(less), list(pivot), quicksort(greater))

	// Suppose we implement quicksort so that the pivot is always chosen to be the first element
	// of the array. What is the running time of this algorithm on an input array that is already
	// sorted? Why?

	## The running time of this algorithm on an input array that is already sorted in the worst case is
	O(n^2). The algorithm doesn't check to see if the array is already sorted, so it's going to perform all
	the necessary comparisons anyway.
	## 

	// Suppose we implement quicksort so that the pivot is always magically chosen to be the median 
	// element of the array. What is the running time of this algorithm? Why?

	## The running time of the algorithm if the pivot is chosen to be the median is O(n^3).


```