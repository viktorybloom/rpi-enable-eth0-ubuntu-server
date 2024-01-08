# rpi-enable-eth0-ubuntu-server
Enable eth0 to run on Raspberry Pi. 

`etc/Netplan/` and edit `.-init.yaml` file with following:
```bash
    ethernets:
      eth0:
        dhcp4: true
        dhcp4-overrides:
          use-dns: false
        nameservers:
          addresses: [127.0.0.1] # Required for docker pihole dns service
        optional: true
```
After saving run `sudo netplan apply`
