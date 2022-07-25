# Task2-Electrical-and-electronic-power
This repository contains two subtasks:
- On off system
- 
## On off system
In this task I made an electronic circuit that consists of the folloiwng components:
- Small Signal nMOS Transistor
- 10 kΩ Resistor
- 30 , 5 Power Supply
- DC Motor
- Diode
- Arduino Uno R3
- Pushbutton1 
- kΩ Resistor

Arduion code:
```
// C++ code
//
#define mosfetGate 6
#define pushButton 2

void setup()
{
  pinMode(mosfetGate, OUTPUT);
  pinMode(pushButton, INPUT);

}

void loop()
{
  int buttonState = digitalRead(pushButton);
  if(buttonState==1){
  	digitalWrite(mosfetGate, HIGH); //turn on the motor
  }
  else{
  	digitalWrite(mosfetGate, LOW); //turn off the motor
  }
}
```
This circuit enable the auto shutdown by the arduino, the motor will rotate only when the pushbutton clicked, otherwise the motor will never rotate.
- Click [here](https://www.tinkercad.com/things/hP8x8h8XdHQ-bodacious-jaiks-crift/editel?sharecode=Dn_C5lPQhzsvtIkSJjDFKiJFKJQM5L63AIrcKs9e6DA) to simulate the circuit on tinkercad.
