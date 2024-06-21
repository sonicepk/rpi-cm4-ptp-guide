# My pins

The Ublox pins need to be connected as follows:

| GPS pin no | u-blox pin name | IO header | header pin no | header pin name | description |
| --- | --- | --- | --- | --- | --- |
| 1 | VCC_ANT | HAT | 2 | 5V | Antenna power |
| 2 | VCC | HAT | 1 | 3V3 | Operating power for GPS |
| 3 | TXD | HAT | 10 | UART0_RXD | GPS to CM4 |
| 4 | RST | HAT |  | | Reset - not connected |
| 5 | RXD | HAT | 8 | UART0_TXD | CM4 to GPS |
| 6 | TP1 | J2 | 9 | SYNC_OUT | Time pulse |
| 7 | TP2 | HAT | 12 | GPIO18 | Time pulse 2 - only on RCB-F9T |
| 8 | GND | HAT | 6 or 14 | GND | Ground |

Pin 1 supplies power to the antenna; the precise range of allowed voltages depends on the board. All boards appear to accept a range of 3.3-5V.


https://www.pi4j.com/1.3/pins/rpi-cm4.html

On J2 we want SYNC_IN (PIN 8 on J2) from the 1pps on the UBlox. When you connect the 1PPS(TP) to SYNC_IN on the CM4 the 1PPS led stops flashing on the UBlox. 

https://wiki.radxa.com/Rock3/CM3/raspcm4io/gpio#:~:text=3%20GPIO%20number-,General%20purpose%20input%2Doutput%20(GPIO)%20connector,pin%20is%20distinguished%20by%20color.

The CM4 GPIO PINS 
1 - 3.3V
6 - GND
8 - GPIO0_D1	UART2_TX_M0 GPIO 25
10 - GPIO0_D0	UART2_RX_M0			24


