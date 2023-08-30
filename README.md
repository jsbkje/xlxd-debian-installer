# xlxd-debian-installer
This script simply runs through the forked install instructions found [HERE](https://github.com/jsbkje/xlxd). 
The script will install XLX Reflector and Webmin Control panel[HERE](https://github.com/webmin/webmin). 
After installing this you will have a private or public D-Star, DMR, and YSF XLX Reflector with a remote Controll panel which you can access at 
---------XLXD Dashboard-----------
http://"machineip".
---------Webmin Control Panel-----
https://"machineip":10000/ <<--Invalid Certificate Warning is Normal more info can be found at http://webmin.com
--------System Stats Glances Monitor--------
http://"machineip":8081/

XLX now natively supports DMR, D-Star, and C4FM. C4FM and DMR do not require any transcoding hardware (AMBE) to work together. If you plan on using D-Star with any of the other modes, you will need hardware AMBE chips.
********Modified Script to Install on Debian 12 ***********

### To Install:
1. Have a fresh Debian 9,10,11 or 12 computer ready and up to date.
2. Have both a FQDN and 3 digit XLX number in mind before beginning.
3. 
```sh
git clone https://github.com/jsbkje/xlxd-debian-installer
cd xlxd-debian-installer
./xlxd-debian-installer.sh
```
## How to find what reflectors are available
Find a current active reflector dashboard, for example, go to http://k0jeb.asuscomm.com/index.php?show=reflectors and you will see the gaps in reflector numbers in the list. Those reflector numbers not listed are available. 

### To interact with xlxd after installation:
```sh
systemctl start|stop|status|restart xlxd
```
 - Installs to /xlxd
 - Logs are in /var/log/messages and *'systemctl status xlxd'*
 - Main config file is /var/www/xlxd/pgs/config.inc.php
 - Be sure to restart xlxd after each config change *'systemctl restart xlxd'*

**For more information, please visit:**

https://n5amd.com/digital-radio-how-tos/create-xlx-xrf-d-star-reflector/
