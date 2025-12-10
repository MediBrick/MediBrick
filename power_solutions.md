# Power Control Solutions

## Breakout Boards
| Source | Link | Voltage | Amperage | Logic| Cost |
| --- |--- |--- |--- |--- | --- |
| Amazon L298N |[Link](https://a.co/d/1e84QhE)|  5-35V | 2A | 5V | $3.50
| Amazon BTS7960 | [Link](https://a.co/d/3osQzfE) | 6V-27V | 43A | 3.3-5V|  $7
| Amazon DRV8871 | [Link](https://a.co/d/hwcKjuL) | 6.5-45V| 3.6A | 1.8-5V |  $4.50
| Pololu Simple Motor Driver| [Link](https://www.pololu.com/product/1365)| 6.5-50V| 12A| USB |$135
| Pololu 8874 | [Link](https://www.pololu.com/product/4035) | 37V | 2.1A | 1.8-5V | $12
| Pololu 8876 | [Link](https://www.pololu.com/product/4036) | 37V | 1.3A | 1.8-5V | $9
| Sparkfun L298| [Link](https://www.sparkfun.com/sparkfun-ardumoto-motor-driver-shield.html) | 46V | 2A |3.3-5V| $25
| Sparkfun TB6612| [Link](https://www.sparkfun.com/tb6612-1-2a-dc-stepper-motor-driver-breakout-board.html)|  15V | 1.2A | 5V | retired
| Adafruit DRV8833| [Link](https://www.adafruit.com/product/3297) | 10V | 2A | | $6
| Adafruit DRV8871| [Link](https://www.adafruit.com/product/3190)| 6.5-45V | 3.6A| 1.8-5V | $7.50

## Discrete Builds

### IR2113 driver and Infinion IRF3205
*obsolet design*

requires 12V gate driver
IRF3205 55V, 110A, 8mOhm
requires careful timing
external current Senses
higher switching rates

Optimizations with replacement parts

Bridge: 
AOI4184 (40V, 50A, 8mOhm), 
BSC340N08(80V,7/23A 34mOhm), 
IPB017N10N5 (100V, 180A, 1.7mOhm)

Gate Driver:
IRS200x (IRS2005, 20V, 100kHz, no disable)
IRS210x (IRS2110STRPBF) 
HIP4081A

### Smart H Bridge Infinion BTS7960 / BTN7970 / BTN8982
*breakout board available*

builtin protection, simpler
BTS7960 45V, 44A, 25kHz, 30mOhm, 5V logic, current sense
BTN7970 45V, 44A, 25kHz, 30mOhm, 5V logic, current sense
BTN8982 40V, 44A, 25kHz, 20mOhm, 5V logic, current sense (newer)

requires 3V to 5V logic buffer with TI SN74HCS244 to operate with 3.3V microcontrollers

P = I*R*I = 160*0.02 = 3.2 W heat @ 40A

### Integrated H Bridge DRV8874 / DRV8876 / DRV887x
*breakout board available*

Easy to use
builtin current limit or current sense
simple interface

DRV8871 6.5V - 45V, 3.6A, protection, current limiter
DRV8876 4.5 - 37V, 3.5A, 700mOhm, 1.8-5V logic, current sense output
DRV8874 4.5 - 37V, 6A, 200mOhm, 1.8-5V logic, current sense output

P = I*R*I 36*0.2 = 7.2 W heat @ 6A