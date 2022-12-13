# NodeMCU and MQTT Protocol
### Introduction to MQTT Protocol and code to demonstrate its working  
<br/>  

***Overview :***  
This repository gives the basics of [MQTT Protocol](https://mqtt.org/) in a way easily understandable by a beginner. It also contains a small demo code for using MQTT with [Adafruit IO](https://io.adafruit.com/) and NodeMCU-ESP8266.  
<br/>

***About MQTT :***  
MQTT is a light weight *Publish and Subscribe* Protocol that provides for a two way communication between the IoT device and the MQTT Hosting Server. There is a feed of data that is being sent and received by devices. All the devices that are *Subscribed* to that particluar stream will recieve the value in case the server sends any data into the stream. In a similar fashion, All the devices that can *Publish* to a stream will keep posting new data to the feed, which will now be received by all the devices that are subscribed.  
<br/>

***The main components of MQTT Protocol :***  
- MQTT Client - The device that either can either publish/subscribe to the feed.
- MQTT Broker - The server which hosts the MQTT Dashboard
<br/>  
  
Popular IoT cloud Dashboard providers like [Adafruit IO](https://io.adafruit.com/), [Blynk](https://blynk.io/), [Arduino Cloud](https://create.arduino.cc/iot), etc. have support for MQTT Protocol in their services. Let's now dive deep into using the MQTT Protocol using NodeMCU Development Board.  
<br/>  

## Demo code for MQTT Protocol using Adafruit IO

***Components Required :***  
- NodeMCU-ESP8266 - Any generic NodeMCU would do just fine
- LED - any colour
- Breadbaord and Jumper Wires (Male to Female)  
<br/>

***Software Requirements :***  
- Arduino IDE ([Download](https://www.arduino.cc/en/software))
- Adafruit IO ([Register](https://io.adafruit.com/))  
<br/>  

***Getting Started with NodeMCU :***  
Refer to my other repository ([this one](https://github.com/Bharadwaj-R/NodeMCU-and-Arduino-Cloud)) in case you need to learn the very basics of NodeMCU. Once you get a basic understanding of how a NodeMCU works, and are comfortable with the coding part, then proceed further with setting up the Arduino IDE.  
<br/>

***Setting up the Arduino IDE Environment :***  
A few additional libraries are required in order to work with MQTT and Adafruit IO. Install all the assiciated dependencies along with the main libraries. Refer [this link]() for a clear step by step guide in installing these libraries. Below is the list of all the required libraries.  
- `Adafruit IO Arduino` by Adafruit  
- `Adafruit MQTT Library` by Adafruit  
- `ArduinoHttpClient` by Arduino  

***Setting up the Adafruit IO Dashboard :***  
- Once you register in the Adafruit IO website, head over to the `Feeds` subsection.  
- Click on the `New Feed` button. Name the feed as `LEDbutton`. Now click on the `Create` button.
- Once done, head over to the `Dashboards` section and click on the `New Dashboard` option.
- Name the dashboard and select `Create`.
- Once done, open the newly created dashboard. Select the small gear icon on the top right, and select `Create New Block` option.
- From the new window, select the "On-Off buttion" block. 
- Select the previously created feed, and go to the next step.
- Assign 0 for OFF and 1 for ON and create the block.
<br/>  

