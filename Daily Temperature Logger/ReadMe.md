
DAILY TEMPERATURE LOGGER

Project Overview

The Daily Temperature Logger is a C programming project developed as part of the Solent University Foundation Computing assessment.

The program records daily temperature readings and progressively develops from a basic temperature logger at Grade D into a more advanced application using arrays, validation, sentinel values, threshold analysis, weekly calculations and pointers at Grade A.

The project demonstrates the progressive development of programming skills and the application of core C programming concepts.

---

Project Objectives

The main objectives of the Daily Temperature Logger are to:

- Record temperature readings for multiple days.
- Store temperature data using arrays.
- Display recorded temperature readings.
- Calculate average temperatures.
- Identify the highest and lowest recorded temperatures.
- Analyse readings against a user-defined temperature threshold.
- Calculate weekly temperature averages.
- Use a sentinel value to identify the end of valid readings.
- Use pointers for data traversal and analysis.
- Reverse the temperature readings using pointer traversal.
- Provide a menu-driven interface for accessing the program's features.
- Apply input validation and control structures.
- Demonstrate progression from basic programming concepts to more advanced C programming techniques.

---

DEVELOPMENT PROGRESSION

The project was developed progressively through four assessment grades.

GRADE D
Basic temperature recording
        ↓
GRADE C
Highest and lowest temperature analysis
        ↓
GRADE B
Threshold analysis + weekly averages + sentinel
        ↓
GRADE A
Pointers + reverse traversal + relative-day labels

Each grade builds upon the functionality introduced in the previous grade.

---

GRADE D – BASIC TEMPERATURE LOGGER

Overview

Grade D establishes the basic functionality of the Daily Temperature Logger.

The program asks the user how many days they want to record, with a maximum of 30 days. Temperature readings are stored in an array.

A menu allows the user to:

1. Display all temperature readings.
2. Calculate the average temperature.
3. Exit the program.

Main Features

- Records between 1 and 30 days.
- Uses a floating-point array to store temperature readings.
- Uses a "for" loop to collect readings.
- Displays each day's temperature.
- Calculates the overall average temperature.
- Uses a "do...while" loop for the menu.
- Uses "switch" statements to process menu selections.
- Validates the number of days entered.

Program Link

Programiz Online Compiler:

https://www.programiz.com/online-compiler/6ysTUDNbcdasH

---

GRADE C – TEMPERATURE ANALYSIS

Overview

Grade C builds upon Grade D by introducing temperature analysis.

In addition to displaying readings and calculating the average, the program identifies the highest and lowest temperatures recorded.

The menu is also expanded and continues looping until the user selects the Exit option.

Main Features

- Retains Grade D functionality.
- Stores temperatures in an array.
- Displays all recorded readings.
- Calculates the average temperature.
- Finds the highest temperature.
- Finds the lowest temperature.
- Uses loops to analyse the temperature array.
- Provides a continuous menu system.
- Uses conditional statements to compare temperatures.

Temperature Analysis

The program initially assumes the first temperature is both the highest and lowest value:

highestTemperature = temperatures[0];
lowestTemperature = temperatures[0];

It then compares subsequent readings and updates the highest or lowest value when required.

Program Link

Programiz Online Compiler:

https://www.programiz.com/online-compiler/8moxeeKZqzIgs

---

GRADE B – ADVANCED TEMPERATURE ANALYSIS

Overview

Grade B extends the Grade C program by introducing additional temperature analysis and data-handling techniques.

The program introduces:

- A larger fixed-size array.
- A sentinel value.
- Temperature threshold analysis.
- Weekly temperature averages.

The menu is expanded to provide six options.

Main Features

1. Temperature Readings

The program records between 1 and 30 days of temperature data.

A fixed-size array is used:

float temperatures[50];

Although the user records a maximum of 30 days, the array provides additional storage capacity.

2. Sentinel Value

The program defines:

const float SENTINEL = -999.0;

The sentinel value is placed after the final valid temperature:

temperatures[numberOfDays] = SENTINEL;

The program can then use the sentinel to identify where valid temperature readings end.

The value "-999.0" is also prevented from being entered as a normal temperature reading.

3. Threshold Analysis

The user can enter a temperature threshold.

The program counts:

- Days above the threshold.
- Days below the threshold.

Readings equal to the threshold are not included in either count.

4. Weekly Averages

The program groups the recorded readings into seven-day periods and calculates an average for each week.

This also works when the final week contains fewer than seven days.

Grade B Menu

1. Display all temperature readings
2. Calculate average temperature
3. Find highest and lowest temperatures
4. Count days above/below a threshold
5. Calculate weekly averages
6. Exit

Program Link

Programiz Online Compiler:

https://www.programiz.com/online-compiler/7dIWZgcK8h69M

---

GRADE A – POINTERS AND REVERSE READINGS

Overview

Grade A represents the most advanced version of the Daily Temperature Logger.

The program retains the functionality developed in Grades D–B and introduces pointers for traversing and analysing the temperature array.

A new menu option also allows the user to display the temperature readings in reverse order using relative-day descriptions.

Main Features

Grade A includes:

- Temperature recording.
- Input validation.
- Array storage.
- Average temperature calculation.
- Highest and lowest temperature analysis.
- Threshold analysis.
- Weekly averages.
- Sentinel-based data traversal.
- Pointer-based array traversal.
- Pointer-based temperature analysis.
- Reverse temperature readings.
- Relative-day labels.
- Menu-driven program control.

---

Pointer Implementation

The program declares a pointer:

float *pointer;

The pointer can be assigned to the beginning of the temperature array:

pointer = temperatures;

Individual elements can then be accessed through pointer arithmetic:

*(pointer + day)

This provides an alternative method of accessing array elements.

Example

pointer = temperatures;

for(day = 0; day < numberOfDays; day++)
{
    printf("Day %d: %.2f C\n",
           day + 1,
           *(pointer + day));
}

The pointer starts at the beginning of the array and moves through the stored temperature values.

---

POINTER-BASED HIGHEST AND LOWEST ANALYSIS

Grade A also uses pointers when identifying the highest and lowest temperatures.

The pointer begins at the first temperature:

pointer = temperatures;

highestTemperature = *pointer;
lowestTemperature = *pointer;

The pointer is then advanced through the array:

pointer++;

The program continues until it reaches the sentinel value.

This demonstrates how pointers can be used to traverse an array without directly using array indexing for the analysis.

---

POINTER-BASED THRESHOLD ANALYSIS

The threshold analysis is also implemented using pointers.

The pointer starts at the first temperature:

pointer = temperatures;

The program then checks each value:

while(*pointer != SENTINEL)

The pointer moves forward after each reading:

pointer++;

This demonstrates pointer traversal while processing data stored in an array.

---

WEEKLY AVERAGES USING POINTERS

Grade A also incorporates pointer traversal into the weekly-average calculation.

The pointer is positioned at the beginning of the relevant section of the array:

pointer = temperatures + startDay;

The program then traverses the required temperature readings using the pointer.

This demonstrates how pointer arithmetic can be used to access a specific position within an array.

---

REVERSE TEMPERATURE READINGS

A new menu option was introduced in Grade A:

6. Reverse readings

The pointer begins at the final recorded temperature:

pointer = temperatures + numberOfDays - 1;

The program then moves backwards through the array using:

pointer--;

The output uses relative-day descriptions.

For example:

Today
Yesterday
2 days ago
3 days ago

This provides a more meaningful interpretation of the temperature history.

---

GRADE A MENU

The final program provides seven menu options:

1. Display all temperature readings
2. Calculate average temperature
3. Find highest and lowest temperatures
4. Count days above/below threshold
5. Calculate weekly averages
6. Reverse readings
7. Exit

---

POINTER EXPLANATION

Pointers are an important feature of C programming because they allow a program to work directly with memory addresses. In this Daily Temperature Logger, a pointer is used to traverse the temperature array and access stored values without relying entirely on array indexing. The pointer is declared as a floating-point pointer using "float *pointer".

When the pointer is assigned to the temperature array, it points to the first stored temperature. Pointer arithmetic can then be used to move through the array. For example, "*(pointer + day)" accesses the temperature at the current position. The pointer can also be incremented using "pointer++" to move to the next temperature.

Pointers are used in Grade A for displaying readings, calculating the highest and lowest temperatures, performing threshold analysis and calculating weekly averages. They are also particularly useful when reversing the readings. The pointer is positioned at the final recorded temperature and then moved backwards using "pointer--".

Using pointers demonstrates an alternative way of traversing arrays and provides practical experience with memory addresses, dereferencing and pointer arithmetic. The Grade A implementation therefore builds upon the array-based techniques used in the earlier grades and demonstrates a more advanced understanding of data manipulation in C.

---

PROGRAMMING CONCEPTS USED

The Daily Temperature Logger demonstrates a range of C programming concepts.

Variables

Variables are used to store:

- Number of days.
- Menu selections.
- Temperature values.
- Totals and averages.
- Highest and lowest temperatures.
- Threshold values.
- Weekly calculations.

Arrays

Arrays provide storage for multiple temperature readings.

Examples include:

float temperatures[30];

and:

float temperatures[50];

Loops

Several loop structures are used:

- "for"
- "while"
- "do...while"

These are used for entering readings, processing temperatures, displaying results and maintaining the menu.

Conditional Statements

"if", "else if" and "else" statements are used for:

- Input validation.
- Comparing temperatures.
- Threshold analysis.
- Sentinel checking.

Switch Statements

The "switch" statement controls the menu options.

Input Validation

The program validates the number of days to ensure it falls between 1 and 30.

Grade B and Grade A also prevent the sentinel value from being entered as a normal temperature reading.

Sentinel Values

The value:

-999.0

is used as a sentinel to mark the end of valid temperature readings.

Pointers

Grade A introduces pointer declaration, dereferencing, pointer arithmetic, forward traversal and reverse traversal.

---

TESTING AND OUTPUT

The Daily Temperature Logger was developed progressively and tested through the Programiz online C compiler.

Testing focuses on the major functions introduced at each grade, including:

- Number-of-days validation.
- Temperature input.
- Displaying temperature readings.
- Average temperature calculation.
- Highest temperature detection.
- Lowest temperature detection.
- Threshold analysis.
- Weekly averages.
- Sentinel handling.
- Pointer-based traversal.
- Reverse temperature display.
- Menu navigation and exit functionality.

Screenshots of source code and program outputs provide visual evidence of the development and testing process.

---

DEVELOPMENT TOOLS

Programming Language

C

The assessment demonstrates fundamental and intermediate C programming techniques, including arrays, loops, conditional statements, switch statements, sentinel values and pointers.

Online Compiler

Programiz Online C Compiler

The individual Programiz links are provided within each grade section.

Source Code

The source code for Grades D, C, B and A is maintained separately to demonstrate the progression of the project.

---

PROJECT STRUCTURE

The portfolio version of the assessment is organised as follows:

ASS5_DAILY TEMPERATURE LOGGER/
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

The progressive Grade D–A structure demonstrates how a basic programming solution can be extended with additional functionality and more advanced programming techniques.

The project provides practical experience with:

- Problem solving.
- Algorithm development.
- Data storage.
- Data analysis.
- Validation.
- Menu-driven applications.
- Array manipulation.
- Pointer manipulation.
- Iterative programming.
- C programming syntax and structures.

---

SUMMARY OF DEVELOPMENT

Grade| Development
D| Basic temperature recording, array storage, display and average
C| Highest and lowest temperature analysis
B| Sentinel value, threshold analysis and weekly averages
A| Pointers, pointer traversal and reverse readings

The final Grade A program combines the functionality developed throughout the assessment and demonstrates progression from basic C programming concepts to more advanced pointer-based data manipulation.

---

AUTHOR

Student: Foundation Computing Student
University: Solent University
Assessment: Assessment 5 – Daily Temperature Logger
Programming Language: C
