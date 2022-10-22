## Analog Input

- The Arduino's Analog pins (on the Arduino Uno, these are A0-A5) allow us to input or "read" a range of values from 0-1023 via the [analogRead](https://www.arduino.cc/reference/en/language/functions/analog-io/analogread/) command.
- You cannot use the analog pins to **output** analog signals
- Similarly to a digital input circuit where you are trying to read the value of a switch or button (which requires a pullup or pulldown resistor), most analog sensors (resistive sensors/variable resistors) require a resistor divider in series with the sensor, where the measurement point is between the resistors. Some sensors already have circuitry (they may even include an integrated circuit) built in that means their wiring is an exception to this. You must check the data sheets for your sensors.
  - A potentiometer is an exception, as a variable resistor that works with an internal wiper, it doesn't require an additional resistor because one leg acts as that resistor.
- Just as with digitalRead(), in order to see the values you are receiving in your Serial Monitor with Arduino, you must use the Serial.begin() command in your setup() function, and Serial.println() to print the value.
  -  Remember that we also used Serial.begin(9600) where 9600 was the baud rate, and were then able to print out the analog and digital values to the console. 

#### [Analog Read](https://www.arduino.cc/en/Tutorial/BuiltInExamples/AnalogInput) potentiometer values
- Refer to the schematic with the potentiometer

## Analog Output

- Remember that the analog input pins on an Arduino only read analog values. As a digital device, Arduino actually can't output an analog signal, it can only simulate an analog signal on the Digital PWM ~ pins (on an Arduino Uno these are: 3, 5, 6, 9, 10, 11). You can distinguish them with the ~ next to them.
- You can use the analog output functionality to fade an LED, operate a motor, a fan, etc.

#### [Pulse Width Modulation](https://www.arduino.cc/en/Tutorial/Foundations/PWM)

- PWM stands for "pulse width modulation", a technique where the digital signal turns on (5V) to off (0V) very quickly 
- As a digital device, microcontrollers actually can't output an analog signal, so they simulate them on the Digital PWM pins (on an Arduino Uno/MetroX these are: 3, 5, 6, 9, 10, 11)
- A **Pulse** refers to the “on” or “high” period
- The length of that period is the **Width**
- The **Modulation** part refers to varying the length of that width, the result being an average between 0V and 5V
- Imagine a very short period of time (let's say 2 milliseconds) where 5V is supplied 25% of the time, and 0V is suppled for 75% of the time. The resulting voltage would be 1/4 of 5V, 1.25V. The period of time where the signal is "on" (5V) is the "pulse." The proportion of the time refers to the "width." The **"duty cycle"** is the total on-off measurement period (100%, in our example, 2 milliseconds).
  - In the diagram linnked in the title, this is the period between the green lines
- Analog Output values written with the analogWrite() function in Arduino can be output on a scale of 0-255, such that 255 requests 100% of the duty cycle. In our example above, requesting 25% of the duty cycle would be analogWrite(64). 50% of the duty cycle would be analogWrite(127), and so on.

#### [Fade an LED](https://www.arduino.cc/en/Tutorial/BuiltInExamples/Fade)


## Sensors
#### Sensors in your kit
- 10K Pot (Single turn rotary potentiometer, variable resistor)
- Force Sensitive Resistor (FSR)
- HW-5P-1 Light Sensor (Photoresistor)
- TMP36 Temperature Sensor

#### Variable resistors
- Flex sensor
- Stretch sensor
- Slide potentiometer
- Linear position sensor
- Photocell/photoresistor
- Thermistor
- Soil moisture sensor 
- Velostat *for building sensors

#### Other sensors
- Humidity and temperature sensor
- Hall effect sensor
- Phototransistor 
- Ultrasonic distance sensor
- IR distance sensor
- Pulse sensor
- Accelerometer
- Air quality sensor

#### Voltage divider circuit
- Now refer to the [Analog Read]((https://www.arduino.cc/en/Tutorial/BuiltInExamples/AnalogInput) schematic with the photoresistor
- Two resistors in series like this create a [voltage divider](https://learn.sparkfun.com/tutorials/voltage-dividers/all)
- To measure a variable resistor, the fixed resistor should be in the approximate same order of magnitude (match the range of the variable resistor)
- The fixed resistor limits the voltage range, so you won’t get a full 0-1023 resolution, like with a potentiometer 
- You can modify the code or the fixed resistor for a different range
