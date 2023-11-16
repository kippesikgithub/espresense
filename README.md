# Espresense setup/config
Espresense config and screenshots  

## Setup and configure Espresense
- install espresense on an ESP32 (esp32 including bluetooth offcourse)  
- add the esp32 containing espresense to your wifi network
- go to the config of the esp32 (espresense) device, and at least fill in the room name and mqtt settings (see image 1)
- click on 'edit other settings' and configure the filter and/or calibration part. the IBeaconID/UUID you can for example get from your HA companion app (see setup and configure HA companion app, image 2)

![image](https://github.com/kippesikgithub/espresense/assets/100353268/803ce9aa-2d57-43a0-abc2-a4271531c817)  
Image 1  

![image](https://github.com/kippesikgithub/espresense/assets/100353268/f4cdfb3e-1ef7-47b7-90e4-14c5169a4112)  
Image 2

## Setup and configure HA companion app
- install the HA companion app, or you already have it
- browse to settings, companion app
- go to maintain sensors
- scroll to the bluetooth sensors section (image 2)
- Switch on the BLE Transmitter sensor
- copy your UUID, you can use those for the recognition of the devices by adding IBeacon: in front of the UUID. (image 4, number 3)
- put measured power/reception somewhere between -80 and -85 (my best practices for android phones) (image 4, number 1)
- transmitting power from 'very low' to 'low' (image 4, number 2)

![image](https://github.com/kippesikgithub/espresense/assets/100353268/60a4b6cc-d3e6-46a4-90b8-05ef0eebd5cd)  
Image 3   

![image](https://github.com/kippesikgithub/espresense/assets/100353268/3ee3082d-650f-4158-803f-46d95958fb11)  
Image 4  

## Extra Info or Best practises
- I created scripts, that turn of or on the blw transmitter, based on the location of the phone. When leaving the 'home' zone, HA will switch of the BLE transmitter on the phone, entering the 'home' zone, will turn on the BLE transmitter. Using Notification command for these scripts. https://companion.home-assistant.io/docs/notifications/notification-commands/
- The more espresense (esp32) devices, the more accurate
