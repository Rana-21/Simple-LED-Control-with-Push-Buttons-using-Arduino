# Simple-LED-Control-with-Push-Buttons-using-Arduino
This Arduino project demonstrates how to control three LEDs (green, blue, and red) using three separate push buttons.
Each button toggles its corresponding LED on or off when pressed. This project helps beginners understand digital input (push buttons) and output (LEDs) in Arduino.

# Components Used:
- Arduino UNO
- Breadboard
- 3 LEDs (Green, Blue, Red)
- 3 Push Buttons
- 3 Resistors (1KΩ)
- 3 Pull-down resistors (optional if internal pull-up used)
- Jumper wires

# How It Works:
- Each button is connected to a digital input pin on the Arduino.
- When a button is pressed, the Arduino reads HIGH and toggles the LED state.
- Simple digitalWrite/digitalRead logic is used.

# Circuit Design:
- Button 1 → Pin 2 → Green LED → Pin 5
- Button 2 → Pin 3 → Blue LED → Pin 6
- Button 3 → Pin 4 → Red LED → Pin 7

# Arduino Code Sample:
const int button1 = 5;
const int button2 = 6;
const int button3 = 7;


const int led1 = 2;
const int led2 = 3;
const int led3 = 4;

void setup() {
  pinMode(button1, INPUT);
  pinMode(button2, INPUT);
  pinMode(button3, INPUT);

  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
}

void loop() {
 
  digitalWrite(led1, digitalRead(button1));
  digitalWrite(led2, digitalRead(button2));
  digitalWrite(led3, digitalRead(button3));
}
