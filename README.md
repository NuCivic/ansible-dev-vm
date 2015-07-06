## Usage

Get the [license.lic](https://github.com/NuCivic/nuams-vm/blob/1.1/license.lic)

### VMWare
  1. Install [vmware fusion](http://www.vmware.com/products/fusion/), [Vagrant](https://www.vagrantup.com/downloads.html), and [Ansible](http://docs.ansible.com/intro_installation.html):
    * OSX (VMWare Fusion)
      - Install VMWare Fusion 6
      -  `$ brew install vagrant`
      -  `$ brew install ansible`
    * OS X (virtualbox)
      - `$ brew cask install virtualbox vagrant`
      - `$ brew install ansible`
  2. Install all the roles required by this playbook with the command `$ ansible-galaxy install -r requirements.txt`
  3. Install vmware plugin ``vagrant plugin install vagrant-vmware-fusion``
  4. Install vmware license ``vagrant plugin license vagrant-vmware-fusion license.lic``
  5. Create a config file based on config.yml.sample
  6. Run! ``vagrant up --provider vmware_fusion``


### VirtualBox
  1. Install [Virtualbox](https://www.virtualbox.org/), [Vagrant](https://www.vagrantup.com/downloads.html), and [Ansible](http://docs.ansible.com/intro_installation.html):
    * Ubuntu
      - `$ sudo aptitude install virtualbox ansible vagrant`
  2. Install all the roles required by this playbook with the command `$ ansible-galaxy install -r requirements.txt`
  3. Create a config file based on config.yml.sample
  4. Run! ``vagrant up --provider vmware_fusion``



#### Vagrant ssh

To start this party:

1) type ``vagrant ssh`` to ssh into new box

#### Using browser

1) type ``ifconfig`` in the vm. Grab the IP number from the eth0. for virtualbox this should just be 33.33.33.33. For VMware it wil be something like 192.168.231.132.
2) add the ip address and site name to the /etc/hosts file. type: "sudo vim /etc/hosts" and enter IP_ADDRESS URL for any sites you use on the vm. 

Example:

```
192.168.231.132 nydmv.local
```

for dmv on VMware

