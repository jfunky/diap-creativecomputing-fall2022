## Electricity Basics

#### Terms

- **Electricity**: Electron flow through a conductive material. Electrons will flow through the path of least resistance.
- **Circuit**: When a power source (let's say a battery) is connected to components that turn electrical energy into some other kind of energy.
- **Load**: The component/s that are doing the work on a circuit.
- **Ground**: The place on a circuit with the lowest potential energy. Sometimes this is the actual ground, but other times it is the grounded part of a circuit. In a circuit, electricity flows from the power source to ground.
- **Short Circuit**: When power and ground connect directly to each other without a load or bypassing a load, the power source overheats.
- **Voltage**: A measure of the potential energy difference between two points on a circuit. Units are Volts (V).
- **Current**: A measure of the magnitude of electron flow at a particular point in a circuit. Units are amperes, or, amps.
- **Resistance**: A measure of materials ability to resist the flow of electrons. Units are ohms.
- **Conductor**: Material that allow for free flow of electrons.
- **Insulator**: Material that prevents the flow of electricity.
- **Resistor**: Materials that resists the flow of electricity.

#### Some Common Components
- **Transducer**: A component that converts one kind of energy into another kind of energy.
  - **Sensors** convert some kind of energy (mechanical, temperature, light, etc.) into electricity, which can be read as a signal.
  - **Actuators** convert electrical energy into some other energy (heat, light, movement, etc.)
- **Switch**: A conductor that acts as a mechanical connector/disconnector in a circuit.
- **Diode**: Allow electricity to flow in one direction but not another direction. Diodes are one kind of polarized component, which means they can only be connected in a circuit in one direction.
- **LED**: Light Emitting Diodes emit light, and are polarized like all diodes.
- **Capacitor**: Store electrical energy while it's being provided, and then release it when it stops. Decoupling capacitors are capacitors used to to smooth electricity flow in a circuit. Capacitors can be polarized or unpolarized.
- **Transistor**: An electronic switch. Transistors have three terminals: collector, base (responsible for activating flow between the collector and emitter), and emitter (connects to ground); or source (connects to ground), gate (responsible for activating flow between the source and drain), drain (for MOSFETS). They are often used to have a small amount of energy (an electronic signal) control a larger amount of energy.
- **Potentiometer**: A variable resistor.
- **Wire**: A conductive material wrapped in an insulated material used to connect components. They can generally be thought of as having zero resistance.
- **Solderless breadboard**: An resuable prototyping material that allows you to create easy electrical connections.
- **Battery holder**: Connect to the positive and negative poles of a battery for easy connection to your circuit.
- **Power Supply**: The circuits we'll be building in this class will use Direct Current (DC) as opposed to Alternating Current (AC) what you're familiar with from a typical outlet. Power supplies are a component you can buy though they are not needed for low-power circuits. You can use the 5V pin on your Arduino, a battery, or an AC to DC converter.

## Circuits

<p align="center">
  <img src="https://github.com/jfunky/diap-creativecomputing-fall2022/blob/main/assets/week7_Arduino/FlashlightSchematic_p10.png">
</p>

*Practical Electronics for Inventors, p.10*

#### Schematics

- Schematic diagrams show the electrical relationship of components in a circuit. They do not (generally) show the spatial relationship of components.
- Components have corresponding symbols, which is how they are represented in schematics.
- In this class we will often use diagrams to present relationships between the Arduino, pinouts, and components along with the schematic.

<p align="center">
  <img width="200" src="https://github.com/jfunky/diap-creativecomputing-fall2022/blob/main/assets/week7_Arduino/FlashlightSchematic_line.png">
</p>

#### Guidelines for building circuits

- Do not: connect + and - terminals directly to each other (i.e. Short circut).
- Do: connect components that use all your voltage (resistors, LEDs, Motors, etc). The voltage requirements of your components should add up to the amount of voltage provided. If your components draw less voltage, they will overheat. If they draw too much voltage, your components might not work (or be dim, slow, etc. depending).
- Circuits must be closed in order for electricity to flow.
- Switches control the opening and closing of your circuit.

#### [Electrical Connections Using a Breadboard](https://learn.sparkfun.com/tutorials/how-to-use-a-breadboard/all)
- Can be used with jumper wires for quick prototyping
- On a typical medium-sized breadboard, power rails run down the side
- The center rows are electrically connected

#### Other Electrical Connections

- Alligator Clips
- Lever nuts
- Crimp connections
- Wire nuts
- Soldering 
- **Do not solder batteries** 
- You also can't solder aluminum or conductive fabric

#### Types of Insulation

- Wire/cable insulation
- Air
- Electrical tape
- Heat-shrink tubing

## Parallel vs. Series Circuits

- Series Circuit: In a series circuit, energy flows from one component to the next component. Components draw voltage, and the voltage drops. In a simple DC circuit, the sum of the voltage drops across each component must equal the source voltage (Kirchoff's Voltage Law). The amount of current going into any component is the same as the current coming out (Kirchoff's Current Law).
- Parallel Circuit: Components are in parellel when energy flows through them at the same time. Voltage across components wired this way is the same, but the current is divided between them.

<p align="center">
  <img width="500" src="https://github.com/jfunky/diap-creativecomputing-fall2022/blob/main/assets/week7_Arduino/BasicCircuit_p49.png">
  <img width="500" src="https://github.com/jfunky/diap-creativecomputing-fall2022/blob/main/assets/week7_Arduino/ParallelCircuit_p49.png">
  <img width="500" src="https://github.com/jfunky/diap-creativecomputing-fall2022/blob/main/assets/week7_Arduino/CombinedCircuit_p50.png">
</p>

*Practical Electronics for Inventors, pp.49-50*

- You can [measure the voltage drop on your circuit using a multimeter](https://learn.sparkfun.com/tutorials/how-to-use-a-multimeter/all#measuring-voltage)

## Arduino

- A microcontroller development board
- The microcontroller we are using with an Arduino development board is a Atmel Atmega328P chip. Compared with other computers that can run whole operating systems, microcontroller are firmware-only processors. No processor can run by itself: it needs components like a voltage regulator and external clock to keep time. The Arduino board provides all the components you need in order to easily connect input and outputs. It runs just one program which you can easily change using the Arduino development environment.

<p align="center">
  <img src="https://github.com/jfunky/diap-creativecomputing-fall2022/blob/main/assets/week7_Arduino/ArduinoOverview.jpg">
  <img src="https://github.com/jfunky/diap-creativecomputing-fall2022/blob/main/assets/week7_Arduino/ArduinoPinOut.png">
</p>

#### [Download the Arduino IDE](https://www.arduino.cc/en/software)
#### Arduino Programming

- We have been practicing programming concepts in p5.js that are transferrable to any programming language, while other languages might have slightly different syntax and work a bit differently.
- Arduino is a programming language built for physical computing and working with microcontrollers while P5.js is a language built for creative coding on the web: visuals, sound, and other media.
- Like p5.js, Arduino is open-source
- Below I've annotated some similarities in the basic program structure between Arduino and P5.js

<p align="center">
  <img width="400" src="https://github.com/jfunky/diap-creativecomputing-fall2022/blob/main/assets/week7_Arduino/P5Comparison.png">
</p>

## Let's Build a Circuit
<p align="center">
  <img src="https://github.com/jfunky/diap-creativecomputing-fall2022/blob/main/assets/week7_Arduino/LED_Circuit.png">
</p>

## Let's add a switch
<p align="center">
  <img src="https://github.com/jfunky/diap-creativecomputing-fall2022/blob/main/assets/week7_Arduino/LED_Circuit_Switch.png">
</p>

## [Ohm's Law](https://www.lyza.com/2016/11/30/voltage-current-resistancewith-gnomes/)

**R = V/I**

- R is Resistance (Ohms)
- V is Voltage (Volts)
- I is Current (Amps)

#### Applying Ohm's Law
- If we measure the voltage drop of the resistor, and know the resistor value in ohms, we can calculate the current running through it:<br>
I = V/R <br>
I = 3.3/220Ω <br>
0.015A or 15mA

- If we know the supply voltage, the required forward voltage of our LED, and the desired current for the LED (from the data sheet), we can calculate the ideal resistor value.<br>
I = V<sub>S</sub>-V<sub>F</sub>/R <br>
R = 3.3V/0.020A <br>
R = 165Ω

## Homework Lab 1: Circuit with a Switch

- Create you own simple circuit that activates with a switch you build from conductive material. You can use the power and ground pins on your Arduino to power your circuit.
- Run the default "blink" sketch with the build-in LED on your Arduino. You can find the sketch by going to File > Examples > 01. Basics > Blink.
- Document your circuit with photo and/or video. How does it work? How did you make it? What questions are you left with?
- If possible, bring you circuit to class.

## Resources:

- [Arduino Language Reference](https://www.arduino.cc/reference/en/)
- [Arduino Variable Declaration reference](https://www.arduino.cc/en/Reference/VariableDeclaration)
- ITP Labs:
  - [Components](https://itp.nyu.edu/physcomp/Labs/Components/)
  - [Setting up a Breadboard](https://itp.nyu.edu/physcomp/Labs/Breadboard/)
  - [Basic Electronics Principles](https://itp.nyu.edu/physcomp/Labs/Electronics/)
  - [Soldering](https://itp.nyu.edu/physcomp/Labs/Soldering/)
- [Tutorials & Circuit diagrams for Arduino Built-In Examples](https://www.arduino.cc/en/Tutorial/BuiltInExamples) including [Blink](https://www.arduino.cc/en/Tutorial/Blink)
- Ohm's Law & Measurement:
  - [Sparkfun tutorial](https://learn.sparkfun.com/tutorials/voltage-current-resistance-and-ohms-law/all)
  - [ITP Video: LED Current](https://vimeo.com/showcase/2801639/video/78674965)
  - [ITP Video: Measuring Current, Resistance, Conntinuity](https://vimeo.com/showcase/2801639/video/87215804)
  - [LED Resistor Calculator](https://www.google.com/url?q=https://www.digikey.com/en/resources/conversion-calculators/conversion-calculator-led-series-resistor&sa=D&source=editors&ust=1666151072946454&usg=AOvVaw20ZlYisobmXpjFU-E-fcPU)
- [Digikey reference for resistor color codes](https://www.digikey.com/en/resources/conversion-calculators/conversion-calculator-resistor-color-code)
- Jody Culkin's [Arduino Comic & related links](https://www.arduino.cc/en/Tutorial/ArduinoComic)
- Chris Crawford: The Art of Interactive Design Ch 1 & 2
- Practical Electronics for Inventors Ch 2 (2.1-2.16)

