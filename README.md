# C - Sorting algorithms & Big O

In this project, I implemented twelve different sorting algorithms.

## Tests :heavy_check_mark:

* [tests](./tests): Folder of test files. Provided by Holberton School.

## Helper Files :raised_hands:

* [print_array.c](./print_array.c): C function that prints an array of
integers. Provided by ALX.
* [print_list.c](./print_list.c): C function that prints a list of integers. Provided by ALX.

## Header Files :file_folder:

* [sort.h](./sort.h): Header file containing definitions and prototypes for
all types and functions written for the project.

Data Structure:
```
/**
 * struct listint_s - Doubly linked list node
 *
 * @n: Integer stored in the node
 * @prev: Pointer to the previous element of the list
 * @next: Pointer to the next element of the list
 */
typedef struct listint_s
{
    const int n;
    struct listint_s *prev;
    struct listint_s *next;
} listint_t;
```

* [deck.h](./deck.h): Header file containing definitions and prototypes for all types and functions written for task `1000-sort_deck.c`.


## Tasks :page_with_curl:

* **0. Bubble sort**
  * [0-bubble_sort.c](./0-bubble_sort.c)
  * Function that sorts an array of integers in ascending order using the Bubble sort algorithm

	* Prototype: `void bubble_sort(int *array, size_t size);`
	* You’re expected to print the array after each time you swap two elements
  * [0-O](./0-O): Text file containing the best, average, and worst case time complexities of the Bubble Sort algorithm, with 1 notation per line.

* **1. Insertion sort**
  * [1-insertion_sort_list.c](./1-insertion_sort_list.c): Function that sorts a doubly-linked list of integers in ascending order using the Insertion Sort algorithm.
	* Prototype: `void insertion_sort_list(listint_t **list);`
	* You are not allowed to modify the integer n of a node. You have to swap the nodes themselves.
	* You’re expected to print the list after each time you swap two elements
  * [1-O](./1-O): Text file containing the best, average, and worst case time complexities of the Insertion Sort algorithm, with 1 notation per line.

* **2. Selection sort**
  * [2-selection_sort.c](./2-selection_sort.c): Function that sorts an array of integers in ascending order using the Selection Sort algorithm.
  * Prototype: `void selection_sort(int *array, size_t size);`
  * You’re expected to print the array after each time you swap two elements
  * [2-O](./2-O): Text file containing the best, average, and worst case time complexities of the Selection Sort algorithm, with 1 notation per line.

* **3. Quick sort**
  * [3-quick_sort.c](./3-quick_sort.c): C function that sorts an array of integers in ascending order using the Quick Sort algorithm.
  * Prototype: `void quick_sort(int *array, size_t size);`
  * You must implement the Lomuto partition scheme.
  * The pivot should always be the last element of the partition being sorted.
  * You’re expected to print the array after each time you swap two elements
  * [3-O](./3-O): Text file containing the best, average, and worst case time complexities of the Quick Sort Lomuto Partition scheme algorithm, with 1 notation per line.

* **4. Shell sort - Knuth Sequence**
  * [100-shell_sort.c](./100-shell_sort.c): function that sorts an array of integers in ascending order using the Shell sort algorithm, using the Knuth sequence

  * Prototype: `void shell_sort(int *array, size_t size);`
  * You must use the following sequence of intervals (a.k.a the Knuth sequence):
	* n+1 = n * 3 + 1
	* 1, 4, 13, 40, 121, ...
  * You’re expected to print the array each time you decrease the interval

  No big O notations of the time complexity of the Shell sort (Knuth sequence) algorithm needed - as the complexity is dependent on the size of array and gap
  

* **5. Cocktail shaker sort**
  * [101-cocktail_sort_list.c](./101-cocktail_sort_list.c): function that sorts a doubly linked list of integers in ascending order using the Cocktail shaker sort algorithm

  * Prototype: `void cocktail_sort_list(listint_t **list);`
  * You are not allowed to modify the integer n of a node. You have to swap the nodes themselves.
  * You’re expected to print the list after each time you swap two elements
  * [101-O](./101-O): Text file containing the best, average, and worst case time complexities of the Cocktail Shaker Sort algorithm, with 1 notation per line.

* **6. Counting sort**
  * [102-counting_sort.c](./102-counting_sort.c): function that sorts an array of integers in ascending order using the Counting sort algorithm

  * Prototype: `void counting_sort(int *array, size_t size);`
  * You can assume that array will contain only numbers >= 0
  * You are allowed to use malloc and free for this task
  * You’re expected to print your counting array once it is set up 
	* This array is of size k + 1 where k is the largest number in array
  * [102-O](./102-O): Text file containing the best, average, and worst case time complexities of the Counting Sort algorithm, with 1 notation per line.

* **7. Merge sort**
  * [103-merge_sort.c](./103-merge_sort.c): function that sorts an array of integers in ascending order using the Merge sort algorithm

  * Prototype: `void merge_sort(int *array, size_t size);`
  * You must implement the top-down merge sort algorithm
	* When you divide an array into two sub-arrays, the size of the left array should always be <= the size of the right array. i.e. {1, 2, 3, 4, 5} -> {1, 2}, {3, 4, 5}
	* Sort the left array before the right array
  * You are allowed to use printf
  * You are allowed to use malloc and free only once (only one call)
  * [103-O](./103-O): Text file containing the best, average, and worst case time complexities of the Merge Sort algorithm, with 1 notation per line.

* **8. Heap sort**
  * [104-heap_sort.c](./104-heap_sort.c): function that sorts an array of integers in ascending order using the Heap sort algorithm

  * Prototype: `void heap_sort(int *array, size_t size);`
  * You must implement the sift-down heap sort algorithm
  * You’re expected to print the array after each time you swap two elements
  * [104-O](./104-O): Text file containing the best, average, and worst case time complexiites of the Heap Sort algorithm, with 1 notation per line.

* **9. Radix sort**
  * [105-radix_sort.c](./105-radix_sort.c): function that sorts an array of integers in ascending order using the Radix sort algorithm

  * Prototype: `void radix_sort(int *array, size_t size);`
  * You must implement the LSD radix sort algorithm
  * You can assume that array will contain only numbers >= 0
  * You are allowed to use malloc and free for this task
  * You’re expected to print the array each time you increase your significant digit
  * [105-O](./105-O): Text file containing the best, average, and worst case time complexities of the Radix Sort algorithm, with 1 notation per line.

* **10. Bitonic sort**
  * [106-bitonic_sort.c](./106-bitonic_sort.c): function that sorts an array of integers in ascending order using the Bitonic sort algorithm

  * Prototype: `void bitonic_sort(int *array, size_t size);`
  * You can assume that size will be equal to 2^k, where k >= 0 (when array is not NULL …)
  * You are allowed to use printf
  * You’re expected to print the array each time you swap two elements
  * [106-O](./106-O): Text file containing the best, average, and worst case time complexities of the Bitonic Sort algorithm, with 1 notation per line.

* **11. Quick Sort - Hoare Partition scheme**
  * [107-quick_sort_hoare.c](./107-quick_sort_hoare.c): function that sorts an array of integers in ascending order using the Quick sort algorithm

  * Prototype: `void quick_sort_hoare(int *array, size_t size);`
  * You must implement the Hoare partition scheme.
  * The pivot should always be the last element of the partition being sorted.
  * You’re expected to print the array after each time you swap two elements
  * [107-O](./107-O): Text file containing the best, average, and worst case time complexities of the Quick Sort Hoare Partition cheme algorithm, with 1 notation per line.

* **12. Dealer**
  * [1000-sort_deck.c](./1000-sort_deck.c): C function that sorts a deck of cards.
  * Prototype: `void sort_deck(deck_node_t **deck);`
  * You are allowed to use the C standard library function qsort
  * Please use the following data structures:
```
typedef enum kind_e
{
    SPADE = 0,
    HEART,
    CLUB,
    DIAMOND
} kind_t;

/**
 * struct card_s - Playing card
 *
 * @value: Value of the card
 * From "Ace" to "King"
 * @kind: Kind of the card
 */
typedef struct card_s
{
    const char *value;
    const kind_t kind;
} card_t;

/**
 * struct deck_node_s - Deck of card
 *
 * @card: Pointer to the card of the node
 * @prev: Pointer to the previous node of the list
 * @next: Pointer to the next node of the list
 */
typedef struct deck_node_s
{
    const card_t *card;
    struct deck_node_s *prev;
    struct deck_node_s *next;
} deck_node_t;
```

  * You have to push you deck.h header file, containing the previous data structures definition
  * Each node of the doubly linked list contains a card that you cannot modify. You have to swap the nodes.
  * You can assume there is exactly 52 elements in the doubly linked list.
  * You are free to use the sorting algorithm of your choice
  * The deck must be ordered:
	* From Ace to King
	* From Spades to Diamonds
