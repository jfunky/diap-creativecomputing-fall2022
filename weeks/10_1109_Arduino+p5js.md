## Connecting P5.js & Microcontroller with Serial
- There are many multimedia programming environments that integrate with Serial, enabling the creation of rich interactive digital experiences
- In order for any two digital devices to communicate, there must be a mutually agreed upong method
- We have some experience with using the Serial communication to read digital and analog signals with a microcontroller and acessing those values on our computers via USB and [Asynchronous Serial Communication](https://itp.nyu.edu/physcomp/lessons/serial-communication-the-basics/)
- We did this by establishing:
    - the rate at which data was to be sent & read (9600 bits per second)
    - what voltage level should be interpreted as 1 or 0 bits: does 1 correspond to HIGH and 0 to LOW "true logic", or is this "inverted logic"?
    - a common ground, so both devices have the same measurement reference
    - a transmit line: sender device sends data to the receiver device
    - a receiver line: receiver device sends data to the sender device
    - the order of bits
- Once (1) devices are connected and  (2) there is a program to address the serial port and (3) the serial port is open, any bytes sent by the connected device can be read by the program in the order they were sent
    - Most processors with a UART (Universal Asynchronous Reciever-Transmitter) have a **serial buffer** which stores incoming data from serial port in memory, which can then be read in the order it was send (First In, First Out)
- **Only one program can access the Serial Port at a time** 
    - For example, you will not be able to see the serial data coming in on your Arduino Serial Monitor and also in your p5.js sketch at the same time

## WebSerial
- W3C has recently developed the [WebSerial API for Javascript](https://developer.mozilla.org/en-US/docs/Web/API/Web_Serial_API), allowing communication between a computer's serial ports and the browser, where historically this has been limited & challenging for security reasons
- In this class we will use [p5.WebSerial](https://github.com/yoonbuck/p5.WebSerial/wiki/API), which relies on the WebSerial API, to integrate Serial with p5.js sketches
- We are familiar with Javascript event listeners from our experience with p5.js (for example, the mouseclick event)
- Similarly, the WebSerial API and p5.js webserial library have events for is a serial port gets connected and disconnected
- **Supported browsers** are Chrome, Edge, and Opera

#### [Serial Input with webserial](https://itp.nyu.edu/physcomp/labs/labs-serial-communication/lab-webserial-input-to-p5-js/)
- Use a simple potentiometer circuit, like from last week's class
- The examples that seem to work best are those using serial.println in the Arduino code and read a String in the p5.js code
- Writing and reading strings also allows for the communication of multiple sensor values

#### [Serial Output with webserial](https://itp.nyu.edu/physcomp/labs/labs-serial-communication/lab-webserial-output-from-p5-js/)
- We will use a simple LED circuit, like those from the last 2 classes
- You can also experiment with the piezo in your kit and the [Circ06](https://learn.adafruit.com/experimenters-guide-for-metro/circ06-intro) tutorial in your handbook

## Resources
- [P5 code from class](https://editor.p5js.org/jfunky/collections/5l-loFx2z)
- ITP:
    - [Serial Communication Videos](https://itp.nyu.edu/physcomp/videos/videos-serial-communication/#Serial_out_to_p5js_multi-part_ASCII)
    - [Intepreting Serial Data](https://itp.nyu.edu/physcomp/lessons/interpreting-serial-data/)
    - [p5.serialport vs. p5.webserial](https://itp.nyu.edu/physcomp/lessons/p5-serialport-and-p5-webserial-compared/)
    - [Two-way duplex Serial Communication](https://itp.nyu.edu/physcomp/labs/labs-serial-communication/lab-two-way-duplex-webserial-communication/)

## Assignment 
- Prototype a simple system that either:
    - Sends data to p5.js from a sensor or button and does something on the screen
    - Sends data from some interaction in p5.js to some actuator
