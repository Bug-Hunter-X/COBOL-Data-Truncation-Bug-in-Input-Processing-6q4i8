# COBOL Data Truncation Bug

This repository demonstrates a common but subtle bug in COBOL programs related to data truncation.  The program takes a numerical input, but lacks error handling for inputs exceeding the defined PIC clause. This can lead to unexpected results or program crashes.

## Bug Description
The `bug.cob` file contains a COBOL program that accepts an amount from the user. If the user enters an amount exceeding the capacity of the `PIC 9(5)V99` data field (values greater than 99999.99), the data will be truncated. This can lead to incorrect calculations and potentially unexpected program behavior.  The program does not include input validation or error handling for such situations.

## Solution
The `bugSolution.cob` file presents a corrected version of the program. It incorporates input validation to prevent data truncation errors. The program now checks if the input exceeds the allowable range before processing, and displays an error message if it does.