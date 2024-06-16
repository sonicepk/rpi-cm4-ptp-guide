# My pins

The pins need to be connected as follows:

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
