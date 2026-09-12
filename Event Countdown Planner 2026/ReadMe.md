
EVENT COUNTDOWN PLANNER 2026

📌 Project Overview

The Event Countdown Planner 2026 is a C programming project developed as part of the Solent University Foundation Computing assessment.

The program progressively develops from Grade D to Grade A, with each grade introducing additional programming concepts and functionality.

The project focuses on:

- Date calculations
- Arrays
- Loops
- Conditional statements
- Switch/case statements
- Input validation
- Modular arithmetic
- String handling
- Event management
- Menu-driven programming
- Event navigation

The program is designed around the year 2026 and calculates the approximate or calendar-based number of days remaining until an event.

---

🎯 Project Objectives

The main objectives of this assessment were to:

1. Develop a C program that calculates the number of days remaining until an event.
2. Work with dates and months in 2026.
3. Apply conditional statements and switch/case statements.
4. Use arrays to store month lengths and weekday names.
5. Implement loops for date calculations and repeated user interaction.
6. Validate user input.
7. Determine event status based on the number of days remaining.
8. Calculate the weekday on which an event occurs.
9. Progress from a basic single-event program to a multi-event planner.
10. Develop a menu-driven event management system.

---

📈 Development Progression: Grade D → Grade A

The assessment demonstrates a progressive development of the same programming concept.

Grade| Main Development
Grade D| Basic date input and approximate countdown using 30-day months
Grade C| Real month lengths, date validation and event status
Grade B| Weekday calculation using modular arithmetic
Grade A| Multiple events, event navigation, validation and event management menu

---

🟢 GRADE D — Basic Event Countdown

Overview

The Grade D program provides a basic event countdown system.

The user enters:

- Current day
- Current month
- Event day
- Event month

The program then calculates the approximate number of days remaining.

Key Features

- Declares variables for current and event dates.
- Accepts user input.
- Assumes every month contains 30 days.
- Converts dates into approximate day numbers.
- Calculates the number of days remaining.
- Detects when the event date has already passed.
- Displays the countdown result.

Date Calculation

The program uses:

Current Date = ((Current Month - 1) × 30) + Current Day

Event Date = ((Event Month - 1) × 30) + Event Day

The remaining days are calculated using:

Days Remaining = Event Date - Current Date

Example Output

======== SOL ASSESSMENT 4 ========
=== EVENT COUNTDOWN PLANNER 2026 ===

======= GRADE D =======

Enter Current Day: 10
Enter Current Month: 3
Enter Event Day: 25
Enter Event Month: 4

Approximate Days Until Event: 45 days

If the event has already passed:

Error: Event date has already passed.

Program

"Programiz — Grade D" (https://www.programiz.com/online-compiler/7oGP4VTsnE5vM)

---

🟡 GRADE C — Date Validation and Event Status

Overview

Grade C improves the countdown system by replacing the fixed 30-day-month assumption with the actual number of days in each month of 2026.

The program uses an array containing the number of days in each month:

int daysInMonth[12] =
{
    31,28,31,30,
    31,30,31,31,
    30,31,30,31
};

Key Features

- Uses the actual number of days in each month.
- Validates current month.
- Validates event month.
- Validates current day.
- Validates event day according to the selected month.
- Converts dates into their day number within the year.
- Calculates days remaining.
- Determines event status.

Event Status

The program identifies events as:

- Today
- Coming Soon
- Later in the Year
- Already Passed

The status is determined from the calculated number of days remaining.

Date Conversion

The program uses a "for" loop to add the number of days in previous months before adding the selected day.

This allows dates to be converted into their position within the year.

Example Output

=====================================
EVENT SUMMARY
=====================================
Days Remaining : ...
Status         : Coming Soon

Program

"Programiz — Grade C" (https://www.programiz.com/online-compiler/5gyGwzLZluiwR)

---

🔵 GRADE B — Event Weekday Calculation

Overview

Grade B extends the program by calculating the weekday of the event.

The program uses the fact that:

1 January 2026 = Thursday

It then uses modular arithmetic to determine the weekday corresponding to the event's position within the year.

Key Features

- Calculates the event's day number within the year.
- Uses the known weekday of 1 January 2026.
- Applies modular arithmetic using "% 7".
- Uses an array of weekday names.
- Displays the event weekday.
- Retains the Grade C date validation and event-status functionality.

Weekday Array

The program stores the weekday names:

Monday
Tuesday
Wednesday
Thursday
Friday
Saturday
Sunday

The calculated weekday index is then used to retrieve the corresponding weekday.

Portfolio Explanation

The program first converts the event date into its day number within the year by adding the days in all previous months and then adding the event day.

Since 1 January 2026 is Thursday, modular arithmetic using "% 7" and an offset is used to determine the weekday. The resulting index is then used to retrieve the correct weekday name from the weekday array.

Example

For:

Current Date: 10/03/2026
Event Date:   25/12/2026

The program produces a countdown and identifies the weekday of the event.

Program

"Programiz — Grade B" (https://www.programiz.com/online-compiler/16V9xbp1IoX2z)

---

🔴 GRADE A — Event Countdown Planner

Overview

Grade A significantly expands the project into a more complete Event Countdown Planner.

Instead of working with only one event, the program can store multiple events and provides a menu for navigating between them.

The program supports up to 10 events.

Key Features

1. Number of Events Validation

The user is asked:

How many events would you like to enter (1 - 10)?

The program ensures that the number entered is between 1 and 10.

---

2. Event Details

For each event, the user enters:

- Event name
- Event month
- Event day

The program validates the event date according to the selected month.

---

3. Current Date Validation

The program asks the user to enter the current:

- Month
- Day

Both values are validated using the "daysInMonth" array.

---

4. Days Remaining

The program calculates the number of days remaining between the current date and the selected event date.

---

5. Weekday

The program calculates the weekday of the event using the event's day number and modular arithmetic.

---

6. Event Status

The program identifies the event as:

- Already Passed
- Event is Today
- Urgent Event — within 7 days
- Later in the Year

---

7. Event Navigation

The menu allows the user to:

1. View Next Event
2. View Previous Event
3. Add Another Event
4. Exit

This allows the user to navigate through stored events.

---

8. Previous Event Protection

The program prevents the user from moving backwards when already viewing the first event.

It displays:

You are already viewing the first event.

---

9. Next Event Protection

The program prevents the user from moving forward when already viewing the last stored event.

It displays:

You are already viewing the last event.

---

10. Add Another Event

The user can add another event through the event menu.

The program checks whether the maximum number of events has already been reached.

If 10 events have already been stored, the program prevents additional events from being added.

---

11. Exit

The user can select option 4 to exit the planner.

The program displays a closing message:

Thank You For Using
EVENT COUNTDOWN PLANNER 2026

---

🧠 Programming Concepts Demonstrated

Across Grades D–A, the project demonstrates several C programming concepts.

Variables

The programs use variables to store:

- Days
- Months
- Dates
- Number of events
- Menu choices
- Days remaining
- Weekday indexes

Input and Output

The project uses:

printf()
scanf()

to communicate with the user.

Conditional Statements

The programs use:

if
else if
else

to determine:

- Valid and invalid dates
- Event status
- Days remaining
- Menu behaviour

Switch/Case

Switch statements are used for menu navigation and program decision-making.

Arrays

The project uses arrays to store:

- Number of days in each month
- Weekday names
- Event names
- Event days
- Event months

Loops

Different loops are used throughout the project, including:

for
do...while

These are used for:

- Calculating day numbers
- Repeating input until valid
- Processing multiple events
- Repeating the event navigation menu

Modular Arithmetic

Grade B and Grade A use:

% 7

to determine the weekday of an event.

String Handling

Grade A uses character arrays to store event names:

char eventName[10][50];

This allows multiple event names to be stored.

Input Validation

Validation is progressively improved throughout the grades.

The programs validate:

- Months
- Days
- Number of events
- Menu choices
- Event information

---

🧪 Testing and Validation

Testing was carried out using different inputs to verify the behaviour of the programs.

Examples include:

Valid Date

Current Day: 10
Current Month: 3

Event Day: 25
Event Month: 4

The program calculates the countdown.

Event Already Passed

Current Day: 20
Current Month: 7

Event Day: 5
Event Month: 6

The program identifies that the event has already passed.

Date Validation

The program checks whether:

- A month is between 1 and 12.
- A day is valid for the selected month.

Grade A Navigation Testing

Testing also covers:

- Moving to the next event.
- Moving to the previous event.
- Attempting to move beyond the first event.
- Attempting to move beyond the last event.
- Adding another event.
- Reaching the maximum of 10 events.
- Exiting the program.

---

🛠️ Development Tools

The project was developed and tested using:

- C Programming Language
- Programiz Online C Compiler
- Visual Studio Code
- GCC Compiler
- GitHub

Programiz was used to write, execute and test the individual assessment programs.

---

🌐 Additional Learning Resource

Cisco Networking Academy was also identified as a useful learning resource for developing future knowledge in networking and cybersecurity.

Cisco Networking Academy (NetAcad):

https://www.netacad.com/

This resource is relevant to the wider learning roadmap because it provides training and learning materials related to networking, cybersecurity and other technology areas.

---

📁 Project Structure

The Assessment 4 folder is organised to keep the source code and supporting evidence clearly separated.

ASS4_EVENT COUNTDOWN PLANNER 2026/
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
│   └── ...
│
└── demonstration/
    └── ...

The screenshot folders contain the authentic visual evidence for each grade, with separate sections for code screenshots and output screenshots.

---

📚 Assessment Learning Progression

Assessment 4 demonstrates a clear progression in programming ability:

GRADE D
Basic Date Calculation
        ↓
GRADE C
Date Validation + Event Status
        ↓
GRADE B
Weekday Calculation
        ↓
GRADE A
Multiple Events + Navigation + Menu

This progression demonstrates how a simple date-calculation program can be developed into a more structured event-planning application using increasingly advanced programming concepts.

---

🎓 Academic Context

This project forms part of the Solent University Foundation Computing coursework.

The assessment demonstrates the practical application of C programming concepts including:

- Variables
- Input/output
- Conditional logic
- Switch statements
- Arrays
- Loops
- Validation
- Modular arithmetic
- String handling
- Menu-driven programming

The progression from Grade D through Grade A demonstrates the development of increasingly complex functionality while maintaining a consistent project theme and output presentation.

---

👨‍💻 Author

Solent University — Foundation Computing

Assessment 4: Event Countdown Planner 2026

Programming Language: C

Academic Year: 2025/
