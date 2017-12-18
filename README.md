NB: You might find useful the [sample proposal](https://github.com/zamfi/cca-programming-electronics-fall-2017/blob/master/hw/sample-proposal.md) useful in completing this assignment!

# Your Project Title Here

Colors convertor

## Summary
Converting colors to sounds with precoded notes. 

What was challenging:
* Understand how the code works
*figure out which code should be executed when the color sensor read different colors.
*build up the motor wheels to spin your color sheet with the right timing.

Interaction:
*people can print out the color sheet that represent the sound they wanted to hear and place the color sheet in the convertor to play the song.

*Press switch button to change the key note.


## Component Parts
Flora Color Sensor x1
Speaker x1
Motor x2 
transistor for motors x2
resistor x2
Arduino UNO board x2
wires 
battery x1 (or two separate batteries if you don’t want to plug your Arduino in your laptop)

before you go to coding part, make sure following this tutorials online and download the libraries that are needed


### Code:

#include "Adafruit_TCS34725.h"
Adafruit_TCS34725 tcs = Adafruit_TCS34725(TCS34725_INTEGRATIONTIME_50MS, TCS34725_GAIN_4X);
int d = 2;
int leftMotorPin = 5;
int leftMotorSpeed = 250;
void setup() {
  pinMode(leftMotorPin, OUTPUT);
  // put your setup code here, to run once:
  Serial.begin(9600);

  if (tcs.begin()) {
    Serial.println("Found sensor");
  } else {
    Serial.println("No TCS34725 found ... check your connections");
    while (1); // halt!
  }
  pinMode(2, INPUT);
}




Include what types of inputs/outputs/data it will use, and a block diagram showing how all those pieces are connected.

## Challenges

A brief discussion of what was hard, challenging, or unexpected about your project.

## Timeline

What did you do in each of the past five weeks?

- Week 1: Write proposal
- Week 2: understand the code and start coding
- Week 3: coding and testing
- Week 4: testing, adjusting and installing 
- Week 5: Present!

## Completed Work

Photos and videos of your completed final project!

## References and links

[piano glove]( https://learn.adafruit.com/pianoglove).
[Installing a Library on Mac OSX](https://learn.adafruit.com/adafruit-all-about-arduino-libraries-install-use/installing-a-library-on-mac-osx)
