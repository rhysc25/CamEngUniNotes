Most microprocessors follow the Von Neumann architecture, with memory, a control unit, an arithmetic logical unit (ALU) connected to inputs and outputs

The simplified architecture of a computer:
![[Pasted image 20250509134059.png]]

The ALU performs mathematical and logical operations
The control unit manages the execution of instructions
The registers are used for temporary storage for instructions and data
The memory is to store long term

Their are buses to connect everything:
* Address bus: To address particular locations
* Data bus: To carry data to and from locations (bidirectional)
* Control bus: To send instructions

An ALU will have many MUX units, which choose which input goes to the output based on control signals
To make an n-bit ALU, connect $n$ one bit ALUs together

Basic bus structure:
![[Pasted image 20250509134553.png]]
If there are n wires, then there can be $2^n$ locations

To read and write data from and to memory, we must set the address of the memory location on the address bus.
Set the $R/\overline{W}$ (read/write) wire of the control bus to HIGH to read, or LOW to write
Set the address valid control wire high
These together will activate the memory $\overline{\text{chip select}}$, which is active LOW
Contents of the memory location are then placed on the data bus
Once the data is read, the control wires can be reset

If $a$ is the number of address wires and $d$ is the number of data wires, then there are $2^{a}$ memory locations that can be addressed, and the total addressed capacity is:
$$d\times 2^a$$
Registers are temporary storage for instructions and data within the microprocessor
Special registers such as STATUS and Program Counter
The working register, w, holds the data the PIC is working on at a current time
The general purpose register file is memory for the PIC

The program counter (PC) is a register which stores the program memory address of the next instruction to be executed

The microprocessor works on a Fetch-Decode-Execute system

Example instruction: 00 0011 1 010 0000
00 0011 is the op code for the instruction, e.g. this is decf
The 1 tells the destination of the result, 1 for F and 0 for W
010 0000 tells the location of the element to have the operation done to, so location $20_H$

## RAM

We need chip select ($\overline{CS}$) to be LOW to be able to read or write
A memory chip with 20 address wires has $2^{20}$ locations, so 1024 bytes. We call this a kilobyte, ignoring the 24. Or more specifically a kibibyte.

In a RAM chip, the memory elements are arranged as rows and columns.
There is one row of memory elements for each address wire and one column for each data wire

Address bus signals are passed to a decoder which selects one row out of $2^n$ possibilities, essentially just a bunch of AND gates with only 1 output being HIGH

![[Pasted image 20250513141711.png]]

This is an individual memory element, where the value is stored in the S-R latch state

![[Pasted image 20250513141835.png]]

We can see here how the driver buffers need to be powered, to select either input or output as the data bus is bidirectional

![[Pasted image 20250513142044.png]]

If we have a memory chip with 20 address wires, and we have a microprocessor with 21 address lines, we can use the MSB to identify 2 individual chips

In general, the first few most significant bits, depending on the number of chips and address wires per chip, tell you which chip, and the rest of the bits tell you which location inside the chip

We can also map an input and an output to the same memory location, e.g. a keyboard and a display
This can be done through the $R/\overline{W}$ signal and some tristate buffers connected to the data bus

Types of Memory:
* RAM - readable and writeable, forgotten when power turned off
* SRAM - Static RAM - simple, speedy, good storage density, used for fast cache memories
* DRAM - Dynamic RAM - complex, must have contents refreshed continuously, slower, but very dense storage
* ROM - Read only memory - set by manufacturer
* EPROM - Erasable Programmable Read Only Memory - can only be programmed using a device that uses a higher voltage than the microprocessor
* FLASH Memory - electronic non-volatile storage that can be electrically erased and reprogrammed

High level code -> Compiler -> Assembly language -> Assembler -> Op-codes

0x before a number indicates hexadecimal
0 before a number indicates octal
b before a number indicates binary
Otherwise it is a decimal number

When we use a mov function, we are not actually moving it, just copying the content into somewhere else

The default destination in Op-code is d=1 if nothing is explicitly mentioned

The PIC12F629 has a memory map organised into two banks of registers

andwf and iorwf can force certain bits to 1 or 0 in a byte
rlf - rotate left through carry so the MSB is now in carry, which will be a 1 if it was a negative number in the 2s complement system
rrf - rotate right through carry so the LSB is now in carry, which will be 0 if it was an even number

The GPIO register acts as a 6 bit wide bidirectional port
The TRISIO register sets the GPIO pins as either input or output, 1 is input

The STATUS register contains the carry flag and the zero flag
The zero flag is 1 if the result of an operation is zero

decfsz F,d decrements F and skips next instruction if the answer is zero, which can be used to implement a small delay in the programme

Flow charts can be used to show program architecture, with diamonds being decision boxes and rectangles being action boxes

For most PIC processors, each instruction takes one internal clock cycle to execute
Exceptions:
* Instructions which need to replace the PC contents (goto, call, return, etc.) take two
* Conditional instructions, if the condition is met, take 2. E.g. to skip an instruction, the nop instruction must be carried out instead

## File Register Indirect Addressing

File register 0x04 is the File Select Register (FSR), used for indirect addressing

If a file register address is loaded into FSR, the contents of that register can be read through the Indirect File Register (INDF)

So if we call a function like movwf INDF, we're putting the data from w into the memory address that's loaded into FSR

This is useful for quickly reading/writing a large amount of data, as the FSR can be incremented, and the same loop can move bits into the new address quickly

The stack is a "Last In, First Out" system. In a PUSH operation, the contents of one or more registers will be placed onto the stack.
The memory address location where the first item is to be stored is held in another register, the SP
To POP items entails loading memory into 1+ registers and adjusting the SP

E.g. for the PC when a sub routine is called, the PC is pushed onto the stack, then popped in the event of a return, retlw or refie

Call is used to jump to a sub routine and return is used to return to the main program

Interrupts are generated by an asynchronous event
The ISR (Interrupt Service Routine) is then ran
The PC is pushed to the stack

## The Reset Pin 

When we want to reset the system, we use the active low $\overline{\text{RESET}}$ pin

![[Pasted image 20250523143031.png]]

When the reset button is pressed, $V_c$ is shorted to ground.
When the reset button is unpressed, the RC circuit means that their is a delay before $V_c$ returns to a high enough value

This is to allow the PC to return to 0x0000 and for the predefined start up programmes to run, and for the microprocessor to reinitialise

