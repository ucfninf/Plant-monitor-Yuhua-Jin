# Plant Monitor - Typically for Blue Jacket Hyacinthus 
Hello! Welcome to the repository for the Plant Monitoring Device designed to cater to the specific needs of Hyacinthus enthusiasts!

## Overview
In this repository is typically including the work process of connecting and putting togther a plant monitor and realtime code and updated data progresses. in this case we specialized to Blue Jacket Hyacinthus

## Prepare Methods
### Connect to Wifi
 First during the process we are going to set-up and connect te Feather Huzzah ESP8266 Wifi, and to connect the wifi, inlude the ESP8266WiFi library to the board.and connect the wifi where you locate.
 
### Publish sensor data to MQTT Explorer to let it flowing across the web
utilize the arduino file to initialize the built in led.
Connect to the MQTT Exporer, login to cetools.org, and find student/casa0014/plant/ucxxxx/inTopic to publish.


## Build up a customated soil moisture sensors
To begin build up the soil moisture sensor, we learned and understand solding, ways to connect the DHT22 sensor, Huzzah and the cada plant Monitor shied. ![image](https://github.com/ucfninf/Plant-monitor-Yuhua-Jin/assets/146268411/3ceefffe-1980-47d2-ad99-79b93fa2bd8b)

Then, I will need to connect and upload the data, turn on serial monitor on visual data sensoring.
![屏幕截图 2023-10-25 155345](https://github.com/ucfninf/Plant-monitor-Yuhua-Jin/assets/146268411/92457c79-5dc9-4206-aaa0-4e6204cc3b73)
 ![e8087ce2200e276a9bf71e17bdca252](https://github.com/ucfninf/Plant-monitor-Yuhua-Jin/assets/146268411/01c5c7df-6ea7-4149-b7bf-d4f5addcfb91)


Since this sensor is typiclly designed for the plant heathcare of the blue jacket hyacinthus, which its seed will begin to sprout after 2 weeks around in 10 degree celsilous, the monitor is customized that the temperature should be at 10 or below 10 degrees or else the led light will blink, reminding user that its not a suitable environments for the typical flower to grow better.
![jpeg 2](https://github.com/ucfninf/Plant-monitor-Yuhua-Jin/assets/146268411/684100af-ffcc-4f33-8c0e-abe6d78c7d7f)

### Store data on a RPi Gateway
Setting up a Resperry Pi, we need to connect to the terminal and name the RPi
![4a74f8a29f6f2a771865be2e400ffb5](https://github.com/ucfninf/Plant-monitor-Yuhua-Jin/assets/146268411/3bc0ad78-474d-4e24-a791-d25d19ead48e)

set up and sign up InfluxDB to save the MQTT feed data.
set up Telegraf  to use to insert data to the database, running live in the terminal using the config file,for us to manage the plant monitor, and be able to explore the data through the Data Explorer.
![image](https://github.com/ucfninf/Plant-monitor-Yuhua-Jin/assets/146268411/390fd620-adc0-4d23-b89d-f7cca004464d)


### Visualise time series data
Grafana is a tool in helping finally visualize the data, after the generated data from Influx DB, http://stud-pi-ucfninf.local:3000 will demonstrate the time span of the plant monitor durations.
![image](https://github.com/ucfninf/Plant-monitor-Yuhua-Jin/assets/146268411/1d08b54b-bcdc-4fd7-af67-36a27e805fe6)



## Key Features:
- Real-time data monitoring
- Early detection of plant diseases and nutritional deficiencies, and alerts for unfavorable conditions.
- Recommendations for maintaining a balanced and healthy growth environment. 

## Purposes of this idea:
- Plant Health Care: The device aims to offer early - detection of plant diseases and nutritional deficiencies to maintain plant health.
- Maintaining Ecological Balance: Emphasizing the importance of ecological balance to ensure the overall health and vitality of the plants.
- Soil and Environmental Management: The system will provide insights into maintaining the ideal soil and environmental conditions for Blue Jacket Hyacinthus growth.

## Future enhancement:
- To add more functions such as a light exposure sensor, pH level detection, and others to monitor the plant at the next level.

Feel free to contribute, provide feedback, or collaborate on this endeavor towards creating an effective plant monitoring process specifically designed for Hyacinthus lovers!
