# 4-bit Adder Block Diagram

The following is a block diagram of a 4-bit adder like that found in a 7483 IC. It takes two 4-bit binary numbers 
in (plus a carry-in) and gives the addition of the two numbers as a 5-bit binary word (4-bit sum and a carry-out).

![4-bit Adder Block Diagram](/d/devops/Screenshot%202024-07-09%20221354.png)

## Description

Write a Verilog code to implement the above 4-bit adder circuit.

### 4-bit Adder 
- **Inputs:**
  - `y3 y2 y1 y0`
  - `x3 x2 x1 x0`
  - `cin` (carry-in, typically "0")

- **Outputs:**
  - `cout` (carry-out)
  - `s3 s2 s1 s0` (sum)

### Input Details
- Use switches `SW[3], SW[2], SW[1], SW0` to input binary number `x3 x2 x1 x0`.
- Use switches `SW[9], SW[8], SW[7], SW[6]` to input binary number `y3 y2 y1 y0`.

### Display the Inputs
- Use the BCD to SSD converter technique (used in Lab 3) to convert and display the inputs:
  - `y3 y2 y1 y0` on the SSD `HEX[3]` and `HEX[2]`
  - `x3 x2 x1 x0` on the SSD `HEX[1]` and `HEX[0]`

### Display the Outputs
- Again use the BCD to SSD converter to convert the output from the adder (`c4 s3 s2 s1 s0`). 
- When converted to BCD, it needs 2 digits to display the number in decimal format.
  - Use `HEX[5]` and `HEX[4]` to show each output as specified above. 
  - If any number is less than 10, the higher decimal should be blank – not zero.

## Modules
This project could be done in several modules. For example:
1. A top module
2. A bitwise full adder module
3. An adder module for all four bits
4. A module to convert the binary number to BCD
5. A module to output the numbers to the 7-segment display

If desired, you may use previous code that you have written for other labs.

## Deliverables
Attach the code for the TOP module and any other modules you have written – i.e., the entire code. Show the working adder and the code to the faculty.
