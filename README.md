# Robotic-Arm-DIY

#include <Servo.h>

Servo myservo1;

Servo myservo2;
Servo myservo3;


void setup(){
    myservo1.attach(5);
    myservo2.attach(6);
    myservo3.attach(3);
    pinMode(A0,INPUT);
    pinMode(A1,INPUT);
    pinMode(A2,INPUT);
}

void loop(){
    int a = analogRead(A0);
    int b = analogRead(A1);
    int c = analogRead(A2);
    
    int x = map(a,0,1023,0,180);
    int y = map(b,0,1023,0,160);
    int z = map(c,0,1023,0,160);
    
    myservo1.write(x);
    myservo2.write(y);
    myservo3.write(z);


}

*Arjun ( Isuru ) 🍁✨️*
