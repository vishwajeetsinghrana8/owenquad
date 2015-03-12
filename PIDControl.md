# Introduction #


**Basics**

Uses two [PID controllers](http://brettbeauregard.com/blog/2011/04/improving-the-beginners-pid-introduction/):
  * First takes desired angular rate (e.g. rotate at x degrees per second) and actual angular rate (from gyro) as input for each axis and outputs motor speeds.
  * Second, takes desired absolute angle (from pilot) and actual absolute angle (from sensors) as input (e.g. maintain angle at 0 degrees), and outputs desired angular rate into first PID.

Much stabler than having one PID.

**Enhancements**
http://diydrones.com/forum/topics/arducopter-2-stability-patch