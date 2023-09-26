  
<h1 align="center">
  <br>
<img src="https://github.com/gugutab/TvOverlay/blob/main/images/tvOverlayIcon_banner.jpg?raw=true" alt="TvOverlay" width="600">
  <br>
  TvOverlay
  <br>
</h1>

<h4 align="center">Elevate your Android TV experience with TVOverlay – the ultimate app that turns your TV into an information hub like never before. Whether you're a casual viewer or a tech enthusiast, TVOverlay enhances your TV content by overlaying essential information and giving you complete control over its appearance.</h4>

<p align="center">
  <a href="#key-features">Key Features</a> •
  <a href="#how-to-use">How To Use</a>
</p>

![screenshot](https://github.com/gugutab/TvOverlay/blob/main/images/Screenshot_20230920_142821.png?raw=true)

## Key Features
1. **Control:**  
Manage TvOverlay effortlessly using its companion app, TvOverlay Remote. Alternatively, control it via Rest API or MQTT, making it compatible with Home Assistant and your smart home ecosystem.  
  
2. **Notifications:**  
Receive notifications from multiple sources, including your Android phone (with TvOverlay Remote app), REST API, and Home Assistant. TVOverlay offers three default notification layouts – Default, Minimalist, and Icon Only – to suit your preferences. Premium users can even design their own notification layouts for a truly tailored experience.  
  
3. **Clock:**  
Stay on schedule with our clock feature, and as a premium user, personalize it to match your style. Choose from a variety of colors and text options to make it uniquely yours.  
  
4. **Fixed Notifications:**  
Keep important information at a glance with fixed notifications. These compact alerts remain visible in the corner of your TV screen for a specified time or until you dismiss them.  
  
5. **Overlay Background:**  
Control the ambiance with our background layer, which sits between overlay content and your TV content. Could be used to artifically change the TV brightness without dealing with menus. Premium users enjoy additional customization options.  
  
6. **Presets for Efficiency:**  
Save time and effort with preset configurations. TvOverlay comes with two presets, and premium users can create and save their own. Apply multiple settings at once to streamline your experience.  
  


## How To Use

 1. Install TvOverlay on your AndroidTv via [PlayStore](https://play.google.com/store/apps/details?id=com.tabdeveloper.tvoverlay)

2. Run TvOverlay and finish all setup steps: 
	- Overlay permission: //TODO description
	- Battery optmization: //TODO description
	
2. (optional) Install TvOverlay Remote on an android device via [PlayStore](https://play.google.com/store/apps/details?id=com.tabdeveloper.tvoverlayremote)
	- Make sure that you both devices are on the same network and connect it by scanning the QR code on TvOverlay main screen, or connect mannualy by input its host and IP.
	- (Optional) On *Notification*, you can give permission to mirror your device notifications to TvOverlay.
	
2. (optional) Connect to MQTT server
	- If you have a MQTT server running, you can connect your TvOverlay device to it to control its main functions. On the TvOverlay or TvOverlay Remote app, find the MQTT option and fill your server information.
	- On TvOverlay app MQTT settings you can enable *Display status on change* to better debug if you have problems.
	- If you are using MQTT on Home Assistant, a new device will be created on connection. By default, it will be named *TvOverlay - [Device Model]*
	
2. (optional) Connect to Home Assistant
	- Follow the samples on the [Home Assistant section](https://github.com/gugutab/TvOverlay/blob/main/home_assistant/configuration_sample.yaml) to be able to send Notifications, Fixed Notifications and manage all the settings.

2. (optional) Import Postman Collection
	- For better understanding of the Rest API, you can import Postman a collection of samples in the [Postman section](https://github.com/gugutab/TvOverlay/blob/main/home_assistant/configuration_sample.yaml)
	- Be sure to modify the Variables to the correct host and port.
