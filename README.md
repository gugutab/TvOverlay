  
<p align="center">
<picture><img src="https://github.com/gugutab/TvOverlay/blob/main/images/readme_main.png?raw=true" alt="TvOverlay" width="600"></picture>
<br>
<a href="https://play.google.com/store/apps/details?id=com.tabdeveloper.tvoverlay">
<img src="https://github.com/gugutab/TvOverlay/blob/main/images/playstore.png?raw=true" width="300" /></a>
<a href="https://play.google.com/store/apps/details?id=com.tabdeveloper.tvoverlayremote">
<img src="https://github.com/gugutab/TvOverlay/blob/main/images/playstore_remote.png?raw=true" width="300" /></a>	
</p>

<span><p align="center">Elevate your Android TV experience with TVOverlay – the ultimate app that turns your TV into an information hub like never before. Whether you're a casual viewer or a tech enthusiast, TVOverlay enhances your TV content by overlaying essential information and giving you complete control over its appearance.</p></span>

<p align="center">
<a href="https://www.youtube.com/watch?v=mdsY084-pr8">
<img src="https://github.com/gugutab/TvOverlay/blob/main/images/youtube_gif.gif?raw=true" /></a>
</p>
<p align="center">
Watch it on YouTube: https://www.youtube.com/watch?v=mdsY084-pr8
</p>
<p align="center">
  <a href="#key-features">Key Features</a> •
  <a href="#how-to-use">How To Use</a> •
  <a href="#premium-features">Premium Features</a> •
  <a href="#use-cases">Use cases</a> •
  <a href="#issues-suggestions--feature-requests">Issues, suggestions & feature requests</a>
</p>

  ## Key Features
1. **Clock:**  
Stay on schedule with our clock feature, and as a premium user, personalize it to match your style. Choose from a variety of colors and text options to make it uniquely yours.  
<p align="center">
  <img src="https://github.com/gugutab/TvOverlay/blob/main/images/clock.jpg?raw=true" />
<br><em>Default clock being displayed at the corner of the screen</em>
</p>

2. **Notifications:**  
Receive notifications from multiple sources, including your Android phone (with TvOverlay Remote app), REST API, and Home Assistant. TVOverlay offers three default notification layouts – Default, Minimalist, and Icon Only – to suit your preferences. Premium users can even design their own notification layouts for a truly tailored experience.
<p align="center">
  <img src="https://github.com/gugutab/TvOverlay/blob/main/images/not1.gif?raw=true" />
  <img src="https://github.com/gugutab/TvOverlay/blob/main/images/not2.gif?raw=true" />
  <img src="https://github.com/gugutab/TvOverlay/blob/main/images/not3.gif?raw=true" />
<br><em>Sample notifications for Default, Minimalist and Icon Only layouts</em>
</p>
  
3. **Fixed Notifications:**  
Keep important information at a glance with fixed notifications. These compact alerts remain visible in the corner of your TV screen for a specified time or until you dismiss them.
<p align="center">
  <img src="https://github.com/gugutab/TvOverlay/blob/main/images/fixed.jpg?raw=true" />
<br><em>Fixed notification examples for: Phone battery ; Light On; Twitch channel online</em>
</p>
  
4. **Overlay Background:**  
Control the ambiance with our background layer, which sits between overlay content and your TV content. Could be used to artifically change the TV brightness without dealing with menus. Premium users enjoy additional customization options.
<p align="center">
  <img src="https://github.com/gugutab/TvOverlay/blob/main/images/background.gif?raw=true" />
<br><em>Example of background visibility going to 50%, then 95% and back to 0%</em>
</p>

5. **Control everywhere & Presets for Efficiency:**  
Manage TvOverlay effortlessly using its companion app, TvOverlay Remote. Alternatively, control it via Rest API or MQTT, making it compatible with Home Assistant and your smart home ecosystem. Save time and effort with Presets, to apply multiple settings at once and streamline your experience.   
<p align="center">
  <img src="https://github.com/gugutab/TvOverlay/blob/main/images/control.gif?raw=true" />
<br><em>TvOverlay being controlled by TvOverlay remote (left) and Home Assistant via MQTT (Right)</em>
</p>
  
## Premium Features
On TvOverlay Remote, users can have access to Premium features by purchasing a one-time In-app product. This purchase unlocks:
* **Multiple devices:** be able to control multiple TvOverlay devices on the same remote app
* **Customization:** personalize Notifications, Clock & Background. Change colors, font styles and more
* **Presets:** create new presets to apply multiple settings at once
* Helps the developer to continue working on this project :)
<p align="center">
  <img src="https://github.com/gugutab/TvOverlay/blob/main/images/customization1.jpg?raw=true" width="200" />
  <img src="https://github.com/gugutab/TvOverlay/blob/main/images/customization2.jpg?raw=true" width="200" />
  <img src="https://github.com/gugutab/TvOverlay/blob/main/images/customization3.jpg?raw=true" width="200" />
	<br><em>Clock & background customization (Left) and Notification customization (middle and right)</em>
</p>

## How To Use

1. Install TvOverlay on your AndroidTv via [PlayStore](https://play.google.com/store/apps/details?id=com.tabdeveloper.tvoverlay)

2. Run TvOverlay and finish all setup steps: 
	- Draw over other apps permission: 
 		Permission required to create an overlay. Depending on the Android version and manufacturer this option may not be available on a system setting menu. In this case, you will have to enable it via ADB command. After [enabling ADB on your AndroidTV](https://www.youtube.com/watch?v=qcpl8SzWzb8), you can send the command using TvOverlay Remote or any other app or computer software that sends ADB commands. The ADB command is:
   
   	    *adb shell appops set com.tabdeveloper.tvoverlay SYSTEM_ALERT_WINDOW allow*

	- Battery optmization:
		This step is optional, but recommended to avoid the app being killed by the system. If you cannot access the system option to disable battery optimizationn, you may have to enable it via ADB command. After [enabling ADB on your AndroidTV](https://www.youtube.com/watch?v=qcpl8SzWzb8), you can send the command using TvOverlay Remote or any other app or computer software that sends ADB commands. The ADB command is:

	    *adb shell dumpsys deviceidle whitelist +com.tabdeveloper.tvoverlay*
   
3. (optional) Install TvOverlay Remote on an android device via [PlayStore](https://play.google.com/store/apps/details?id=com.tabdeveloper.tvoverlayremote)
	- Make sure that you both devices are on the same network and connect it by scanning the QR code on TvOverlay main screen, or connect mannualy by input its host and IP.
	- (Optional) On *Notification*, you can give permission to mirror your device notifications to TvOverlay.
	
4. (optional) Connect to MQTT server
	- If you have a MQTT server running, you can connect your TvOverlay device to it to control its main functions. On the TvOverlay or TvOverlay Remote app, find the MQTT option and fill your server information.
	- On TvOverlay app MQTT settings you can enable *Display status on change* to better debug if you have problems.
	- If you are using MQTT on Home Assistant, a new device will be created on connection. By default, it will be named *TvOverlay - [Device Model]*
	
5. (optional) Connect to Home Assistant
	- Follow the samples on the [Home Assistant section](https://github.com/gugutab/TvOverlay/blob/main/home_assistant/configuration_sample.yaml) to be able to send Notifications, Fixed Notifications and manage all the settings.

6. (optional) Import Postman Collection
	- For better understanding of the Rest API, you can import Postman a collection of samples in the [Postman section](https://github.com/gugutab/TvOverlay/blob/main/home_assistant/configuration_sample.yaml)
	- Be sure to modify the Variables to the correct host and port.

## Use cases
| Description | Plataform | Image| Link |
|---|---|---|---|
| Notification on person arrive | Home Assistant | <img src="https://github.com/gugutab/TvOverlay/blob/main/images/person.jpg?raw=true" /> | [🔗](https://github.com/gugutab/TvOverlay/blob/0de278111002079452fd96c5662b4ea09f6c3729/home_assistant/notification_samples.yaml#L21-L41) |
| Notification with image when a motion is detect in a camera | Home Assistant | <img src="https://github.com/gugutab/TvOverlay/blob/main/images/motion.jpg?raw=true" /> | [🔗](https://github.com/gugutab/TvOverlay/blob/0de278111002079452fd96c5662b4ea09f6c3729/home_assistant/notification_samples.yaml#L43C1-L68C13) |
| Fixed notification for phone battery | Home Assistant | <img src="https://github.com/gugutab/TvOverlay/blob/main/images/battery.jpg?raw=true" /> | [🔗](https://github.com/gugutab/TvOverlay/blob/0de278111002079452fd96c5662b4ea09f6c3729/home_assistant/fixed_notification_samples.yaml#L20C1-L36C13) |
| Fixed notification indicating light on | Home Assistant | <img src="https://github.com/gugutab/TvOverlay/blob/main/images/lights.jpg?raw=true" /> | [🔗](https://github.com/gugutab/TvOverlay/blob/0de278111002079452fd96c5662b4ea09f6c3729/home_assistant/fixed_notification_samples.yaml#L20C1-L36C13) |
| Fixed notification indicating twitch channel online | Home Assistant | <img src="https://github.com/gugutab/TvOverlay/blob/main/images/twitch.jpg?raw=true" /> | [🔗](https://github.com/gugutab/TvOverlay/blob/0de278111002079452fd96c5662b4ea09f6c3729/home_assistant/fixed_notification_samples.yaml#L64-L87) |
| Fixed notification indicating weather | Home Assistant | <img src="https://github.com/gugutab/TvOverlay/blob/main/images/weather.jpg?raw=true" /> | [🔗](https://github.com/gugutab/TvOverlay/blob/0de278111002079452fd96c5662b4ea09f6c3729/home_assistant/fixed_notification_samples.yaml#L89-L123) |
| Darker screen after sunset; reseting after sunrising | Home Assistant with MQTT| <img src="https://github.com/gugutab/TvOverlay/blob/main/images/background.gif?raw=true" /> | [🔗](https://github.com/gugutab/TvOverlay/blob/0de278111002079452fd96c5662b4ea09f6c3729/home_assistant/background_samples.yaml#L3-L31) |

## Issues, suggestions & feature requests
For Issues, suggestions & feature requests, [create a Issue](https://github.com/gugutab/TvOverlay/issues).
