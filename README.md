# TesseractRFIDGUI
This project will be built into a working GUI for OCR and RFID scanner meant to run in conjunction with an ardino and a webcam,  This is a senior project for Cleveland State University and made with help from Zin Technology.

This project is to do the following tasks:<br/>
1. OCR(Optical Character Recognition) of a label. <br/>
2. Reading RFID(Radio Frequency IDentification) on the label. <br/>
3. Sort the data in a meaning way. <br/>
4. Output to a TSV(tab-separated values) file. <br/>

This will all be done in a simple and easy to use GUI(graphical user interface).
# Beginner Tutorial + Project
 #define BLYNK_PRINT Serial


#include <ESP8266WiFi.h>
#include <BlynkSimpleEsp8266.h>

// You should get Auth Token in the Blynk App.
// Go to the Project Settings (nut icon).
char auth[] = "your auth token code from blynk app";

// Your WiFi credentials.
// Set password to "" for open networks.
char ssid[] = "your wifi name";
char pass[] = "your wifi password";

void setup()
{
  // Debug console
  Serial.begin(9600);

  Blynk.begin(auth, ssid, pass);
  // You can also specify server:
  //Blynk.begin(auth, ssid, pass, "blynk-cloud.com", 80);
  //Blynk.begin(auth, ssid, pass, IPAddress(192,168,1,100), 8080);
}

void loop()
{
  Blynk.run();
  // You can inject your own code or combine it with other sketches.
  // Check other examples on how to communicate with Blynk. Remember
  // to avoid delay() function!
}
