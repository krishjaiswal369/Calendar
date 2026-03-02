# C Yearly Calendar Generator

A lightweight, terminal-based **Gregorian Calendar** application written in C. This program allows users to input any year and generates a fully formatted 12-month calendar, accounting for leap years and correct weekday alignments.

## 🚀 Features

* **Dynamic Year Input:** Generate a calendar for any year (AD).
* **Leap Year Logic:** Accurately calculates February's length (29 days) based on the Gregorian rules (divisible by 400 or divisible by 4 but not 100).
* **Precision Alignment:** Uses a mathematical algorithm to determine the exact starting weekday of each month.
* **Clean CLI Output:** Displays months in a structured grid format for easy readability.

## 🛠️ How It Works

The core of the program relies on three main components:

1. **dayNumber()**: Implements a variation of Zeller’s Congruence to find the day of the week for January 1st of the chosen year.
2. **numberOfDays()**: A helper function that returns the total days in a month, including the logic for leap years.
3. **printCalendar()**: The rendering engine that calculates the necessary padding (spaces) for the first week of each month and prints the dates in a 7-column grid.

## 💻 Usage

### Compilation

Use any standard C compiler (like `gcc`) to compile the source code:

```bash
gcc calendar.c -o calendar

```

### Running the Program

```bash
./calendar

```

Upon execution, the program will prompt you to enter a year (e.g., `2024`), and it will output the full 12-month calendar to the terminal.

## 📋 Example Output

```text
     Calendar - 2024

 ------------January-------------
  Sun  Mon  Tue  Wed  Thu  Fri   Sat
         1    2    3    4    5     6
    7    8    9   10   11   12    13
   14   15   16   17   18   19    20
   ...

```

---

Would you like me to help you refactor the code to allow users to export the calendar to a `.txt` file instead of just printing it to the console?
