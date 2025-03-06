# FlukeServer


## Networking

Fedora
192.168.1.100

### KVM
| VM | IP
|--- | --
| HomeAssistantOS | 192.168.1.101


### Docker
| Container | IP  
| --------- | ---
| Jellyfin  | 192.168.1.110
| PiHole    | 192.168.1.111
| qBitTorrent | 192.168.1.112


# Setup Notes
### Here's the Plan:
Docker containers:
	jellyfin
	pihole
	qbittorrent
	RustDesk
	DuckDNS or something?
	Guacamole?

VM:
	DONE homeassistant




### To Set Up a Bridge
For the HA VM to get an IP from my router.
nmcli
Create a bridge.
Add the ethernet connection to the bridge (it's called a slave)
Remove the ethernet connection from the NIC. (Or something)



### Docker macvlan Networking
Docker networking is all in docker compose. 



# Other Random Notes
### Zooz Dimmer Switch Scene control 
Docs:
https://www.support.getzooz.com/kb/article/1354-how-to-program-scene-control-on-your-zooz-light-switches/

 node_id: X [where X is the node ID of your Zooz switch, which can be found under Configuration > Devices > Zooz Switch] 
 label: Scene 001 [use 001 for top paddle and 002 for bottom paddle]
 value: KeyPressed [KeyPressed = 1 x tap, KeyReleased = released, KeyHeldDown = held, KeyPressed2x = 2 x tap, KeyPressed3x = 3 x tap, KeyPressed4x = 4 x tap, KeyPressed5x = 5 x tap]


### Google Assistant
 If you want to control devices that are connected to Home Assistant primarily, you need https://www.home-assistant.io/integrations/google_assistant/

If you want to control devices that are connected to Google Home primarily you need https://www.home-assistant.io/integrations/google_assistant_sdk/
	This is the one.

### Zwave Stick Causing Boot Loop Fiasco 11/23/2024
In the morning I updated HA. Fine. Then I added the Google Assistant SDK, and set it up. Then I set up and successfully tested an HA automation that turned on white noise on Mason Mini.
Then I don’t know if I restarted HA or not, but it no device could access HA. 
Found it boot looping. Forums hinted at either corrupted SD card, or a usb stick.
It boots fine when the Zwave stick is out.





### Devices
S2 dimmer 800
Zooz ZEN77 800LR
