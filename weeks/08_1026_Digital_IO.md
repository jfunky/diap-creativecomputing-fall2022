## [Ohm's Law](https://www.lyza.com/2016/11/30/voltage-current-resistancewith-gnomes/)

- "Ohm's Law" refers to the relationship Georg Simon Ohm observed regarding the behavior of materials: that there is a linear relationship between how much current flows through material when a given voltage is applied across it. It is resistance defined in terms of the ratio of applied voltage and resultant current flow:
- R = V/I where R is Resistance (Ohms); V is Voltage (Volts); I is Current (Amps)
- One ohm is the resistance through which 1 Amp flows when 1 Volt is applied. 
- For circuit analysis you can predict what voltage must exist across a known resistance and measured current using V=IR and similarly predict amperage across a known resistance and measured voltage using I=V/R.(For a given voltage, more resistance means less current.)

## Digital IO

- Electricity as power vs. electronics as signal: With some logic, we can use electricity as a signal. For example, we can read a digital input from an Arduino pin as "HIGH" (5V) and do something based on this information, in contrast to when it is 0V ("LOW").
- Arduino pins also allow us to "write" or output binary values of 5V or 0V. Think back to when we used the 5 volt output as a power source for an LED. All of the digital pins can do the same thing--the difference is you can control this with code: you can tell the Arduino to supply 5V or 0V to a particular pin.
- Digital inputs are binary, which means they only have two states. Analog inputs can have a range of values.
- When we configure Arduino pins as inputs, it is important to use a pulldown (connected to ground) or pullup (connected to V+) resistor. This does a few things: 
  - It protects your circuit from a short 
  - It prevents a "floating ground", which is when there is no electrical connection to ground 
  - (3) It creates a path of resistance when the circuit is closed, so the arduino can read the voltage.
- In order to see the values you're receiving with Arduino, use the Serial Monitor. In addition to introduce the serial monitor, the link shows how to include Serial.begin in your setup() function and Serial.println() in your loop in order to print digital values.

#### Reading & Writing Digital Signals

- Digital pins (0-13) allow us to "write" or output binary values of 5V or 0V using [digitalWrite()](https://www.arduino.cc/reference/en/language/functions/digital-io/digitalwrite/)
- With some logic, we can use electricity as a binary signal: Is this pin sending "HIGH" (5V) or 0V ("LOW") using digital pins (0-13) and [DigitalRead()](https://www.arduino.cc/reference/en/language/functions/digital-io/digitalread/)
- For example, if our switch/button is pressed, there is electricity flowing (HIGH). If is not pressed, there is no electricity flowing (0V). So we can say, if we read 5V the switch/button is pressed; if it is 0V it is not pressed.
- When we configure Arduino pins as inputs, [it is important to use a pull-down (connected to ground) or pull-up (connected to V+) resistor](https://www.seeedstudio.com/blog/2020/02/21/pull-up-resistor-vs-pull-down-differences-arduino-guide/). This does a few things:
  - It protects your circuit from a short
  - It prevents a "floating ground", which is when there is no electrical connection to ground
  - It creates a path of resistance when the circuit is closed, so the arduino can read the voltage

## In-class Circuits
- [Working with an LED and a push button](https://create.arduino.cc/projecthub/SBR/working-with-an-led-and-a-push-button-71d8c1)
- [Digital Input Pull-Up Resistor](https://docs.arduino.cc/tutorials/generic/digital-input-pullup)
- Arduino Code: [Control an LED with a button](https://create.arduino.cc/editor/jfunky7/b8a53f0d-396b-4fee-a31d-438140557e3f/preview)

<p align="center">
  <img width="800" src="https://github.com/jfunky/diap-creativecomputing-fall2022/blob/main/assets/week8_DigitalIO/LED_switch.png">
</p>

#### Program 2 LEDs

<p align="center">
  <img width="800" src="https://github.com/jfunky/diap-creativecomputing-fall2022/blob/main/assets/week8_DigitalIO/2LED_switch.png">
</p>

## [Serial communication](https://www.arduino.cc/reference/en/language/functions/communication/serial/)
- A common way that computers send data over a communication channel
- How we will get sensor data from a microcontroller to your computer via the USB port
- “Baud rate” is data rate 

#### Memory
- 1 bit = 0 or 1
- 1 byte = 8 bits
- These permutations allow for 256 unique values (0-255)<br>
eg. <br>
1 0 0 0 0 0 0 0 0 <br>
0 1 0 0 0 0 0 0 0 <br>
<br>


## Resources: 
- Arduino References:
  - [Digital Pins](https://www.arduino.cc/en/Tutorial/Foundations/DigitalPins)
  - [Arduino Variables](https://www.arduino.cc/en/Reference/VariableDeclaration)
- ITP Tutorials:
  -  [Digital Input & Output](https://itp.nyu.edu/physcomp/lessons/digital-input-output/)
  -  [Microcontrollers: The Basics](https://itp.nyu.edu/physcomp/lessons/microcontrollers-the-basics/)
  -  [Interpretting Serial Data](https://itp.nyu.edu/physcomp/lessons/interpreting-serial-data/)
- ITP Videos:
  -  [Digital Input](https://vimeo.com/86548673)
  -  [Digital Output](https://vimeo.com/86534049)
  -  [Schematics](https://itp.nyu.edu/physcomp/videos/videos-schematic-diagrams/)


## Homework
Complete one of the following:
- Modify the Arduino code from class and the 2 LEDs + switch circuit to create some new behavior
- [CIRC07: Button Pressing project](https://learn.adafruit.com/experimenters-guide-for-metro/circ07-intro) from the MetroX kit

