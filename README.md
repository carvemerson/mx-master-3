# Mx-master-3
My mouse configuration for Ubuntu.

# Install

**Debian/Ubuntu:**
```bash
sudo apt install cmake libevdev-dev libudev-dev libconfig++-dev
```

**Clone Repository:**
```bash
git clone https://github.com/PixlOne/logiops.git
```

**Build:**
```bash
cd logiops
mkdir build
cd build
cmake ..
make
```
To install, run `sudo make install` after building. You can set the daemon to start at boot by running `sudo systemctl enable logid` or `sudo systemctl enable --now logid` if you want to enable and start the daemon.

**Copy file config**

Enter on mx-master-3 folder and copy file config:

```bash
sudo cp logid.cfg /etc/logid.cfg
```

**Restart the logid**

```bash
systemctl restart logid
```

Check the status

```bash
systemctl status logid
```

# Important!!
Disable the Scroll Lock when using the ABNT2 keyboard.

* Steps:
1. open this file: sudo nano /usr/share/X11/xkb/symbols/br
2. comment the line: "modifier_map Mod3   { Scroll_Lock };"
3. save and reboot.

# References:
https://github.com/PixlOne/logiops/wiki/Configuration

https://gist.github.com/johnathanmay/77e8cfefda6744dca39cb1311bdf741a
