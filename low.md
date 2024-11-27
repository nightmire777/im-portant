# LOW LEVEL 

# What is a Computer 
A Computer is a Programmable Electronic Device that can Store, Retrieve, and Process Data 
Accept input, process it, maybe store it, then give an output

## history of a computer
- 1st gen: vacumn tube (1940-1950)
- 2nd gen: transistor (1950-1960)
- 3rd gen: Intergrated Circuit (1960-1970)
- 4th gen: VLSI (1970-now)
- 5th gen: ULSI, ALML (future)

## computer system
hardware, software, procedure, data/info, user/ppl

## types of computer 
Supercomputer
- most powerful
- high cap computer for high complexity calculation 
- made to calculate alot of shit 
- used in military, weather

Mainframe
- snaller n simpler calculations
- real time data transactions
- better for things with 0 down time
- e business, banking, airline

Minicomputer
- midrange server
- intermediate between microcomputer and mainframe in speed size and cap
- used in smaller business 
- data management, manufacturring

Microcomputer
- computer with microprocessor as a CPU 
- smaller than all others in speed, size and cap 
- can be config
-  laptop, desktop etc..

# Data Representation 
computer only know on(1) and off(0)
represented by binary digits (bits)
WE count in base 10, THEY count in base 2
a byte is 8 bit 

>theres also octal and hexadecimal =)

Data is collection of unprocessed items (can be anything)
Information is organized and presentable information to ppl 

Data Processing cycle:
Input -> processing -> output 

Computer Data Formats 
- basically file extensions... or also known as computer usable form
- different way a human data (png/audio) can be represented, stored and processed by a computer

proprietary formats: unique to comapny (docx, safetensor, )

standards: Standardized formats are developed and maintained by open organizations, committees, or consortia. universal compatibility and interoperability across platforms and applications.

`ASCII: American Standard Code for Information Interchange `

Originally 7 bit, then there is Extended ASCII which is 8 bit which can represent special chars like `µ`

`Unicode: Universal Code`

Extended ASCII also not enough for the amount of BS in the world

it is 16 bit code, 1st 256 bit is from extended ascii


EBCDIC: Extended Binary Coded Decimal Interchange Code(eight-bit character encoding used mainly on IBM mainframe and IBM midrange computer operating systems)

# Computer Registers
## wat is a processor
- also a central processing unit. 
- a lil chip that manage instructions (I/O, aritmetic)
- can have many core
- speed depends on clock speed, cache size and num of core

## CPU components
>Arithmetic and logic unit (ALU)
- allows arithmetic and logic operation
>Control unit
- read shit from memory
- address of on instruction is stored in the program counter (pc) 
- ensure synchronization of data flow and program instructions 

>registers and busses
- address bus: has address between processo and memory , unidirectional
- data bus: send data between processors and I/O and memory units, bidirectional 
- control bus: has signals related to instructions and coordination to components , bidirectional  

>sytstem clock


## types of registers
>general purpose register
- can store data 
- can store intermidiate data when calculation 
- 


>user visible registers
- data registers: mul, cx, 
- address registers: stack pointer, segment pointer, index pointer 

>user invisible registers
- usually have a special purpose / use by OS
- program count register (pc), instruction register (IR), MAR, MDR, stat/plag register 


# LMC
>1 add
>
>2 sub
>
>3 store
>
>5 load
>
>6 branch unconditionally
>
>7 branch is 0
>
>8 branch on positive 
>
>0 halt
>
>901 input
>
>902 output
