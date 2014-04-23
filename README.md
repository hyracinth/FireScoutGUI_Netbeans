FireScoutGUI_Netbeans
=====================

This folder contains the code for the FireScout client side software. The team consisted of Gabriel Begun, Mikhail Andreev, Jonah Lou, Kelsey Warda and Benjamin Corman.

This code is meant to be ran on a Windows machine and it is coded in Java in Netbeans. The project file has been included and can be edited thus in Netbeans. 


---------
Java code
---------

Code structure:

FireScoutGui
	PingSensor
	TwoWaySerialComm

FireScoutGui holds the designs of the GUI components and their corresponding required actions. It has a TwoWaySerialComm class that allows for the handling of serial communication with your COM ports. 

In addition, FireScoutGui has an nested runnable class called PingSensor, which allows the creation of a thread (if it does not exist already) to ping FireScout for sensor data at the rate of one ping per second. The idea behind this class is the ability to have this running on a separate thread to prevent interference between the main thread. 

The Point of Interest tab is a section that is not fully integrated as it has not been integrated onto FireScout. The idea is to allow the display of the map / points of interests. 

This code requires an XBee connected to one of your COM ports. The first action taken by the code is to prompt a dialog box asking for the COM port the XBee is connected to; if a connection cannot be made, the program will exit. 


------------
Distribution
------------

In the dist folder, you will find an executable jar. This current distribution version has the latest build version (as of 04/23/2014). Simply copy and paste the entire dist folder onto whichever machine you would like to use the client side software on and it will run. The RXTXcomm.jar and rxtxSerial.dll files needs to be located as they currently are. 

In addition, the XBee drivers needs to be installed on your computer. The XBee model that was used for the purpose of this project was XBee PRO 900, however, the XBee model should not deter the program as long as the proper drivers are installed. 


-----------
Other files
-----------

Flight logs are stored under the root folder

There are two files RXTXcomm.jar and rxtxSerial.dll. These files are used to get the TwoWaySerialComm working. 

If you have any other questions feel free to contact me (Jonah) at jonahlou@gmail.com
