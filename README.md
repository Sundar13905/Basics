# BASICS

# EXPERIMENT 2 To study and implement C++ Program Structure  (Data types): -
## AIM: -
To learn how to run and implement the basic fundatamentals of C++ for example the varibales and their sizes, the different type of storage classes.

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

## Code for size of datatypes

~~~
//sundaravadivelan karthikeyan 
//23070123136
//ENTC B3
//Experiment 2 Finding the sizes of primitive datatypes 
#include <iostream>
using namespace std;

int main() 
{
    char a = 's';
    cout << "The size of a character is: "<< sizeof(a) << endl;
    int b = 123456;
    cout << "The size of an integer is: "<< sizeof(b) << endl;
    short int c = 1233;
    cout << "The size of a short integer is: "<< sizeof(c) << endl;
    long int d = 12739482;
    cout << "The size of a long integer is: "<< sizeof(d) << endl;
    long long int e = 122388728;
    cout << "The size of a long long integer is: "<< sizeof(e) << endl;
    float f = 27168.5;
    cout << "The sie of a float is: " << sizeof(f) << endl;
    double g = 84273923.89877;
    cout <<"The size of a double floating point is: "<< sizeof(g) << endl;
    long double h = 8742980.789793;
    cout<< "The size of long double floating point is: "<<sizeof(h) << endl;
    cout<< "The size of a wide character is: "<<sizeof(wchar_t) << endl;
    return 0;
}


/*output

The size of a character is: 1
The size of an integer is: 4
The size of a short integer is: 2
The size of a long integer is: 4
The size of a long long integer is: 8
The sie of a float is: 4
The size of a double floating point is: 8
The size of long double floating point is: 16
The size of a wide character is: 2


*/


~~~
![Experiment_2_output](https://github.com/Sundar13905/Basics/blob/main/Experiment_2%20(1).png)
## Code for storage classes 

~~~
#include<iostream>
using namespace std;

extern int extern_variable =30;


int main()
{
    auto a = 8;
    register int registered_variable = 100;
    static int s = 7;
    cout << "The local variable: "<< a << std::endl;
    cout <<"The variable in register: "<<registered_variable<<endl;
    std::cout<<"External variable: "<<extern_variable<<endl;
    s = 10;
    cout<<"The static variable: "<<s<<endl;

}

~~~


![Experiment_2_output](https://github.com/Sundar13905/Basics/blob/main/Experiment_2%20(2).png)



# EXPERIMENT 3 To study and implement operators in C++ : -

### DIFFERENT TYPES OF OPERATORS
There are different types of operations used in C++ to perform different actions.
An operator is a symbol that operates on a value to perform specific mathematical or logical computations. They form the foundation of any programming language. In C++, we have built-in operators to provide the required functionality.
An operator operates the operands.
For example, 
int c = a + b;
Here, ‘+’ is the addition operator. ‘a’ and ‘b’ are the operands that are being ‘added’.



#### Operators in C++ can be classified into 6 types:
1.	Arithmetic Operators
2.	Relational Operators
3.	Logical Operators
4.	Bitwise Operators
5.	Assignment Operators
6.	Ternary or Conditional Operators



#### 1.	Arithmetic Operations: -
Arithmetic Operators in C++ are used to perform arithmetic or mathematical operations on the operands. For example, ‘+’ is used for addition, ‘–‘ is used for subtraction,  ‘*’ is used for multiplication, etc. In simple terms, arithmetic operators are used to perform arithmetic operations on variables and data; they follow the same relationship between an operator and an operand.

#### 2.	Comparison Operations: -

There are mainly 6 Comparison Operators namely:

1.	Greater than (>)  :  this operator checks whether 1 variable is greater than other variable 
2.	Greater than or equal to (>=)  :  this operator checks whether operand1 is greater than or equal to operand2. If the result turns out to be true, it returns true, or else returns false. example 5>=5 ->returns true
3.	Less than (<)  :  this operator checks whether operand1 is lesser than operand2. If the result turns out to be true, it returns true, or else returns false. example 3<5 ->returns true
4.	Less than or equal to (< =)  :  this operator checks whether operand1 is lesser than or equal to operand2. If the result turns out to be true, it returns true or else returns false. example 5<=5 ->returns true
5.	Equal to (==)  :  this operator checks whether operand1 is equal to operand2. If the result turns out to be true, it returns true or else returns false. example 5==5 ->returns true
6.	Not Equal to (! =)  :  this operator checks whether operand1 is not equal to operand2. If the result turns out to be true, it returns true or else returns false. example 5!=3 ->returns true

Comparison Operators have only two return values, either true (1) or False (0).


#### 3.	Assignment Operators 

Assignment operators are used to assign values to variables.
For Example: -
Int x = 10;

Here we have assigned the variable x to the integer value 10.

In C++, the assignment operator forms the backbone of many algorithms and computational processes by performing a simple operation like assigning a value to a variable. It is denoted by equal sign ( = ) and provides one of the most basic operations in any programming language that is used to assign some value to the variables in C++ or in other words, it is used to store some kind of information.


## Code

~~~
/*Sundaravadivelan Karthikeyan
23070123136
ENTC B3 
EXPERIMENT 3- TYPES OF OPERATORS(ARITHEMATIC, LOGICAL, COMPARSION)
*/


#include<iostream>
using namespace std;

int main()
{
    int a,b;
    printf("Enter 2 variables: ");
    scanf("%d %d",&a, &b);
    int c = a+b;
    cout << "The addition of 2 numbers "<<c<<endl;
    int d = a-b;
    cout << "The subtraction of 2 numbers "<<d<<endl;
    int e = a*b;
    cout << "The multiplication of 2 numbers "<<e<<endl;
    float f = a/b;
    cout << "The division of 2 numbers "<<f<<endl;
    if(a==b)
    {
        cout << "The numbers are equal" << endl;
    }
    else if(a>b)
    {
        cout <<"The first number is greater than the second one "<< endl;
    }
    else
    {
        cout <<"The second number is greater than the first one" << endl;
    }
    float g = a%b;
    cout<< "The reminder of the numbers is: " <<g<<endl;
    long int k = a*a;
    cout<<"The square of the first number is: "<<k<<endl;
    for(int i = 0;i<2;i++)
    {
        if(a<b && a!=b)
        {
            b =- 10;
            a =+ 1;
        }
        else if(a>b || a==b)
        {
            a =-10;
            b += 1;
        }
        cout<<a<<endl;
        cout<<b<<endl;
    }

}

/* OUTPUT


Enter 2 variables: 15
19
The addition of 2 numbers 34
The subtraction of 2 numbers -4
The multiplication of 2 numbers 285
The division of 2 numbers 0
The second number is greater than the first one
The reminder of the numbers is: 15
The square of the first number is: 225
1
-10
-10
-9


*/

~~~


## Output of the code: - 
![Experiment_3_output](https://github.com/Sundar13905/Basics/blob/main/Experiment_3_output.png)


# EXPERIMENT 4  To study and implement C++ Bitwise Operators: -

#### 4. Bitwise Operators 

Bitwise Operators are the operators that are used to perform operations on the bit level on the integers. While performing this operation integers are considered as sequences of binary digits. In C++, we have various types of Bitwise Operators.

Bitwise AND (&)
Bitwise OR (|)
Bitwise XOR (^)
Bitwise NOT (~)
Left Shift (<<)
Right Shift (>>)


#### 1. Bitwise AND (&)
Bitwise AND operation is performed between two integers, It will compare each bit on the same position and the result bit will be set(1) only and only if both corresponding bits are set(1). The symbol which is used to perform bitwise AND operation is &.

#### 2. Bitwise OR (|)
If Bitwise OR operation is performed between two integers , It will compare each bit on same position and the result bit will be set(1) if any of corresponding bits are set(1). The symbol which is used to perform bitwise OR operation is |.

#### 3. Bitwise XOR (^)
If Bitwise XOR operation is performed between two integers , It will compare each bit on same position and the result bit will be set(1) if any of corresponding bits differ i.e. one of them should be 1 and other should be zero. The symbol which is used to perform bitwise XOR operation is ^.

#### 4. Bitwise NOT (~)
The Bitwise NOT operation is performed on a single number. It change the current bit to it’s complement , i.e. if current bit is 0 then in result it will be 1 and if current bit is 1 then it will become 0. It is denoted by the symbol ~.

#### 5. Left Shift (<<)
This operator shifts the bits of Integer to left side by specific number (As mentioned) . This left shift operation is equivalent to multiplying the integer by 2 power number of positions shifted. The symbol which is used to represent Left Shift Operator is <<.

#### Right Shift (>>)
This operator shifts the bits of Integer to right side by specific number (As mentioned) . This right shift operation is equivalent to dividing the integer by 2 power number of positions shifted. The symbol which is used to represent Left Shift Operator is >>.

## Code
~~~
/*Sundaravadivelan karthikeyan 
23070123136
EXPREIMENT 4 - BITWISE OPERATORS (AND ,OR, NOT, XOR, LEFT SHIFT, RIGHT SHIFT)
*/


#include<iostream>
using namespace std;

int main()
{
    int a = 16; // 16 in binary is 10000
    int b = 14; // 14 in binary is 01110
    int c = a & b;
    int d = a | b;
    int e = a ^ b ;
    int f = ~a;
    cout << "The bitwise and value of 16 and 14 is: "<< c<< endl;
    cout << "The bitwise or value of 16 and 14 is: "<< d<< endl;
    cout << "The bitwsie xor value of 16 and 14 is: "<< e<< endl;
    cout << "The butwise not value of 16 is: "<< f<< endl;
    cout << "Left shifted value of a "<< (a<<1)<< endl;
    cout << "Right shifted value "<< (b>>1)<< endl;
    return 0;

}

/*

OUTPUT OF THE CODE: -

The bitwise and value of 16 and 14 is: 0
The bitwise or value of 16 and 14 is: 30
The bitwsie xor value of 16 and 14 is: 30
The butwise not value of 16 is: -17
Left shifted value of a 32
Right shifted value 7

*/
~~~

### OUTPUT OF THE CODE
![Output of the bitwise operator code](https://github.com/Sundar13905/Basics/blob/main/Output_image_Basics.png)
