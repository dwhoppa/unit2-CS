![11e470e9022f4fc5b367429bcbb285bc](https://github.com/comsci-uwc-isak/unit2_2023/assets/53995212/1d14b1d3-ae39-4ef3-8ec9-3329630eacae)

# Unit 2: A Distributed Weather Station for ISAK

## Criteria A: Planning

## Problem definition

Cabbages are members of the Brassicaceae (Cruciferae) family which includes crops such as Kale, Cauliflower, Broccoli and Radish. One of the most widely grown, popular and nutritious vegetables in Japan mainly for the domestic market.The length of the total growing period varies between 90 (spring-sown) and 200 (autumn-sown) days, depending on climate, variety and planting date, but for good production the growing period is about 120 to 140 days. Most varieties can withstand a short period of frost of -6°C, some down to -l0°C. Long periods (30 to 60 days) of -5°C are harmful. The plants with leaves smaller than 3 cm will survive long periods of low temperature but when the leaves are 5 to 7 cm, the plant will initiate a seed stalk and this leads to a poor quality yield. Optimum growth occurs at a mean daily temperature of about 17°C with daily mean maximum of 24°C and minimum of 10°C. Mean relative humidity should be in the range of 60 to 90 percent.Our client owns the Cabbage field, which contains multiple greenhouses. Due to fluctuating temperature and humidity levels, the client struggles to maintain marvellous environmental conditions for their plants. These fluctuations, if not monitored, can lead to plant stress, producing smaller harvests and increasing the vulnerability to pests and diseases. Currently, the client lacks an efficient and working system where he can continuously monitor the changes in temperature and humidity. As a result of this issue, the cabbage field has been suffering massive losses on the harvests, causing stress and frustration among the local farmers. This situation has been noticed by the local businesses, who are extremely concerned and are considering changing their food suppliers as the quantity and quality of the products have decreased. The company's reputation in the local community was being ruined, so they approached us to create a solution. The owner, scared by this situation, requested our services to design a server to address the monitoring of environmental factors and ensure accurate data collection and real-time analysis, allowing fast and proactive actions to reduce risks and better manage the plant's development.


## Proposed Solution
Considering the client requirements an adequate solution includes a low cost sensing device for humidity and temperature and a custom data script that process and anaysis the samples acquired. For a low cost sensing device an adequate alternative is the DHT11 sensor[^1] which is offered online for less than 5 USD and provides adequare precision and range for the client requirements (Temperature Range: 0°C to 50°C, Humidity Range: 20% to 90%). Similar devices such as the DHT22, AHT20 or the AM2301B [^2] have higher specifications, however the DHT11 uses a simple serial communication (SPI) rather than more eleborated protocols such as the I2C used by the alternatives. For the range, precision and accuracy required in this applicaiton the DHT11 provides the best compromise. Connecting the DHT11 sensor to a computer requires a device that provides a Serial Port communication. A cheap and often used alternative for prototyping is the Arduino UNO microcontroller [^3]. "Arduino is an open-source electronics platform based on easy-to-use hardware and software"[^4]. In additon to the low cost of the Arduino (< 6USD), this devide is programable and expandable[^1]. I considered alternatives such diffeerent versions of the original Arduino but their size and price make them a less adequate solution.

Considering the budgetary constrains of the client and the hardware requirements, the software tool that I proposed for this solution is Python. Python's open-source nature and platform independence contribute to the long-term viability of the system. The use of Python simplifies potential future enhancements or modifications, allowing for seamless scalability without the need for extensive redevelopment [^5][^6]. In comparison to the alternative C or C++, which share similar features, Python is a High level programming language (HLL) with high abstraction [^7]. For example, memory management is automatic in Python whereas it is responsability of the C/C++ developer to allocate and free up memory [^7], this could result in faster applications but also memory problems. In addition a HLL language will allow me and future developers extend the solution or solve issues proptly.  

## Design Statement

Our team is developing a program using Arduino and DHT_11 sensors to monitor humidity and temperature required for the 
growing cabbage in greenhouses. The data will be uploaded to a real-time server within 48 hours and accessed via a secure login. This reliable, proven system will be ready within three weeks and will meet our client's needs (done using Pycharm)

## Success Criteria

[^1]: Industries, Adafruit. “DHT11 Basic Temperature-Humidity Sensor + Extras.” Adafruit Industries Blog RSS, https://www.adafruit.com/product/386. 
[^2]: Nelson, Carter. “Modern Replacements for DHT11 and dht22 Sensors.” Adafruit Learning System, https://learn.adafruit.com/modern-replacements-for-dht11-dht22-sensors/what-are-better-alternatives.   
[^3]:“How to Connect dht11 Sensor with Arduino Uno.” Arduino Project Hub, https://create.arduino.cc/projecthub/pibots555/how-to-connect-dht11-sensor-with-arduino-uno-f4d239.  
[^4]:Team, The Arduino. “What Is Arduino?: Arduino Documentation.” Arduino Documentation | Arduino Documentation, https://docs.arduino.cc/learn/starting-guide/whats-arduino.  
[^5]:Tino. “Tino/PyFirmata: Python Interface for the Firmata (Http://Firmata.org/) Protocol. It Is Compliant with Firmata 2.1. Any Help with Updating to 2.2 Is Welcome. the Capability Query Is Implemented, but the Pin State Query Feature Not Yet.” GitHub, https://github.com/tino/pyFirmata. 
[^6]:Python Geeks. “Advantages of Python: Disadvantages of Python.” Python Geeks, 26 June 2021, https://pythongeeks.org/advantages-disadvantages-of-python/. 
[^7]: Real Python. “Python vs C++: Selecting the Right Tool for the Job.” Real Python, Real Python, 19 June 2021, https://realpython.com/python-vs-cpp/#memory-management. 

1. The solution provides a visual representation of the Humidity and Temperature values outside the residences for a period of minimum 48 hours. The issue tackled here is the lack of a real-time monitoring system for tracking fluctuations in temperature and humidity in a cabbage field, which contains multiple greenhouses. This lack of monitoring has resulted in reduced harvest quality and quantity, pest and disease vulnerability, and multiple losses for the farm. By creating a system which can create a visual detailed representation of those fluctuations in the area over a 48-hour period, this will immediately allow our client to take action in order to control the temperature and humidity inside the greenhouses, reducing the losses, and protecting their reputation among the local community. This  monitoring and data analysis system is essential to ensuring the farm maintains ideal conditions for cabbage cultivation.
   
2. ```[HL]``` The local variables will be measured using a set of 2 sensors placed outside. One focused on collecting the temperature values and one focused on collecting the humidity data.
   
3. The solution provides a mathematical modelling for the Humidity and Temperature levels for each Local and Remote locations. ```(SL: linear model)```, ```(HL: non-lineal model)```
These models will allow our client to comprehend the fluctuations on the environmental conditions and take action in order to improve the quality and quantity of their products.

4. The solution provides a comparative analysis for the Humidity, Temperature (HL) levels for each Local and Remote locations including mean, standard deviation, minimum, maximum, and median.
   
5. ```(SL)```The Local samples are stored in a csv file and ```(HL)``` posted to the remote server as a backup.
   
6. The solution provides a prediction for the subsequent 12 hours for Humidity, and Temperature (HL). 
   
7. The solution includes a poster summarizing the visual representations, model and analysis created. The poster includes a recommendation about healthy levels for Humidity, and Temperature(HL). 

## TOK Connection
To what extent does ```the use of data science``` in climate research influence our understanding of environmental issues, and what knowledge questions arise regarding the ```reliability, interpretation, and ethical implications``` of data-driven approaches in addressing climate change

1. How does our use of technology shape our understanding of the environment
   
2. What responsibilities do we have as technologists when it comes to handling personal data related to our living spaces?
   
3. What cultural and contextual factors might impact our interpretation of the results, especially when comparing our local readings with those from the campus? 

# Criteria B: Design

## System Diagram **HL**

![System Diagrams unit 2 (1)](https://github.com/user-attachments/assets/7ec53d20-7afa-4279-8ac2-b5798e38f4db)

**Fig.1** System diagram (HL) for the proposed system to visualize and analyze temperature and humidity data in our campus. Physical variables measured with a network of DHT11/BMP280 sensors locally. A remote server provides and API for remote monitoring and storage via the ISAK-S network. 

Add pic
**Fig.2** 

Add pic
**Fig.3**

## Flow Diagrams

## Record of Tasks
| Task No | Planned Action                                                | Planned Outcome                                                                                                 | Time estimate | Target completion date | Criterion |
|---------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|---------------|------------------------|-----------|
| 1       | Write the Problem context                        | 10min         | Nov 22                 | A         |

## Test Plan

# Criteria C: Development

## List of techniques used

## Development


# Criteria D: Functionality

A 7 min video demonstrating the proposed solution with narration
