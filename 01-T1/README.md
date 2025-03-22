#  config F4WSE_MK1.5

| | | | | | | | | | | | | | | |
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|BAT| | |SBUS| 5V|GND|TX6|RX6|TX1|RX1| | | VTX|Vbat|Gnd|
| - | | |RSSI| 5V|GND|TX5|RX5|TX3|RX3| | | CAM|Vbat|Gnd| 
|ESC| | | | | | | | | | | | S1|+5|Gnd|   
| - | | | | | | | | | | | | S2|+5|Gnd| 
|   | | | | | | | | | | | | | 
|ESC| | | | | | | | | | | | S3|+5|Gnd| 
| + | | | | | | | | | | | | S4|+5|Gnd| 
|BAT| | |    |   |GND|io1|io2|4v5|BZ-| | | S5|+5|Gnd| 
| + | | |    |RX4|TX4|SCL|SDA|4v5|GND| | | S6|+5|Gnd| 

- USART2 (wDMA)-> Serial6 -> IBUS  (+5,Gnd,Rx6)
- USART6 (wDMA)-> Serial5 -> Telemetry (Tx5)
- USART1 (wDMA)-> Serial1 -> OSD HD (Tx1,Rx1,Vbat,Gnd)
- UART4 (noDMA)-> Serial4 -> GPS Ublx7 (Gnd,Rx4, Tx4, 4v5) 
- UART5 (noDMA)-> Serial3 -> ()
- UART3 (noDMA)-> Serial2 -> ()
- S1 - ESC Left
- S2 - ESC Right
- S3 - Elevator
- S4 - Aileron Left
- S5 - Aileron Right
- S6

- (4v5,	BZ) - Buzzer

- S7
- S8
- S9
- S10
- S11
- S12 - LED strip



#  config SPEEDYBEE WING MINI

|  |  |  |  |  |  |  |  |  |    |
|- | -| -| -| -| -| -| -| -| -  |
|S9|S8|S7|S6|S5|S4|S3|S2|S1|SBUS|
||Gim|  |Pith||Ele|Ele |Mot |Mot |    |
||bal|  |  |   |Left|Righ|Left|Righ|    |


USB VCP MSP  
UART1 Serial RX  
UART2   
UART3 GPS  
UART4  
UART5  DisplayPort  
UART6 MSP  


![](https://store-fhxxhuiq8q.mybigcommerce.com/product_images/img_SpeedyBee_F405_WING_MINI/SB_F405-WING-MINI-16.jpg) 

