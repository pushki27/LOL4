import RPi.GPIO as GPIO
from time import sleep

GPIO.setmode(GPIO.BCM)
GPIO.setup(17, GPIO.IN)

while True:
    if GPIO.input(17):
        print("Motion Detected!")
    sleep(0.5)

GPIO.cleanup() 
