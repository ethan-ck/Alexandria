Big-O Notation 

Refers to the complexity related to the number of items in an algorithm. 

Add Sugar to Tea

	1. Fetch the bowl containing the sugar
	2. Get a spoon
	3. Scoop out sugar using the spoon
	4. Pour the sugar from the spoon into the tea
	5. Repeat steps 3 and 4 until you've added the desired amount of sugar. 

Number of desired sugars = n

Total number of steps = 2n + 2

As n grows, the number of steps grow

The "2" in 2n and the "+ 2" remain constant, so they don't factor into the time complexity.

The value of n determines the growth rate. 

Time complexity is represented as O(n)

It is a linear time complexity

Types of Big-O Notation
	From best to worst: 
	O(1)                       Constant 
	O(logn)                  Logarithmic
	O(n)                          Linear
	O(nlogn)                n log-star n
	O(n^2)                    Quadratic


![[1280px-Comparison_computational_complexity.svg.png]]

A Big-O Notation gives us a way to compare the time complexity of different algorithms in a independent manner. It is useful for measuring performance for hardware. 

Arrays - A data structure that consists of integers, floats, strings, and Boolean. 

It is stored as a contiguous block in memory

Every element in an array occupies the same amount of space in memory

But what if you create an array with differing lengths of strings? 

It still occupies the same amount of space, because when you create an array and fill it with objects, the data that is stored in the variables is an **object reference**.

When calling each element in an array, the program is retrieving the references to the object in the array. Each object reference is the exact same size. 

If we know the index of an element in the array, we can find it very quickly. 

Big-O Values for Array Operations 

No matter how many elements we have, it will always take 3 steps to retrieve an element for an array.

	1. Multiple the size of the element by its index
	2. Get the start address of the array
	3. Add the start address to the result of the multiplication

The biggest advantage of an Array is the fact that it is the most efficient way to retrieve data provided you know the index of the element. 

If the code requires a loop, it will be a linear time complexion.

O(n)

If the code does not require a loop, it will be constant time. 

O(1)
