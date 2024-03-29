#  FlyingRC F4WSE MK1.5
links &amp; pinout инструкция по подключению

## Внимание! цвета проводов на разъёмах, мягко говоря, не совсем привычные.  
- STM32F405RGT6, гироскоп ICM-42688-P, барометр SPL06-001,
- Аналоговое/HD OSD, 5xUART, 1xSBUS, 12 ШИМ (6+6), 1I2C, 1ADC (RSSI), 2xPinIO
- Черный ящик: внешний модуль TF-карты, максимальная доступная емкость 4 ГБ, максимальная поддерживаемая емкость 32 ГБ
- Амперметр: непрерывный 40А, мгновенный 80А
- Вход постоянного тока 7–28 В (2–6S LiPo)
- Двa BECa: MP9943+MP9447, 5V2A (оборудование) и 5V4A (сервопривод)
- Используются разъёмы SH1.0 
- Размер и вес: 20 x 40 x 9 мм, 9 г  

ArduPlane **MatekF405-TE**, ArduCopter **MatekF405-TE**, INAV **MatekF405TE_SD**, BF [STM32F405 MTKS F405TE_SD](https://github.com/betaflight/unified-targets/blob/master/configs/default/MTKS-MATEKF405TE_SD.config)  

![Внешний вид](1-general.png)

![вид сверху](2-top.png)
![вид снизу](3-bottom.png)
![разъёмы](4-connectors.png)
![Внешний USB](5-usb.png)
![Внешний TFCard](6-card.png)
![Внешний PWM](7-pwm.png)

Обозначения, T4 это TX UART4, а R1 = RX USART1.

![Датчики](8-pinout.png)

- LED панель WS2812 можно подключать в порт S12 на внешней плате ШИМ
- Порты ШИМ в одной группе не могут одновременно использоваться для Dshot ESC и сервоприводов PWM
- S9~S11 не имеет функции DMA и не может использовать ESC c протоколом DShot.
![PWM/Timers](mcu-pwm.png)

! ! ! Обратите внимание, что в прошивке Ardupilot серийный номер и номер UART/USART не находятся в однозначном соответствии.Таблица соответствия показана ниже! ! !  
- USART2 предназн только для SBUS **(!!!)**, а функции RX2 и TX2 недоступны.
- Устройства с большими объемами данных, такие как приемники CRSF и OSD HD, рекомендуется подключать к портам с функциями DMA, например USART1 (SERIAL1).
![UARTs](mcu-uart.png)

Встроенный барометр занимает адрес 0x76 и не может быть подключен к какому-либо внешнему устройству с адресом 0x76.
![I2C](mcu-i2c.png) 

ADC также можно использовать для внешнего амперметра. PIN 8, как показано в таблице.

- Общие настройки параметров Ardupilot:  
  LOG_BACKEND_TYPE = 1, включите функцию черного ящика TF-карты и записывайте журналы полетов.  
  БАТТ_VOLT_PIN 14  
  BATT_VOLT_MULT 21.0, значение коэффициента вольтметра по умолчанию, ошибка 5%, дополнительная калибровка не требуется  
  BATT_CURR_PIN 15 
  BATT_AMP_PERVLT 39.2, значение коэффициента амперметра по умолчанию, ошибка 10%, требуется дополнительная калибровка  

- Общие настройки параметров INAV:  
 Значение коэффициента вольтметра по умолчанию 2100, погрешность 5%, дополнительная калибровка не требуется.  
 Значение коэффициента амперметра по умолчанию — 255, погрешность — 10 %, требуется дополнительная калибровка.  

![ADC](mcu-adc.png)

