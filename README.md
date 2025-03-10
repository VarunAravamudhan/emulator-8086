# emulator-8086
## Theory
# Stack in Assembly
The stack is a section of memory used for temporary storage. It operates in a LIFO (Last In, First Out) manner. The SP (Stack Pointer) register manages the stack.

#  Instructions Used
PUSH → Stores a value into the stack.
POP → Retrieves the last value stored in the stack.
MOV → Transfers data between registers.
CALL/RET → Used for function calls (not used in this basic example).
Data Transfer Using Stack
Data is pushed onto the stack from registers.
The stack pointer (SP) adjusts accordingly.
Data is then popped into another register for processing or transfer.
# Program:
~~~
MOV AX, BX
PUSH AX
POP BX
IN AL, 60H
OUT 70H, AL
HLT
~~~
# Output:
![Uploading Screenshot 2025-03-10 085740.png…]()
# Program Flow:
~~~
MOV AX, BX → AX gets BX’s value.
PUSH AX → AX value is saved on the stack.
POP BX → BX retrieves the last pushed value (AX).
IN AL, 60H → Reads a value from port 60H (keyboard).
OUT 70H, AL → Sends that value to port 70H (RTC).
HLT → Stops execution.
~~~


