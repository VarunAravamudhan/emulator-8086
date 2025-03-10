![0981152b-fb28-46bc-a2f9-71a6701a7c6a](https://github.com/user-attachments/assets/a1e53903-9620-4e6d-8bba-c783dcc99689)![0981152b-fb28-46bc-a2f9-71a6701a7c6a](https://github.com/user-attachments/assets/18596bfe-63a7-4eb6-bcac-b3a0a188854d)# DATA TRANSFER USING STACK
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
# Diagram:
![0981152b-fb28-46bc-a2f9-71a6701a7c6a](https://github.com/user-attachments/assets/48109d6c-972a-49e7-9282-f3a90296814b)

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
![Screenshot 2025-03-10 085740](https://github.com/user-attachments/assets/382395f2-2dbb-4d06-b521-3ce4a443215f)

# Program Flow:
~~~
MOV AX, BX → AX gets BX’s value.
PUSH AX → AX value is saved on the stack.
POP BX → BX retrieves the last pushed value (AX).
IN AL, 60H → Reads a value from port 60H (keyboard).
OUT 70H, AL → Sends that value to port 70H (RTC).
HLT → Stops execution.
~~~


