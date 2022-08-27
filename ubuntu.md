# Removing things
https://askubuntu.com/questions/32730/how-to-remove-postgres-from-my-installation

# What's my shell?
* `echo $SHELL`

# Services

## list services
* service --status-all

## stop a service for now
* sudo systemctl stop postgresql

## stop a service on reboot
* sudo systemctl disable postgresql

## start, enable on startup
* sudo systemctl start postgresql
* sudo systemctl enable postgresql

# Networking

## speed test
* `ssh username@myserver.example.com 'dd if=/dev/zero bs=1GB count=3 2>/dev/null' | dd of=/dev/null status=progress`

## Copying with status
* cp -v a.txt b.txt

## turn off annoyances
  systemctl list-units --type service --user | grep evolution
  systemctl --user mask evolution-addressbook-factory.service
  systemctl --user mask evolution-calendar-factory.service
  systemctl --user mask evolution-source-registry.service
  systemctl --user mask evolution-user-prompter.service
  systemctl --user mask tracker-miner-fs-3.service

## encrypt drives
  sudp parted -l
  sudo fdisk -l
  man luks
  sudo apt-get install cryptsetup
  man cryptsetup
  cryptsetup luksFormat /dev/sda3
  sudo cryptsetup luksFormat /dev/sda3
  cd /dev/sda3
  sudo cryptsetup open /dev/sda3
  sudo cryptsetup open /dev/sda3 data
