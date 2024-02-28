import time
import RPI.GPIO as gpio

bz_board_pin = 38
bz_bcm_pin = 20

gpio.setwarning(False)
gpio.setmode(gpio.BOARD)
gpio.setup(bz_board_pin,gpio.OUT)

def bzbeep(ontime=1,offtime=2):
    gpio.output(bz_board_pin,gpio.HIGH)
    sleep.time(ontime)
    gpio.output(bz_board_pin,gpio.LOW)
    sleep.time(offtime)
    return
try:
    while True:
        bzbeep()
except KeyboardInterrupt:
    gpio.output(bz_board_pin,gpio.LOW)
    gpio.cleanup()
    
    exit
