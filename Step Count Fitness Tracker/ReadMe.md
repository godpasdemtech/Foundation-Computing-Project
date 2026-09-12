
STEP COUNT FITNESS TRACKER LOOP CHALLENGE

📌 Project Overview

The Step Count Fitness Tracker Loop Challenge is a C programming project developed as part of my Foundation Computing studies at Solent University.

The project demonstrates the progressive development of a fitness tracking application through four assessment grades: Grade D, Grade C, Grade B and Grade A.

The system develops from a basic one-day step calculator into a multi-day fitness tracker capable of recording different forms of activity input, calculating distance and calories, monitoring daily goal progress, applying activity-intensity factors, maintaining running totals and tracking goal-achievement streaks.

---

🎯 Project Objectives

The main objectives of the project were to:

- Develop a step-count fitness tracking application using C.
- Accept and process daily step information.
- Convert steps into kilometres.
- Estimate calories burned.
- Track activity across multiple days.
- Apply loops to repeatedly record fitness activities.
- Maintain running totals.
- Provide different methods of entering activity data.
- Allow users to set a personal daily step goal.
- Calculate progress towards the daily goal.
- Apply activity-intensity factors to calorie calculations.
- Validate user input.
- Produce daily and overall fitness summaries.
- Track consecutive days on which the daily goal is achieved.

---

📈 Project Development

The project was developed progressively through four grades.

---

Grade D — Daily Step Calculation

Grade D represents the basic foundation of the Step Count Fitness Tracker.

The program asks the user to enter the number of steps completed in one day.

The entered steps are then converted into:

- Distance walked in kilometres.
- Estimated calories burned.

Conversion Rates

The program uses the following fixed conversion rates:

1 kilometre = 1,250 steps

1,000 steps = 40 calories

Calculations

Distance:

Kilometres = Steps ÷ 1,250

Calories:

Calories = (Steps ÷ 1,000) × 40

The results are displayed to 2 decimal places.

Example

For 8,000 steps:

Distance Walked : 6.00 km
Calories Burned : 320.00 kcal

Concepts Demonstrated

- Variable declaration
- Integer data types
- Floating-point data types
- User input using "scanf()"
- Output using "printf()"
- Arithmetic calculations
- Unit conversion
- Formatted decimal output

Online Program

The Grade D program was developed/tested using the Programiz online C compiler.

"Open Grade D Program in Programiz" (https://www.programiz.com/online-compiler/6aYzo4HYEeDRP?utm_source=chatgpt.com)

---

Grade C — Multi-Day Fitness Tracking

Grade C extends the system by introducing loop-based multi-day tracking.

Instead of processing only one day's activity, the program allows the user to repeatedly enter daily step counts.

After each entry, the program calculates and displays:

- Distance for the day.
- Calories burned for the day.

The user is then asked whether another day should be added.

Add another day? (y/n):

Running Totals

The program maintains running totals for:

- Total steps.
- Total kilometres.
- Total calories.
- Number of days tracked.

When the user chooses to stop, the program produces a final fitness tracker summary.

Example

=====================================
      FITNESS TRACKER SUMMARY
=====================================
Days Tracked      : 2
Total Steps       : 15000
Total Distance    : 12.00 km
Total Calories    : 600.00 kcal

Concepts Demonstrated

- "do...while" loops
- Repeated user input
- Running totals
- Counters
- Character input
- Conditional loop control
- Arithmetic calculations
- Daily and overall summaries

Online Program

The Grade C program was developed/tested using the Programiz online C compiler.

"Open Grade C Program in Programiz" (https://www.programiz.com/online-compiler/8wjDNBapATnUG?utm_source=chatgpt.com)

---

Grade B — Multiple Activity Input Methods

Grade B further develops the fitness tracker by allowing the user to choose how activity information is entered.

Activity Menu

The user can select:

1. Steps
2. Kilometres
3. Walking Minutes

This allows activity to be entered as:

- Number of steps.
- Distance in kilometres.
- Walking duration in minutes.

Conversion Rates

The system converts all activity inputs into an equivalent step count.

1 kilometre = 1,250 steps

1 walking minute = 100 steps

1,000 steps = 40 calories

Therefore, regardless of how the user enters the activity, the program can calculate:

- Total steps.
- Total distance.
- Total calories.

Entry Tracking

The program also records how many entries were made using each method:

Steps
Kilometres
Walking Minutes

Example

A user enters:

3 kilometres
30 walking minutes

The program converts these activities into:

Total Steps        : 6750
Total Distance     : 5.40 km
Total Calories     : 270.00 kcal

The system then reports the number of entries recorded through each input method.

Concepts Demonstrated

- Menu selection
- "switch" / "case"
- "do...while" loops
- Multiple input methods
- Unit conversion
- Running totals
- Entry counters
- Conditional logic
- Input validation
- Repeated activity tracking

Online Program

The Grade B program was developed/tested using the Programiz online C compiler.

"Open Grade B Program in Programiz" (https://www.programiz.com/online-compiler/2S5FeGCOF68xw?utm_source=chatgpt.com)

---

Grade A — Advanced Fitness Tracker

Grade A represents the most developed version of the Step Count Fitness Tracker.

The program introduces a daily step goal, goal-progress tracking, activity intensity, multi-day tracking, input validation, daily summaries, overall statistics and goal-achievement streak tracking.

---

🎯 Daily Step Goal

When the program starts, the user sets a daily step goal.

For example:

Enter your daily step goal: 8000

The goal is then used to measure the user's progress on each tracked day.

---

📊 Goal Progress

After each day's activity is entered, the program calculates the percentage of the daily goal achieved.

The calculation is:

Progress = (Today's Steps ÷ Daily Goal) × 100

For example:

Today's Steps = 7,500
Daily Goal    = 8,000

Progress = (7,500 ÷ 8,000) × 100
          = 93.75%

The program then determines whether the goal was achieved.

Goal Progress       : 93.75%
Goal Not Achieved.

If the progress reaches or exceeds 100%, the program displays:

Goal Achieved!

---

🚶 Activity Intensity

Grade A introduces an activity-intensity factor that affects estimated calories burned.

The user can select:

L = Light
M = Moderate
F = Fast

The intensity is then incorporated into the calorie calculation.

Intensity Factors

- Light: 10% reduction from the base calorie estimate.
- Moderate: Base calorie estimate.
- Fast: 20% increase from the base calorie estimate.

This demonstrates how conditional logic can modify a calculated value according to user-selected activity intensity.

---

🔄 Multi-Day Tracking

The Grade A system allows fitness activity to be recorded across multiple days.

For each day, the program records:

- Steps.
- Distance.
- Calories burned.
- Goal progress.
- Goal achievement status.

The user can continue entering additional days:

Track another day? (y/n):

The program continues until the user chooses to stop.

---

🛡️ Input Validation

Grade A includes validation for the major user inputs.

The program validates:

- Daily step goal.
- Daily step count.
- Activity intensity.
- Continue/stop responses.

Invalid values cause the program to display an appropriate message and re-prompt the user until valid information is supplied.

Examples include:

Daily goal must be greater than 0.

Steps cannot be negative.

Invalid intensity! Please enter L, M or F.

This improves the reliability and usability of the program.

---

📋 Daily Summary

After each day's activity is processed, the program displays a daily activity summary containing:

- Total steps.
- Distance travelled.
- Calories burned.
- Percentage of the daily goal achieved.
- Goal achievement status.

Example:

========== DAILY SUMMARY ==========
Steps               : 7500
Distance            : 6.00 km
Calories Burned     : 300.00 kcal
Goal Progress       : 93.75%
Goal Not Achieved.

---

📊 Overall Fitness Report

When the user finishes tracking, the program displays an overall fitness report.

The report contains:

- Number of days tracked.
- Total steps across all days.
- Total distance across all days.
- Total calories burned.
- Average steps per day.
- Average distance per day.
- Average calories per day.
- Longest goal-achievement streak.

Example:

=========================================
        FITNESS TRACKER REPORT
=========================================
Days Tracked        : 1
Total Steps         : 7500
Total Distance      : 6.00 km
Total Calories      : 300.00 kcal
Average Steps       : 7500.00
Average Distance    : 6.00 km
Average Calories    : 300.00 kcal
Longest Goal Streak : 0 Day(s)

---

🔥 Goal Streak Tracking

The Grade A program tracks consecutive days on which the user meets or exceeds the daily step goal.

If:

Today's Steps >= Daily Goal

the current streak increases.

If the daily goal is not achieved, the current streak resets.

The program also records the longest streak achieved during the tracking period.

Longest Goal Streak : X Day(s)

This demonstrates the practical use of:

- Counters.
- Conditional statements.
- Loops.
- Running values.
- Comparisons.
- Historical tracking.

---

🧮 Core Calculations

The project uses several calculations throughout its development.

Distance

Kilometres = Steps ÷ 1,250

Base Calories

Calories = (Steps ÷ 1,000) × 40

Goal Progress

Progress = (Today's Steps ÷ Daily Goal) × 100

Average Steps

Average Steps = Total Steps ÷ Number of Days

Average Distance

Average Distance = Total Distance ÷ Number of Days

Average Calories

Average Calories = Total Calories ÷ Number of Days

The Grade A version additionally adjusts the calorie estimate according to activity intensity.

---

💻 Programming Concepts Demonstrated

Across Grades D–A, the project demonstrates progressive application of C programming concepts including:

- "stdio.h"
- Variables
- Integer data types
- Floating-point data types
- Character data types
- "printf()"
- "scanf()"
- Arithmetic operators
- Assignment operators
- Relational operators
- Conditional statements
- "if"
- "else"
- "else if"
- "switch"
- "case"
- "do...while" loops
- Nested loops
- Input validation
- Running totals
- Counters
- Menu-driven programming
- Unit conversion
- Percentage calculations
- Average calculations
- Multi-day data processing
- Streak tracking
- Formatted output

---

🛠️ Technologies and Tools

Technology / Tool| Purpose
C| Programming language
GCC| C compiler
Visual Studio Code| Development environment
GitHub| Source-code storage and version control
Programiz Online Compiler| Online C development and testing
Cisco Networking Academy| Additional learning resource for networking and cybersecurity

Additional Learning Resource

"Cisco Networking Academy" (https://www.netacad.com?utm_source=chatgpt.com)

---

📁 Project Structure

ASS3_STEP COUNT FITNESS TRACKER LOOP CHALLENGE/
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

Testing was carried out progressively as the program developed from Grade D to Grade A.

Grade D Testing

Testing focuses on:

- Step-count input.
- Kilometre conversion.
- Calorie calculation.
- Two-decimal output formatting.

Grade C Testing

Testing includes:

- Daily step entry.
- Multiple-day tracking.
- Continue/stop functionality.
- Running totals.
- Final summary calculations.

Grade B Testing

Testing includes:

- Steps input.
- Kilometres input.
- Walking-minutes input.
- Conversion into steps.
- Running totals.
- Entry counters.
- Invalid menu choices.
- Continue/exit functionality.

Grade A Testing

Testing includes:

- Daily goal validation.
- Daily step validation.
- Activity-intensity validation.
- Yes/no response validation.
- Goal-progress calculation.
- Daily summaries.
- Multi-day tracking.
- Calorie-intensity adjustments.
- Goal achievement.
- Goal streak tracking.
- Overall fitness reporting.

Testing evidence is organised within the project's "test-results/" folder.

---

📸 Screenshots

Authentic screenshots documenting the development and execution of the Step Count Fitness Tracker are organised by grade.

Each grade contains separate folders for:

CODE screenshots/
OUTPUT screenshots/

The CODE screenshots provide visual evidence of the program source code, while the OUTPUT screenshots demonstrate the actual results produced when the programs were executed.

---

🎥 Demonstration

Demonstration materials are organised within the:

demonstration/

folder.

The demonstrations can provide evidence of the programs running and show the progression of functionality from the basic Grade D implementation through to the more advanced Grade A fitness tracking system.

---

🎓 Academic Context

Assessment: Assessment 3
Project: Step Count Fitness Tracker Loop Challenge
Course: Foundation Computing
Programming Language: C
Institution: Solent University

---

💡 Learning Outcome

This project demonstrates the progressive development of a practical fitness tracking application using C programming.

The progression from Grade D → Grade C → Grade B → Grade A demonstrates how increasingly advanced programming techniques can be applied to the same real-world problem.

The project progresses from:

Basic calculation → Loop-based tracking → Multiple input methods → Advanced multi-day fitness tracking

Through this progression, the project demonstrates practical application of:

- Problem solving.
- Computational thinking.
- Decision making.
- Input validation.
- Repetition and loops.
- Data processing.
- Mathematical calculations.
- User interaction.
- Program structure.
- Tracking and analysing accumulated activity data.

The completed system provides a practical example of how programming can be used to transform user activity data into meaningful fitness information.
