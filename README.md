# Task2-Electrical-and-electronic-power
This repository contains two subtasks:
- [On off system](https://github.com/farahhrs/Task2-Electrical-and-electronic-power/blob/main/README.md#on-off-system)
- [Forward kinematics & inverse kinematics](https://github.com/farahhrs/Task2-Electrical-and-electronic-power/blob/main/README.md#forward-kinematics--inverse-kinematics)
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

## Forward kinematics & inverse kinematics
In this task I draw a robot arm with a 3 DOF, then I applied the forward kinematics and the inverse kinematics to find angle measures and (x, y) point.
- Inverse kinematics:
    - The given data: (x, y) = (50, 30)
    - The calculations:
   
    > Pythagoras theorem:
    > 
    > 𝒉^𝟐= 𝒂^𝟐+𝒃^𝟐 
    > 
    > 𝒉^𝟐= 〖𝟏𝟓〗^𝟐+〖𝟏𝟓〗^𝟐 
    > 
    > 𝒉=√(〖𝟏𝟓〗^𝟐+〖𝟏𝟓〗^𝟐)
    > 
    > 𝒉=𝟐𝟏.𝟐𝟏
    > 
    > L1 and L3 are equal 21.21
    > 
    > 𝒔𝒊𝒏 𝜽=𝑶𝒑𝒑𝒐𝒔𝒊𝒕𝒆/𝑯𝒚𝒑𝒐𝒕𝒆𝒏𝒖𝒔𝒆
    > 
    > 𝒔𝒊𝒏 𝜽=𝟏𝟓/(𝟐𝟏.𝟐𝟏)
    > 
    > 𝜽=𝒂𝒓𝒄𝒔𝒊𝒏 𝟏𝟓/(𝟐𝟏.𝟐𝟏)
    > 
    > 𝜽=𝟒𝟓.𝟎𝟏°
    > 
    > 𝜽1 and 𝜽2 are equal 45.01
    > 
    > 𝜽𝟒=𝟏𝟖𝟎− (𝟒𝟓.𝟎𝟏+𝟗𝟎)
    > 
    > 𝜽𝟒=𝟒𝟒.𝟗𝟗°
    > 
    > 𝜽𝟓=𝟒𝟒.𝟗𝟗+𝟗𝟎
    > 
    > 𝜽𝟓=𝟏𝟑𝟒.𝟗𝟗 °
    > 
    > 𝜽𝟐=𝟏𝟖𝟎−𝟏𝟑𝟒.𝟗𝟗
    > 
    > 𝜽𝟐=  45.01 °
    > 
    > 𝜽𝟐  and 𝜽𝟑 are equal 45.01 °

   
    - The solution:
    
    >  L1= 21.21
    >  
    >  L2= 20
    >  
    >  L3=21.21
    >  
    >  𝜽1= 45.01°
    >  
    >  𝜽𝟐= 45.01°
    >  
    >  𝜽𝟑= 45.01°


- Forward kinematics:
    - The given data: 
    
    L1= 12
    
    L2= 15
    
    L3= 18
    
    𝜽𝟏=𝟒𝟓°
    
    𝜽𝟐=𝟒𝟓°
    
    𝜽𝟑=𝟑𝟐

    - The calculations:
      > X= (L1 cos 𝜽𝟏)+𝑳𝟐+"(L3 cos " 𝜽𝟑)
      > 
      > Y= (L1 sin 𝜽𝟏 + L3 sin 𝜽𝟑)
      >
      >  X= (12 cos 𝟒𝟓)+𝟏𝟓+"(18 cos " 𝟑𝟐)
      >  
      >  X= 38.75
      >  
      >  Y= (12 sin 𝟒𝟓 + 18 sin 𝟑𝟐)
      >  
      >  Y= 18.02
      >  
      >  (x,y)= (38.75, 18.02)

Click [here]() to see the file that contains the whole calculations and soltuions 
