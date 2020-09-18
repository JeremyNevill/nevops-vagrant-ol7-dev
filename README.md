# nevops-vagrant-ol7-dev

Generic and minimal Vagrant Oracle Linux 7 Development machine.

Why https://www.oracle.com/linux/ 7 ? 

... OL7 is used in https://www.oracle.com/cloud/ so a good fit if you are developing for OCI.

***

## Setup

Assuming you have a mac, install the following:

* Homebrew - https://brew.sh/
* VirtualBox - https://www.virtualbox.org/
* Ansible
```
brew install ansible
```
* Vagrant - https://www.vagrantup.com/


## Start

```
vagrant up
```

## Stop

```
vagrant suspend
```

## Destroy

```
vagrant destory
```

## SSH

```
vagrant ssh
```

## Provision (runs ansible playbook)

```
vagrant provision
```

## Connect to with Visual Studio Code

```
vagrant ssh-config
```

* Copy the ssh config 
* Add to the remote ssh section
* Connect to the remote ssh connection and wait as the vagrant box is configured as a remote vs code destination
* When vs code has installed the required server component on the vagrant box you should be able to open folders on the box
* To clone git repos on the vagrant box add your relevant id_rsa key to ~/.ssh and chmod 600
