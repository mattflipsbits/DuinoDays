## Day 2: Hello, World!
When a programmer learns a new language, often the first program they write is "Hello, world." This program
is very simple; it prints, "Hello, world," to the screen. This course will be no different. Since your
Arduino does not have a screen attached, it must first send the message to a host computer, which
then prints it through a component in the Arduino programming environment called the Serial Monitor.

### Today's Goals
- Introduction to the Serial Monitor
- Learn about program syntax and compilation

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
### The Serial Monitor ***(Arduino only)***
As stated above, the Arduino has no screen of its own on which you can display text. 

### Serial.begin()
In order to use the Serial Monitor, it must first be initialized. You do this by adding the
following line of code to your `setup()` function:
```
  Serial.begin(9600);
```
### Serial.println()


### 
##

### Topics
- Syntax
- Compilation
- Semi-colon
- Serial.begin()
- Serial.println()
- Serial.print()

### Activities
- Tinkercad: ***Code Walk: Hello, world!***
- Tinkercad: ***Debug: Hello, world!***
- Tinkercad: ***From Scratch: Hello, world!***
- Serial.print() vs. Serial.println()
