# Plant Monitor - Blue Jacket Hyacinth
Hello! Welcome to the repository for the Plant Monitoring Device designed to cater to the specific needs of Hyacinthus enthusiasts!

## Overview
In this repository is typically including the work process of connecting and putting togther a plant monitor and realtime code and updated data progresses. in this case we specialized to Blue Jacket Hyacinthus.

## Purposes of this idea:
- Plant Health Care: The device aims to offer early - detection of plant diseases and nutritional deficiencies to maintain plant health.
- Maintaining Ecological Balance: Emphasizing the importance of ecological balance to ensure the overall health and vitality of the plants.
- Soil and Environmental Management: The system will provide insights into maintaining the ideal soil and environmental conditions for Blue Jacket Hyacinth's growth.

## User-Centric Approach
- The main idea of building this plant monitor is mainly for real-time data monitoring, act for early detection of plant diseases and nutritional deficiencies, and alerts for unfavorable conditions, and recommendations for maintaining a balanced and healthy growth environment.
- Anticipated end user: this plant monitor is mainly designed for home gardeners and Plant Enthusiasts: Individuals who enjoy gardening at home or have a passion for cultivating plants are a primary target audience. The system caters to their desire for a more informed and connected approach to plant care, offering real-time insights and recommendations for optimal growth conditions.

### Conditions
Hyacinth bulbs normally plant in the fall, about 4-6 weeks before the ground freezes. This allows them to establish roots before winter.
- Temperature: The bulbs need the cool of winter to simulate their natural environment and encourage proper sprouting in the spring.
- Soil: well-draining soil, preferably enriched with organic matter. Avoid waterlogged or overly wet soil.

## Key Features:
- Real-time data monitoring
- Early detection of plant diseases and nutritional deficiencies, and alerts for unfavorable conditions.
- Recommendations for maintaining a balanced and healthy growth environment.
  
## Prepare Methods
### Connect to Wifi
 First during the process we are going to set-up and connect te Feather Huzzah ESP8266 Wifi, and to connect the wifi, inlude the ESP8266WiFi library to the board.and connect the wifi where you locate.
 
### Publish sensor data to MQTT Explorer to let it flowing across the web
utilize the arduino file to initialize the built in led.
Connect to the MQTT Exporer, login to cetools.org, and find student/casa0014/plant/ucxxxx/inTopic to publish.


## Build up a customated soil moisture sensors with Huzzah ESP8266
To begin build up the soil moisture sensor, we learned and understand solding, ways to connect the DHT22 sensor, Huzzah and the casa plant Monitor shield. ![image](https://github.com/ucfninf/Plant-monitor-Yuhua-Jin/assets/146268411/3ceefffe-1980-47d2-ad99-79b93fa2bd8b)


Next is to connect and upload the data, turn on serial monitor on visual data sensoring.
![屏幕截图 2023-10-25 155345](https://github.com/ucfninf/Plant-monitor-Yuhua-Jin/assets/146268411/92457c79-5dc9-4206-aaa0-4e6204cc3b73)
 ![e8087ce2200e276a9bf71e17bdca252](https://github.com/ucfninf/Plant-monitor-Yuhua-Jin/assets/146268411/01c5c7df-6ea7-4149-b7bf-d4f5addcfb91)


*This plant monitor is designed for specific plants, and users re-edit the Arduino code of the plant and the growing conditions required at each stage. In this blog, the test object I chose is hyacinth, which is currently in the bulb stage and needs to be activated in an environment with a temperature of ten degrees Celsius before it can germinate.

This sensor is typiclly designed for the plant heathcare of the blue jacket hyacinthus, which its seed will begin to sprout after 2 weeks around in 10 degree celsilous, the monitor is customized that the temperature should be at 10 or below 10 degrees or else the led light will blink, reminding user that its not a suitable environments for the typical flower to grow better.
![jpeg 2](https://github.com/ucfninf/Plant-monitor-Yuhua-Jin/assets/146268411/684100af-ffcc-4f33-8c0e-abe6d78c7d7f)

### Store data on a RPi Gateway
Setting up a Resperry Pi, we need to connect to the terminal and name the RPi
![4a74f8a29f6f2a771865be2e400ffb5](https://github.com/ucfninf/Plant-monitor-Yuhua-Jin/assets/146268411/3bc0ad78-474d-4e24-a791-d25d19ead48e)
![Process 2023-11-01 105536](https://github.com/ucfninf/Plant-monitor-Yuhua-Jin/assets/146268411/a24b5237-5169-4693-8b61-31358b577081)
set up and sign up InfluxDB to save the MQTT feed data.
set up Telegraf  to use to insert data to the database, running live in the terminal using the config file,for us to manage the plant monitor, and be able to explore the data through the Data Explorer.
![image](https://github.com/ucfninf/Plant-monitor-Yuhua-Jin/assets/146268411/390fd620-adc0-4d23-b89d-f7cca004464d)


### Visualise time series data
Grafana is a tool in helping finally visualize the data, after the generated data from Influx DB, http://stud-pi-ucfninf.local:3000 will demonstrate the time span of the plant monitor durations.
![image](https://github.com/ucfninf/Plant-monitor-Yuhua-Jin/assets/146268411/1d08b54b-bcdc-4fd7-af67-36a27e805fe6)

![屏幕截图 2023-11-16 013023](https://github.com/ucfninf/Plant-monitor-Yuhua-Jin/assets/146268411/d0d24a4d-d609-4518-bcd3-70bd5c7e0384)

Also try to place the plant and the plant monitor in different temperatures, retrieved temperature data shown as follow:
![plant monitor NOV12-15](https://github.com/ucfninf/Plant-monitor-Yuhua-Jin/assets/146268411/8d606b4c-b2fb-4c1c-8fc6-ff0813f23945)

## Future enhancement:
- The next stage is to build a multi Led or Sensors to output a more advanced development to the plant monitor. 
- The user can create an LED screen at the next stage after the germination of the plant. 
- To add more functions such as a light exposure sensor, detects for over or less watered soils, and others to monitor the plant at the next level. 

Despite adding the corresponding function and code testing about the light exposure and moisture level and the temperature, I am also thinking about implement from the diode to a display such as add a smile face and a sad face whenever the plant is in the right environmental condition or not. 

### And finally, 
Feel free to contribute, provide suggestion and feedback, or collaborate on this endeavor towards creating an effective plant monitoring process specifically designed for Hyacinthus lovers or even other type of plants!
