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

### Network Setup

```bash title="Set DNS server"
nano /etc/resolv.conf
```

Change `nameserver` to `8.8.8.8`

```bash title="Set IP address and gateway"
nano /etc/network/interfaces
```

### Helper Scripts

Proxmox VE Post Install

:   > This script provides options for managing Proxmox VE repositories, including disabling the Enterprise Repo, adding or correcting PVE sources, enabling the No-Subscription Repo, adding the test Repo, disabling the subscription nag, updating Proxmox VE, and rebooting the system. 

    ```bash
    bash -c "$(wget -qLO - https://github.com/tteck/Proxmox/raw/main/misc/post-pve-install.sh)"
    ```

Home Assistant OS VM

:   > This script automates the process of creating a Virtual Machine (VM) using the official KVM (qcow2) disk image provided by the Home Assistant Team. It involves finding, downloading, and extracting the image, defining user-defined settings, importing and attaching the disk, setting the boot order, and starting the VM. It supports various storage types, and does not involve any hidden installations.

    ```bash
    bash -c "$(wget -qLO - https://github.com/tteck/Proxmox/raw/main/vm/haos-vm.sh)"
    ```