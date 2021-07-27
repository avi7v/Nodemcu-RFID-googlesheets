# Nodemcu-RFID-googlesheets

Things needed:
* Nodemcu
* RFID reader and cards
* jumper wires
* led
* buzzer
* Led display

![Click here for the connection](https://github.com/avi7v/Nodemcu-RFID-googlesheets/blob/main/1.jpg?raw=true)

After connecting the wires, connect the nodemcu, download all the files and open arduino code in ArduinoIDE.

Dowloand :
* arduino code https://github.com/avi7v/Nodemcu-RFID-googlesheets/blob/main/nodemcu_rfid_excel.ino
* google script code https://github.com/avi7v/Nodemcu-RFID-googlesheets/blob/main/GoogleScript.js
* RFID RC522 lib https://github.com/miguelbalboa/rfid
* liquid crystal for esp family lib https://github.com/lucasmaziero/LiquidCrystal_I2C

here is a video of how to include the lib into arduino.
https://www.digikey.com/en/maker/blogs/2018/how-to-install-arduino-libraries

Steps to prepare google sheet: 
* create new google sheets called LOG and enter UID, Name, Access, Text in the ROW
![Click here for the connection](https://github.com/avi7v/Nodemcu-RFID-googlesheets/blob/main/2.jpg?raw=true)
* click tools and open script editor 
![Click here for the connection](https://github.com/avi7v/Nodemcu-RFID-googlesheets/blob/main/3.jpg?raw=true)
* copy and paste the code from googlescrpt https://github.com/avi7v/Nodemcu-RFID-googlesheets/blob/main/GoogleScript.js
* change the timezone accordingly ( i had hard time findting the correct zone because the google sheet records different zone from my nodemcu. 
* create new google sheets called Data ID and enter UID,	Name,	Access,	Text in the ROW
* copy the ID in the url of Data ID ( please be focused on this step because this is where i cocked up.)
![Click here for the connection](https://github.com/avi7v/Nodemcu-RFID-googlesheets/blob/main/4.jpg?raw=true)
* plate the Data Id into the var logSpreadSheetId="" in google script page 
![Click here for the connection](https://github.com/avi7v/Nodemcu-RFID-googlesheets/blob/main/5.jpg?raw=true)
* click deploy > new deployment > rfid, me(avi7v@gmai.com), anyone > deploy (try using firefox instead of chrome if googlesheets show some error or delay)
* copy the Deployment ID
* open arduinoIDE and key in your wifi and password into the SSID and PASSWORD and key in the deplyment ID into googlescript id
![Click here for the connection](https://github.com/avi7v/Nodemcu-RFID-googlesheets/blob/main/6.jpg?raw=true)
* IF you read and followed all the steps, your device will be working perfectly!
