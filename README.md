## Project: 05_STM32_ADC_HAL

## Objective: Use the ADC (Analog to Digital Converter) on STM32F446RE to read an analog voltage from pin PA2 and control two LEDs (PA5 and PA6) based on the voltage level.

## Functionality: 
The system reads a voltage between 0V and 3.3V from pin PA2 using 8-bit resolution (which converts the voltage into a digital number between 0 and 255):
- If the voltage is **less than 0.9V** , the LED on **PA5** turns ON, and PA6 turns OFF.
- If the voltage is **0.9V or higher** , the LED on **PA6** turns ON, and PA5 turns OFF.
  VIN = 0.9 volt
  
## Technical Focus: 
Configuring the ADC1 peripheral using the HAL library in polling mode. The project focuses on reading real-world analog signals and using simple "if-else" logic to trigger different digital outputs.

## Key Concepts:
- Understanding how the microcontroller converts analog voltage into a digital number.
- Using 8-bit resolution (values from 0 to 255).
- Using HAL functions: `HAL_ADC_Start`, `HAL_ADC_PollForConversion`, and `HAL_ADC_GetValue`.
- Setting a clean switching point (threshold at value 70) to control two LEDs.

### 📸 Calcul the digital value of VIN (0.9V)  :
<img width="747" height="559" alt="calcul Value of VIN" src="https://github.com/user-attachments/assets/ac4fe50d-a3b2-44fb-9251-4fa93f2e791c" />
