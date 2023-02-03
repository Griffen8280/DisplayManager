# DDCUtil Setup Info

## Install
`sudo apt isntall ddcutil`

`sudo usermod -aG i2c $USER`

`sudo su -`

`echo 'KERNEL=="i2c-[0-9]*", GROUP="i2c"' >> /etc/udev/rules.d/10-local_i2c_group.rules`

## The Keyboard command mappings

KVM Switch    
`ddcutil setvcp 60 0x1b`

Input Switch to HDMI    
`ddcutil setvcp 60 0x11`

Input Switch to DP    
`ddcutil setvcp 60 0x0f`
