## Instructions


1. Download DietPi image
2. Flash DietPi image

```
dd if=dietpi.img of=/dev/cardidentifier bs=1M status=progress
```

3. Customize configuration files in first `/boot` (FAT32)

`dietpi.txt`:

```
AUTO_SETUP_KEYBOARD_LAYOUT=us
AUTO_SETUP_TIMEZONE=America/Indiana/Indianapolis

AUTO_SETUP_NET_ETHERNET_ENABLED=0
AUTO_SETUP_NET_WIFI_ENABLED=1

AUTO_SETUP_NET_WIFI_COUNTRY_CODE=US

AUTO_SETUP_NET_HOSTNAME=phpidash


```

`dietpi-wifi.txt`:

- Set `aWIFI_SSID[0]` to Wi-Fi SSID
- Set `aWIFI_KEY[0]` to Wi-Fi password