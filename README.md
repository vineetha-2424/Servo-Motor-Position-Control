#include <Servo.h>

Servo motor;

void setup() {
  motor.attach(9);
}

void loop() {
  int value = analogRead(A0);
  int angle = map(value, 0, 1023, 0, 180);
  motor.write(angle);
  delay(20);
}# Servo-Motor-Position-Control
