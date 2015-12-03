# Thinkpad

## Wifi

Add none free to source.list

```
apt-get install iw firmware-iwlwifi
modprobe -r iwlwifi
modprobe iwlwifi

ip link set wlan0 up
wpa_passphrase BillingskogNyberg >> /etc/wpa_supplicant.conf
wpa_supplicant -B -i wlan0 -c /etc/wpa_supplicant.conf
dhclient wlan0
ip route add default via 192.168.85.1 dev wlan0
```

Add wireless_up script to /usr/local/bin

### SSH keys
Move over keys from
