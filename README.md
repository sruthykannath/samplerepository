# RDKC-WebRTC Integration

Release Source Code [WebRTC 72 branch checkout], prerequisite and steps for testing PC based streamer using webcam.Instructions for running Peercoonection application in two different ubuntu PC as given below.
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. 

## Instructions set up PC streamer(gtk trimmed client with webcam)

-git clone(https://github.com/rdkcteam/native-webrtc)to one ubuntu PC
-Move to the Folder "PC_Streamer" in the local repository
```
cd path to PC_Streamer
````
```
$sudo chmod +x webrtc_cam.sh
```
-Execute the script **webrtc_cam.sh** to install gtk trimmed client
```
./webrtc_cam.sh
```
-connect webcam 
-Move to out folder of webrtc 
```
cd wertc-checkout/src/out/Defaults
```
-Execute 
```
. /peerconnection_Server”
```
-check the following message indicating that server is running:
 ```
 Server listening on port 8888
```
-Take one more command prompt and move to out directory
```
cd wertc-checkout/out/Defaults
```
-Export library path as path to **wertc-checkout/out/Defaults**
```
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:’pwd’(Export path to /out/Defaults)
```
-Run the peerconnection client executable
```
./peerconnection_client
```
-Enter the server address and listening port on command line

## Instructions set up Viewving side (gtk window application)

-git clone(https://github.com/rdkcteam/native-webrtc)to one ubuntu PC
-Move to the Folder "PC_Streamer" in the local repository
```
cd path to PC_Streamer
````
```
$sudo chmod +x webrtc_browser.sh
```
-Execute the script **webrtc_browser.sh** to install client with gtk window for displaying video
```
./webrtc_browser.sh
```
-Move to out/Default folder of webrtc checkout directory
```
cd wertc-checkout/out/Defaults
```
-Export library path as path to **wertc-checkout/out/Defaults**
```
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:’pwd’(Export path to /out/Defaults)
```
-Run the peerconnection client executable
```
./peerconnection_client
```
-Verify gtk window for enering server address and port will display
-Enter the server hosting’s machine IP and listening port to that GTK window.
-Click on connect button.
-Double click on the peer name list down in the window
-Verify the video captured by the webcam connected in another PC display in the GTK window.
