#include <Servo.h>

// Create servo objects
Servo servo1;
Servo servo2;
Servo servo3;
Servo servo4;

void setup() {
  // Attach servos to digital pins
  servo1.attach(8);
  servo2.attach(9);
  servo3.attach(10);
  servo4.attach(11);
  
  // Move servos to initial positions
  servo1.write(0);
  servo2.write(0);
  servo3.write(0);
  servo4.write(0);
  
  delay(1000); // Wait for 1 second
}

void loop() {
  // Example: sweep all servos from 0 to 180 degrees
  for (int pos = 0; pos <= 180; pos += 1) {
    servo1.write(pos);
    servo2.write(pos);
    servo3.write(pos);
    servo4.write(pos);
    delay(15); // Wait 15ms for the servo to reach the position
  }
  
  // Sweep back from 180 to 0
  for (int pos = 180; pos >= 0; pos -= 1) {
    servo1.write(pos);
    servo2.write(pos);
    servo3.write(pos);
    servo4.write(pos);
    delay(15);
  }
}
