## Day 1: Arduino Program Structure

### Today's Goals
- Introduction to microcontrollers and the Arduino ecosystem
- Learn how to comment code
- Learn the structure of an Arduino program

##
### What is a microcontroller?
A **microcontroller** is essentially an all-in-one computer designed to be programmed to execute
a specific task.

In a general-purpose computer, such as a desktop or laptop, elements of the system are divided
into separate components. In order to build a desktop PC, you would have to buy the processor,
short-term memory (like RAM), long-term memory (like hard drives or solid state drives) all
separately. However, in a microcontroller, all these are combined into one chip, along with
other peripherals. The trade-off is that microcontrollers tend to be slower and have far less
RAM and storage space compared to a general-purpose computer.

Microcontrollers are used in everything: coffee makers, cars, internet routers, even satellites
and rockets. A device that uses a microcontroller as its "brain" is called an **embedded system**.

### What is Arduino?
Arduino is an open-source ecosystem designed for easy embedded system prototyping. Arduino produces
various [development boards](https://docs.arduino.cc/hardware/) using a large variety of microcontrollers.
In this course we will be using a virtual [Arduino Uno R3](https://docs.arduino.cc/hardware/uno-rev3/)
featuring the [ATmega328P](https://www.microchip.com/en-us/product/atmega328p) microcontroller in the
Tinkercad sections, and the [Arduino Mega 2560](https://docs.arduino.cc/hardware/mega-2560/) which features
the [ATmega 2560](https://www.microchip.com/en-us/product/atmega2560) in the hands-on section.
##
### Code: The First Steps
#### Code Comments
Code comments are essentially notes you can leave to yourself or other programmers. They will not affect
how the program runs. C++ supports two kinds of comments: **single-line comments** and **block comments**.

#### Single-line comment
A single-line comment begins with `//` and ends at the end of the line. They do not have to start at
the beginning of a line.

Examples:
```
//  A basic comment, all by its lonesome self.

Serial.println("Hello, world!");     // prints "Hello, world!" to the Serial Monitor
```
Note that in the second example, the comment only begins after the `//` following the semi-colon.
The first portion `Serial.println("Hello, world!");` is actual code that will affect what the program does.

#### Block comment
A block comment begins with `/*` and ends with `*/`. Anything between these two constructs is part of the
comment. They do not have to start at the beginning of a line.

Examples:
```
/* This can be used as an alternate single-line comment, just don't forget to close it with this! ---> */

/*
    A block comment can
    also span multiple lines
*/

/*********************************************
 * Sometimes you'll see something like this  *
 * to make the comment stand out...          *
 *********************************************/

/*
 * ... or sometimes this.
 * How you use them is a matter of personal
 * preference and style.
 */
```

#### Arduino Program Structure ***(Arduino only)***
Arduino programs (also called sketches, we will use both interchangeably) consist of two parts, `setup()` and
`loop()`. The parentheses indicate that these are **functions**, which are small blocks of code that can be
thought of as mini-programs that normally you can run on demand (known as **calling the function**). `setup()` and
`loop()` are slightly different in that they will run automatically when the Arduino is powered up or reset.

The `setup()` function runs only once and usually contains any setup or initialization code you may need. The
`loop()` function runs after the `setup()` function and will run repeatedly as long as the board is powered.

Here's what they look like in code, with comments for clarification:
```
void setup() {
  // Anything that needs to run just once goes here
}

void loop() {
  // Anything that needs to run repeatedly goes here
}
```
The curly braces are used to delimit the "boundaries" of the function. Any code between them are considered to be
part of the function. We will learn what exactly `void` is and why the parentheses are there when we dive deeper
into how functions are constructed a bit later. You can also review this structure in the ***Arduino Structure***
Tinkercad activity.
##


### From the Docs
- [What is Arduino?](https://docs.arduino.cc/learn/starting-guide/whats-arduino/)
- [Single-line comment](https://docs.arduino.cc/language-reference/en/structure/further-syntax/singleLineComment/)
- [Block comments](https://docs.arduino.cc/language-reference/en/structure/further-syntax/blockComment/)
- [setup()](https://docs.arduino.cc/language-reference/en/structure/sketch/setup/)
- [loop()](https://docs.arduino.cc/language-reference/en/structure/sketch/loop/)
- [curly braces](https://docs.arduino.cc/language-reference/en/structure/further-syntax/curlyBraces/)

### Activities
- Tinkercad: ***Comments*** - write your own single-line and block comments
- Tinkercad: ***Arduino Structure*** - basic template for reference/review
- Tinkercad: ***Bare Minimum*** - guided practice writing the basic template on your own
