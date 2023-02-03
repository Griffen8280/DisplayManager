# DDCUtil Setup Info

## Install
`sudo apt isntall ddcutil`

`sudo usermod -aG i2c $USER`

`sudo su -`

`echo 'KERNEL=="i2c-[0-9]*", GROUP="i2c"' >> /etc/udev/rules.d/10-local_i2c_group.rules`
