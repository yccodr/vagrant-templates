# free5GC vagrant

## Prerequisites

- Ansible 2.10 or later
- Vagrant (tested in 2.4.1)
- VirtualBox (tested in 7.0)

## Usage

- Spin up VM: `vagrant up`
- Ssh into VM: `vagrant ssh`
- Get ssh-config: `vagrant ssh-config`

## Connect VM with VSCode

1. Get ssh-config with `vagrant ssh-config`.
2. Open ssh config file ($HOME/.ssh/config)
3. Paste ssh-config from 1. to the file
4. Change `default` to other name

Example `$HOME/.ssh/config`:
```
Host ubuntu-vm
  HostName 127.0.0.1
  User vagrant
  Port 2222
  UserKnownHostsFile /dev/null
  StrictHostKeyChecking no
  PasswordAuthentication no
  IdentityFile /home/yccodr/dev/vagrant/vagrant-templates/free5gc/.vagrant/machines/default/virtualbox/private_key
  IdentitiesOnly yes
  LogLevel FATAL
  PubkeyAcceptedKeyTypes +ssh-rsa
  HostKeyAlgorithms +ssh-rsa
```
