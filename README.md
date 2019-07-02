# Automatically Unplug usb device before Sleep and after Resume Plug it back in. 

Sometimes this is usefull.

### Installing

Locate the correct driver under: /sys/bus/usb/drivers/usb/

It will disappear when you unplug the usb device.

Edit the .service file to match your device.

```
git clone https://github.com/ericwoud/unplug-sleep-resume-plug.git
cd unplug-sleep-resume-plug/
sudo cp unplug-sleep-resume-plug.service /etc/systemd/system/
sudo systemctl daemon-reload
sudo systemctl enable unplug-sleep-resume-plug.service
sudo systemctl start  unplug-sleep-resume-plug.service
```

