# VirtualBox

## How to install Debian 12.1 server on VirtualBox under Windows 10
Vido tutorial: [How to install Debian 12 1 server on VirtualBox under Windows 10](https://youtu.be/5SBj0VYWpJE)

Visit Debian download page [www.debian.org/CD/netinst/](https://www.debian.org/CD/netinst/)

## How to install Debian 12.1 server on VirtualBox under Windows 10 part 2

Video tutorial: [How to install Debian 12.1 server on VirtualBox under Windows 10 part 2](https://youtu.be/GIux_IcUESc)

```sh
# chake current IP LAN address
ip a

# ssh login example
ssh developer@192.168.1.207

```

## How to install Debian 12.1 server on VirtualBox under Windows 10 part 3

Video tutorial: [How to install Debian 12.1 server on VirtualBox under Windows 10 part 3](https://youtu.be/qVbwLyB0sJc)

![](./files/How-to-install-Debian-12.1-server-on-VirtualBox-under-Windows-10-part-3-home-cloud-servers-diagram-02.png)

[ExcaliDraw file with diagram ](./files/VirtuaBox-network-bridged-adapter-001.excalidraw)


## Export Virtual Machine to .OVA File in Oracle VM VirtualBox

Video tutorial variant: [https://youtu.be/EYlVYd7xgiE](https://youtu.be/EYlVYd7xgiE)

Open VirtualBox , select wnated virtual machine and pres right mouse click
![](./files/virtualBox-export-ova-file-001.png)

Example export settings
![](./files/virtualBox-export-ova-file-002.png)

Format:
- [x] Open Virtualization Format 2.0

MAC Address Policy: 
- [x] Include all network adapter MAC addresses – keep all MAC addresses assigned on network cards on the virtual machine
Additionally:
- [x] Write Manifest File – this file will automatically check the data integrity and prevent the deployment of damaged appliance.




# Ansible

see DevSharing developer-roadmap ...

source: /mnt/hgfs/D/1-tutorials/Udemy - Mastering ansible in an hour and the half

To use Ansible you need to have on your machine Python 3 or via package, 
for remote machines you need to have python3 too ,but without to install nothing.
Ansible just use integrated modules in Python3 to interact with remote machine


## Install on linux

Use pip in your selected Python environment to install the full Ansible package for the current user:
```
python3 -m pip install --user ansible
```


## Inventory
Inventory is list of Hosts located in /etc/ansible/hosts
Gorups with hosts

```yml
[db]
database.host[1:2]

[webserver]
apache.host1
nginx.host2
```

Flag "-i" is used


## Modules
Modules are tools for particular task
```yml
- name: install Apache
  yam:
    name: httpd-2.2.2-2.2.amzn1
    state: present
```

## Variables
Variables are how we deal with differences betwean systems

## Facts
facts provide information about target host
facts gathering may be disabled

## Playbooks
Playbooks are Ansible's configurations, deployment and orchestration language
Playbooks are expressed in YAML format
The goal of a play is to map a group of some well defined roles

## Configuration Files
ansible.cfg in current directory

# Ad-hock

Ad-hoc is just single module run
check logs
check for packages
gather system information

```
ansible -i inventory 127.0.0.1 - setup
```

Common modules
ping - validate server i up
setup - gather facts
apt - apt package manager
yum - Yum package manager 
service - control system users: start stop and restart services
copy - copy files
file - work with files

Other usage: restart server, add or remove user and users groups, copying files to or from servers, cron jobs,

