1. Internet is not work after install vpn
```bash
sudo rm /etc/resolv.conf
sudo chattr +i /etc/resolv.conf
sudo restart
```
2. Stop VScode to collect data from user
disable this `Settings > Search "telementry" > Telemetry: Enable Telemetry`
3. Java_Home setup
```bash
sudo apt install openjdk-11-jdk
sudo vim /etc/enviroment
JAVA_HOME="/usr/lib/jvm/java-11-openjdk-amd64"
```
4. Black screen, not booting into GUI desktop
```bash
sudo apt install gdm3 pop-desktop; sudo systemctl enable --now gdm3
```