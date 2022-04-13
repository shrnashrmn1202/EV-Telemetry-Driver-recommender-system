# EV-Telemetry-system
A Recommender &amp; Telemetry system for improvement of Electric Vehicle and driver’s performance analysis for the Formula Student event. The project was set-up to help the racing team at Brunel University London https://www.brunelracing.com/formula-student-electric/ in car's and driver's analysis by developing a data acquisition system (currently using Bosch C60 data logging system). A reliable DAQ system and monitoring system is proposed to the team as a useful tool for vehicle analysing and improvement. The sensors are:
1. Temperature - Tyre temperature & Battery temperature of EV
2. Ultrasonic - Suspension of car
3. GPS - Speed and position of car on track
4. Accelerometer - Acceleration of car 

![image](https://user-images.githubusercontent.com/100325884/159704121-501fa5e3-d4fd-401d-819d-5a63e138491f.png)

![image](https://user-images.githubusercontent.com/100325884/159601784-94f12a0c-00dc-4705-844a-7b1714a019f3.png)

![image](https://user-images.githubusercontent.com/100325884/159704518-91fec712-58b4-4e6e-9579-b0b85920d653.png)

![image](https://user-images.githubusercontent.com/100325884/159704874-3d86afe0-5931-461a-a718-32e94f1b9a1d.png)

The measurements read by sensors is processed with Arduino and sent to ThingSpeak.  ThingSpeak receives data from sensor through ESP8266 Wifi module by serial communication

The following training experiment was created in Microsoft Azure Machine Learning 
![image](https://user-images.githubusercontent.com/100325884/159705624-30be16bb-6657-4ca2-b276-f323a67cf2db.png)

After training experiment, Predictive experiment (using Multiclass Decision Forest) was perfomed. 
![image](https://user-images.githubusercontent.com/100325884/159705892-68aa2576-8025-4540-b2cf-180745b5267d.png)

A web service will test the input values to give a predicted results for the driver. For example, input the values of speed, acceleration, shock absorbance, and tyre temperature then predict if driver drives as normal (N), safe driving (SD) or danger (D). Based on this, the suitable driver for specific event can be selected.

Key features of project: 
1. Telemetry system is built and tested. Real-time results are obtained where data is logged on channel every 15 seconds. Data visualized on ThingSpeak are of real data obtained from CV testing. 
2. System that allows for more functionality and flexibility to the old system: Add CAN shield for more sensors to be visualized
3. Convincing based on results obtained from configuration of sensor and Wifi module made also results from Thingspeak. Can be verified later once BR0E car is built and tested
4. Overall cost for telemetry unit is £73
