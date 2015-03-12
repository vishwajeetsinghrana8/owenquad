# Introduction #

It's common to use two sensors (each with three axes):

  * Accelerometer: Measures the direction of gravity, from which we can calculate roll and pitch; however, very sensitive to noise in short term.
  * Gyroscopes: Measures angular rotation rate (e.g. degrees per second).  Can integrate (sum measurements over time, e.g. roll += gyroY\_measurement `*` timestep) to calculate absolute angles.  Gyroscopes drift though, measuring up to 2 deg/second rotation when stationary.

[More detail on both of the sensors here](http://www.instructables.com/id/Accelerometer-Gyro-Tutorial/)

The solution is to combine the two using a sensor fusion algorithm.  A basic one is a Complimentary Filter or the more complex Kalman filter.

The MPU6050 has a built in sensor fusion chip (that outputs orientation (roll,pitch,yaw)) and can be used by the excellent [arduino library here](http://www.i2cdevlib.com/devices/mpu6050#source) saving you having to worry about low level details of sensor fusion.