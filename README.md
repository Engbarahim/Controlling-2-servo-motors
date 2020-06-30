# Controlling-2-servo-motors

// Include the Servo library 
#include <Servo.h> 

// Declare the Servo pins 
int servoPin1 = 7; 
int servoPin2 = 6; 

// Create a servo object 
Servo Servo1; 
Servo Servo2; 

void setup() 
{ 
   // We need to attach the servo to the used pin number 
   Servo1.attach(servoPin1);
   Servo2.attach(servoPin2);
   Servo1.write(0);
   Servo2.write(0);  
}

void loop()
{ 
   // Make servo1 goes to 45 degrees and servo2 goes to 30 degrees
   Servo1.write(45);
   Servo2.write(30); 
   delay(2000); 
   
   // Make servo1 go to 90 degrees and servo2 goes to 60 degrees
   Servo1.write(90);
   Servo2.write(60); 
   delay(2000); 
   
   // Make servo1 go to 180 degrees and return servo2 to 30 degrees
   Servo1.write(180); 
   Servo2.write(30);
   delay(2000); 
}

