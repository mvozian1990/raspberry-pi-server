# raspberry-pi-server

### Setup
1. `sudo apt update`
2. `sudo apt install cups`
3. `sudo usermod -a -G lpadmin pi`
4. `sudo nano /etc/dhcpcd.conf`
  - Edit /etc/dhcpcd.conf file and add the following lines at the end of it:
```
interface wlan0
sttic ip_address=10.0.0.2/27
static routers=10.0.0.1
static domain_name_servers=10.0.0.1
```
5. `sudo cupsctl --remote-any`
6. Find out rasperi's Pi IP address, and go there with port 631
7. In the admin page, add the printer you need
8. Done. Now the printer should be available and vizible on the network
