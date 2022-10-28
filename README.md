![](https://img.shields.io/badge/version-v.0.0.1-orange)
[![](https://img.shields.io/badge/Contact_me_in-Telegram-blue.svg)](https://t.me/avkulikoff)
[![](https://img.shields.io/badge/donate-Beer-yellow.svg)](https://www.buymeacoffee.com/ntguest)
[![](https://img.shields.io/badge/donate-Yandex-blueviolet.svg)](https://yoomoney.ru/to/410011383527168)

# Universal Home Assistant docker containers one-click interactive installer
_Also you can get the most popular Universal Home Assistant Supervised one-click installer for all platforms visit [https://hassinstall.top](https://hassinstall.top?ref=2)_

## Description

Let me introduce a one-click install interactive script for home automation and some useful selfhosted services in isolated docker containers.
It fully functional on x86-64 and arm64 architectures (x86 and arm with exeptional, at this moment). Docker and docker-compose will be also installed if nessesary.

## Installation

First of all you need to update system to make sure you have all the latest updates, security patches and required dependacy's installed. To do this, log into the terminal of your machine as a root (su - or sudo su -),  and:

```bash
apt update && apt upgrade -y && apt autoremove -y
```

Install curl if necessary:

```bash
apt-get install curl -y
```

**Run this script at server:**

```bash
curl -sL https://hassinstall.top/getdocker | bash
```

Follow instructions.

## Updating

To update and rebuild all containers change location to docker compose configuration file (/home as default)
```bash
cd /home
```
Run this script as a root
```bash
docker-compose pull && docker-compose up -d && docker image prune
```
____________________________________________________________________________________________
<details>
<summary>Services to be installed</summary>

* ## [Home Assistant](https://www.home-assistant.io)
![](https://img.shields.io/badge/aarch64-yes-green.svg)
![](https://img.shields.io/badge/amd64-yes-green.svg)
![](https://img.shields.io/badge/armv7-yes-green.svg)
![](https://img.shields.io/badge/i386-yes-green.svg)

Open source home automation that puts local control and privacy first. Powered by a worldwide community of tinkerers and DIY enthusiasts.

**Will avaiable at YOUR_SERVER_IP:8123**

* ## [File Editor](https://github.com/CausticLab/hass-configurator-docker)
![](https://img.shields.io/badge/aarch64-yes-green.svg)
![](https://img.shields.io/badge/amd64-yes-green.svg)
![](https://img.shields.io/badge/armv7-yes-green.svg)
![](https://img.shields.io/badge/i386-yes-green.svg)

Configuration UI for Home Assistant.

The HASS-Configurator is a small webapp (you access it via web browser) that provides a filesystem-browser and text-editor to modify files on the machine the configurator is running on. It has been created to allow easy configuration of Home Assistant. It is powered by Ace editor, which supports syntax highlighting for various code/markup languages. YAML files (the default language for Home Assistant configuration files) will be automatically checked for syntax errors while editing.

**Will avaiable at YOUR_SERVER_IP:3218 or Home Assistant panel**

* ## [ESPHome](https://esphome.io/)[^1]
![](https://img.shields.io/badge/aarch64-yes-green.svg)
![](https://img.shields.io/badge/amd64-yes-green.svg)
![](https://img.shields.io/badge/armv7-yes-green.svg)
![](https://img.shields.io/badge/i386-to_do-blue.svg)

ESPHome is a system to control your ESP8266/ESP32 by simple yet powerful configuration files and control them remotely through Home Automation systems.

**Will avaiable at YOUR_SERVER_IP:6052 or Home Assistant panel**

* ## [MariaDB](https://mariadb.org/)
![](https://img.shields.io/badge/aarch64-yes-green.svg)
![](https://img.shields.io/badge/amd64-yes-green.svg)
![](https://img.shields.io/badge/armv7-yes-green.svg)
![](https://img.shields.io/badge/i386-yes-green.svg)

MariaDB Server is one of the most popular open source relational databases. It’s made by the original developers of MySQL and guaranteed to stay open source. It is part of most cloud offerings and the default in most Linux distributions.

* ## [Portainer](https://www.portainer.io/)
![](https://img.shields.io/badge/aarch64-yes-green.svg)
![](https://img.shields.io/badge/amd64-yes-green.svg)
![](https://img.shields.io/badge/armv7-yes-green.svg)
![](https://img.shields.io/badge/i386-yes-green.svg)
  
Portainer's multi-cluster, multi-cloud container management platform supports Kubernetes, Docker, Swarm, and Nomad running in any Data Center, Cloud, Network Edge or IIoT Device. ...

**Will avaiable at YOUR_SERVER_IP:9000 or Home Assistant panel**

* ## [Heimdall Dashboard](https://heimdall.site/)[^2]
![](https://img.shields.io/badge/aarch64-yes-green.svg)
![](https://img.shields.io/badge/amd64-yes-green.svg)
![](https://img.shields.io/badge/armv7-yes-green.svg)
![](https://img.shields.io/badge/i386-no-red.svg)
  
Heimdall Application Dashboard is a dashboard for all your web applications. It doesn't need to be limited to applications though, you can add links to anything you like. There are no iframes here, no apps within apps, no abstraction of APIs. if you think something should work a certain way, it probably does.

**Will avaiable at YOUR_SERVER_IP:8080**

* ## [aaPanel](https://www.aapanel.com/)[^3]
![](https://img.shields.io/badge/aarch64-yes-green.svg)
![](https://img.shields.io/badge/amd64-yes-green.svg)
![](https://img.shields.io/badge/armv7-to_do-blue.svg)
![](https://img.shields.io/badge/i386-to_do-blue.svg)
  
aaPanel is a simple but powerful control panel for linux server.one-click install LNMP/LAMP/OpenLiteSpeed developing environment and software. ... One-click installation of LEMP/LAMP website environment. Become a master of server management easily. aaPanel encapsulates common Linux commands into functional modules, such as creating a website, binding a domain name, reverse proxy, etc. It can be completed in a few clicks on the panel. 

**Will avaiable at YOUR_SERVER_IP:8886/aapanel**
  
**Initial credentials: aapanel/aapanel123**

* ## [Duplicati](https://www.duplicati.com/)[^4]
![](https://img.shields.io/badge/aarch64-yes-green.svg)
![](https://img.shields.io/badge/amd64-yes-green.svg)
![](https://img.shields.io/badge/armv7-yes-green.svg)
![](https://img.shields.io/badge/i386-to_do-blue.svg)
  
Duplicati is free software and open source. You can use Duplicati for free even for commercial purposes. Source code is licensed under LGPL. Duplicati runs under Windows, Linux, MacOS. It requires .NET 4.5 or Mono. Strong encryption. Duplicati uses strong AES-256 encryption to protect your privacy. You can also use GPG to encrypt your backup. Built for online. Duplicati was designed for online backups from scratch. It is not only data efficient but also handles network issues nicely.

**Will avaiable at YOUR_SERVER_IP:8200 or Home Assistant panel** 

* ## [Tailscale](https://tailscale.com/)
![](https://img.shields.io/badge/aarch64-yes-green.svg)
![](https://img.shields.io/badge/amd64-yes-green.svg)
![](https://img.shields.io/badge/armv7-yes-green.svg)
![](https://img.shields.io/badge/i386-yes-green.svg)
  
Tailscale is a zero config VPN for building secure networks. Install on any device in minutes. Remote access from any network or physical location.

* ## [Cloudflare Tunnel](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/)
![](https://img.shields.io/badge/aarch64-yes-green.svg)
![](https://img.shields.io/badge/amd64-yes-green.svg)
![](https://img.shields.io/badge/armv7-yes-green.svg)
![](https://img.shields.io/badge/i386-yes-green.svg)
  
Cloudflare Tunnel provides you with a secure way to connect your resources to Cloudflare without a publicly routable IP address. 

* ## [NextCloud](https://nextcloud.com/)   [^5]
![](https://img.shields.io/badge/aarch64-yes-green.svg)
![](https://img.shields.io/badge/amd64-yes-green.svg)
![](https://img.shields.io/badge/armv7-yes-green.svg)
![](https://img.shields.io/badge/i386-yes-green.svg)
  
A safe home for all your data. Access & share your files, calendars, contacts, mail & more from any device, on your terms ...

**Will avaiable at YOUR_SERVER_IP:8088**

* ## [AdGuard](https://adguard.com)   [^5]
![](https://img.shields.io/badge/aarch64-yes-green.svg)
![](https://img.shields.io/badge/amd64-yes-green.svg)
![](https://img.shields.io/badge/armv7-yes-green.svg)
![](https://img.shields.io/badge/i386-yes-green.svg)
  
AdGuard Home is a network-wide software for blocking ads and tracking. After you set it up, it'll cover all your home devices, and you won't need any client-side software for that.

**Initial setup at YOUR_SERVER_IP:3000 later will avaiable at YOUR_SERVER_IP:8081 or Home Assistant panel**

* ## *[Eclipse Mosquitto](https://mosquitto.org/)*   [^5]
![](https://img.shields.io/badge/aarch64-yes-green.svg)
![](https://img.shields.io/badge/amd64-yes-green.svg)
![](https://img.shields.io/badge/armv7-yes-green.svg)
![](https://img.shields.io/badge/i386-yes-green.svg)
  
Eclipse Mosquitto is an open source (EPL/EDL licensed) message broker that implements the MQTT protocol versions 5.0, 3.1.1 and 3.1. Mosquitto is lightweight and is suitable for use on all devices from low power single board computers to full servers.

* ## *[Zigbee2MQTT](https://www.zigbee2mqtt.io/)*   [^5]
![](https://img.shields.io/badge/aarch64-yes-green.svg)
![](https://img.shields.io/badge/amd64-yes-green.svg)
![](https://img.shields.io/badge/armv7-yes-green.svg)
![](https://img.shields.io/badge/i386-partial-yellow.svg)
  
Allows you to use your Zigbee devices without the vendor's bridge or gateway. It bridges events and allows you to control your Zigbee devices via MQTT. In this way you can integrate your Zigbee devices with whatever smart home infrastructure you are using.

* ## *[Network UPS Tools](https://networkupstools.org/)*   [^5]
![](https://img.shields.io/badge/aarch64-yes-green.svg)
![](https://img.shields.io/badge/amd64-yes-green.svg)
![](https://img.shields.io/badge/armv7-yes-green.svg)
![](https://img.shields.io/badge/i386-yes-green.svg)
  
The primary goal of the Network UPS Tools (NUT) project is to provide support for Power Devices, such as Uninterruptible Power Supplies, Power Distribution Units, Automatic Transfer Switches, Power Supply Units and Solar Controllers. NUT provides a common protocol and set of tools to monitor and manage such devices, and to consistently name equivalent features and data points, across a vast range of vendor-specific protocols and connection media types.

* ## 	*[Rclone](https://rclone.org/)*   [^5]
![](https://img.shields.io/badge/aarch64-yes-green.svg)
![](https://img.shields.io/badge/amd64-yes-green.svg)
![](https://img.shields.io/badge/armv7-yes-green.svg)
![](https://img.shields.io/badge/i386-yes-green.svg)
  
Rclone is a command-line program to manage files on cloud storage. It is a feature-rich alternative to cloud vendors' web storage interfaces. Over 40 cloud storage products support rclone including S3 object stores, business & consumer file storage services, as well as standard transfer protocols.
</details>

[^1]: _Installation in a virtual environment for 32 bit will be available a bit later_
[^2]: _x86-64, arm, arm64 only_
[^3]: _Non Docker installation for x86 and arm will be available a bit later_
[^4]: _On some installations the memory consumption of this container can increase up to 200Mb or more. To control this container from Home Assistant you may use [Monitor Docker](https://github.com/ualex73/monitor_docker) from HACS._
[^5]: _Needs to be improved. I don't use these services. Please let me know if you have working stable configuration of these services._
  
[![Donate](https://img.shields.io/badge/Contact_me_in-Telegram-blue.svg)](https://t.me/avkulikoff)
[![Donate](https://img.shields.io/badge/donate-Beer-yellow.svg)](https://www.buymeacoffee.com/ntguest)
[![Donate](https://img.shields.io/badge/donate-Yandex-blueviolet.svg)](https://yoomoney.ru/to/410011383527168)
