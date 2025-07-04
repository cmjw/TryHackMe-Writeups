# ELF Reversal

## Part 1

* Run the executable crackme1 to reveal the flag.

## Part 2

* Running the executable crackme2, we need to enter a password.
* Examine the strings in the executable by running $strings crackme2.
* The flag is revealed as one of the strings.

## Part 3

* Running crackme3, we again need to enter a password.
* Using $strings crackme3, we see a value with a "==" suffix, indicating base64 encoding.
* Decode the string, revealing the password.

## Part 4

* This time, running strings does not reveal anything yet.
* Use gdb to list the functions of the executable, using $info functions.
* Notice the function "strcmp". This probably compares the input string to the key.
* Set a breakpoint at the address for this function.
* Run the program.
* Upon the breakpoint, check the register values.
* Register %rax holds a string value of the key.
