# BASICS

## AIM: -
To learn the basic fundatamentals of C++ for example the varibales and their sizes, the different type of storage classes, the different types of operators like arithmeatic, logical, comparsion and bitwise

## Theory: -

All variables use data type during declaration to restrict the data storage type. Whenever a variable is defined in C++, the compiler allocates some memory based on the data type with which it is declared.
 Every data type requires a different amount of memory. C++ supports a wide variety of data types, and the programmer can select the data type appropriate to the requirements of the applications. Data types specify the size and types of values to be stored. However, storage representation and machine instructions to manipulate each data type differ from machine to machine.
C++ has the following data types: - 
Character (ch)
Integer (int)
Boolean (bool)
Floating point (float)
Double Floating point (double)
Void ()
Wide Character
sizeof() operator

These data types can have modifiers, for example: -
Short
Long
Signed 
Unsigned

These modifiers can make the variable either increase or decrease in size. For example, Long can extend an integer to be 4 bytes 

### The above-mentioned variables can be stored in different storage classes like 

### Auto: -
This is the default storage class for all the variables declared inside a function or a block.  Auto variables can be only accessed within the block/function they have been declared and not outside them

### Extern: -
The extern storage class tells us that the variable is defined elsewhere and not within the same block where it is used. the value is assigned to it in a different block and this can be overwritten/changed in a different block as well. So an extern variable is nothing but a global variable initialized with a legal value where it is declared in order to be used elsewhere. It can be accessed within any function/block.

### Static: -
Static storage class is used to declare static variables which are popularly used while writing programs in C language. Static variables have the property of preserving their value even after they are out of their scope! Hence, static variables preserve the value of their last use in their scope. So we can say that they are initialized only once and exist till the termination of the program. Thus, no new memory is allocated because they are not re-declared.
Their scope is local to the function to which they were defined. Global static variables can be accessed anywhere in the program. By default, they are assigned the value 0 by the compiler. 

### *Register: - 
This storage class declares register variables with the same functionality as auto variables. The key difference is that the compiler attempts to store these variables in the microprocessor's registers if a free register is available. This makes register variables faster to access than variables stored in memory during program runtime. If no free register is available, the variables are stored in memory instead. Typically, variables that are accessed frequently in a program are declared with the register keyword to improve the program's runtime efficiency. Notably, the address of a register variable cannot be obtained using pointers.


### DATA TYPES: - THEIR SIZES AND RANGE 
### Data Type	Size (in bytes)	Range
#### short int
(2 bytes )	(-32,768 to 32,767)
#### unsigned short int 
(2 bytes) 	(0 to 65,535)
#### unsigned int
(4 bytes) 	(0 to 4,294,967,295)
#### int
(4 bytes)	(-2,147,483,648 to 2,147,483,647)
#### long int (4 bytes)
(-2,147,483,648 to 2,147,483,647)
#### unsigned long int
(4 bytes)  (0 to 4,294,967,295)
#### long long int
(8 bytes) {-(2^63) to (2^63)-1}
#### unsigned long long int
(8 bytes)	(0 to 18,446,744,073,709,551,615)
#### signed char
(1 byte)	(-128 to 127)
#### unsigned char
(1 byte) 	(0 to 255)
#### float
(4 bytes)	(-3.4×10^38 to 3.4×10^38)
#### double
(8 bytes) (-1.7×10^308 to1.7×10^308)
#### long double
(12 bytes)	(-1.1×10^4932 to1.1×10^4932)
#### wchar_t (2 or 4 bytes)	(1 to wide character)

### OUTPUT OF THE CODE
![Output of the bitwise operator code](https://github.com/Sundar13905/Basics/blob/main/Output_image_Basics.png)
