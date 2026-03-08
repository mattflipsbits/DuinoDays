## Day 2: Blink, but Better!

### Today's Goals
- Introduction to Variables
- Rewrite the Blink sketch from a blank sketch

### Learn
1. [Using Variables in Sketches](https://docs.arduino.cc/learn/programming/variables/)
2. [Assignment Operator](https://docs.arduino.cc/language-reference/en/structure/arithmetic-operators/assignment/)
3. [Statement Terminator (semi-colon)](https://docs.arduino.cc/language-reference/en/structure/further-syntax/semicolon/)
4. [Code Blocks (curly braces)](https://docs.arduino.cc/language-reference/en/structure/further-syntax/curlyBraces/)

### Challenge
- Using the [Blink_empty.ino](https://github.com/mattflipsbits/DuinoDays/blob/main/Day2/Blink_empty/Blink_empty.ino) sketch provided, rewrite the Blink sketch using the comments as a guide.

So how is this a "better" version of Blink? By using the variables `ledPin` and `delayTime` to store the relevant values, we
are able to change those values throughout the code with one simple edit.<br>
<details>
  <summary>Consider this alternate (and worse) version:</summary>

```
void setup() {
  pinMode(13, OUTPUT);
}

void loop() {
  digitalWrite(13, HIGH);
  delay(500);
  digitalWrite(13, LOW);
  delay(500);
}
```
</details>

If we wanted to change the pin driving the LED (e.g. to drive an off-board LED), or change the delay time, we would need to make
several changes throughout the code (and hope we found them all!). It is considered to be bad practice to use 'raw' numbers (also 
called 'magic numbers') in code like the above example. Using variables allows the code to both be more modifiable and more
readable. With just a single edit, we can make several changes throughout the code, and as long as the variable is well-named, it is
obvious what each variable is describing.

### Tomorrow: Voltage, Resistance, and Current! Ohm My!
