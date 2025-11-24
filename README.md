🌦️ STM32 Weather Station Pro

This project is a real-time embedded weather monitoring system built using the STM32F4 microcontroller.
It reads environmental parameters such as:

🌡️ Temperature (DHT22)

💧 Humidity (DHT22)

🔆 Light Intensity (LDR)

🌧️ Rain Level (Analog + Digital Detection)

The collected data is displayed on an I2C LCD (PCF8574 + 16×2 LCD) and sent over UART for logging or external processing.

A SysTick timer triggers periodic sensor reads, while a buzzer and LED provide alerts for rain conditions.

This firmware uses direct register-level programming (no HAL), ensuring fast and efficient operation.
