# Ala-Carte


## Table of Contents
* [Table of Contents](#TableOfContents)
* [Classes, Objects, and Modules](#Classes.Objects.Modules)
---

## Classes, Objects, and Modules

### Description & Code



```python
import time
import board
from rgb import LED   # import the RGB class from the rgb module

r1 = board.D7
g1 = board.D4
b1 = board.D5

r2 = board.D8
g2 = board.D9
b2 = board.D10

myblueLED1 = LED(b1)
mygreenLED1 = LED(g1)
myredLED1 = LED(r1)

myblueLED2 = LED(b2)
mygreenLED2 = LED(g2)
myredLED2 = LED(r2)

# myRGB1 = RGB(r1,g1,b1)   # create a new RGB object, using pins 3, 4, and 5
# myRGB2 = RGB(r2,g2,b2)   # create a new RGB object, using pins 8, 9, and 10
while True:
    myblueLED1.fade()
    time.sleep(1)
    mygreenLED1.fade()
    time.sleep(1)
    myredLED1.fade()
    time.sleep(1)
    myblueLED2.fade()
    time.sleep(1)
    mygreenLED2.fade()
    time.sleep(1)
    myredLED2.fade()
    time.sleep(1)

```
---------

```python
import time
import board
import pwmio

class LED:

    #note: I had a blue led, so I named my incoming ardument "bluePin"
    def __init__(self, ledPin):
       # init = like void Setup() from arduino.  Initialize your pins here
       # start each object with "self.object"
       self.led = pwmio.PWMOut(ledPin, frequency=5000, duty_cycle=0)

    def fade(self):
        # write your code to make it fade, here
        for i in range(100):
        # PWM LED up and down
            if i < 50:
                self.led.duty_cycle = int(i * 2 * 65535 / 100)  # Up
            else:
                self.led.duty_cycle = 65535 - int((i - 50) * 2 * 65535 / 100)
            print(self.led.duty_cycle)
            time.sleep(0.01)

```

### Images 

<img src="https://github.com/aniyahmoore28/Ala-Carte/blob/main/images/fed%20LED%20Gif.gif" width="250" />

### Reflection

This assignment was confusing but interesting. Making an led fade doesn't seem that hard, but adding classes and all that stuff really makes you think. Using the internet and help from my peers we got it done though. I definitely did get confused many times with the code and understanding what I had to do moving forward with it. The wiring was pretty straight forward, except you need to make sure you identify the rgb and power ends of the led. 







## Next thing

### Description & Code



```C++

```

### Evidence
[]()

### Images 



### Reflection
