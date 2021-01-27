# Board - Speedy Bee F7 AIO

## Description
The Speedy Bee F7 AIO is an AIO flight controller that integrates PDB, Bluetooth chip, Barometer, 32MB OnBoard Flash (Used for BlackBox), 
and users can adjust the parameters of the flight controller using the Speedy Bee App with an integrated Bluetooth chip.

### Hardware Features
* MCU: STM32F722
* IMU: ICM20689
* OSD: BetaFlight OSD w/ AT7456E chip
* BLE Module: inner connect to UART3 for remote setting with SpeedyBee App or other similar apps
* BlackBox: 32MB onboard dataflash
* Current Sensor: 200A(Scale 102)
* BetaFlight Camera Control Pad: Yes
* Power input: 3s - 6s Lipo
* Power output: 5V *5(Including BZ+), the maximum load current is 2.5A. 9V * 1, the maximum load current is 2.5A.
* ESC power output: 4 * VCC output
* UART: UART Pads * 4(UART1, UART2, UART4, UART5)
* RSSI input: RSSI input solder pad
* SmartPort: Use Softserial1 to support SmartPort
* I2C: Used for external Magnetometer, Sonar, etc.
* Buzzer: BZ+ and BZ- pad used for 5V Buzzer
* ESC signal: S1 - S5
* LED pin: Used for WS2812 LED
* Boot button: Used to easy enter DFU mode
* BetaFlight Target: SPEEDYBEEF7




## Description
The Speedy Bee F7 AIO is an AIO flight controller that integrates PDB, Bluetooth chip, Barometer, 32MB OnBoard Flash (Used for BlackBox), 
and users can adjust the parameters of the flight controller using the Speedy Bee App with an integrated Bluetooth chip.
### Hardware Features
* MCU: STM32F722
* IMU: ICM20689
* OSD: BetaFlight OSD w/ AT7456E chip
* BLE Module: inner connect to UART3 for remote setting with SpeedyBee App or other similar apps
* BlackBox: 32MB onboard dataflash
* Current Sensor: 200A(Scale 102)
* BetaFlight Camera Control Pad: Yes
* Power input: 3s - 6s Lipo
* Power output: 5V *5(Including BZ+), the maximum load current is 2.5A. 9V * 1, the maximum load current is 2.5A.
* ESC power output: 4 * VCC output
* UART: UART Pads * 4(UART1, UART2, UART4, UART5)
* RSSI input: RSSI input solder pad
* SmartPort: Use Softserial1 to support SmartPort
* I2C: Used for external Magnetometer, Sonar, etc.
* Buzzer: BZ+ and BZ- pad used for 5V Buzzer
* ESC signal: S1 - S5
* LED pin: Used for WS2812 LED
* Boot button: Used to easy enter DFU mode
* BetaFlight Target: SPEEDYBEEF7

### All uarts have pad on board 
| Value | Identifier   | RX   | TX   | Notes                                                                                       |
| ----- | ------------ | -----| -----| ------------------------------------------------------------------------------------------- |
| 1     | USART1       | PA10  |  PA9 |  PB7 FOR SBUS IN(inverter built-in)                                                         |
| 2     | USART2       | PA3  |  PA2 |  PA3 for SBUS signal through SBUS pad,                                                               and normally connect to RX2 pad for other types receiver |
| 3     | USART3       | PC11 |  PC10|  USE FOR GPS                                                                                |
| 4     | USART4       | PA1  |  PA0 |  PA0 FOR RSSI/FPORT/TEL etc                                                                 |
| 5     | USART5       | PD2  |  PC12|  PAD                                                                                        |

### I2C, use for Barometer or compass
| Value | Identifier   | function |  pin   | Notes                                                                                 |
| ----- | ------------ | ---------| -------| ------------------------------------------------------------------------------------- |                                                                                      
| 1     | I2C1         |    SDA   |  PB9   | 
| 2     | I2C1         |    SCL   |  PB8# Board - Speedy Bee F7 AIO

### Buzzer/LED output 
| Value | Identifier   | function |  pin   | Notes                                                                                 |
| ----- | ------------ | ---------| -------| ------------------------------------------------------------------------------------- |                                                                                      
| 1     | LED0         |    LED   |  PC14  | 
| 2     | BEEPER       |    BEE   |  PC13  | 

### Analog signal input
| Value | Identifier   | function  |  pin  | Notes                                                                                 |
| ----- | ------------ | ----------| ------| ------------------------------------------------------------------------------------- |                                                                                       
| 1     | ADC1         |    VBAT   |  PC2  | 
| 2     | ADC1         |    CURR   |  PC1  | 
| 3     | ADC1         |    RSSI   |  PC3  | 

### 7 PWM Outputs
| Value | Identifier   | function  |  pin  | Notes                                                                                 |
| ----- | ------------ | ----------| ------| ------------------------------------------------------------------------------------- |                                        
| 1     | TIM8_CH1     |    MOTOR1 |  PC6  |  
| 2     | TIM8_CH2     |    MOTOR2 |  PC7  |  
| 3     | TIM8_CH3     |    MOTOR3 |  PC8  |  
| 4     | TIM8_CH4     |    MOTOR4 |  PC9  |  
| 5     | TIM4_CH1     |    CAMERA_CONTROL |  PB6 |  
| 6     | TIM4_CH2     |    LED_STRIP |  PB7  |  DMA1_Stream3

### LED & PPM Input 
| Value | Identifier   | function  |  pin  | Notes                                                                                 |
| ----- | ------------ | ----------| ------| ------------------------------------------------------------------------------------- |                                        
| 1     | TIM5_CH4     |    PPM |  PB0  | 
| 2     | TIM4_CH1     |    LED Strip Signal Input |  PB7  | 


### Gyro & ACC(MPU6000) x
| Value | Identifier   | function |  pin   | Notes                                                                                 |
| ----- | ------------ | ---------| -------| ------------------------------------------------------------------------------------- |                                                                                      
| 1     | SPI1         |    SCK   |  PA5   | 
| 2     | SPI1         |    MISO  |  PA6   | 
| 3     | SPI1         |    MOSI  |  PA7   | 
| 4     | SPI1         |    CS    |  PB11   | 

### OSD(AT7456E)
| Value | Identifier   | function |  pin   | Notes                                                                                 |
| ----- | ------------ | ---------| -------| ------------------------------------------------------------------------------------- |                                                                                      
| 1     | SPI2         |    SCK   |  PB13  | 
| 2     | SPI2         |    MISO  |  PB14  | 
| 3     | SPI2         |    MOSI  |  PB15   | 
| 4     | SPI2         |    CS    |  PB12  |

### 32Mbyte onboard flash
| Value | Identifier   | function |  pin   | Notes                                                                                 |
| ----- | ------------ | ---------| -------| ------------------------------------------------------------------------------------- |                                                                                      
| 1     | SPI3         |    SCK   |  PB3  | 
| 2     | SPI3         |    MISO  |  PB4  | 
| 3     | SPI3         |    MOSI  |  PB5   | 
| 4     | SPI3         |    CS    |  PC0  | 




