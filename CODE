#include <Servo.h>
char data = 0;   
Servo myservo;             //Variable for storing received data
void setup() 
{
Serial.begin(9600);         //Sets the data rate in bits per second (baud) for serial data transmission
pinMode(TRIG_PIN, OUTPUT);   // set arduino pin to output mode
  pinMode(ECHO_PIN, INPUT);    // set arduino pin to input mode
  pinMode(BUZZER_PIN, OUTPUT); 
  myservo.attach(9);// set arduino pin to output mode     //Sets digital pin 13 as output pin
}
void loop()

 digitalWrite(TRIG_PIN, HIGH);      
  delayMicroseconds(10);
  digitalWrite(TRIG_PIN, LOW);
 duration_us = pulseIn(ECHO_PIN, HIGH);
  // calculate the distance
  distance_cm = 0.017 * duration_us;
   if(distance_cm < DISTANCE_THRESHOLD){                               //when there is someone in front of the door
    digitalWrite(BUZZER_PIN, HIGH); // turn on Piezo Buzzer
   }else{
    digitalWrite(BUZZER_PIN, LOW);  // turn off Piezo Buzzer           //when no one is in proximity
   }
{
if(Serial.available() > 0)  // Send data only when you receive data:
{
data = Serial.read();      //Read the incoming data and store it into variable data
Serial.print(data);        //Print Value inside data in Serial monitor
Serial.print("\n");        //New line 

if(data == 'O')            //Checks whether value of data is equal to "O" - open
myservo.write(120); 
delay(1000);

else if(data == 'C')       //Checks whether value of data is equal to "C" - close
myservo.write(0);   //If value is 0 then LED turns OFF
delay(1000);
}
