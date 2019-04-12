# Computer Hardware

## CPU Components

#### Control Unit (CU)

The Control Unit of a CPU is the part of the CPU responsible for directing electrical signals to the computer, in order to execute program instructions. It doesn't perform any execution of the instructions itself, only directs other parts of the computer system to do so.

#### Arithmetic Logic Unit (ALU)

Performs basic arithmetic, such as addition, subtraction, multiplication and division. It also performs logical operations, typically comparisons, such as Equal-To, Less-than, Greater-than NOT, OR, AND etc.

#### Registers

The CPU has its own high speed memory, called registers. They are far faster than RAM, as they are physically inside the CPU, but have the downsize of being extremely limited in capacity. These registers are 32 bits wide on a 32 bit system, and 64 bits wide on a 64 bit one. (The width is how many bits it can hold).

## CPU Registers

#### General Purpose Registers

An example of a sort of general purpose register is the **EAX** register (*Extended Accumulator register*), 32 bits wide, sort of like a calculator on a system, used for stuff like integer multiplication. Although it is 32 bits wide, we can access a smaller number of bits, like 16 bits for example. Specifically 16 bits is called **AX**, which are the 16 bits of the lower section of the EAX register. If we only need 8 bits, we can use **AH/L**, which are the higher/lower 8 bits of the *AX* register.

There are another 3 sort of general purpose registers, which have basically the same naming conventions as the EAX, AX, AH/L, but for EBX, ECX and EDX, so like BX, BH/L etc.

There are then a few sort of general purpose registers, which have more specific use cases:

- ESP - Stack Pointer register, contains a memory address, which points to the top of the current stack frame in RAM.
- EBP - The Base Pointer, contains a memory address, which points to the bottom of the current stack frame in RAM.
- ESI - Source Index, typically used to hold a memory address of data when the data is being used as a source in an operation, like copying data from one place to another, this will contain the location of the data that you are copying.
- EDI - Destination Index, holds the destination memory address. If you were to copy data from one location to another, this holds the memory address that the data is going to be copied into.

These can be addressed as SP, BP, SI and DI to access the lower 16 bits, however they cannot be split up any further to *k*H/L or whatever, where K is some letter.

#### Special Purpose Registers

An example of a special purpose register is called **EIP** (32 bit system) or **RIP** (64 bit system). The *Extended Instruction Pointer*, holds the memory address of the next instruction we want to execute. It directs the CPU to find the next bit of code to execute after the present one, and it is interesting as the ability to hijack the EIP allows us to control the flow of execution or redirect it, for example moving it to code that we have supplied.

(By the way, EIP/RIP, EAX and AH/L registers are Intel registers, and x86 systems are 32 bit Intel systems).

### The Fetch - Decode - Execute Cycle

The CPU's job is to execute program instructions. The way it does this is as follows:

- The control unit 'fetches' the next instruction from RAM.
- The control unit 'decodes' the instruction (translates it into a form it can understand) and retrieves the necessary data from memory and places it into the arithmetic logic unit (ALU) of the CPU.
- The arithmetic logic unit (ALU) 'executes' the instruction, and operates on the data provided in the previous step.
- The arithmetic logic unit stores the result of the execution either in a memory register or RAM.

Once these four steps are complete, the cycle begins again, and the next instruction is retrieved.

## Stack and Heap

There are 2 sections to the RAM, the **Stack** and the **Heap**.

#### The Stack

Very structured and ordered, when a program is loaded, the instructions are loaded onto the stack. Each function in the program has local variables, which are assigned an area of memory called a 'stack frame'.

So like, user input would go to the variables in the 'stack frame' of whatever function they have been called from. At the bottom of the stack frame there will be the return pointer. When the CPU enters a function, it will save the previous value of the EIP to the bottom of the stack frame (not the one concerning this stack frame), this is the return pointer. Once the CPU reaches a 'return' or 'ret' statement, it will load the return pointer from the bottom of the stack frame into the EIP, and therefore leave the function and the stack frame, and carry on with the previous flow of code.

#### The Heap

The heap is an unstructured area of memory used to store data. It is somewhat slower to access than the stack but you can store whatever you like so long as you know what the size of the data will be. By contrast the stack is very structured, and you need to know how much data to reserve on the stack when you write the program.

#### Instructions vs Data

As both instructions and data are both just binary, if we manage to make the instruction pointer point to the bottom of a stack frame (the data section), the data after that will be processed as instructions, but will likely crash as they were not made to be instructions, though this is clearly exploitable. Likewise, if you try to perform an operation on a memory address that is high up in the stack frame (instructions), the CPU would treat it as data rather than an instruction, because it expects to get data.