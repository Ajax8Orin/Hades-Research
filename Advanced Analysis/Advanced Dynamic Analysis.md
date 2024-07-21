### Introduction to Debugging

- Understanding a debugger layout:
![[Pasted image 20240704115112.png]]
1. CPU Process flow
2. Registers window highlighting EIP
3. Stack Window
4. Function called name
5. Debugger Functions and shortcuts

- **Step Over:** Skipping the calling function while debugging based on the assumption that all the instructions are fulfilled and the program needs to continue
- **Step Into:** Upon encountering a call function, we read all the instructions inside it and execute them then in that order to understand their purpose before stepping back to the main program
- **Breakpoint:** It is a marker that allows full debugging to stop at that point while executing the code allowing us to control the flow of program

Creating Breakpoint : Main method discovered

![[Pasted image 20240721142054.png]]