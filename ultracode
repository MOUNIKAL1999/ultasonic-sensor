#author:mounika L
#Program to measure the distance of any object using Raspberry pi Library 

import RPi.GPIO as GPIO                                  #Importing GPIO Function from RPi Module as GPIO 
import time                                                 #Importing time module for giving a time delay 
GPIO.setmode(GPIO.BCM)                                        # Setting Raspberry Pi GPIO as a BCM Mode (GPIO numbers) 
TRIG = 23 ECHO = 24                                     #In TRIG=23 equal to pin number 16 and ECHO =24 equal to pin number 18
print("Distance Measurement In Progress") 
GPIO.setup(TRIG,GPIO.OUT) 
GPIO.setup(ECHO,GPIO.IN) 

GPIO.output(TRIG, True)
time.sleep(0.00001)                     #setting the delay time (seconds)
GPIO.output(TRIG, False) 
while GPIO.input(ECHO)==0:
      pulse_start = time.time() 
while GPIO.input(ECHO)==1: 
      pulse_end = time.time() 
pulse_duration = pulse_end - pulse_start
distance = pulse_duration * 17150
distance = round(distance, 2) 
print("Distance:",distance,"cm") 
GPIO.cleanup() 



