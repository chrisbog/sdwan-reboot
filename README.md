# sdwan-reboot

## Description
This is a very basic application to query the vManage application within a Cisco SD-WAN (Viptela) Infrastructure. It will return a very basic report to show the reason of the of the last reboot of all sdwan devices within the infrastructure.



## Requirements and Prerequisites
### package_config.ini
The code uses a file called the package_config.ini to house the information about the vManage and the credentials that the application uses.     In the repository, there is a ```package_config.ini.sample``` that you should rename to ```package_config.ini```.   Then modify the package_config.ini to reflect the following information:
* **serveraddress** - Represents the ip address of the vManage server
* **username** -  username of the login credentials on the vManage server
* **password** - password of the login credentials on the vManage server

### python
This demo example is based on Python 3.7 and was tested successfully under that version.

There are two main requirements for external libraries:
* requests
* configparser

You can install these prerequisites by the following commands:
```
pip install requests
pip install configparser
```


## Example Output
```
Viptela vManage Engine Starting...

Viptela Configuration:
vManage Server Address: 172.18.52.16:8443
vManage Username: admin
Retrieving the inventory data from Cisco vManage at 172.18.52.16:8443

2.1.1.1         1564967300000 Software initiated - Kernel Panic
2.1.1.3         1558394019000 Initiated by user - activate 18.3.1
2.1.1.4         1558393999000 Initiated by user - activate 18.3.1
2.1.1.5         1558394273000 Initiated by user - activate 18.3.1
2.1.1.2         1558393747000 Initiated by user - activate 18.3.1
1.1.200.1       1560412117000 PowerOn
1.1.250.1       1557086110000 BootRomUpgrade
1.1.100.1       1560465996000 PowerOn
1.1.135.1       1565624527000 LocalSoft
1.1.250.2       1565793042000 Initiated by user - unpatch
1.1.150.1       1565105378000 Initiated by user
1.1.201.1       1565657629000 Initiated by user - unpin flows triggered reboot

