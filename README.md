# SmartClap-Firmware
SmartClap-Firmware is an AI-created firmware which works on an ESP32 and a INMP441 microphone.
This firmware is intented for personal practise and is used to create a solution to switch Shelly devices (on/off or dimmers) in your network by clapping with your hands.
Feet may also work, but set your sensitivity level a little higher.
I am in no way responsible, nor liable for the safety of your network(devices). Please make sure that, when using any network device, that you have full-control over the safety of your own network. 

**Features:**
- The smartclap.local portal lets you set-up five different clap-scenarios which can control up to 5 Shelly devices (via each Shelly IP-address)
- Relais and Dimmer support is available to toggle or set a dimmable % to your lights (if your bulb is also dimmable)
- There is an OTA-update function included which on request checks this Github Repository if there are any new updates available
- When starting up your device, it will set the Noise-Floor in the first 10 seconds and uses a multiplier to calculate the Detection threshold. After that the device will only trigger when a sound is detected above threshold

Sensitivity	Multiplier  Detection threshold

0%	        9,00×      	noise floor × 9

25%	        7,125×	    noise floor × 7,125

50%	        5,25×	      noise floor × 5,25

75%	        3,375×    	noise floor × 3,375

90%	        2,25×      	noise floor × 2,25

100%	      1,50×	      noise floor × 1,5

**Set-up instructions:**
1. Connect the ESP32 to a 5V charging device
2. If not already connected to an available network, the ESP32 will create an own hotspot which you can connect to (_SMARTCLAP sensor AP_)
3. Navigate in your webbrowser to the following address: 192.168.4.1
4. Scan your environment and select your own Wi-Fi network. Fill in your Wi-Fi password
5. When connected, _SMARTCLAP sensor AP_ will dissapear and you can approach your SmartClap in your browser via the following address: smartclap.local
