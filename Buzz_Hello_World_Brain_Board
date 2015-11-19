/*
 This is an example sketch for Buzz and the Brain Board, a Pixel Pal learning kit
 
 Thank you to all our Kickstarter supporters who made it Possible!
 
 Pick up your own Chip in the Soldering Sunday shop:
 http://solderingsunday.com/shop/pixel-pals/pixel-pals-buzz-brain-board/
 
 Soldering Sunday supports and invests time and resources in open source code,
 please suport us by purchasing from solderingsunday.com
 
 This code  is based on the Arduino Melody

 http://www.arduino.cc/en/Tutorial/Tone
 originally created  21 Jan 2010 and modified 30 Aug 2011
 by Tom Igoe

 This example code is in the public domain.
 
 Created 2015-11-18
 By: SolderingSunday.com
 Rev: 1.0
  

 */
#include "pitches.h"



// Brain Baord Pinouts
// D0 = Sound (Buzz's Buzzer)
// D1 = Right Eye LED (Buzz)
// D4 = Left Eye LED (Buzz)
// D2 / A1 = Touch sensor (Brain Board)
// D5 / A0 = IR Emitter / Collector
 


// notes in the melody:
int melody[] = {
  NOTE_C4, NOTE_G3, NOTE_G3, NOTE_A3, NOTE_G3, 0, NOTE_B3, NOTE_C4
};

// note durations: 4 = quarter note, 8 = eighth note, etc.:
int noteDurations[] = {
  4, 8, 8, 4, 4, 4, 4, 4
};

void setup() {
  // iterate over the notes of the melody:
  for (int thisNote = 0; thisNote < 8; thisNote++) {

    // to calculate the note duration, take one second
    // divided by the note type.
    //e.g. quarter note = 1000 / 4, eighth note = 1000/8, etc.
    int noteDuration = 1000 / noteDurations[thisNote];
    tone(0, melody[thisNote], noteDuration);

    // to distinguish the notes, set a minimum time between them.
    // the note's duration + 30% seems to work well:
    int pauseBetweenNotes = noteDuration * 1.30;
    delay(pauseBetweenNotes);
    // stop the tone playing:
    noTone(0);
  }
  // initialize the digital pin as an output.
  pinMode(4, OUTPUT); //LED on Model B
  pinMode(1, OUTPUT); //LED on Model A   
}

void loop() {
  // no need to repeat the melody.
  digitalWrite(4, HIGH);   // turn the LED on (HIGH is the voltage level)
  digitalWrite(1, HIGH);
  delay(1000);               // wait for a second
  digitalWrite(4, LOW);    // turn the LED off by making the voltage LOW
  digitalWrite(1, LOW); 
  delay(1000);               // wait for a second
  for (int thisNote = 0; thisNote < 8; thisNote++) {

    // to calculate the note duration, take one second
    // divided by the note type.
    //e.g. quarter note = 1000 / 4, eighth note = 1000/8, etc.
    int noteDuration = 1000 / noteDurations[thisNote];
    tone(0, melody[thisNote], noteDuration);

    // to distinguish the notes, set a minimum time between them.
    // the note's duration + 30% seems to work well:
    int pauseBetweenNotes = noteDuration * 1.30;
    delay(pauseBetweenNotes);
    // stop the tone playing:
    noTone(0);
  }
}
