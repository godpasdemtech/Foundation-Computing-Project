

BOOK ORGANIZER

Project Overview

The Book Organizer is a C programming project developed as part of the Solent University Foundation Computing assessment.

The project begins with a two-dimensional string array containing eight book titles in deliberately mixed alphabetical order. It then progressively develops through Grades D, C, B and A.

The assessment demonstrates the development of string manipulation, case-insensitive comparison, array processing, sorting algorithms, searching, deletion and data shifting.

By Grade A, the program allows the user to delete a book from the collection and implements a second sorting algorithm, Bubble Sort, in addition to the sorting approach developed in Grade B.

---

PROJECT OBJECTIVES

The main objectives of the Book Organizer are to:

- Store multiple book titles using a two-dimensional character array.
- Display book titles using loops.
- Access specific elements of a string array.
- Compare book titles alphabetically.
- Perform case-insensitive string comparisons.
- Swap strings within an array.
- Sort book titles alphabetically.
- Implement nested loops for sorting.
- Search for a book title entered by the user.
- Delete a selected book.
- Shift remaining books to remove gaps in the array.
- Implement Bubble Sort as an alternative sorting algorithm.
- Compare two sorting approaches in terms of logic and performance.
- Develop practical understanding of strings and arrays in C.

---

DEVELOPMENT PROGRESSION

The assessment was developed progressively from Grade D to Grade A.

GRADE D
String array and basic display
        ↓
GRADE C
Single-pass alphabetical positioning
        ↓
GRADE B
Complete alphabetical sorting
        ↓
GRADE A
Book deletion + Bubble Sort + algorithm comparison

Each grade builds upon the functionality introduced in the previous grade.

---

GRADE D – BOOK ARRAY AND BASIC DISPLAY

Overview

Grade D establishes the basic Book Organizer.

Eight book titles are stored in a two-dimensional character array:

char books[8][100]

The titles are deliberately stored in mixed alphabetical order.

A "for" loop is used to display each current title together with the first title stored at index "0".

Main Features

- Stores eight book titles.
- Uses a two-dimensional character array.
- Uses a "for" loop to process the books.
- Displays the current book title.
- Displays the title stored at index "0".
- No sorting or manipulation is performed at this stage.

Initial Book List

The program contains:

1. Moonlight Over Lagos
2. Atomic Habits
3. The Silent Patient
4. Deep Work
5. A Brief History of Time
6. Rich Dad Poor Dad
7. Educated
8. Zero to One

The deliberately mixed ordering provides the starting point for the sorting tasks introduced in later grades.

Program Link

Programiz Online Compiler:

https://www.programiz.com/online-compiler/4NT1STkHOB9eb

---

GRADE C – SINGLE-PASS ALPHABETICAL COMPARISON

Overview

Grade C builds upon the Grade D program by introducing alphabetical comparison and string swapping.

The program performs a single pass through the array to determine which title should be placed at index "0".

The comparison is case-insensitive, meaning titles such as:

Atomic Habits
atomic habits

can be compared without the capitalisation affecting the alphabetical comparison.

Main Features

- Retains the Grade D book array.
- Displays the list before processing.
- Compares each title with the title at index "0".
- Creates lowercase copies for comparison.
- Uses "strcmp()" to perform alphabetical comparison.
- Swaps titles when a title occurs earlier alphabetically.
- Displays the list after the single pass.
- Does not print during the sorting loop.

String Handling

The program uses:

strcpy()

to copy titles into temporary strings.

It then uses:

tolower()

to convert the temporary copies to lowercase.

Finally:

strcmp()

is used to determine the alphabetical order.

Sorting Logic

The program compares:

books[i]

with:

books[0]

If the current title comes before the title at index "0", the two strings are swapped.

This ensures that the earliest alphabetical title encountered during the pass is moved towards the front.

Program Link

Programiz Online Compiler:

https://www.programiz.com/online-compiler/8Z2V7dFpzcmPz

---

GRADE B – FULL ALPHABETICAL SORTING

Overview

Grade B extends the Grade C approach into a complete sorting algorithm.

Instead of only determining the earliest title for index "0", the program uses nested loops to process every position in the array.

The algorithm repeatedly searches the remaining unsorted section and swaps a book into the appropriate position.

Main Features

- Displays the books before sorting.
- Uses an outer loop to select the position being processed.
- Uses an inner loop to examine remaining titles.
- Performs case-insensitive comparisons.
- Swaps strings using a temporary character array.
- Produces a fully alphabetically ordered list.
- Displays the list after sorting.

Sorting Process

The outer loop controls the current position:

for(i = 0; i < 8 - 1; i++)

The inner loop checks the remaining books:

for(j = i + 1; j < 8; j++)

The two titles being compared are copied into temporary strings and converted to lowercase.

If the second title comes before the current title alphabetically, they are swapped.

Conceptually:

Find the appropriate title
        ↓
Place it in the current position
        ↓
Move to the next position
        ↓
Repeat until the list is sorted

Result

The supplied Grade B output demonstrates the final alphabetical ordering:

1. A Brief History of Time
2. atomic habits
3. Deep Work
4. Educated
5. Moonlight Over Lagos
6. Rich Dad Poor Dad
7. The Silent Patient
8. Zero to One

Program Link

Programiz Online Compiler:

https://www.programiz.com/online-compiler/7dIWZgcK8h69M

---

GRADE A – BOOK DELETION AND BUBBLE SORT

Overview

Grade A represents the most advanced version of the Book Organizer.

It retains the sorting functionality developed previously and introduces two major additions:

1. Book deletion
2. A second sorting algorithm – Bubble Sort

The program therefore demonstrates searching, deletion, array shifting and comparison of two sorting approaches.

---

BOOK DELETION

The user is asked to enter the title of the book they want to delete:

scanf(" %[^\n]", deleteTitle);

The program then searches through the current book list.

The comparison is performed case-insensitively by converting temporary copies of the book title and user input to lowercase.

If a matching title is found:

Book deleted successfully.

is displayed.

If no matching title exists:

Book not found.

is displayed.

---

SHIFTING BOOKS AFTER DELETION

When a book is found, the remaining titles are shifted one position to the left.

The program uses:

for(j = i; j < numberOfBooks - 1; j++)
{
    strcpy(books[j], books[j + 1]);
}

This prevents an empty gap from being left in the middle of the book array.

For example:

Before deletion:

1. A Brief History of Time
2. atomic habits
3. Deep Work
4. Educated
5. Moonlight Over Lagos

Delete:
3. Deep Work

After deletion:

1. A Brief History of Time
2. atomic habits
3. Educated
4. Moonlight Over Lagos

The number of active books is then reduced:

numberOfBooks--;

---

SECOND SORTING ALGORITHM – BUBBLE SORT

Grade A introduces Bubble Sort as a second sorting algorithm.

Bubble Sort repeatedly compares adjacent titles.

The program compares:

books[j]

with:

books[j + 1]

If the first title comes after the second alphabetically, they are swapped.

The process is repeated through multiple passes until the list is ordered.

Bubble Sort Logic

Compare adjacent titles
        ↓
Are they in the wrong order?
        ↓
YES → Swap them
        ↓
Continue through the list
        ↓
Repeat passes
        ↓
Sorted list

The comparison remains case-insensitive because temporary copies are converted to lowercase before "strcmp()" is used.

---

COMPARISON OF THE TWO SORTING ALGORITHMS

The Grade A program demonstrates two different sorting approaches.

Original Sorting Algorithm

The sorting approach developed in Grade B uses nested loops where the current position is compared with the remaining titles.

Its basic logic is:

Select a position
        ↓
Compare with remaining books
        ↓
Swap when an earlier title is found
        ↓
Move to the next position

This approach progressively places the appropriate title into each position of the array.

Bubble Sort

Bubble Sort instead compares adjacent elements.

Its basic logic is:

Compare neighbouring books
        ↓
Swap if they are incorrectly ordered
        ↓
Continue across the list
        ↓
Repeat multiple passes

---

SORTING PERFORMANCE

Both approaches use nested loops and therefore have a worst-case time complexity of approximately:

O(n²)

where "n" represents the number of books.

For a small collection such as eight books, both algorithms are practical and fast enough for the application.

However, their internal behaviour is different.

Feature| Original Sorting Approach| Bubble Sort
Main comparison| Current position vs remaining titles| Adjacent titles
Uses nested loops| Yes| Yes
Swapping| Yes| Yes
Case-insensitive comparison| Yes| Yes
Worst-case complexity| O(n²)| O(n²)
Suitable for 8 books| Yes| Yes
Main learning purpose| Position-based sorting| Adjacent-element sorting

For this assessment, the number of books is very small, so performance differences are not significant. The main value of implementing both algorithms is to demonstrate an understanding of different approaches to sorting data.

---

STRING MANIPULATION

String handling is an important part of the Book Organizer.

The program uses functions from:

#include <string.h>

including:

"strcpy()"

Used to copy book titles between character arrays.

"strcmp()"

Used to compare two strings alphabetically.

The program also uses:

#include <ctype.h>

for:

"tolower()"

This allows the program to create lowercase copies of titles before comparison, making the sorting process case-insensitive.

---

PROGRAMMING CONCEPTS USED

The project demonstrates several important C programming concepts.

Two-Dimensional Character Arrays

Book titles are stored using:

char books[8][100];

This provides storage for eight strings, with each string capable of holding up to 99 characters plus the null terminator.

Loops

The project uses:

- "for" loops
- Nested "for" loops

These are used for displaying, searching, sorting and shifting book titles.

Strings

Book titles are handled as character arrays.

String Functions

The program uses:

- "strcpy()"
- "strcmp()"

Character Processing

"tolower()" is used to support case-insensitive comparisons.

Searching

Grade A searches the book collection for a title entered by the user.

Deletion

A matching title is removed by shifting subsequent titles one position to the left.

Sorting

Two sorting approaches are demonstrated:

- The original position-based sorting approach.
- Bubble Sort.

Variables and Counters

Variables such as:

numberOfBooks
found
i
j
k

control the number of active books, search results and loop operations.

---

TESTING AND OUTPUT

The Book Organizer was developed progressively and tested using the Programiz online C compiler.

Testing evidence focuses on the functionality introduced at each grade.

Grade D

Testing includes:

- Displaying all eight book titles.
- Confirming the current title is displayed.
- Confirming the first title remains associated with index "0".

Grade C

Testing includes:

- Displaying the original list.
- Performing a single sorting pass.
- Confirming case-insensitive comparisons.
- Confirming the earliest title is moved to the front.

Grade B

Testing includes:

- Displaying the unsorted list.
- Running the complete sorting process.
- Confirming the final alphabetical order.

Grade A

Testing includes:

- Displaying the original book list.
- Performing the initial sorting process.
- Entering a book title for deletion.
- Confirming successful deletion.
- Confirming remaining books shift correctly.
- Handling a book that cannot be found.
- Performing Bubble Sort.
- Displaying the final sorted list.

Screenshots of the source code and program outputs provide visual evidence of the development and testing process.

---

DEVELOPMENT TOOLS

Programming Language

C

The assessment focuses on arrays, strings, loops, searching, sorting and data manipulation.

Online Compiler

Programiz Online C Compiler

Individual Programiz links are provided for each assessment grade.

Source Code

Each grade is stored separately in the portfolio to demonstrate the progression of the programming solution.

---

PROGRAMIZ LINKS

Grade| Program
Grade D| https://www.programiz.com/online-compiler/4NT1STkHOB9eb
Grade C| https://www.programiz.com/online-compiler/8Z2V7dFpzcmPz
Grade B| https://www.programiz.com/online-compiler/7dIWZgcK8h69M
Grade A| https://www.programiz.com/online-compiler/2X1nPCz2OQupf

---

PROJECT STRUCTURE

The portfolio version of Assessment 6 is organised as follows:

ASS6_BOOK ORGANIZER/
│
├── README.md
│
├── source-code/
│   ├── GRADE D.txt
│   ├── GRADE C.txt
│   ├── GRADE B.txt
│   └── GRADE A.txt
│
├── screenshots/
│   ├── GRADE D/
│   │   ├── CODE screenshots/
│   │   └── OUTPUT screenshots/
│   │
│   ├── GRADE C/
│   │   ├── CODE screenshots/
│   │   └── OUTPUT screenshots/
│   │
│   ├── GRADE B/
│   │   ├── CODE screenshots/
│   │   └── OUTPUT screenshots/
│   │
│   └── GRADE A/
│       ├── CODE screenshots/
│       └── OUTPUT screenshots/
│
├── test-results/
│   └── .gitkeep
│
└── demonstration/
    └── .gitkeep

---

ACADEMIC CONTEXT

This project forms part of the Solent University Foundation Computing assessment work.

The assessment provides practical experience in manipulating collections of text data using C.

The progression from Grade D to Grade A demonstrates increasing programming complexity:

Basic Array
    ↓
String Comparison
    ↓
Sorting
    ↓
Searching and Deletion
    ↓
Alternative Sorting Algorithm
    ↓
Algorithm Comparison

The project therefore demonstrates both practical programming implementation and an understanding of the underlying logic used to manipulate and organise data.

---

SUMMARY OF DEVELOPMENT

Grade| Main Development
D| Store and display eight book titles
C| Single-pass case-insensitive alphabetical comparison
B| Full alphabetical sorting using nested loops
A| Book deletion, array shifting and Bubble Sort

The final Grade A program demonstrates a complete progression from basic string-array manipulation to searching, deletion, sorting and comparison of sorting algorithms.

---

AUTHOR

Student: Foundation Computing Student
University: Solent University
Assessment: Assessment 6 – Book Organizer
Programming Language: C
