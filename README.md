## Instructions

1. Download DietPi image
2. Flash DietPi image

```
dd if=dietpi.img of=/dev/cardidentifier bs=1M status=progress
```

3. Customize configuration files in first partition `/boot` (FAT32)

`dietpi.txt`:

```
AUTO_SETUP_KEYBOARD_LAYOUT=us
AUTO_SETUP_TIMEZONE=America/Indiana/Indianapolis

AUTO_SETUP_NET_ETHERNET_ENABLED=0
AUTO_SETUP_NET_WIFI_ENABLED=1

AUTO_SETUP_NET_WIFI_COUNTRY_CODE=US

AUTO_SETUP_NET_HOSTNAME=phpidash

AUTO_SETUP_SSH_SERVER_INDEX=0

# Install Chromium by default
AUTO_SETUP_BROWSER_INDEX=-2

# Use Chromium kiosk mode for autostart
AUTO_SETUP_AUTOSTART_TARGET_INDEX=11

# Automate initial setup
AUTO_SETUP_AUTOMATED=1

# Install LXDE and Chromium
AUTO_SETUP_INSTALL_SOFTWARE_ID=23 113

SURVEY_OPTED_IN=0

# Adjust Chromium resolution as necessary
SOFTWARE_CHROMIUM_RES_X=1920
SOFTWARE_CHROMIUM_RES_Y=1080
SOFTWARE_CHROMIUM_AUTOSTART_URL=https://night.purduehackers.com/
```

`dietpi-wifi.txt`:

```
aWIFI_SSID[0]='PAL3.0'

aWIFI_KEYMGR[0]='WPA-EAP'

aWIFI_PROTO[0]='RSN'
aWIFI_PAIRWISE[0]='CCMP'
aWIFI_AUTH_ALG[0]='OPEN'
aWIFI_EAP[0]='PEAP'
aWIFI_IDENTITY[0]='purdue username here'
aWIFI_PASSWORD[0]='purdue password here'
aWIFI_PHASE1[0]='peaplabel=0'
aWIFI_PHASE2[0]='auth=MSCHAPV2'
```