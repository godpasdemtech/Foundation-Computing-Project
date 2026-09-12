
MEDIA LAB EQUIPMENT LOAN MANAGER

Project Overview

The Media Lab Equipment Loan Manager is a C programming project developed as part of the Solent University Foundation Computing assessment.

The project manages equipment records for a media laboratory using structures, functions, text files, arrays, searching, updating, deleting and data persistence.

The solution progresses from a basic file-based equipment record system at Grade D to a more complete equipment management application at Grade A.

By Grade A, the program supports:

- Adding equipment.
- Viewing equipment.
- Searching for equipment.
- Updating equipment.
- Deleting equipment.
- Saving equipment records.
- Loading existing records when the program starts.
- Persistent storage using a text file.
- A menu-driven interface.

The project demonstrates the progression from basic file input/output to structured data management and persistent application state.

---

PROJECT OBJECTIVES

The main objectives of the Media Lab Equipment Loan Manager are to:

- Create an equipment record using a C structure.
- Store equipment IDs, asset tags and status information.
- Create and read a plain-text data file.
- Use functions to organise program functionality.
- Use function parameters and return values.
- Search equipment records by ID.
- Prevent duplicate equipment IDs.
- Update existing equipment records.
- Delete equipment records.
- Shift remaining records after deletion.
- Load records from a file into an in-memory array.
- Save updated records back to the file.
- Implement a menu-driven equipment management system.
- Demonstrate file persistence.
- Demonstrate local variables and global constants.
- Develop a practical understanding of structured data management in C.

---

DEVELOPMENT PROGRESSION

The assessment was developed progressively through four grades.

GRADE D
Structures + basic file storage
        ↓
GRADE C
Functions with parameters + searching + duplicate checking
        ↓
GRADE B
Return values + updating records
        ↓
GRADE A
Full equipment manager + persistence + deletion

Each grade builds upon the functionality introduced in the previous grade.

---

GRADE D – BASIC FILE-BASED EQUIPMENT MANAGER

Overview

Grade D establishes the basic equipment management system.

A structure called "Item" is created to represent an equipment record.

struct Item
{
    int id;
    char assetTag[30];
    char status;
};

Each item therefore contains:

- An integer equipment ID.
- A character array for the asset tag.
- A character representing the equipment status.

The program uses a text file called:

loans.txt

to store equipment records.

---

Adding Equipment

The "addItem()" function collects equipment information from the user and appends the record to the file.

The file is opened using:

fopen("loans.txt", "a");

The ""a"" mode allows new records to be added to the existing file.

The record is written using:

fprintf(file, "%d %s %c\n",
        item.id,
        item.assetTag,
        item.status);

---

Displaying Equipment

The "displayItems()" function opens the file for reading:

fopen("loans.txt", "r");

It then reads records using "fscanf()" and displays them in a formatted table.

The program continues reading while three values are successfully obtained from each record.

---

Grade D Functions

The Grade D program uses two no-parameter functions:

addItem()
displayItems()

These functions handle their own input, output and file operations.

---

Program Link

Programiz Online Compiler:

https://www.programiz.com/online-compiler/1cfGUV466gl57

---

GRADE C – FUNCTIONS, SEARCHING AND DUPLICATE CHECKING

Overview

Grade C refactors the program so that functions receive information through parameters.

The "addItem()" function becomes:

void addItem(int id, char assetTag[], char status[])

This allows the main program to collect the input and pass the values to the function.

The "displayItems()" function remains parameterless because it reads and displays the contents of the file itself.

---

SEARCHING BY EQUIPMENT ID

Grade C introduces:

int searchItemById(int id)

The function opens "loans.txt", reads the equipment records and checks each ID.

If the requested ID is found, the function returns:

1

If the ID cannot be found, it returns:

0

This provides a reusable method for checking whether an equipment record exists.

---

DUPLICATE ID CHECKING

Before adding an equipment record, the program calls:

searchItemById(id)

If the ID already exists, the program displays:

Error: ID already exists.

The record is therefore not appended to the file.

This prevents duplicate equipment IDs.

---

GRADE C FUNCTION STRUCTURE

The main functions are:

addItem()
searchItemById()
displayItems()

The introduction of parameters makes the functions more reusable than the Grade D implementation.

---

Program Link

Programiz Online Compiler:

https://www.programiz.com/online-compiler/1cfGUV466gl57

---

GRADE B – SEARCH, RETURN VALUES AND UPDATE FUNCTIONALITY

Overview

Grade B extends Grade C by making the functions return meaningful results.

The "searchItemById()" function now returns the position of the matching record rather than simply returning "1" or "0".

For example:

0 → first record
1 → second record
2 → third record

If the item is not found:

-1

is returned.

---

ADD ITEM RETURN VALUE

The Grade B "addItem()" function now returns an integer.

int addItem(int id, char assetTag[], char status[])

The function returns:

1 → item successfully added
0 → item not added

This allows the main program to determine whether the operation was successful.

---

UPDATE FUNCTION

Grade B introduces:

int updateItem(int id,
               const char newAssetTag[],
               const char newStatus[])

The function performs the following process:

Open loans.txt
       ↓
Load records into an array
       ↓
Search for the requested ID
       ↓
Update the matching record
       ↓
Open the file for writing
       ↓
Rewrite all records

This provides a practical method of modifying an existing file-based record.

---

UPDATING THE FILE

The program first loads the records into:

struct Item items[MAX_ITEMS];

After finding the matching equipment ID, the relevant asset tag and status are changed.

The complete file is then rewritten using:

fopen("loans.txt", "w");

The updated records are written back to the file.

---

GRADE B TESTING

The main program tests:

1. Adding three equipment records.
2. Displaying the equipment.
3. Searching for an ID.
4. Updating an equipment record.
5. Displaying the updated equipment list.

---

Program Link

Programiz Online Compiler:

https://www.programiz.com/online-compiler/8Lq9uiwvASs0Y

---

GRADE A – COMPLETE MEDIA LAB LOAN MANAGER

Overview

Grade A represents the most advanced version of the project.

The program introduces a complete menu-driven equipment management system with in-memory data management and file persistence.

The program loads existing records when it starts and allows the user to manage the records before saving them back to the file.

---

GLOBAL CONSTANTS

Grade A introduces two global constants:

#define MAX_ITEMS 100
#define FILENAME "loans.txt"

"MAX_ITEMS" defines the maximum number of equipment records that can be stored in the in-memory array.

"FILENAME" provides a single named reference to the data file.

Using constants avoids repeatedly writing the same values throughout the program.

---

LOADING DATA FROM FILE

The program introduces:

int loadItems(struct Item items[])

When the program starts, it attempts to open "loans.txt".

Existing records are loaded into the "items" array.

The function returns the number of records loaded.

Conceptually:

Program starts
      ↓
Open loans.txt
      ↓
Read existing records
      ↓
Store records in array
      ↓
Return record count
      ↓
Display menu

This allows existing data to remain available between program runs.

---

SAVING DATA TO FILE

Grade A introduces:

void saveItems(struct Item items[], int count)

The function opens the file using write mode and writes the current records from memory back into "loans.txt".

This provides file persistence.

The program saves the data when the user selects:

6. Save Data

It also automatically saves the current data when the user chooses:

7. Exit

---

ADD EQUIPMENT

The "addItem()" function now works with the in-memory array.

int addItem(struct Item items[], int *count,
            int id, char assetTag[], char status[])

The function checks whether the ID already exists.

It also checks whether the maximum capacity has been reached.

If the ID is unique and there is available space, the new record is stored in the array.

The record count is then increased.

---

VIEW EQUIPMENT

The "displayItems()" function receives the array and the number of active records:

void displayItems(struct Item items[], int count)

It then displays the equipment records in a formatted table.

If there are no records, the program reports:

No equipment records found.

---

SEARCH EQUIPMENT

The Grade A search function is:

int searchItemById(struct Item items[], int count, int id)

The function searches the in-memory array.

If the equipment is found, it returns its array position.

If it cannot be found, it returns:

-1

The main program can then use the returned position to display the matching record.

---

UPDATE EQUIPMENT

The Grade A update function is:

int updateItem(struct Item items[], int count,
               int id, const char newAssetTag[],
               const char newStatus[])

The function searches for the equipment ID.

If the record exists, the asset tag and status are updated directly in the in-memory array.

If the record does not exist, the function returns "0".

---

DELETE EQUIPMENT

Grade A introduces:

int deleteItem(struct Item items[], int *count, int id)

The function first searches for the requested equipment ID.

If the record is found, the remaining records are shifted one position to the left.

for(i = position; i < *count - 1; i++)
{
    items[i] = items[i + 1];
}

The number of active records is then reduced:

(*count)--;

This removes the equipment record without leaving an empty gap in the array.

---

GRADE A MENU

The final program provides seven menu options:

1. Add Equipment
2. View Equipment
3. Search Equipment
4. Update Equipment
5. Delete Equipment
6. Save Data
7. Exit

The menu is controlled by a "do...while" loop and continues until the user selects Exit.

---

COMPLETE PROGRAM FLOW

The Grade A application follows this general workflow:

START
  ↓
Load records from loans.txt
  ↓
Display main menu
  ↓
┌──────────────────────┐
│ 1. Add Equipment     │
│ 2. View Equipment    │
│ 3. Search Equipment  │
│ 4. Update Equipment  │
│ 5. Delete Equipment  │
│ 6. Save Data         │
│ 7. Exit              │
└──────────────────────┘
  ↓
Perform selected operation
  ↓
Return to menu
  ↓
Save on Exit
  ↓
END

This creates a more complete equipment management application compared with the earlier grades.

---

FILE PERSISTENCE

File persistence means that the program's data can remain available after the program closes.

In Grade A:

loans.txt

acts as the persistent storage location.

The application uses two stages of data handling:

In-Memory Data

Records are temporarily stored in:

struct Item items[MAX_ITEMS];

Persistent Data

Records are permanently stored between program runs in:

loans.txt

The relationship can be represented as:

loans.txt
    ↕
loadItems() / saveItems()
    ↕
items[MAX_ITEMS]
    ↕
Add / Search / Update / Delete

---

LOCAL AND GLOBAL SCOPE

The Grade A implementation uses a small number of global constants while keeping operational variables local to functions.

The global constants are:

#define MAX_ITEMS 100
#define FILENAME "loans.txt"

These values are required in several parts of the program, so defining them once makes the program easier to maintain.

Most working variables, however, are declared locally inside functions.

For example, variables such as:

file
count
position
i
choice
id
result

are used only where they are required.

Local scope is useful because it limits where variables can be accessed and reduces the possibility of accidental changes from other parts of the program.

The implementation therefore keeps the global scope small while using local variables for individual function operations. This improves organisation, readability and maintainability.

---

PROGRAMMING CONCEPTS USED

The Media Lab Equipment Loan Manager demonstrates several important C programming concepts.

Structures

The "struct Item" structure groups related equipment information:

struct Item
{
    int id;
    char assetTag[30];
    char status;
};

This allows an equipment record to be treated as a single structured object.

---

Functions

The project uses multiple functions, including:

loadItems()
saveItems()
addItem()
displayItems()
searchItemById()
updateItem()
deleteItem()

This separates the program into manageable components.

---

Function Parameters

Functions receive information through parameters.

For example:

int searchItemById(struct Item items[], int count, int id)

This makes the function reusable with different arrays, record counts and IDs.

---

Return Values

Functions return values to communicate the result of an operation.

For example:

1  → successful operation
0  → unsuccessful operation
-1 → item not found

This allows the main program to respond appropriately.

---

Arrays

The Grade A program uses:

struct Item items[MAX_ITEMS];

to hold equipment records in memory.

---

File Handling

The project uses C file-handling functions including:

- "fopen()"
- "fscanf()"
- "fprintf()"
- "fclose()"

These allow equipment records to be stored and retrieved from "loans.txt".

---

Searching

Equipment is searched by its unique ID.

The search function returns the position of the matching record.

---

Updating

Existing records can be modified by changing their asset tag and status.

---

Deletion

Records are removed from the in-memory array by shifting subsequent records to the left.

---

Menu-Driven Programming

The Grade A application uses a menu controlled by a "do...while" loop.

This allows users to repeatedly perform different equipment-management operations.

---

CRUD FUNCTIONALITY

The Grade A system demonstrates the core CRUD operations:

CRUD Operation| Program Function
Create| "addItem()"
Read| "displayItems()" / "searchItemById()"
Update| "updateItem()"
Delete| "deleteItem()"

The addition of "saveItems()" and "loadItems()" provides persistent storage for these operations.

---

TESTING AND OUTPUT

The Media Lab Equipment Loan Manager was developed progressively and tested through the Programiz online C compiler.

Testing focuses on the functionality introduced at each grade.

Grade D Testing

Testing includes:

- Creating equipment records.
- Writing records to "loans.txt".
- Reading records from the file.
- Displaying equipment information.
- Handling file-opening errors.

Grade C Testing

Testing includes:

- Passing equipment details through function parameters.
- Searching for equipment IDs.
- Detecting duplicate IDs.
- Preventing duplicate records.
- Displaying equipment records.

Grade B Testing

Testing includes:

- Adding equipment.
- Searching for an ID and returning its position.
- Updating an existing equipment record.
- Rewriting the file after an update.
- Displaying the updated equipment list.

Grade A Testing

Testing includes:

- Loading existing records.
- Adding equipment.
- Viewing equipment.
- Searching equipment.
- Updating equipment.
- Deleting equipment.
- Saving data.
- Exiting while saving the current records.
- Handling invalid menu selections.
- Handling records that cannot be found.

Screenshots of the source code and program outputs provide visual evidence of the development and testing process.

---

DEVELOPMENT TOOLS

Programming Language

C

The assessment demonstrates structures, functions, arrays, strings, file handling, searching, updating, deletion and persistent data management.

Online Compiler

Programiz Online C Compiler

Individual Programiz links are provided for the assessment grades.

Data File

loans.txt

The text file is used to store equipment records.

---

PROGRAMIZ LINKS

Grade| Program
Grade D| https://www.programiz.com/online-compiler/1cfGUV466gl57
Grade C| https://www.programiz.com/online-compiler/1cfGUV466gl57
Grade B| https://www.programiz.com/online-compiler/8Lq9uiwvASs0Y
Grade A| https://www.programiz.com/online-compiler/2Uz5DGRk1ZPH7

«Note: The supplied Grade C link is the same Programiz link provided for Grade D. It has therefore been reproduced exactly rather than inventing a different link.»

---

PROJECT STRUCTURE

The portfolio version of Assessment 7 is organised as follows:

ASS7_MEDIA LAB EQUIPMENT LOAN MANAGER/
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

Assessment 7 provides practical experience in developing a structured data-management application using the C programming language.

The progression demonstrates increasing programming complexity:

Structure
   ↓
File Input/Output
   ↓
Functions
   ↓
Parameters and Return Values
   ↓
Searching
   ↓
Updating
   ↓
Deletion
   ↓
Arrays and In-Memory Data
   ↓
Persistent Storage
   ↓
Complete Menu-Driven Application

The final Grade A implementation brings these concepts together into a practical Media Lab Equipment Loan Manager.

---

SUMMARY OF DEVELOPMENT

Grade| Main Development
D| Structure, text-file storage, adding and displaying equipment
C| Function parameters, searching and duplicate-ID checking
B| Return values, record-position searching and updating
A| Loading, saving, adding, viewing, searching, updating, deleting and persistent menu-driven management

The final Grade A application demonstrates a significant progression from basic file handling to a complete structured equipment-management system.

---

AUTHOR

Student: Foundation Computing Student
University: Solent University
Assessment: Assessment 7 – Media Lab Equipment Loan Manager
Programming Language: C
