# [ARDU configuration](https://ardupilot.org/plane/docs/common-speedybeef4-v3.html)

## Specifications  
  ### Processor and Sensors  
 - STM32F405 ARM microcontroller
 - V3:BMI270 IMU, V4:ICM42688 (Gyro and Accelerometers)
 - V3:SPL06, V4:DPS310 Barometer
 - AT7456E OSD
### Interfaces
 - 9x PWM outputs (PWM9 for Neopixel LED)
 - 1x RC input (PWM/PPM, SBUS)
 - 6x serial port inputs (including RC input listed above)
 - 1x I2C for external compass or airspeed sensor
 - Micro SD card slot ( you could use any SD card less than 32GB, but the Betaflight can only recognize 4GB maximum )
 - 4 in 1 ESC connector
 - DJI Air Unit connector
 - USB-C connector
### Power
 - 9V ~ 25V DC input power (3S-6S)
 - 5V 2A BEC for peripheral
 - 9V 2A for Video
### Size and Dimensions
 - 41.6mm x3 9.4mm x 7.8mm (30.5mm x 30.5mm mount pattern)
 - 9.6g
### UART
 - UART2 ELRS
 - UART4 Dedicated for Bluetooth connection
 - UART5 Dedicated for ESC telemetry

### Power
 - Input 	3-6S LiPo. The flight controller is powered through the **G**, **V** wires of the **8pin** cable or G, V pads from the bottom side of the flight controller.
 - 5V Output 	9 groups of 5V output, four +5V pads and 1 BZ+ pad( used for Buzzer) on front side, and 4x LED 5V pads. The total current load is 2A.
 - 9V Output 	2 groups of 9V output, one +9V pad on front side and other included in a connector on bottom side. The total current load is 2A.
 - 3.3V Output 	Supported. Designed for 3.3V-input receivers. Up to 500mA current load.
 - 4.5V Output 	Supported. Designed for receiver and GPS module even when the FC is powered through the USB port. Up to 1A current load.
## Pinouts
![top side](https://ardupilot.org/plane/_images/speedybeef4-v3-pinout-top.jpg)
![bot side](https://ardupilot.org/plane/_images/speedybeef4-v3-pinout-bottom.jpg)

