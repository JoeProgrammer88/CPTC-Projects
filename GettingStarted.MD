# Getting Started

These cars have already been assembled and configured. This page will explain the process to connect to the RaspberryPI's on the car and view/modify any existing settings.

## Requirements
1. DonkeyCar (or Raspberry PI with software installed)
2. Cable to connect PI to monitor (Classroom computers use HDMI to DVI)
3. USB Keyboard to plug into Raspberry PI

## Log Into the PI
Username: PI

Password: raspberry

*Note: Linux does not show password characters as you are entering them. Pay close attention as you enter the password
raspberry is also the default password and is not recommended. If the password is different, please refer to physical documentation with the cars*

## Changing/Viewing WiFi Settings

General Raspberry PI settings including WiFi can be set up with

```
    sudo raspi-config
```

Raspi-config is the simple way. Connection settings can also be set using a file. The file for WiFi settings is located at
 /etc/wpa_supplicant/wpa_supplicant.conf

To open up the file with a text editor:
 ```
    sudo nano /etc/wpa_supplicant/wpa_supplicant.conf
 ```

 Make any necessary changes and Ctrl+X will exit the text editor and prompt you to save changes if there are any.

 WiFi Settings in wpa_supplicant.conf
 ```
    country=US
    ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
    update_config=1

    network={
        ssid="<your network name>"
        psk="<your password>"
    }
```

## Enterprise Scenarios: Connecting to a HotSpot
To connect the cars to WiFi in an enterprise setting (like CPTC) you can set up a tablet or Windows 10 machine up as a hotspot. **If the PI only communicates over 2.4 GHz you may need to adjust your WiFi adapter. The default is auto and will most likely default to 5GHz**