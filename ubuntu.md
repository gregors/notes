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
