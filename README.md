# thingspeak-monitoring
This project demonstrates how to monitor and analyze humidity and temperature data using a NodeMCU ESP8266 and a DHT11 sensor, with data visualization provided by the ThingSpeak IoT platform and the ThingView mobile app.

Project Components
A list of required hardware and software for this project includes:

Hardware

NodeMCU ESP8266 with a Micro-USB cable 

DHT11 temperature and humidity sensor 

Jumper wires 

Software and Services

Arduino IDE 

ThingSpeak IoT Web Server 

ThingView IoT App 

Necessary libraries for the Arduino IDE, including "ThingSpeak Communication Library" and "DHT sensor library" 


System Architecture and Functionality
The DHT11 sensor is connected to the NodeMCU to collect temperature and humidity readings. The NodeMCU, in turn, connects to a Wi-Fi network to transmit this data to a ThingSpeak channel. The block diagram shows the DHT11's data pin connected to pin D1 on the NodeMCU.





The system operates as follows:

The 

setup() function in the Arduino code initializes the serial communication, connects the NodeMCU to the specified Wi-Fi network, and begins the DHT sensor readings .

In the main 

loop(), the device continuously reads the humidity and temperature from the DHT11 sensor.

These readings are then sent to two separate fields in a ThingSpeak channel using a unique Channel ID and Write API Key. A 2-second delay is added between each reading to manage the data upload frequency.




The data is then visualized in real-time on the ThingSpeak platform, which provides charts for both temperature and humidity.

Users can also monitor the data on a smartphone using the ThingView app, which connects to the ThingSpeak channel.
