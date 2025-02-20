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

### To Set Up a Bridge
For the HA VM to get an IP from my router.
nmcli
Create a bridge.
Add the ethernet connection to the bridge (it's called a slave)
Remove the ethernet connection from the NIC. (Or something)
