# CPyProjectTemplate
for this project we just needed to make a servo turn  using python
this project was very simple as it was the one of our first project of the year so all we needed was the arduino and the computer and the servo 
here is the code i used:

# SPDX-FileCopyrightText: 2018 Kattni Rembor for Adafruit Industries
#
# SPDX-License-Identifier: MIT

"""CircuitPython Essentials Servo standard servo example"""
import time  #importing all the things
import board
import pwmio
from adafruit_motor import servo

pwm = pwmio.PWMOut(board.A2, duty_cycle=2 ** 15, frequency=50) # this is where we set of the code


my_servo = servo.Servo(pwm) #defining my serco 

while True:
    for angle in range(0, 180, 5):  # tells it how fast to go and where to stop
        my_servo.angle = angle
        time.sleep(0.05) # pauses it for a second 
    for angle in range(180, 0, -5):  # same code just with the values to turn it around            
        my_servo.angle = angle
        time.sleep(0.05)

I didnt have any real problems this project, just had to set up all the wires and the servo in code
