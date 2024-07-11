# IoT_Project_LowEnergyBluetoothService
Code for the Dev. board that you choose to broadcast Bluetooth services. (not a beacon) Services to broadcast: 1. Temperature Measurement 2. Humidity Either interface the sensor with the development board or just write a function that mimic the sensor behavior in code.
To do this assignment, we will be using an ESP32-development board because it comes with inbuilt BLE support, which is essential for advertisement services such as Temperature Measurement and Humidity.

Steps to Performing the Task
Setting Up Development Environment

Download and install Arduino IDE if not already installed.
Install the ESP32 Board Support in Arduino IDE.
Add Required Libraries

We will be using the BLEDevice library, that provides every principal fundamental function needed to work with BLE.
Create BLE Services and Characteristics

Services would be created for Temperature Measurement and Humidity. Characteristics would also be created for each service to hold the values.  
Simulate Sensor Data

Functions are created which simulate real temperature and humidity readings.  
Advertise the Services

Firstly, the BLE Device would be initialized.  It would start advertising the defined services and characteristics.  
Explanation  
Setup of BLE Device:  

The BLE Device would be initialized with the name, "ESP32_BLE_Device."  A BLE server would be created.  Services and Characteristics:  

A Temperature Service with a Temperature Measurement characteristic would be created.
Create a Humidity Service with a Humidity Measurement characteristic. Simulate Sensor Data: getSimulatedTemperature and getSimulatedHumidity are functions returning random values within a certain range to emulate data from real sensors. Broadcast the Services: Start advertising the services so that they can be discovered by BLE clients. Main Loop: Update the characteristics with simulated data. Optionally notify connected clients. Print the values to serial monitor to be able to debug. Documentation BLEDevice Library: This library makes the basic BLE functionalities available.
BLEService Class: to be used for creating a BLE service.
BLECharacteristic Class: used for creating a BLE characteristic.
BLEAdvertising Class: used to start and manage BLE advertising.
Conclusion
This code sets up an ESP32 and advertises simulated Temperature and Humidity readings via BLE. You can interface real sensors to get actual data by replacing the simulated functions with sensor read functions.
