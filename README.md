# JNPRztplic

This script installs the license information on a Juniper device based on the serial number of the device. 

The script expects the license file for the device to be lcoated on the HTTP server in the following format. 

DeviceSerial.csv

For example,
PD3713490661.csv

The script will download this file from HTTP server and install it on the device. 

This is an operations script that can be run as part of the JUNOS ZTP process. 

Overview of the ZTP process with this script
- ZTP process installs OS and the new config
- An Pseudo event is generated every three minutes according to this configuration
- When this event is generated, this script is called as a response to the generated event
- The script finds the serial number of the switch, locates the file on the HTTP server and installs the license on the device

For this script to work, ensure that the license files for all the devices should be stored on the http server in the format stored earlier. 
