
Sort Algorithms - Bubble Sort Theory 

Bubble Sort Theory does not create a new partition for an array, it works within the same array. 

With an array of [-15,22,59,30,1,7]
	Bubble sort starts at the unsorted partition index. 

Bubble Sort will start at the first index in the array and ask if -15 is greater than 22. It is not, so nothing changes. 22 < 59, nothing changes. 59 > 30, so the 59 and 30 are switched in the array. The logic continues until the 59 is the last integer in the array. 

Then, the first iteration is complete and there are now two partitions, the unsorted partition and the sorted partition. The cycle will then repeat. 

	So unsortedPartitionIndex = 6

	I = 6 - index 

Bubble Sort Implementation

O to the n^2, making it quadratic. The performance of the algorithm will quickly degrade. 

Stable vs Unstable Sort Algorithms 

A Stable sort algorithm preserves the order of duplicated objects while an unstable sort algorithm does not.

	For Example, in an array of integers: 1, 9, 4, 3, 9, 8

	9 is presented twice, in a stable sort, the first 9 will always come before the second 9. 

Selection Sort (Theory)

	Selection Sort is similar to Bubble sort in the way that it creates two separate partitions, an unsorted partition and a sorted partition. 

	 Consider an array of integers: 20, 35, -15, 7, 55, 1, -22 

	lastUnsortedIndex = 6: This is the last index of the unsorted partition 

	i = 1: index used to traverse the array from left to right

	largest = 0: the index of the largest element in the unsorted partition 

	The sort will start at 20, it will compare 20 to 35, and see that 35 is greater, so the largest = 1. It will then traverse from left to right and see that 55 is greater than 35, so largest = 4. Each time the largest integer will compare itself to the others, the i will update accordingly. After it completes the traverse, the largest integer will be selected and stored at the end of the array, and the lastUnsortedIndex = 5. This process will continue. Selection Sort is an unstable sort.


Insertion Sort (Theory)
	Consider an array of integers: 20, 35, -15, 7, 55, 1, -22

	firstUnsortedIndex = 1 - This is the first index of the unsorted petition 

	i = 0 - index used to transverse the sorted partition from right to left  

	newElement = 35 - the value we want to insert into the sorted partition - array[firstUnsortedIndex]

	Unlike the previous sorting algorithmns, the sorted partition is on the left side of this array. 

	This algorithm will considered 20 sorted already, and compare if 20 is greater than 35, it is not, so 20 and 35 are considered to be sorted. the firstUnsortedIndex will now be updated to 2, and the algorithm will compare 35 to -15, -15 is less than 35, so it will continue from right to left until it reaches the last element position, then the -15 will be inserted into index 0. This algorithm is considered a stable sort.  Quadratic Algorithm if it is unsorted 


Shell Sort (Theory)
	