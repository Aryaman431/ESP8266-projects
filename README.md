# INTRODUCTION 
  This project falls under the subject **Internet of things** . This project is based on **ESP8266** also referd to as **NodeMCU** a microcontrollers which is abel to connect to the internet and is user friendly.
  This project consists of a DHT11 sensor, a 16X2 LCD display, a servo motor(SG90) and a cloud server (I used Blynk but you can use ThingSpeak as well). I made a device which senses the room temperature and displays the collected data to the user remotely over the internet.
# Working of the project
  When the DHT11 sensor collects data and sends it over to the NodeMCU which is connceted to the internet the microcontroller sends the data over to the cloud server.
  This data can be accessed by us using the Blynk applications on our laptops or phones. The data is also printed on a LCD screen which is attached to the device . Now what if the device is plcaed in a storage facility which has fresh produce and the temperature has risen enogh to spoil the produce here' where the servo motor comes in play.
  The purpose for the servo motor is that it turns on flips a switch on and off when we manually send a signal from the Blynk applications remotely.We have to use a bunch of libraries in order for our device to function at all, we use the `ESP8266WiFi.h`(for being able to connect ESP8266 to the internet),`BlynkSimpleEsp8266.h`(for being able to use Blynk application),`DHT.h`(for being able to use the DHT11 sensor),`Servo.h`(to use the servo motor) and `LiquidCrystal.h`(for the LCD display).
  Also make sure that your ESP is connected to a different internt connection than you laptop.
# How to Run# How to Run
  In your **arduino IDE** go to file and then preferences then in the additional boards manager url paste :https://arduino.esp8266.com/stable/package_esp8266com_index.json. 
  Paste the code `temperature and humidity` in your **arduino IDE** make sure you have downloaded all the libraries from the library tab before using them in your code.
  Connect the components together(i used ChatGPT for the connections)
  ### For the DHT sensor
    ESP     DHT
    3v       vcc
    GND      GND
    D4       DATA
  ### For the servo motor
      Servo                       ESP
      VCC (Red)                  	3.3V or Vin (5V)
      GND (Black/Brown)	          GND
      Signal (Yellow/Orange)	    D3 (GPIO0)
  ### For the LCD display 

      ![WhatsApp Image 2025-02-05 at 01 46 47_18a5c5e3](https://github.com/user-attachments/assets/75550fc0-d408-4d16-a035-91c695232646)

# Results
  The results should look like this
  ### LCD
      
      ![WhatsApp Image 2025-02-05 at 01 00 05_259d2d55](https://github.com/user-attachments/assets/e3984ec7-a654-4afa-b086-f5465604a2a9)
  ### Blynk application (both phone and laptop)
      
      ![WhatsApp Image 2025-02-05 at 01 00 06_8f9c97b5](https://github.com/user-attachments/assets/2e6aafb6-3bb0-4e51-888f-b2426fddb64a)
      
      ![WhatsApp Image 2025-02-05 at 01 01 07_19f2c414](https://github.com/user-attachments/assets/461d6054-6a57-4baf-b758-af2c583b53f8)
  ### Serial monitor

      ![image](https://github.com/user-attachments/assets/bceebc31-136d-44d2-8e8f-55301e57f560)
  ### The servo motor

      ![Demo]()



     
