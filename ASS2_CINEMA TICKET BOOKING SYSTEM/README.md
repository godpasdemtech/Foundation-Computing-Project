ASS2 — CINEMA TICKET BOOKING SYSTEM

📌 Project Overview

The Cinema Ticket Booking System is a C programming project developed as part of my Foundation Computing studies at Solent University.

The project demonstrates the progressive development of a cinema ticket booking application through four assessment grades: Grade D, Grade C, Grade B and Grade A.

The program develops from a basic fixed-value ticket pricing system into an interactive booking system that accepts user input, validates information, calculates ticket costs, applies group discounts, adds optional snack combinations, and provides a repeating menu with ticket-price information.

---

🎯 Project Objectives

The main objectives of the project were to:

- Develop a cinema ticket booking system using C.
- Apply programming concepts to a practical booking scenario.
- Determine ticket prices based on movie and ticket types.
- Accept movie, ticket and quantity information from the user.
- Validate user input.
- Calculate the total cost of tickets.
- Apply a group discount when the required ticket quantity is reached.
- Allow users to add an optional snack combination.
- Calculate the final booking cost.
- Provide a ticket-price table.
- Develop a repeating menu-driven system.

---

📈 Project Development

The project was developed progressively through four grades.

Grade D — Basic Ticket Pricing

Grade D represents the starting point of the Cinema Ticket Booking System.

The program uses fixed values rather than asking the user for input.

The variables include:

- "movieType"
- "ticketType"
- "ticketPrice"

A "switch" statement is used to determine the ticket price based on the selected movie type, while conditional logic determines whether the ticket is a Standard or Premium seat.

Movie Types

- Action
- Comedy
- Horror

Ticket Types

- Standard Seat
- Premium Seat

Ticket Pricing

Movie Type| Standard Seat| Premium Seat
Action| £10.00| £15.00
Comedy| £8.00| £13.00
Horror| £9.00| £14.00

Example Output

Movie Type  : Action
Ticket Type : Standard Seat
Ticket Price: £10.00

Concepts demonstrated

- Variable declaration
- Character data types
- Floating-point values
- Fixed values
- "switch" / "case"
- "if" / "else"
- "printf()" output
- Basic decision making

Online Program

The Grade D program was developed/tested using the Programiz online C compiler.

"Open Grade D Program in Programiz" (https://reference-url-citation.invalid/0)

---

Grade C — User Input and Ticket Cost Calculation

Grade C introduces user interaction into the system.

The user is asked to enter:

- Movie type
- Ticket type
- Number of tickets

The program then determines the appropriate ticket price and calculates the total movie cost.

Input Validation

The program validates the number of tickets.

If the user enters zero or a negative number, the program displays:

Invalid number of tickets!

The program also validates the selected movie type and ticket type.

Cost Calculation

The total movie cost is calculated using:

Total Cost = Ticket Price × Number of Tickets

Example

For four Comedy Premium tickets:

Movie Type: Comedy
Ticket Type: Premium Seat
Number of Tickets: 4
Total Movie Cost: £52.00

Concepts demonstrated

- User input using "scanf()"
- Character input
- Integer input
- Input validation
- "switch" / "case"
- Conditional statements
- Arithmetic calculations
- Floating-point calculations
- Formatted output

Online Program

The Grade C program was debugged and tested using the Programiz online C compiler.

"Open Grade C Program in Programiz" (https://reference-url-citation.invalid/1)

---

Grade B — Discounts and Snack Combos

Grade B extends the Cinema Ticket Booking System by introducing additional booking features.

The system continues to calculate ticket costs while adding:

- Group discounts
- Optional snack combinations
- Additional validation

🎟️ Group Discount

If the customer purchases more than 6 tickets, a 10% discount is applied.

If Number of Tickets > 6
Discount = 10% of Total Before Discount

🍿 Snack Combo

The user is asked:

Need a Snack Combo? (y/n):

The snack combination costs:

£5.50 per ticket

If the customer selects "y" or "Y", the snack cost is calculated based on the number of tickets.

🧮 Final Total

The final booking cost is calculated as:

Final Total = Total Before Discount - Discount + Snack Cost

Example Scenario

For seven Horror Standard tickets with snack combinations:

Movie Type            : Horror
Ticket Type           : Standard Seat
Number of Tickets     : 7
Total Before Discount : £63.00
10% Discount          : £6.30
Snack Combo Cost      : £38.50
Final Total           : £95.20

Validation

Grade B validates:

- Movie type
- Ticket type
- Ticket quantity
- Snack-combo decision

Concepts demonstrated

- User input
- Validation
- Nested conditional logic
- "switch" statements
- "if" / "else if" / "else"
- Group discount calculation
- Optional purchase logic
- Arithmetic calculations
- Character comparison
- Case-insensitive input handling
- Formatted output

Online Program

The Grade B program was tested using the Programiz online C compiler.

"Open Grade B Program in Programiz" (https://reference-url-citation.invalid/2)

---

Grade A — Menu-Driven Cinema Booking System

Grade A represents the most developed version of the Cinema Ticket Booking System.

The program introduces a repeating menu that allows the user to select different system functions.

🎬 Main Menu

The system provides three options:

=========================================
      CINEMA TICKET BOOKING SYSTEM
=========================================
1. Book Tickets
2. View Ticket Prices
3. Exit
-----------------------------------------
Enter Choice:

Option 1 — Book Tickets

The user can:

- Select a movie type.
- Select a ticket type.
- Enter the number of tickets.
- Choose whether to add a snack combo.
- Receive a complete booking summary.

The system calculates:

- Ticket price
- Total before discount
- Group discount
- Snack-combo cost
- Final total

Option 2 — View Ticket Prices

The user can view the available ticket prices without making a booking.

=========== TICKET PRICE TABLE ===========
------------------------------------------
MovieType      StandardSeat     PremiumSeat
------------------------------------------
Action            £10.00          £15.00
Comedy            £8.00           £13.00
Horror            £9.00           £14.00

Option 3 — Exit

The system displays a closing message and terminates the menu loop.

Thank you for using the Cinema Ticket
Booking System.
Goodbye!

---

🔄 Repeating Menu

The Grade A program uses a "do...while" loop to keep the main menu running.

The menu continues to appear after completing an action and only exits when the user selects:

3. Exit

This provides a more interactive, menu-driven user experience.

---

🛡️ Validation

Grade A is designed to validate:

- Menu choice
- Movie type
- Ticket type
- Ticket quantity
- Snack choice

The program provides appropriate error messages when invalid information is entered.

---

🧮 Booking Calculations

The booking system calculates:

Total Before Discount = Ticket Price × Number of Tickets

When more than six tickets are purchased:

Discount = Total Before Discount × 10%

For customers selecting a snack combo:

Snack Cost = Number of Tickets × £5.50

The final booking cost is:

Final Total = Total Before Discount - Discount + Snack Cost

---

📋 Programming Concepts Demonstrated

Across Grades D–A, this project demonstrates:

- "stdio.h"
- Variables
- Character data types
- Integer data types
- Floating-point data types
- User input using "scanf()"
- Output using "printf()"
- "switch" statements
- "case" statements
- "if" statements
- "else if"
- "else"
- "do...while" loops
- Menu-driven programming
- Input validation
- Arithmetic operations
- Conditional calculations
- Repeating program execution
- Formatted output
- Case-insensitive character handling

---

🛠️ Technologies and Tools

Technology / Tool| Purpose
C| Programming language
GCC| C compiler
Visual Studio Code| Development environment
GitHub| Source-code storage and version control
Programiz Online Compiler| Online C program development/testing

---

📁 Project Structure

ASS2_CINEMA TICKET BOOKING SYSTEM/
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
│   ├── GRADE A/
│   │   ├── CODE screenshots/
│   │   └── OUTPUT screenshots/
│   │
│   ├── GRADE B/
│   │   ├── CODE screenshots/
│   │   └── OUTPUT screenshots/
│   │
│   ├── GRADE C/
│   │   ├── CODE screenshots/
│   │   └── OUTPUT screenshots/
│   │
│   └── GRADE D/
│       ├── CODE screenshots/
│       └── OUTPUT screenshots/
│
├── test-results/
│
└── demonstration/

---

🧪 Testing and Validation

Testing forms an important part of the development of the Cinema Ticket Booking System.

The programs were tested using valid and invalid input scenarios appropriate to each grade.

Grade D Testing

Testing focuses on:

- Fixed movie type
- Fixed ticket type
- Correct ticket-price selection
- Correct two-decimal currency output

Grade C Testing

Testing includes:

- Valid movie types
- Valid ticket types
- Valid ticket quantities
- Zero ticket quantity
- Invalid movie types
- Correct total-cost calculations

Grade B Testing

Testing includes:

- Valid booking information
- Invalid movie type
- Invalid ticket type
- Invalid ticket quantity
- Invalid snack choice
- Group discount calculation
- Snack-combo calculation
- Final booking total

Grade A Testing

Testing includes:

- Valid menu choices
- Invalid menu choices
- Ticket booking
- Ticket-price table
- Exit option
- Movie-type validation
- Ticket-type validation
- Ticket-quantity validation
- Snack-choice validation
- Group discount
- Snack-combo calculation
- Final booking total
- Repeating menu behaviour

Actual testing evidence is organised within the project's "test-results/" section.

---

📸 Screenshots

Screenshots documenting the development and execution of the Cinema Ticket Booking System are organised by grade.

Each grade contains separate folders for:

CODE screenshots/
OUTPUT screenshots/

This provides visual evidence of both the source-code development and the resulting program output.

---

🎥 Demonstration

Demonstration material for the completed Cinema Ticket Booking System will be organised within the:

demonstration/

folder.

The demonstration can show the main menu, ticket booking process, ticket-price table, validation, discount calculation, snack-combo calculation and final booking summary.

---

🎓 Academic Context

Assessment: Assessment 2
Project: Cinema Ticket Booking System
Course: Foundation Computing
Programming Language: C
Institution: Solent University

---

💡 Learning Outcome

This project demonstrates the progression from a simple fixed-value ticket pricing program to an interactive menu-driven booking system.

The progression from Grade D → Grade C → Grade B → Grade A demonstrates the application of increasingly developed programming concepts, including:

- Decision making
- User input
- Validation
- Calculations
- Conditional logic
- "switch" statements
- Repetition using "do...while"
- Menu-driven programming
- Multiple booking options

The project provides practical experience in translating a real-world cinema booking scenario into a working C program.

---

👨‍💻 Portfolio

This project forms part of my Foundation Computing programming portfolio and demonstrates my practical development of programming, problem-solving and computational thinking skills using C.
