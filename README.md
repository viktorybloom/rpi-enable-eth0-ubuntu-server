# rpi-enable-eth0-ubuntu-server
Enable eth0 to run on Raspberry Pi. 

`etc/Netplan/` and edit `.-init.yaml` file with following:
```bash
  network:
    version: 2
    ethernets:
      eth0:
        dhcp4: true
        optional: true
```
