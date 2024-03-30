# Blinking-Banners

A microcontroller is a compact integrated circuit (IC) that includes a processor, memory, and input/output (I/O) ports on a single chip
The main components of ESP32:-
1. Micro-USB Jack: The micro USB jack is used to connect the ESP32 to the computer through a USB cable.
2. EN Button: The EN button is the reset button of the ESP module. Pressing this button will reset the code running on the ESP module.
3. Boot Button: This button is used to upload the Program from Arduino to the ESP module. It has to be pressed after clicking on the upload icon on the Arduino IDE. When the Boot button is pressed along with the EN button, ESP enters into firmware uploading mode. Do not play with this mode unless you know what you are doing.
4. Red LED: The red LED on the board is used to indicate the power supply. It glows red when the board is powered.
5. Blue LED: The blue LED on the board is connected to the GPIO pin. It can be turned on or off through programming.
6. I/O Pins: This is where the development takes place. These pins are used as inputs and outputs. We’ll delve into the details regarding these pins, a little later on.
7. ESP-WROOM-32: This is the heart of the ESP32 module. It is a 32-bit microprocessor


Download Arduino Software
Go to Downloads
● Open Software
● Click on I Agree
Click on Next
Click on Install
Click on Close
Open Software

To make it compatible with ESP 32 we need to adjust the settings as follows:
Click on File> Preferences
Now copy the following link and paste the copied text into Additional Boards Manager URLs:
https://dl.espressif.com/dl/package_esp32_index.json
Click on OK.
Now go to the Tools >Board: “Arduino Uno”> Boards Manager.
Type esp32 and then click on Install.
Click on Close

The next task is to select the board, We are using ESP32 board, ESP32 has a lot of variations like Dev Module, Woven module, Node MCU
Board name need to be checked from the back of the ESP32 board. Check the name and select the right board



Let’s try to make an LED blink using the ESP32 controller and Arduino IDE.
Let’s gather the following material from the WHJR-IoT kit:
1. 1 x ESP32
2. 1 x USB Cable
3. 1 x LED
4. 1 x 330-ohm Resistors
5. 1 x Jumper Wires
6. 1 x Battery
7. 1 x Battery Socket

The first and most important thing to do is to mount the ESP32 on the breadboard across both sides of the middle breakers.

Mount Components
● Mount LED & Resistor
○ Insert the LED into the breadboard.
○ Connect the longer leg of the LED to one end of the resistor

Wiring Connections:
● Connect longer leg OF LED with one end of resistor.
● Connect the other end of the resistor with ESP 32 GPIO pin no 18.
● Connect the shorter leg of the LED with the GND of the ESP32.

Open the Arduino IDE software on your computer. Code in the Arduino language will control your circuit
The first and most important thing is to initialize the variables:
● Let’s initialize the LED.
● Declare the LED before void setup()

In ESP32, the LED on the board is connected to pin number 18. However, we can choose any number on the breadboard.
The next task is to configure the pin. To configure the pin we use the pinMode() function.

pinMode() configures the specified pin to behave either as input or output.
Syntax: pinMode(pin, mode)
pin: The pin do we need to set mode: Set the mode INPUT, OUTPUT

The pin needs to be programmed to be either ON or OFF, that is, we can command it to be ON (output 5 volts), or OFF (output 0 volts).
To switch it on and off, we need to use a function called digitalWrite().

Let’s upload the program to check if we are able to program our ESP32 module.
For uploading, we need a USB cable.
Take the USB cable, from the IoT kit.
Insert one end of the USB cable into the ESP32 USB port and another end in the computer’s USB port.

Output:
Compile and upload the program to ESP32 board using Arduino IDE
● Verify the program by clicking the Tick option
● Upload the program by clicking the arrow option

Note: If the port is not selected, insert the USB cable in Computer’s port and select the port.
Make sure hardware is connected properly.
● You will see different colors on the LED 
Note: We can find the port number by accessing the device manager on Windows

Click on the tick to verify the syntax
OR
Click on Sketch >>Verify/Compile.
When you click on the tick button, the program you have written in Arduino IDE will be compiled for any errors.

Now, the next thing is to upload the program,
Click on the arrow to upload the program
OR
Click on Sketch >>Upload

If you look at your ESP32, you can see the 2 LEDs near Tx and Rx blinking. This is an indication of successful communication between your PC and the ESP32 board. If the program has been uploaded successfully, you will see a message like Done Uploading. If the uploading process was not successful, you will see an error message accordingly.
Now, you will see the LED will blink on and off after 10 seconds. 
This is how LEDs can be made to blink using a microcontroller.
