# DDCUtil Setup Info

## Install
`sudo apt install ddcutil`

`sudo usermod -aG i2c $USER`

`sudo su -`

`echo 'KERNEL=="i2c-[0-9]*", GROUP="i2c"' >> /etc/udev/rules.d/10-local_i2c_group.rules`

### Load the i2c-dev module for operation
In some cases the i2c-dev module is installed but not loaded on boot, to load it initially do the following:    
`sudo modprobe i2c-dev`    
This will load the module and allow you to try out the commands below to see if they work.
To load the module by default at boot time run the following:    
`sudo touch /etc/modules-load.d/i2c.conf`    
`echo "i2c-dev" | sudo tee /etc/modules-load.d/i2c.conf`    
The previous 2 commands will create the needed conf file and then put the name of the module we need to load.  At boot the .conf files within the directory are processed and the modules called out are loaded.

## The Keyboard command mappings

KVM Switch    
`ddcutil setvcp 60 0x1b`

Input Switch to HDMI    
`ddcutil setvcp 60 0x11`

Input Switch to DP    
`ddcutil setvcp 60 0x0f`
