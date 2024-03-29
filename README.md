Also on gist
> https://gist.github.com/fruitgum/d562f4c6b699728c82e8a6ad1d68a50d

# lenovo-E15-fingerprint


Manual how to activate fingerprint on Lenovo E15 Gen 4

Tested on *__Ubuntu 23.04 lunar__* with fingerprint device *__27c6:550a__ - Shenzhen Goodix Technology Co.,Ltd. FingerPrint*


# Step-by-step
1. Find your device ID with lsusb:
   ```
   user@lenovo:~$ lsusb
   Bus 004 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub
   Bus 003 Device 003: ID 0bda:4853 Realtek Semiconductor Corp. Bluetooth Radio
   Bus 003 Device 002: ID 27c6:550a Shenzhen Goodix Technology Co.,Ltd. FingerPrint --- This's our reader
   Bus 003 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
   Bus 002 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub
   Bus 001 Device 002: ID 30c9:0057 Luxvisions Innotech Limited Integrated RGB Camera
   Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
   ```
2. Install/update fprintd
   ```
   sudo apt update
   sudo apt intsall fprintd
   ```
3. Dowload driver
   > https://download.lenovo.com/pccbbs/mobiles/r1slg01w.zip
   
   Mirror:
   > https://mega.nz/file/wysAlaza#X1MukixHyDNk326-0S5GX0c-j5DmyduVbSG-UmLrdHo

   Second mirror:
   > https://github.com/fruitgum/lenovo-E15-fingerprint-27c6-550a/releases/tag/latest
4. Unpack it and install
   ```
   sudo dpkg -i libfprint-2-tod-goodix_amd64.deb
   ```
5. Now fingerprint login is available
   
   You can enroll your fingerprint either with fprintd-enroll or via Settings>User
