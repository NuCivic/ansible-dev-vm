## Usage

  1. Install [vmware fusion](http://www.vmware.com/products/fusion/), [Vagrant](https://www.vagrantup.com/downloads.html), and [Ansible](http://docs.ansible.com/intro_installation.html):
    * OS X
      - `$ brew cask install virtualbox vagrant`
      - `$ brew install ansible`
    * Ubuntu
      - `$ sudo aptitude install virtualbox ansible vagrant`
  2. Install all the roles required by this playbook with the command `$ ansible-galaxy install -r requirements.txt`
  3. Install vmware plugin ``vagrant plugin install vagrant-vmware-fusion``
  4. Install vmware license ``vagrant plugin license vagrant-vmware-fusion license.lic``
  5. Run! ``vagrant up``


#### Vagrant ssh

To start this party:

1) type ``vagrant ssh`` to ssh into new box

#### Using browser

1) type ``ifconfig`` in the vm. Grab the IP number from the eth0. for virtualbox this should just be 33.33.33.33. For VMware it wil be something like 192.168.231.132.
2) add the ip address and site name to the /etc/hosts file. type: "sudo vim /etc/hosts" and enter IP_ADDRESS URL for any sites you use on the vm. Example:

```
192.168.231.132 nydmv.local
```

for dmv on VMware

