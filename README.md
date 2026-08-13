Components:
1. Wiring and Hardware Setup:

    ESP32-C3 with MPU6050:
        Connect the MPU6050 to the ESP32-C3 using I2C:
            MPU6050 SDA (Data): Connect to ESP32-C3 GPIO21 (or another pin that supports I2C SDA).
            MPU6050 SCL (Clock): Connect to ESP32-C3 GPIO21 (or another pin that supports I2C SCL).
            Power: Connect VCC to 3.3V or 5Vand GND to GND.
    ESP32-C3 with Servo:
        Connect the control pin of the servo to a GPIO pin on the ESP32-C3 (e.g., GPIO1).
        Power the servo with an appropriate external power source (many servos require 5V).

2. Software and Communication:

    ESP-NOW Communication:
        Set up ESP-NOW on both ESP32-C3 devices.
        The device with the MPU6050 will send sensor data (like angle or acceleration) over ESP-NOW to the second device.
        The second ESP32-C3 will receive this data and move the servo accordingly.
