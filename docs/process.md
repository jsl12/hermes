# Setup Process

## HA OS on Raspberry Pi

[Home Assistant installation](https://www.home-assistant.io/installation/)

> Home Assistant Operating System: Minimal Operating System optimized to power Home Assistant. It comes with Supervisor to manage Home Assistant Core and Add-ons. Recommended installation method.

[Full instructions](https://www.home-assistant.io/installation/raspberrypi#install-home-assistant-operating-system)

- Download the [Raspberry Pi Imager](https://www.raspberrypi.com/software/).
- Use it to install HA OS on a USB stick, following these prompts
    - Other specific-purpose OS
    - Home assistants and home automation
    - Home Assistant
    - Home Assistant OS X.X (RPi 4/400)
- Boot the RPi from the USB stick and follow installation prompts

## Proxmox

- Download the latest proxmox ISO file from [here](https://www.proxmox.com/en/downloads/proxmox-virtual-environment/iso)
- Use [Rufus](https://rufus.ie/en/) to write it to a USB stick
- Boot the machine from the USB stick and follow the installation prompts