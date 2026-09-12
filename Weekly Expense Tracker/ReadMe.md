WEEKLY EXPENSE TRACKER

📌 Project Overview

The Weekly Expense Tracker is a C programming project developed as part of my Foundation Computing studies at Solent University.

The project demonstrates the progressive development of a simple expense-tracking program through four assessment grades: Grade D, Grade C, Grade B and Grade A.

The program develops from a basic fixed-value expense calculator into a more flexible system that allows users to enter spending categories, record expenses for two weeks, calculate totals and daily averages, validate inputs, compare individual categories, and provide an overall spending summary.

---

🎯 Project Objectives

The main objectives of the project were to:

- Develop a working expense-tracking program using C.
- Apply fundamental programming concepts to a practical problem.
- Calculate weekly spending totals.
- Calculate daily average spending.
- Accept and process user input.
- Validate user-entered expense values.
- Compare spending against a defined budget.
- Compare spending between two weeks.
- Compare individual spending categories.
- Produce clear and structured output.

---

📈 Project Development

The project was developed progressively through four grades.

Grade D — Basic Expense Calculation

Grade D represents the starting point of the project.

The program uses fixed values embedded directly within the code for:

- Food
- Transport
- Entertainment

It then calculates the total weekly spending.

Example:

Food:           £15000
Transport:      £8000
Entertainment:  £5000

Total Weekly Spending: £28000

Concepts demonstrated

- Variable declaration
- Integer data types
- Arithmetic calculations
- Fixed values
- "printf()" output

---

Grade C — User Input, Validation and Budget Comparison

Grade C introduces user interaction.

The user enters expenses for:

- Food
- Transport
- Entertainment

The program then:

1. Accepts user input using "scanf()".
2. Validates the entered values.
3. Rejects negative spending values.
4. Calculates total weekly spending.
5. Calculates the daily average.
6. Compares the total against a £40,000 budget.

Validation

If a negative expense is entered, the program displays:

Invalid Input! Spending cannot be negative.
Try again!

Budget comparison

The program determines whether spending is:

Within Budget

or:

Over Budget

Concepts demonstrated

- User input
- "scanf()"
- "if" / "else"
- Input validation
- Arithmetic calculations
- Floating-point calculations
- Budget comparison

Online Program

The Grade C program was also tested using the Programiz online C compiler.

"Open Grade C Program in Programiz" (https://reference-url-citation.invalid/0)

---

Grade B — Two-Week Expense Tracking

Grade B extends the Grade C program by introducing two weeks of expense data.

The user enters:

Week 1

- Food
- Transport
- Entertainment

Week 2

- Food
- Transport
- Entertainment

The program then calculates:

- Week 1 total spending
- Week 1 daily average
- Week 2 total spending
- Week 2 daily average

It also compares the two weekly totals.

The final status can be:

Your Spending INCREASED

Your Spending DECREASED

or:

Your Spending REMAINED THE SAME

Validation

Grade B retains validation to prevent negative expense values.

Concepts demonstrated

- Multiple sets of user input
- Variables
- "scanf()"
- Input validation
- "if" / "else if" / "else"
- Arithmetic calculations
- Weekly comparison
- Daily average calculation
- Structured output

Online Program

The Grade B program was tested using the Programiz online C compiler.

"Open Grade B Program in Programiz" (https://reference-url-citation.invalid/1)

---

Grade A — Dynamic Weekly Expense Tracker

Grade A represents the most developed version of the project.

Instead of limiting the program to three predefined categories, the user can choose the number of spending categories they want to track, up to a maximum of 10 categories.

The user then enters:

- The category names
- Week 1 expenses
- Week 2 expenses

The program processes the information and produces detailed reports.

Grade A Features

1. Dynamic Category Selection

The user chooses the number of categories to track.

How many spending categories do you want to track (Maximum 10):

2. Category Names

The user can create their own categories, such as:

Food
Data
Water
Gas

3. Two-Week Expense Recording

The program records spending separately for:

- Week 1
- Week 2

4. Expense Validation

The program checks for negative expense values and terminates the input process if invalid spending is entered.

5. Weekly Totals

The program calculates the total spending for each week.

6. Daily Averages

The daily average is calculated by dividing the weekly total by seven:

Daily Average = Weekly Total / 7.0

7. Category Comparison

Each category is compared between Week 1 and Week 2.

The result can be:

- Increased
- Decreased
- Stayed the Same

8. Overall Spending Comparison

The program compares the total spending for both weeks and reports whether overall spending:

- Increased
- Decreased
- Stayed the Same

---

🧠 Programming Concepts Demonstrated

Across Grades D–A, the project demonstrates the following C programming concepts:

- Standard input/output using "stdio.h"
- "printf()"
- "scanf()"
- Variables
- Integer data types
- Floating-point data types
- Character arrays
- Two-dimensional arrays
- Constants using "#define"
- Arithmetic operations
- "for" loops
- "if" statements
- "else if"
- "else"
- User input
- Input validation
- Conditional decision making
- Arrays
- Iteration
- Calculations
- Formatted output

---

🛠️ Technologies and Tools

Technology / Tool| Purpose
C| Programming language
GCC| C compiler
Visual Studio Code| Development environment
GitHub| Source-code storage and version control
Programiz Online Compiler| Online C program testing

---

📁 Project Structure

ASS1_WEEKLY EXPENSE TRACKER/
│
├── README.md
│
├── source-code/
│   ├── GRADE A.txt
│   ├── GRADE B.txt
│   ├── GRADE C.txt
│   └── GRADE D.txt
│
├── screenshots/
│   └── [Project screenshots]
│
├── test-results/
│   └── [Testing evidence]
│
└── demonstration/
    └── [Demonstration material]

The "source-code" folder contains the four stages of the assessment.

The "screenshots", "test-results" and "demonstration" folders are reserved for supporting project evidence.

---

🧪 Testing and Validation

Testing was incorporated throughout the development of the project.

Examples include:

Valid Input

The program accepts valid positive expense values and calculates the required totals and averages.

Negative Input

Negative expense values are rejected with an appropriate validation message:

Invalid Input! Spending cannot be negative.
Try again!

Budget Testing

Grade C includes a budget comparison using a defined budget of:

£40,000

The program determines whether spending is within or over the budget.

Two-Week Comparison

Grade B compares the Week 1 and Week 2 totals and reports whether spending increased, decreased or remained the same.

Category Comparison

Grade A compares individual categories between the two weeks.

Detailed screenshots and test evidence will be stored in the corresponding project folders.

---

📊 Example Grade A Scenario

A user could select four categories:

Food
Data
Water
Gas

For example:

Week 1
Food: £12000
Data: £9000
Water: £8000
Gas: £7

and:

Week 2
Food: £2000
Data: £5000
Water: £1000
Gas: £2000

The program calculates the totals and daily averages and then compares each category.

It can subsequently produce an overall result such as:

Week 1 Total : £29007
Week 2 Total : £10000

Overall Spending Decreased.

---

📸 Screenshots

Screenshots demonstrating the development and execution of the Weekly Expense Tracker will be added to the:

screenshots/

folder.

These may include program input, validation messages, calculations, reports and comparison results.

---

🧪 Test Results

Testing evidence will be added to:

test-results/

This section will document the inputs used, expected results, actual results and whether each test passed.

---

🎥 Demonstration

Demonstration material for the Weekly Expense Tracker will be added to:

demonstration/

The demonstration will show the program being executed and the main functionality of the completed system.

---

🎓 Academic Context

Assessment: Assessment 1
Project: Weekly Expense Tracker
Course: Foundation Computing
Programming Language: C
Institution: Solent University

---

💡 Learning Outcome

This project provided practical experience in developing a C program from a simple fixed-value implementation into a more flexible user-driven application.

The progression from Grade D → Grade C → Grade B → Grade A demonstrates the application of increasingly advanced programming concepts, including user input, validation, conditional logic, calculations, iteration, arrays and data comparison.

---

👨‍💻 Portfolio

This project forms part of my Foundation Computing programming portfolio and demonstrates my practical development of programming, problem-solving and computational thinking skills using C.
