## Day 2: Hello, World!
When a programmer learns a new language, often the first program they write is "Hello, world." This program
is very simple; it prints, "Hello, world," to the screen. This course will be no different. Since your
Arduino does not have a screen attached, it must first send the message to a host computer, which
then prints it through a component in the Arduino programming environment called the Serial Monitor.

### Today's Goals
- Learn about program syntax and compilation
- Introduction to the Serial Monitor
- Learn the "Hello, world!" program

### A Note about Activities
Many of the Tinkercad activities in this course will be split into three formats. A **Code Walk**,
a **Debug** activity, and a **From Scratch** activity. 

Code Walks will show the entire, correct program with a line-by-line explanation given in the comments. 

Debug projects will provide you with a program that is incorrect and/or incomplete, which may or may not
compile (if you don't know what 'compile' means, don't worry - you'll learn about that very shortly).
Your task is to bring the program into working order.

Finally, From Scratch activities will provide you with no code at all, only comments that will guide you
through the steps required to recreate the program on your own.

##
### Syntax
Like any spoken language, programming languages have a set of rules that they must follow in order to
be valid. We will slowly introduce these rules as the course progresses rather than overload you with
them right at the start.

The first, and arguably the most important rule of syntax in C++, is the use of the semi-colon, which
serves to terminate a programming **statement**. The most common statements we will see will be
function calls (which we will be using today), and variable declaration and assignment (covered later).
Think of the semi-colon as the programming equivalent of a period in the English language.

Here is a code example from the program you will be working with today:
```
void setup() {
  Serial.begin(9600);
}
```
Note that the semi-colon is only placed at the end of the statement inside the `setup()` function.
There is NO semi-colon after the closing brace of the function.

#### On Whitespace and Brace Placement
C++ is very permissive when it comes to both whitespace (spaces, tabs, and newlines) and brace placement.

All of these code snippets are identical as far as C++ is concerned:
```
// Example 1
void setup() {
  Serial.begin(9600);
}

// Example 2
void setup()
{
  Serial.begin(9600);
}

// Example 3
void setup() {Serial.begin(9600)};

// Example 4 - DON'T DO THIS
                                                  void


          setup()


{



                                                                        Serial.begin(9600);




                                                      }
```
The first two examples are the most common code formats you will see. Whichever you choose is a matter
of personal preference. Example 3 you will sometimes see for very short functions called "one-liners."
Example 4 is an extreme example that, while it looks very odd and is borderline unreadable, will still
compile and run perfectly fine.

### Compilation
A computer or a microcontroller cannot understand the code as you have typed it. It must first translate
the code you have written into **machine language** that it can understand, then generate an **executable**
file which it can then run. In Windows, a `.exe` file is an example of an executable. This translation process
is called **compilation** or **compiling**. In order for a program to successfully compile, it must be 100%
syntactically correct. Any program with any syntax errors whatsoever will generate an error message, and you
will not be able to run the program. In Tinkercad, this process is taken care of using the 'Start Simulation'
button. In the real Arduino programming software, it is done using the 'Verify' or 'Upload' buttons.

There are two levels of compiler errors: **errors** and **warnings**.
#### Compiler Errors
A compiler error is a fatal error that will force the compiler to abort compilation. It will not generate
an executable file, and thus you will not be able to run your program. Syntax errors, such as missing a
semi-colon or not closing a parenthesis or brace, are the most common compiler errors.

#### Compiler Warnings
A compiler warning occurs when a program is syntactically correct, but contains a mistake that may
cause the program to exhibit unexpected behavior. Address all compiler warnings whenever possible as
they can be the source of difficult bugs.

### The Serial Monitor ***(Arduino only)***
As stated above, the Arduino has display of its own. It must first send data (such as text) over a USB
cable connected to a desktop or laptop running the Arduino Integrated Development Environment (IDE for short),
which then displays the data in the Serial Monitor within the IDE. The Serial Monitor will be your primary 
form of communication with your Arduino.

#### Serial.begin() ***(Arduino only)***
In order to use the Serial Monitor, it must first be initialized. This is done by adding the
following line of code to your `setup()` function:
```
  Serial.begin(9600);
```
This "turns on" the Serial Monitor, and allows you to use it for both input and output. Without
this line of code, *the Serial Monitor **will not** work*. If you're expecting output on your
Serial Monitor and you're not seeing any, double-check that you properly initialized it in your
`setup()` function with the above line of code.

The first part of this function is `Serial` This references the Serial Monitor, which has an entire
family of functions within it (see *From the Docs* below). One of these functions is `begin()` which
tells the Arduino to initialize the Serial Monitor for use. Note the period in-between `Serial` and `begin()`.
This is necessary to delineate between the name of the **object** (`Serial`) and one of its functions (`begin()`).
We will discuss objects in more detail later in the course. For now, just know that they are constructs which
can contain a host of their own functions.

Now, what is that bizarre number in between the parentheses just after `begin`? This is called a **function argument**.
It means that the function requires some extra information in order to work properly. In the case of the `Serial.begin()`
function, it needs to know at what speed to communicate. This is called the **baud rate** which is measured in bits
per second. 9600 is the most common baud rate used in Arduino programming, and it is what we will use here. In the Tinkercad
simulator, we can actually use any number we choose, and things will work just fine. However, in the real Arduino software
we will be using later, some additional configuration is required, and you will need to make sure all baud rates match.
We will cross that bridge when we come to it. For now, we will always set the baud rate to 9600.

Finally, the function call is terminated with a semi-colon.

***NOTE:*** C++ is case-sensitive. Things like `serial.Begin()` or `SERIAL.BEGIN()` will cause an error.

#### Serial.println() ***(Arduino only)***


#### Serial.print() ***(Arduino only)***



##

### Topics (* indicates done for now)
- Syntax *
- Compilation *
- Semi-colon *
- Serial.begin() *
- Serial.println()
- Serial.print()

### From the Docs
- [semi-colon](https://docs.arduino.cc/language-reference/en/structure/further-syntax/semicolon/)
- [Serial Functions](https://docs.arduino.cc/language-reference/en/functions/communication/serial/#functions)
- [Serial.begin()](https://docs.arduino.cc/language-reference/en/functions/communication/serial/begin/)


### Activities
- Tinkercad: ***Code Walk: Hello, world!***
- Tinkercad: ***Debug: Hello, world!***
- Tinkercad: ***From Scratch: Hello, world!***
- Tinkdercad: ***Serial.print() vs. Serial.println()***
