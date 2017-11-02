# IOT-Compressor
IOTCompressor is a simple air compressor controller and internet pressure gauge

It uses Canvas Gauges to display the gauge on a web page.
https://canvas-gauges.com/

 * PARTS LIST:
 * 1 X ESP-8266 LoLin NodeMCU
 *      https://www.aliexpress.com/item/New-Wireless-module-NodeMcu-Lua-WIFI-Internet-of-Things-development-board-based-ESP8266-with-pcb-Antenna/32656775273.html?spm=a2g0s.9042311.0.0.SYBead
 * 1 X 5V 240V Switch Mode PSU
 * 1 X Pressure Sensor Transmitter DC 5V G1/4 0-1.2 MPa / 0-174 PSI For Water Gas Oil
 *      Model Number:SE0006 from https://www.aliexpress.com/item/Wholesale-price-5-pcs-DC-5V-0-1-2-MPa-pressure-transmitter-water-gas-pressure-sensor/1669537885.html?spm=a2g0s.9042311.0.0.LfHA4n
 * 1 X FORTEK SSR-40DA     
 *      https://www.aliexpress.com/item/24V-380V-40A-250V-SSR-40-DA-Solid-State-Relay-Module-3-32V-DC-To-AC/32604610744.html?spm=a2g0s.9042311.0.0.i7tRzm
 * 1 X 10K resistor     
 * 1 X 15k resistor
 * 
 * The resistors are used for a voltage divider as the sensor outputs 5V and the ESP-8266 is 3.3V I should have used a 10K and 20K however did not haveone on hand.
 * 
 * The sensor and Voltage divider is connected to A0
 * The SSR is connected to D5 
 * 
 * You may need to alter the settings for the wifi side as well as adjust the calibration list for the pressure settings dependent on the PSU you have selected
 * 
 * CONTROLL
 * Its prety simple, Set your base levels in the code. these are
 * float SetPressure = 40.0;
 * float pressureWindow = 5.0;
 * Then log in to the web interface and you can adjust the sliders to change your SetPressure and pressureWindow.
 * SetPressure is the minimum pressure you want
 * pressureWindow is the amount of pressure above your set pressure the pump will pump up to before cutting off.
