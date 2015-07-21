# sorting.js
A visualization for a bunch of different sorting algorithms in Javascript that I wrote while bored on a plane.

See a demo here:
http://cs.stanford.edu/people/jcjohns/sorting.js/

More specifically, we visualize in-place comparison-based sorting algorithms by highlighting each comparison in blue and each swap in red. Currently the following sorting algorithms are implemented:

* [Bubble sort](https://en.wikipedia.org/wiki/Bubble_sort)
* [Selection sort](https://en.wikipedia.org/wiki/Selection_sort)
* [Insertion sort](https://en.wikipedia.org/wiki/Insertion_sort)
* [Odd-even sort](https://en.wikipedia.org/wiki/Odd%E2%80%93even_sort)
* [Cocktail sort](https://en.wikipedia.org/wiki/Cocktail_sort)
* [Quicksort](https://en.wikipedia.org/wiki/Quicksort)
* [Heapsort](https://en.wikipedia.org/wiki/Heapsort)
* [Merge sort](https://en.wikipedia.org/wiki/Merge_sort)
* [Introsort](https://en.wikipedia.org/wiki/Introsort)

The current partitioning implementation (used in quicksort and introsort) chooses a random element as a pivot rather than doing something fancier like median-of-medians, so the worst-case performance of algorithms that depend on it is quadratic.

The current mergesort implementation isn't *really* in-place; during the merge step, we scan the sorted subarrays to build up a permutation that will merge them, then convert the permutation to a sequence of swaps. These intermediate data structures use a linear amount of extra memory.
