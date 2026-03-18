# 🚗 Arduino OLED Car Monitor (Battery + Coolant + Oil Temp)

A compact Arduino-based vehicle monitoring system using an SSD1306 OLED display.  
Designed for real-time display of:

- 🔋 Battery voltage  
- 🌡️ Coolant temperature (CLT)  
- 🛢️ Oil temperature (logarithmic sensor calibration)  

Includes a startup logo screen and a visual coolant temperature bar with overheat warning.


## 🧰 Hardware Requirements

- Arduino (Uno / Nano / compatible)
- SSD1306 OLED Display (128x64, I2C)
- NTC temperature sensors:
  - Coolant sensor
  - Oil temperature sensor
- Voltage divider (for battery monitoring)
- Resistors (for biasing sensors)


---

## 🔌 Wiring

| Function        | Arduino Pin |
|----------------
| Battery input  | A3         
| Coolant sensor | A1         
| Oil sensor     | A2        
| PWM output     | D9         
| OLED SDA       | A4         
| OLED SCL       | A5         






Features in this code, that you can adjust : 
1. Resistance-Temperature relation of the sensor in 
- 5 point table for oil sensor 
- 3 point table for coolant sensor. 
2. Bias resistors (the analog measuring circuit consists of two resistors one of them being the sensor and second one is a bias resitor)
3. Greeting image (you can paste your own bitmap in the code. Bitmap can be generated in imagetoCpp webpage) 
4.Voltage divider ratio for the voltage measurement circuit ( you can fine tune the voltage reading until correct) 
5. Coolant alarm (if the value exceeds certain threshold it will make the coolant bar on the display blink. 
