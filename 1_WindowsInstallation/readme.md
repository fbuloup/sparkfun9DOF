# Sparkfun 9DOF installation guide under Windows

[Link to orignal document.](https://learn.sparkfun.com/tutorials/9dof-razor-imu-m0-hookup-guide?_ga=2.99420060.326620079.1517431239-364404356.1517431239)

Windows steps are :

1. Connect IMU to USB port
2. Optional : install driver (you will need admin rights)
3. Download Tera Term's and first tests

## 1. Connect IMU to USB port
Connecter le module sur un port USB de l'ordinateur et attendre qu'il soit bien reconnu par Windows.

## 2. Optional : install driver (you will need admin rights)
IMU seems to work properly even if driver adviced from Sparkfun is not installed. If any problem, it's possible to install this driver if you have admin rights, just follow this [link.](https://learn.sparkfun.com/tutorials/9dof-razor-imu-m0-hookup-guide?_ga=2.99420060.326620079.1517431239-364404356.1517431239) Locate document part which show Windows driver installation, as you can seen in image below :

![Windows driver](WindowsDriver.PNG)

Then click on "DOWNLOAD THE SPARKFUN SAMD21 WINDOWS DRIVER" in order to download driver. Then click on "instructions in the SAMD21 Breakout hookup guide" to follow driver installation dteps. Finally if you see a small blue blinking led on PCB, you are on your good way !

## 3. Tera Term's downloading and first step
If you don't have any serial terminal on your Windows version, you can download Tera Term's following this [link.](https://osdn.net/projects/ttssh2/downloads/68719/teraterm-4.97.exe/) Start Tera Term's, choose radio bouton *Serial* then click OK. Data should print in real time into the terminal. Pushing space bar on your keyboard will pause or resume data acquistion. You can use following commands to configura the IMU :

    (SPACE) – Pause/resume serial port printing
    t - turn time readings on or off
    a – Turn accelerometer readings on or off
    g – Turn gyroscope readings on or off
    m – Turn magnetometer readings on or off
    q – Turn quaternion readings on or off (qw, qx, qy, and qz are printed after mag readings)
    e – Turn Euler angle calculations (pitch, roll, yaw) on or off (printed after quaternions)
    c – Switch to/from calculated values from/to raw readings
    r – Adjust log rate in 10Hz increments between 1-100Hz (1, 10, 20, …, 100)
    A – Adjust accelerometer full-scale range. Cycles between ± 2, 4, 8, and 16g.
    G – Adjust gyroscope full-scale range. Cycles between ± 250, 500, 1000, 2000 dps.
    s – Enable/disable SD card logging

When you are finished with Tera Terms, don't forget to close it and to remember serial port number you've used (COMx), It will be usefull in Python and Matlab scripts.
