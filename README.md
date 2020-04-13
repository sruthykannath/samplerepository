# WebRTC PC Streamer

Release Source Code [WebRTC 72 branch checkout], prerequisite and steps for testing PC based streamer using webcam. Instructions for running Peer connection application in two different ubuntu PC as given below.
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. 

## Instructions set up PC streamer (gtk trimmed client with webcam)

1. git clone (https://github.com/rdkcteam/native-webrtc)to one ubuntu PC
2. Move to the Folder "PC_Streamer" in the local repository
```
cd path to PC_Streamer
````
```
$sudo chmod +x webrtc_cam.sh
```
3. Execute the script **webrtc_cam.sh** to install gtk trimmed client
```
./webrtc_cam.sh
```
-connect webcam 
4. Move to out folder of webrtc 
```
cd wertc-checkout/src/out/Defaults
```
5. Execute 
```
. /peerconnection_Server”
```
6. check the following message indicating that server is running:
 ```
 Server listening on port 8888
```
7. Take one more command prompt and move to out directory
```
cd webrtc-checkout/out/Defaults
```
8. Export library path as path to **webrtc-checkout/out/Defaults**
```
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:’pwd’(Export path to /out/Defaults)
```
9. Run the peerconnection client executable
```
./peerconnection_client
```
10. Enter the server address and listening port on command line

## Instructions set up Viewing side (gtk window application)

1. git clone (https://github.com/rdkcteam/native-webrtc)to one ubuntu PC
2. Move to the Folder "PC_Streamer" in the local repository
```
cd path to PC_Streamer
````
```
$sudo chmod +x webrtc_browser.sh
```
3. Execute the script **webrtc_browser.sh** to install client with gtk window for displaying video
```
./webrtc_browser.sh
```
4. Move to out/Default folder of webrtc checkout directory
```
cd wertc-checkout/out/Defaults
```
5. Export library path as path to **webrtc-checkout/out/Defaults**
```
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:’pwd’(Export path to /out/Defaults)
```
6. Run the peer connection client executable
```
./peerconnection_client
```
7. Verify gtk window for entering server address and port will display

8. Enter the server hosting’s machine IP and listening port to that GTK window.

9. Click on connect button.

10. Double click on the peer name list down in the window.

11. Verify the video captured by the webcam connected in another PC display in the GTK window.

