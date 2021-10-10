# R3-SoftwareTask1-TaskinRahman

Steps:
  In a loop:
    1 - The input reading from the potentiometer is taken and is mapped to a range of 0-99.
    2 - Then each digit of the reading is converted to binary decimal (0-9) --> binary (4-bit).
    3 - Each 4-bit binary number is sent to the BCD to 7 segment decoder (4-bits --> 4 inputs).
    4 - It is converted to a 7 segment value and displayed on a 7 segment display. Since there are 2 digits 
    there are 2 corresponding CD4511's each connected to a 7 segment display. 
    
First digit:
  - 4-bit binary number : output pins - 2, 3, 4, 5 (2 - MSB, 5 - LSB)
  - output pins 2, 3, 4, 5 go to input pins 1, 2, 3, 4 of first CD4511
 
Second digit:
  - 4-bit binary number : output pins - 8, 9, 10, 11 (2 - MSB, 5 - LSB)
  - output pins 8, 9, 10, 11 go to input pins 1, 2, 3, 4 of second CD4511

The outputs ABCDEF are mapped to --> abcdef inputs of the 7 segment display for each corresponding CD4511
